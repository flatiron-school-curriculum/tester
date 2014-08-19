# Tester


## Form_tag

### collection_select
- In this case, this form assumes that there is a one-to-many relationship in place (movie has one director, director has many movies)

```
<%= form_for(@movie) do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>

  <%= f.collection_select :director_id, Director.all, :id, :name %>

  <%= f.submit %>
<% end %>
```

## Stop

```html
<form accept-charset="UTF-8" action="/cats" method="POST">
  <label for="cat_name">Name</label>
  <input id="cat_name" name="cat[name]" type="text">
  <label for="cat_color">Color</label>
  <input id="cat_color" name="cat[color]" type="text">
  <input name="commit" type="submit" value="Create Cat">
</form>
```

