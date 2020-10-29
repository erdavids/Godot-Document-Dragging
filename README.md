# Godot Document Dragging

An example system of dragging documents around in Godot.

![Alt Text](https://github.com/erdavids/Godot-Document-Dragging/blob/master/GitHubGif.gif)

The process is fairly simple. Each paper is represented as a KinematicBody2D with an intuitive collision shape. The script applied to the Paper.tscn scene allows for clicking a dragging without snapping the paper's center to the cursor. It is important to make sure that the Paper scene is not checking for collisions on the it's same layer, or else the papers will collide.

When multiple pages or documents are present, it's important to include something like the PaperGetter Area2D node. The logic here is that each paper exists in a stack or list and the z-index of each page corresponds to it's place in the list. When the player selects a paper, it is moved to the top of the list and therefore the highest z-index. If more than one page is underneath the cursor, the PaperGetter will make sure that the paper with the highest z-index is selected.


