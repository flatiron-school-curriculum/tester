---
  tags: BFS, DFS, cs, algorithms, computer science
  languages: ruby
  resources: 2
---

# Maze Solver

## Objective

Implement a Breadth First Search algorithm to solve a maze programmatically. 

## Introduction

The [Breadth First Search](http://en.wikipedia.org/wiki/Breadth-first_search) algorithm is a common way to solve node-based path executions. Given a graph of nodes, BFS will basically collect all the possible paths that can be traveled, and visit them until the destination node is reached. This [4 Minute Video on BFS](http://www.youtube.com/watch?v=QRq6p9s8NVg) explains it well.

The basic psuedocode can be described as:

    bfs(start, looking_for)
      create arrays (node_queue, visited_nodes, and traveled_path)
      add the start to the arrays
      while the queue is not empty
        take out the first element in the queue
        for each of the neighbors of this first element 
          if its not in the visited set and not blocked
            add this to the arrays
            if this contains what we are looking for
              return the backtrack of this node
            end if
          end if
        end for
      end while
    end method

There are three arrays we create, `node_queue`, `visited_nodes`, and `traveled_path` are storing data about the progress of the BFS.

- `node_queue` is storing nodes to travel.
- `visited_nodes` is storing nodes already traveled.
- `traveled_path` is storing nodes that traveled, have led to the destination.
