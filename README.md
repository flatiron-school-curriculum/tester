# Tester

## Other Form Elements

### accepts_nested_attributes_for  
- this goes into the model
- Allows you to implicitly create nested attributes for object associations
- closely tied in with the `fields_for` concept

### collection_check_boxes
- It assumes that there is a many-to-many relationship in place (books have many authors, authors have many books)

```ruby
<%= form_for(@book) do |f| %>
  <%= f.label :title %>
  <%= f.text_field :title %>

  <%= f.collection_check_boxes :author_ids, Author.all, :id, :name %>

  <%= f.submit %>
<% end %>
```

- This form has a `collection_check_boxes` field, and there are several parameters passed in:
  - The first parameter of the method is `:author_ids`: this is a collection of all of the `:author_id`s that will be passed in if the corresponding checkbox is checked
  - The second parameter is `Author.all`: this is collection of all of the possible check box options that will be available in the form
  - The third parameter is `:id`: this is the parameter of an author that will be passed into the `:author_ids` collection once a checkbox is checked
  - The final parameter is `:name`: this is the attribute of author that will be rendered on the page next to the checkbox
