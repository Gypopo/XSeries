I'm really thankful for all the bug fixes and performance improvements.\
Even if you changed a single line that has a good impact on the performance, it's welcomed. 

Some changes may need a discussion about quality and usage.
Make sure to explain your changes clearly when creating a pull request.
Most of the pull requests are merged directly into the master branch.

You have to import the original Spigot JAR directly to the plugin as SkullUtils uses `com.mojang.authlib`
This project has no original maven repository and cannot have one legally.
It's also used for JavaX nullability annotations.

### Rules
* Only Java 8 should be used. All the functions in the latest version of Java 8 can be used.
* Make sure the utility works on different versions.
* Use method and variable names that make sense and are related to the context.
* Don't use Optional everywhere that can return null.
* Using Guava's lib and Apache Commons is a plus, but make sure that what you're using is supported in
older versions of Bukkit.
* Add JavaDocs with proper formatting. It's also preferred to explain how the complex parts of a method work
inside the method. Use simple English when possible.
* All the functions used in the utilities should be compatible with Bukkit, Spigot and Paper.
Using extra methods from Spigot is a plus as long as it supports Bukkit, but do not use any methods that are included in any fork of Spigot.
* Change the class version properly. If you're not sure how versioning works don't change it.
* Each utility should be independent except the ones that are intended.
Functions such as the common ISFLAT boolean check should not depend on XMaterial's isNewVersion() Except
XBlock which is intended, since it already uses XMaterial for materials. Same for XParticle and ParticleDisplay.
* Do not attempt to support older versions than 1.8 even if it can be fixed with a single line.
* Do not use one liner if statements if it doesn't fit the screen.
* Try to avoid streams for frequently used methods.