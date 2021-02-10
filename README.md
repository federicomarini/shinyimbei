# shinyimbei

A collection of Shiny apps, created by research fellows at the IMBEI (Institute of Medical Biostatistics, Epidemiology and Informatics). Curated by Federico Marini

## Maintenance, made easy

### Setup 

- Clone this repo
- Make sure to have a fairly recent version of `blogdown` and Hugo installed

### Adding apps: you'll need that...

- A mid-sized image goes into `static/images/full`, at best some small sized png
- A thumbnail-sized image goes into `static/images/thumbs`, width of 250 px required to look nice
  - to convert the mid-sized image to a thumbnail, via `ImageMagick`:
  `convert static/images/full/yourimage.png -resize x250 static/images/thumbs/thumb_image.png `
- An entry goes into `data/items.toml`. See the existing entries in there and adapt the content for your new entry. 
  Essential info: a link, a description, the link to a publication, this kind of stuff.

Another option for resizing images and having them nicely squared:
`convert [inputimg] -resize 250x250 -background black -gravity center -extent 250x250 [outputimg]` (Credits to https://superuser.com/questions/1358715/how-do-i-resize-and-pad-an-image-to-a-given-size-using-imagemagick)

### Building and checking

```
blogdown::build_site()
# check it worked
blogdown:::preview_site()
# should open up in the Viewer pane. Please also open up in browser to check the full size
```

### Updating on the server

Please notify [@federicomarini](https://github.com/federicomarini) by tagging him

Ideally it is a matter of copying over the `public/` folder. _Ideally_...
