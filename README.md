# bluegrass
Blue noise "textures," both original and pseudo-randomly editable, in pure Java.

You may want to use this code to generate areas of blue noise textures or blue noise point sets
without any image dependencies or any need for visuals at all. It can also produce almost-blue noise
that is pseudo-randomly seeded (one kind looks better to people, and one kind detects better to machines).
See [Alan Wolfe's blog](https://blog.demofox.org/2018/01/30/what-the-heck-is-blue-noise/) for an introduction
to blue noise, if you're lost here. Blue noise point sets are quite useful for placing objects and terrain
features in natural ways, not to mention a primary use they have in dithering graphics.

This provides 64 blue noise textures, each 64x64 (tiling), in code. You can use these as blue noise point samples
by placing a point where a particular value is less than some threshold, where the lowest values equal -128 and all
values are less than 128.

All the API docs are in the one file's class documentation, and are also in methods docs.

The code here is straightforward to use as a library, but it can be quite frustrating to copy the code into
your own project by hand because of encoding issues. So, even though you could copy BlueNoise.java into your
code, unless it goes just right... the encoding used by some large Strings could be wrong, and the blue noise
textures would be incorrect. That's why I encourage using a dependency manager like Gradle or Maven here.

The current version is 0.1.2; it should be available on Maven Central using:
 - Gradle: `implementation "com.github.tommyettinger:bluegrass:0.1.2"` (may need `api` instead of `implementation`).
 - Maven:
 ```xml
 <dependency>
   <groupId>com.github.tommyettinger</groupId>
   <artifactId>bluegrass</artifactId>
   <version>0.1.2</version>
 </dependency>
 ```

If Maven Central isn't working, try [JitPack](https://jitpack.io/#tommyettinger/bluegrass).

Major changes are expected to be quite rare; if something is added, the rest will probably stay as it is.

