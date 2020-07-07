Port of Squeak's FreeCell Solitare game to Cuis to test PackageEnvironments.

STATUS: just started

````Smalltalk
"Environment w Cuis FreeCell"
Feature require: 'System-Environments'.
Feature require: 'Morphic-Games-Solitaire'.
Environment fromFeature: 'Morphic-Games-Solitaire'.  
Smalltalk at: #Klondike put: nil.
Smalltalk at: #FreeCell put: nil.
Smalltalk flushClassNameCache.

"Feature w Squeak FreeCell"
Feature require: 'Etoys-Squeakland-Morphic-Games'.
````