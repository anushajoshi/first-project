INSTALLATION
--------------------------------------------------------------------------------
1) Extract the module into your sites/all/modules or sites/xx/modules folder (where xx is your site name)
2) Visit the modules page admin/build/modules and enable the module
3) Follow the configuration steps below

CONFIGURATION
--------------------------------------------------------------------------------
To setup you must:
a) Create a content type
b) Add a nodereference field to the content type that references Ubercart product nodes
c) Under the display settings for the nodereference field choose Uc Sub-product add to cart form
d) Create your sub products as regular Ubercart products
e) Create a node of this content type (the parent node) and choose the sub-products (child nodes) in the node reference field
f) When you view the parent node, the child nodes will appear in a nice add to cart table

CUSTOMISATION
----------------------------------------------------------------------------------
Cart Icon
----------
If you want to change the cart icon, override the css using your theme, the selector is input.uc-subproduct-cart - just add something more specific,
eg
body input.uc-subproduct-cart {
 background-image: url(path/to/your/image.png);
}


Display Fields
---------------
To customise the display of fields in the table, go to /admin/content/types/list and edit the content type created at (a) above, under submission form settings enable the 'Setup display fields for UC Sub-product' checkbox and save.

Now when creating nodes of this type, you will get an additional fieldset allowing you to customise the display of fields in the table, including support for CCK.
To control the way fields are output visit the 'display fields' pages in the CCK admin pages for the product node type (admin/content/node-type/product/display/uc_subproduct), there is a new tab 'UC Sub Product' in addition to the standard normal and RSS modes.

If the core Ubercart fields (weight, dimensions etc) don't display in your table as expected, make sure they are enabled at admin/store/settings/products/edit/fields

Catalog
-----------
To get your new node types to act like standard products and appear in the
catalog (grid display only) and have their images appear like normal products,
visit /admin/content/types/list and edit the content type created at (a)
above, under submission form settings enable the 'Treat as normal Ubercart
product' checkbox and save. If you've created any nodes previously of this type, you'll need to edit and re-save them.

CREDITS
-------
This module was written by Lee Rowlands (larowlan) of Rowlands Group (http://www.rowlandsgroup.com). The author is available for paid customisations.

This module was sponsored by The Gallerie (http://www.thegallerie.com.au) and Website Express (http://www.website-express.co.uk).

Shopping cart icon from Glossy eCommerce Icons Pack - author Eoin McGrath from Starfish Web Consulting (http://www.starfishwebconsulting.co.uk) distributed under the LGPL
