# Helm Spotify Plus
A search & play interface for Spotify

There are several changes to the prior Helm-spotify package. 

Helm is used only to narrow the candidates get from the Spotify API.


# How to install
For now, there are only one way to install this package. You need to have the *use-package* functionality and load the package provided here through:

``` emacs-lisp
(add-to-list 'load-path "~/helm-spotify-plus")
(require 'helm-spotify-plus)
```

This will install the helm-core and two more libraries necessary to run Helm spotify plus: json and multi.


# How to use it

There are one basic command *helm-spotify-plus* that will ask for an input from the user:

**Enter the (partial/full) name of a Track:**

This will fill a list of 250 candidates from where you can choose the right one through Helm interface. 


Example of string query:

| String input           | Action                                                          |
|:----------------------:|:---------------------------------------------------------------:|
| a: metallica t: master | Explicitly write the Artist and the Track (partially is allowed)|
| a: metallica           | Only pass the author                                            |
| t: master of puppets   | Only the track                                                  |
| master of              | If no identifier is given, the request will use a free Track search|

Press TAB in Helm to see Actions over it.

# More features

As there are no downside of adding quick IBUS control over Emacs there are some small commands such as *spotify-pause, spotify-play, spotify-next* which can be called from M-x.

# Some already fixed bugs
+ Encoding
+ Difficulty to interact with Spotify API directly through Helm interface
+ Album play was only playing the first song of the album. Now its fixed.

# Credits

The original script was created by Kris Jenkis in 2013.



