# TikiMari website

Tikimari is a custom clothing store. The website aims to let people design their own clothes using Tikimari's pre-defined pieces.

All the files are currently on [Google Drive](https://drive.google.com/drive/u/0/folders/0B7z6gxP0LvZWTWRQcWJwaFVvM3M).

# Development

Design will be mobile first to enable easy sharing across platforms.

- [ ] **Phase 1 - Clothing designer**
  - [ ] **User side**
    - [ ] Show the final design
    - [ ] Constructor: change parts of design or start from scratch
    - [ ] Somehow see what parts this design consists of in text
    - [ ] Save session - user can return to hir custom design
    - [ ] Custom design URL - user can share effortlessly (char == design && int == tex)
    - [ ] Clicking on drawing will present an example photo of that piece
    - [ ] User sees a texture for every piece of design
    - [ ] Clicking on texture will show an example of it in photo
    - [ ] Clicking on texture will enable to change it
  - [ ] **Tikimari side**
    - [ ] Easily upload images somewhere like dropbox
    - [ ] Connect images to eachother via JSON
      - [ ] id
      - [ ] Price
      - [ ] Path
      - [ ] Name
      - [ ] Children
- [ ] **Phase 2 - Gallery**
  - [ ] **User side**
    - [ ] User sees many photos of completed designs
    - [ ] Filtering by types of event/gender
    - [ ] By clicking on one user also sees the drawing (design) behind it
    - [ ] User can now 1. back to gallery 2. customize this design 3. cherry-pick
  - [ ] **Tikimari side**
    - [ ] Upload pictures to somewhere comfy like dropbox
    - [ ] Define each images construct a.k.a. what design elements are at play (or just a link)
- [ ] **Phase 3 - Final**
  - [ ] User can always return to hir custom design
  - [ ] "How to measure yourself" page
  - [ ] "Order this design" page
    - [ ] Enter measurements
    - [ ] Enter contact details

- Checks
  - id's have no numbers
  - missing images
  - textures have no chars
  
# Others apps like it

- https://www.spreadshirt.com/create-your-own?department=0&productType=812&appearance=2
- https://paom.com/editor?do=basic-sweatshirt

# From scanning to vector

1. When scanning use white background and press on the lid to remove shadows.
1. To convert from image to vector use imagemagick in Linux: `for PHOTO in LEGO/*; do BASE=`basename $PHOTO`; echo "Converting $PHOTO"; convert "$PHOTO" -fuzz 30% -transparent white "LEGO-vector/$BASE.svg"; done`

# Copyright

This repo is not to be used by anyone in any circumstance, except the company Tikimari OÜ. If however you want to, get in contact, we'd love to hear how you actually could use it.
