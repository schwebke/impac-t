# Impac't

A Breakout/Bolo clone, augmented with a physics engine


## TODO

 - let user select a certain level
 - amend {{{Level::load()}}} with the ability to load complete levels (tile map, graphics) from a zip file. The zip file must have a flat directory structure.
 - display gravity vector as a visual aid for the player
 - nicer visual effect when the racket hits a block
 - nicer visual effect for killing spree bonus
 - special blocks that ...
   - blur the screen
   - make blocks semi-transparent
   - distort the screen
   - cause a kind of asteroid shower (or other dangerous things that fall from the sky and can severely harm the racket)
   - increase inertia of racket
   - speed up/slow down ball (friction?)
 - place racket on level's default position in case it was caught in between wall segments or something like that
 - integrate with Steam:
   - leaderboard for every level
   - leaderboard for campaigns
   - stats & achievements

### Architecture

Currently {{{ParticleSystem}}} uses a shader common to all objects due to performance reasons. In effect one {{{ParticleSystem}}} object influences the display of another. 
Maybe it would be helpful to create an array of reusable shaders. At each instantiation of a {{{ParticleSystem}}} object a currently unused shader from that array is assigned to the {{{ParticleSystem}}} object.



Nutzungshinweise und Lizenz
---------------------------


Copyright (c) 2015 Oliver Lau <<ola@ct.de>>, <a href="http://www.heise.de/">Heise Zeitschriften Verlag</a>.

Dieses Programm ist freie Software. Sie können es unter den Bedingungen der <a href="http://www.gnu.org/licenses/gpl-3.0">GNU General Public License</a>, wie von der Free Software Foundation veröffentlicht, weitergeben und/oder modifizieren, entweder gemäß Version 3 der Lizenz oder (nach Ihrer Wahl) jeder späteren Version.

__Diese Software wurde zu Lehr- und Demonstrationszwecken programmiert und ist nicht für den produktiven Einsatz vorgesehen. Der Autor und der Heise Zeitschriften Verlag haften nicht für eventuelle Schäden, die aus der Nutzung der Software entstehen, und übernehmen keine Gewähr für ihre Vollständigkeit, Fehlerfreiheit und Eignung für einen bestimmten Zweck.__

