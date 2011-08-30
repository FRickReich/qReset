# qReset - a quick and tiny CSS Reset

After using Eric Meyers reset for many years, i recently changing over to haml/sass, and didnt like how eric's reset looked converted, so after i couldnt find any alternative that pleased me, i decided to write my own reset.

## How to install (css)
copy the file "qreset.css" into your stylesheets folder and add  
```
<link rel="stylesheet" type="text/css" href="stylesheets/qreset.css" />
```   
into the head section of your .html file above other css links.

## How to install (sass)
copy the file "qreset.sass" into your stylesheets folder and put the line below into your .haml file  
```
%link{:href => "stylesheets/qreset.sass", :rel => "stylesheet", :type => "text/css"}/
```   
the qreset.css file should be at he topmost position of your css links inside the head tag of your .haml file.

## a little trick
if you are using ruby (sinatra), you should add   
   
> get '/stylesheets/:name.css' do   
>  	content_type 'text/css', :charset => 'utf-8'   
>	sass :"/stylesheets/#{params[:name]}"   
> end   
   
into your .rb file, this will automaticly read any .sass file in the stylesheets folder and convert it to css. this way you dont have to do it for every single file.  

*qReset 2008 by F. Rick Reich (frederikreich@googlemail.com)*