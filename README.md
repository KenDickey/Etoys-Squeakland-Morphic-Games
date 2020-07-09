Port of Squeak's FreeCell Solitare game to Cuis to test PackageEnvironments.

STATUS: just started

````Smalltalk
"Environment w Cuis FreeCell"
ChangeSet fileIn: (DirectoryEntry smalltalkImageDirectory parent // 'PackageEnvironments/4242-CuisCore-PreEnvironment-2020Jul01-14h23m-KenD.001.cs.st').
ChangeSet fileIn: (DirectoryEntry smalltalkImageDirectory parent // 'PackageEnvironments/4243-CuisCore-EnvPart2-2020Jun21-01h19m-KenD.001.cs.st').
ChangeSet fileIn: (DirectoryEntry smalltalkImageDirectory parent // 'PackageEnvironments/4244-CuisCore-EnvPart3-2020Jul01-14h29m-KenD.001.cs.st').
Feature require: 'System-Environments'.
Feature require: 'Morphic-Games-Solitaire'.
Environment fromFeature: 'Morphic-Games-Solitaire'.  
"Klondike and FreeCell classes ask to be exported from Environments.
 Undo this."
Smalltalk removeKey: #Klondike ifAbsent: [nil].
Smalltalk removeKey: #FreeCell ifAbsent: [nil].
Smalltalk flushClassNameCache.

"These are already required 
  by Etoys-Squeakland-Morphic-Games:
Feature require: 'Morphic-Misc1'.
Feature require: 'SqueakCompatibility'.
"

"Feature w Squeak FreeCell"
Feature require: 'Etoys-Squeakland-Morphic-Games'.
````
