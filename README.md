# New Theatre Backstage Catalogue

# Archived and now exists at [the New Theatre organisation](http://github.com/newtheatre/backstage)

[Jekyll](http://jekyllrb.com/) based site to catalogue set, props and costumes. Based on [lx](http://github.com/newtheatre/lx)

![Screenshot](https://github.com/samozzy/backstage/blob/gh-pages/backstage.png?raw=true)

## Editing

Stock lists are stored in [YAML](http://yaml.org/) files within the `_data/` directory.

### Set and Props 

- For large set pieces, edit file `_data/set.yml`; for small props edit `_data/props.yml`
  - `material`, the primary materials the object is made of e.g. Wood, Leather
  - `name`, useful name of the item 
  - `color`, primary colours of the item e.g. Brown, Red
  - `paint`, whether the item can be painted (`true` or `false`)
  - `category` of the item, as per the list at the top of the file. The list determines the available filters.
  - `image`, photo filename including extension, stored in category subfolders.
  - `measurements`, where relevant, including units e.g. 400x400x300mm
  - `notes`, other descriptions of the item, surrounded in quotes where using special characters.
  - `stock`, the number of the item:
    - `good`, in working order
    - `broken`, in need of repair

**Props-only properties**
  - `batteries`, if the item requires batteries (`true` or `false`) and type is unknown.
  - `battery_type`, the type and quantity of batteries e.g. 2xAA (`batteries` is **not** also required)
  - `fragile`, set `true` if the item is easily breakable.
  - `restricted`, set `true` if the item is only to be used with permission, or stored in a locked area.

### Costumes and Props

- For costumes edit file `_data/costumes.yml`. The format hasn't been finalised yet.

### Categories

When adding a new category for an item, add it to the list at the top of the items list, and also define a colour for it in the relevant map in `_sass/_categories.scss`.

## Forking

This project is designed to be hosted using [GitHub Pages](https://pages.github.com/) and requires some knowlege of Git. To use this project for your own venue:

1. Fork the repository.
2. Modify (or delete) `CNAME`, this specifies what host to serve the pages at - see the [Pages documentation](https://help.github.com/articles/adding-a-cname-file-to-your-repository/) for more information.
3. Modify the `_config.yml` changing New Theatre specific values to that of your venue.
4. Modify the data files - see the editing section.
