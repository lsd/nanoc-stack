Nanoc cheat sheet
===============================================

# Generate a nanoc app and cd into it
nanoc create-site sandbox
cd sandbox/

# nanc.yml
data_sources:
  -
    type: filesystem_unified
    items_root: /
    layouts_root: /
    allow_periods_in_identifiers: false

# Rules for compile + route items
compile '/stylesheet/' do
  # :filter :scss
end

route '/stylesheet/' do
  '/style.css'
end
 
# Edit content/stylesheet.css (make any change) and save
nano content/stylesheet.css

# Run 'nanoc co' to compile changes into output dir
nanoc co[mpile]

# Rendered output
SOURCE FILE                COMPILED FILE
content/stylesheet.css     output/style.css

# Exposed path to item (public URL)
http://phirl.com/style.css map to :items_root/stylesheet.css
