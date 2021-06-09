# Project

## Properties

### id
The project id of the project object.

### title
The title of the project.

### description
The description of the project.

### instructions
The instructions of the project.

### visible
A boolean representing if the project is visible or not.

### public
A boolean representing if the project is public or not.

### comments_allowed
A boolean representing if the project has comments allowed or not.

### is_published
Boolean representing whether the project is published or not.

### author
The author of the project.

## Methods

### get_comment(commentId)
Gets the comment with the given commentId.

### love()
*Note: You shouldn't be using this method. Bots that do social actions get banned on scratch. This is just a proof of concept.*
Loves the project.

### unlove()
*Note: You shouldn't be using this method. Bots that do social actions get banned on scratch. This is just a proof of concept.*
Unloves the project.

### favorite()
*Note: You shouldn't be using this method. Bots that do social actions get banned on scratch. This is just a proof of concept.*
Favorites the project.

### unfavorite()
*Note: You shouldn't be using this method. Bots that do social actions get banned on scratch. This is just a proof of concept.*
Unfavorites the project.

### view()
*Note: You shouldn't be using this method. Bots that do social actions get banned on scratch. This is just a proof of concept.*
Adds a view to the project.

### get_scripts()
Gets the Project JSON of the project.

### get_remixes(all=False, limit=20, offset=0)
Gets the remixes of the project. If all=True, the script will continue to loop through all the remixes. If not, you can use the limit and offset to customize it for your needs.

### get_studios(all=False, limit=20, offset=0)
Gets the studios that the project is in. If all=True, the script will continue to loop through all the studios the project is in. If not, you can use the limit and offset to customize it to your needs.

### post_comment(content, parent_id="", commentee_id="")
*Note: You shouldn't be using this method. Bots that do social actions get banned on scratch. This is just a proof of concept.*
Posts a comment on the project.

### get_comments(all=False, limit=20, offset=0)
Gets the comments of the project. If all=True, the script will continue to loop through all the comments. If not, you can use the limit and offset to customize it for your needs.

### toggle_commenting()
Toggles commenting on and off on the project. Will throw an error if you are not the project's author.

### turn_on_commenting()
Turns on commenting on the project. Will throw an error if you are not the project's author.

### turn_off_commenting()
Turns off commenting on the project. Will throw an error if you are not the project's author.

### report(category, reason, image=None)
Reports the project.

### unshare()
Unshares the project. Will throw an error if you are not the project's author.

### share()
Shares the project. Will throw an error if you are not the project's author.

### set_thumbnail(file)
Sets the project thumbnail to the file given.

