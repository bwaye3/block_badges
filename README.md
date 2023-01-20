# *Add to the SUBTHEME.libraries.yml*

gt-badges:<br>
version: "1.0.x"<br />
css:<br />
theme:<br />
templates/block/custom/badges/css/gt-badges.css: {}<br>
js:<br />
dependencies:<br />
- core/jquery<br />

# *Add to the repositories section in SUBTHEME composer.json*

"repositories": [<br />
{ <br />
"type": "vcs", <br />
"url": "https://github.gatech.edu/ICWebTeam/block_badges.git" <br />
}
# *Add to the require in SUBTHEME composer.json*

"require": { <br />
"gt/badges": "dev-master" <br />
"mnsami/composer-custom-directory-installer": "^2.0"<br />
},

# *Add to the installer paths in SUBTHEME composer.json*
"installer-paths": { <br />
"web/themes/contrib/SUBTHEME/templates/block/custom/badges": [ <br />
"gt/badges" <br />
] <br />
},

# *Implements hook_page_attachments_alter(). in subtheme.theme*
function SUBTHEME_page_attachments_alter(&$page) {<br />
$page['#attached']['library'][] = 'SUBTHEME/badges';<br />
}


# **CUSTOM BLOCK  SET-UP**
![](images/set-up.png)

# **TAXONOMY SET-UP**
![](images/animations.png)

