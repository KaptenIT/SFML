# Changelog

## SFML 2.4.2

Also available on the website: http://www.sfml-dev.org/changelog.php#sfml-2.4.2

  * **System**
    * (Bugfix) [Windows] Removed thread affinity changes in sf::Clock ([#1107](https://github.com/SFML/SFML/issues/1107))
  * **Window**
    * (Bugfix) Fixed bug where TransientContextLock would hang ([#1165](https://github.com/SFML/SFML/issues/1165), [#1172](https://github.com/SFML/SFML/issues/1172))
    * (Bugfix) [Linux] Fixed GLX extensions being loaded too late ([#1183](https://github.com/SFML/SFML/issues/1183))
    * (Bugfix) [Linux] Fix wrong types passed to XChangeProperty ([#1168](https://github.com/SFML/SFML/issues/1168) [#1171](https://github.com/SFML/SFML/issues/1171))
    * (Bugfix) [Windows] Make context disabling via wglMakeCurrent more tolerant of broken drivers ([#1186](https://github.com/SFML/SFML/issues/1186))
  * **Graphics**
    * (Bugfix) Optimized sf::Image::create and made it more exception safe ([#1166](https://github.com/SFML/SFML/issues/1166))

## SFML 2.4.1

Also available on the website: http://www.sfml-dev.org/changelog.php#sfml-2.4.1

  * **General**
    * [kFreeBSD] Define SFML_OS_FREEBSD when compiling for kFreeBSD ([#1129](https://github.com/SFML/SFML/issues/1129))
    * [Windows] Added some simple messaging when trying to build under Cygwin ([#1153](https://github.com/SFML/SFML/issues/1153))
  * **Window**
    * (Bugfix) Fixed stack overflow on GlContext creation with multiple threads ([#989](https://github.com/SFML/SFML/issues/989), [#1002](https://github.com/SFML/SFML/issues/1002))
    * (Bugfix) Adjusted mouse cursor grab documentation ([#1133](https://github.com/SFML/SFML/issues/1133))
    * (Bugfix) [iOS] Fixed orientation change not rescaling window size properly ([#1049](https://github.com/SFML/SFML/issues/1049), [#1050](https://github.com/SFML/SFML/issues/1050))
    * (Bugfix) [Linux] Fixed fullscreen issue ([#921](https://github.com/SFML/SFML/issues/921), [#1138](https://github.com/SFML/SFML/issues/1138))
    * (Bugfix) [Linux] Switched from XCB back to Xlib for windowing ([#1138](https://github.com/SFML/SFML/issues/1138))
    * (Bugfix) [Linux] Fixed window icon not showing up on some distros ([#1087](https://github.com/SFML/SFML/issues/1087), [#1088](https://github.com/SFML/SFML/issues/1088))
    * (Bugfix) [Linux] Fixed an issue where GNOME flags window unresponsive ([#1089](https://github.com/SFML/SFML/issues/1089), [#1138](https://github.com/SFML/SFML/issues/1138))
    * (Bugfix) [Linux] Fixed leak of XVisualInfo objects during GlxContext creation ([#1135](https://github.com/SFML/SFML/issues/1135))
    * (Bugfix) [Linux] Fixed possible hang when setting visibility if external window sources ([#1136](https://github.com/SFML/SFML/issues/1136))
    * (Bugfix) [OS X] Fixed inconsistency between doc and impl on OS X for the grab feature ([#1133](https://github.com/SFML/SFML/issues/1133), [#1148](https://github.com/SFML/SFML/issues/1148), [#1150](https://github.com/SFML/SFML/issues/1150))
    * (Bugfix) [Windows] Fixed context memory leaks ([#1143](https://github.com/SFML/SFML/issues/1143), [#1002](https://github.com/SFML/SFML/issues/1002))
  * **Graphics**
    * (Bugfix) Adjusted uniform error message ([#1131](https://github.com/SFML/SFML/issues/1131))
    * (Bugfix) Clarify documentation on Rect::contains function bounds ([#1151](https://github.com/SFML/SFML/issues/1151))
  * **Network**
    * (Bugfix) Fixed a typo in comment for void unbind() ([#1121](https://github.com/SFML/SFML/issues/1121))

## SFML 2.4.0

Also available on the website: http://www.sfml-dev.org/changelog.php#sfml-2.4.0

  * **General**
    * Added deprecation macro ([#969](https://github.com/SFML/SFML/issues/969))
    * Fixed issues reported by Coverity Scan static analysis ([#1064](https://github.com/SFML/SFML/issues/1064))
    * Fixed some initialization issues reported by Cppcheck ([#1008](https://github.com/SFML/SFML/issues/1008))
    * Changed comment chars in FindSFML.cmake to # ([#1090](https://github.com/SFML/SFML/issues/1090))
    * Fixed some typos ([#1098](https://github.com/SFML/SFML/issues/1098), [#993](https://github.com/SFML/SFML/issues/993), [#1099](https://github.com/SFML/SFML/issues/1099), [#956](https://github.com/SFML/SFML/issues/956), [#963](https://github.com/SFML/SFML/issues/963), [#979](https://github.com/SFML/SFML/issues/979))
    * Updated/fixed string comparisons in Config.cmake ([#1102](https://github.com/SFML/SFML/issues/1102))
    * Added the missing -s postfix for the RelWithDebInfo config ([#1014](https://github.com/SFML/SFML/issues/1014))
    * [Android] Fixed current Android compilation issues ([#1116](https://github.com/SFML/SFML/issues/1116), [#1111](https://github.com/SFML/SFML/issues/1111), [#1079](https://github.com/SFML/SFML/issues/1079))
    * [OS X] Update Xcode template material ([#976](https://github.com/SFML/SFML/issues/976), [#968](https://github.com/SFML/SFML/issues/968))
    * [Windows] Added support for VS 2015 ([#972](https://github.com/SFML/SFML/issues/972))
    * [Windows] Create and install PDB debug symbols alongside binaries ([#1037](https://github.com/SFML/SFML/issues/1037))
  * **Deprecated API**
    * sf::RenderWindow::capture(): Use a sf::Texture and its sf::Texture::update(const Window&) function and copy its contents into an sf::Image instead.
    * sf::Shader::setParameter(): Use setUniform() instead.
    * sf::Text::getColor(): There is now fill and outline colors instead of a single global color. Use getFillColor() or getOutlineColor() instead.
    * sf::Text::setColor(): There is now fill and outline colors instead of a single global color. Use setFillColor() or setOutlineColor() instead.
    * sf::LinesStrip: Use LineStrip instead.
    * sf::TrianglesFan: Use TriangleFan instead.
    * sf::TrianglesStrip: Use TriangleStrip instead.
  * **System**
    * (Feature) [Android] Added sf::getNativeActivity() ([#1005](https://github.com/SFML/SFML/issues/1005), [#680](https://github.com/SFML/SFML/issues/680))
    * (Bugfix) Added missing <iterator> include in String.hpp ([#1069](https://github.com/SFML/SFML/issues/1069), [#1068](https://github.com/SFML/SFML/issues/1068))
    * (Bugfix) Fixed encoding of UTF-16 ([#997](https://github.com/SFML/SFML/issues/997))
    * (Bugfix) [Android] Fixed crash when trying to load a non-existing font file ([#1058](https://github.com/SFML/SFML/issues/1058))
  * **Window**
    * (Feature) Added ability to grab cursor ([#614](https://github.com/SFML/SFML/issues/614), [#394](https://github.com/SFML/SFML/issues/394), [#1107](https://github.com/SFML/SFML/issues/1107))
    * (Feature) Added Multi-GPU preference ([#869](https://github.com/SFML/SFML/issues/869), [#867](https://github.com/SFML/SFML/issues/867))
    * (Feature) Added support for sRGB capable framebuffers ([#981](https://github.com/SFML/SFML/issues/981), [#175](https://github.com/SFML/SFML/issues/175))
    * (Feature) [Linux, Windows] Improved OpenGL context creation ([#884](https://github.com/SFML/SFML/issues/884))
    * (Feature) [Linux, Windows] Added support for pbuffers on Windows and Unix ([#885](https://github.com/SFML/SFML/issues/885), [#434](https://github.com/SFML/SFML/issues/434))
    * (Bugfix) Updated platform-specific handle documentation ([#961](https://github.com/SFML/SFML/issues/961))
    * (Bugfix) [Android] Accept touch events from "multiple" devices ([#954](https://github.com/SFML/SFML/issues/954), [#953](https://github.com/SFML/SFML/issues/953))
    * (Bugfix) [Android] Copy the selected EGL context's settings to SFML ([#1039](https://github.com/SFML/SFML/issues/1039))
    * (Bugfix) [Linux] Fixed modifiers causing sf::Keyboard::Unknown being returned ([#1022](https://github.com/SFML/SFML/issues/1022), [#1012](https://github.com/SFML/SFML/issues/1012))
    * (Bugfix) [OS X] Improved memory management on OS X ([#962](https://github.com/SFML/SFML/issues/962), [#790](https://github.com/SFML/SFML/issues/790))
    * (Bugfix) [OS X] Fixed crash when resizing a window to a zero-height/width size ([#986](https://github.com/SFML/SFML/issues/986), [#984](https://github.com/SFML/SFML/issues/984))
    * (Bugfix) [OS X] Use the mouse button constant instead of 0 to avoid a compiler error on OSX ([#1035](https://github.com/SFML/SFML/issues/1035))
    * (Bugfix) [OS X] OS X improvement: warnings + bugfix + refactoring, the lot! ([#1042](https://github.com/SFML/SFML/issues/1042))
  * **Graphics**
    * (Feature) Added support for outlined text ([#840](https://github.com/SFML/SFML/issues/840))
    * (Feature) Add support for geometry shaders ([#886](https://github.com/SFML/SFML/issues/886), [#428](https://github.com/SFML/SFML/issues/428))
    * (Feature) Feature/blend mode reverse subtract ([#945](https://github.com/SFML/SFML/issues/945), [#944](https://github.com/SFML/SFML/issues/944))
    * (Feature) Implemented support for mipmap generation ([#973](https://github.com/SFML/SFML/issues/973), [#498](https://github.com/SFML/SFML/issues/498), [#123](https://github.com/SFML/SFML/issues/123))
    * (Feature) Added new API to set shader uniforms ([#983](https://github.com/SFML/SFML/issues/983), [#538](https://github.com/SFML/SFML/issues/538))
    * (Feature) Rewrite RenderWindow::capture ([#1001](https://github.com/SFML/SFML/issues/1001))
    * (Bugfix) Exporting some Glsl utility functions due to linking issues ([#1044](https://github.com/SFML/SFML/issues/1044), [#1046](https://github.com/SFML/SFML/issues/1046))
    * (Bugfix) Fixed missing initialisation of Font::m_stroker ([#1059](https://github.com/SFML/SFML/issues/1059))
    * (Bugfix) Changed primitive types to be grammatically correct ([#1095](https://github.com/SFML/SFML/issues/1095), [#939](https://github.com/SFML/SFML/issues/939))
  * **Audio**
    * (Feature) Implemented stereo audio recording ([#1010](https://github.com/SFML/SFML/issues/1010))
    * (Bugfix) Added an assignment operator to SoundSource ([#864](https://github.com/SFML/SFML/issues/864))
    * (Bugfix) [OS X] Updates OpenAL-soft for OS X to version 1.17.2 ([#1057](https://github.com/SFML/SFML/issues/1057), [#900](https://github.com/SFML/SFML/issues/900), [#1000](https://github.com/SFML/SFML/issues/1000))
    * (Bugfix) Fixed a bug where vorbis can't handle large buffers ([#1067](https://github.com/SFML/SFML/issues/1067))
    * (Bugfix) Added support for 24-bit .wav files ([#958](https://github.com/SFML/SFML/issues/958), [#955](https://github.com/SFML/SFML/issues/955))
    * (Bugfix) Fixed threading issue in sf::SoundRecorder ([#1011](https://github.com/SFML/SFML/issues/1011))
    * (Bugfix) Made WAV file reader no longer assume that data chunk goes till end of file to prevent reading trailing metadata as samples ([#1018](https://github.com/SFML/SFML/issues/1018))
    * (Bugfix) Fixed seeking in multi channel FLAC files ([#1041](https://github.com/SFML/SFML/issues/1041), [#1040](https://github.com/SFML/SFML/issues/1040))
  * **Network**
    * (Feature) Added optional argument on which address to bind (socket). ([#850](https://github.com/SFML/SFML/issues/850), [#678](https://github.com/SFML/SFML/issues/678))
    * (Bugfix) Fixed FTP directory listing blocking forever ([#1086](https://github.com/SFML/SFML/issues/1086), [#1025](https://github.com/SFML/SFML/issues/1025))

## SFML 2.3.2

Also available on the website: http://www.sfml-dev.org/changelog.php#sfml-2.3.2

  * **General**
    * Fixed an issue where FindSFML.cmake couldn't find older versions of SFML ([#903](https://github.com/SFML/SFML/issues/903))
    * Robust alCheck and glCheck macros ([#917](https://github.com/SFML/SFML/issues/917))
    * Fixed FindSFML.cmake to use the uppercase FLAC name ([#923](https://github.com/SFML/SFML/issues/923))
    * Added a CONTRIBUTING file so GitHub shows a message when creating a new issue ([#932](https://github.com/SFML/SFML/issues/932))
  * **Window**
    * (Bugfix) [Linux] Fixed an issue where the keypad's key weren't being detected ([#910](https://github.com/SFML/SFML/issues/910))
    * (Bugfix) [Linux] Revert to Xlib event handling ([#934](https://github.com/SFML/SFML/issues/934))
    * (Bugfix) [Linux] Fixed `XK_*` inconsistency in InpuImpl.cpp ([#947](https://github.com/SFML/SFML/issues/947))
    * (Bugfix) [Linux] Fix `_NET_WM_PING` messages not being replied to properly ([#947](https://github.com/SFML/SFML/issues/947))
  * **Graphics**
    * (Bugfix) Fixed clear bug on RenderTextures ([#915](https://github.com/SFML/SFML/issues/915))
    * (Bugfix) Fixed image file extension detection ([#929](https://github.com/SFML/SFML/issues/929), [#930](https://github.com/SFML/SFML/issues/930), [#931](https://github.com/SFML/SFML/issues/931))
    * (Bugfix) Secure function against random data return ([#935](https://github.com/SFML/SFML/issues/935), [#942](https://github.com/SFML/SFML/issues/942))

## SFML 2.3.1

Also available on the website: http://www.sfml-dev.org/changelog.php#sfml-2.3.1

  * **Window**
    * (Bugfix) [Android] Make sure a window still exists before trying to access its dimensions ([#854](https://github.com/SFML/SFML/issues/854))
    * (Bugfix) [Android] Added Android API level checks ([#856](https://github.com/SFML/SFML/issues/856))
    * (Bugfix) [Android] Updated the JNI/event handling code ([#906](https://github.com/SFML/SFML/issues/906))
    * (Bugfix) [Linux] Resized events are only spawned when the window size actually changes ([#878](https://github.com/SFML/SFML/issues/878), [#893](https://github.com/SFML/SFML/issues/893))
    * (Bugfix) [Linux] Whitelisted X SHAPE events ([#879](https://github.com/SFML/SFML/issues/879), [#883](https://github.com/SFML/SFML/issues/883))
    * (Bugfix) [Linux] Remap Unix keyboard when user changes layout ([#895](https://github.com/SFML/SFML/issues/895), [#897](https://github.com/SFML/SFML/issues/897))
    * (Bugfix) [Linux] Fix undefined behavior in ewmhSupported() ([#892](https://github.com/SFML/SFML/issues/892), [#901](https://github.com/SFML/SFML/issues/901))
  * **Graphics**
    * (Bugfix) Added support for GL_EXT_texture_edge_clamp for systems that don't expose GL_SGIS_texture_edge_clamp ([#880](https://github.com/SFML/SFML/issues/880), [#882](https://github.com/SFML/SFML/issues/882))
  * **Audio**
    * (Bugfix) [Android] Fixed audio files not loading (and possibly crashing) ([#855](https://github.com/SFML/SFML/issues/855), [#887](https://github.com/SFML/SFML/issues/887))

## SFML 2.3

Also available on the website: http://www.sfml-dev.org/changelog.php#sfml-2.3

  * **General**
    * Examples only link against sfml-main in release mode ([#610](https://github.com/SFML/SFML/issues/610), [#766](https://github.com/SFML/SFML/issues/766))
    * Replaced unsigned int with std::size_t for array indices and sizes ([#739](https://github.com/SFML/SFML/issues/739))
    * Fixed some issues with the Doxygen documentation ([#750](https://github.com/SFML/SFML/issues/750))
    * Added support for EditorConfig ([#751](https://github.com/SFML/SFML/issues/751))
    * Hide success message for CMake in quiet mode ([#753](https://github.com/SFML/SFML/issues/753))
    * Improved documentation for statuses with sf::Ftp ([#763](https://github.com/SFML/SFML/issues/763))
    * Moved stb_image into the extlibs directory ([#795](https://github.com/SFML/SFML/issues/795))
    * Changed the SOVERSION to major.minor ([#812](https://github.com/SFML/SFML/issues/812))
    * Fixed warnings about switch-statements ([#863](https://github.com/SFML/SFML/issues/863))
    * Added missing includes in the general headers ([#851](https://github.com/SFML/SFML/issues/851))
    * [Android] Updated toolchain file and dependencies ([#791](https://github.com/SFML/SFML/issues/791))
    * [Linux] Fixed missing pthread dependency ([#794](https://github.com/SFML/SFML/issues/794))
    * [OS X] Relaxed CMake installation rules regarding framework dependencies ([#767](https://github.com/SFML/SFML/issues/767))
  * **Deprecated API**
    * sf::Event::MouseWheelEvent: This event is deprecated and potentially inaccurate. Use MouseWheelScrollEvent instead.
  * **Window**
    * (Feature) Added new events for handling high-precision scrolling ([#95](https://github.com/SFML/SFML/issues/95), [#810](https://github.com/SFML/SFML/issues/810), [#837](https://github.com/SFML/SFML/issues/837))
    * (Feature) Switched from Xlib to XCB ([#200](https://github.com/SFML/SFML/issues/200), [#319](https://github.com/SFML/SFML/issues/319), [#694](https://github.com/SFML/SFML/issues/694), [#780](https://github.com/SFML/SFML/issues/780), [#813](https://github.com/SFML/SFML/issues/813), [#825](https://github.com/SFML/SFML/issues/825))
    * (Feature) Added support for OpenGL 3 core context creation ([#654](https://github.com/SFML/SFML/issues/654), [#779](https://github.com/SFML/SFML/issues/779))
    * (Bugfix) Fixed glXSwapIntervalSGI being broken for some driver implementations ([#727](https://github.com/SFML/SFML/issues/727), [#779](https://github.com/SFML/SFML/issues/779))
    * (Bugfix) Fixed simultaneous context operations causing crashes on some AMD hardware ([#778](https://github.com/SFML/SFML/issues/778), [#779](https://github.com/SFML/SFML/issues/779))
    * (Bugfix) Fixed joystick identification ([#809](https://github.com/SFML/SFML/issues/809), [#811](https://github.com/SFML/SFML/issues/811))
    * (Bugfix) [iOS] Fixed various issues including stencil bits, device orientation and retina support ([#748](https://github.com/SFML/SFML/issues/748))
    * (Bugfix) [iOS] Fixed inconsistency between sf::Touch::getPosition and touch events ([#875](https://github.com/SFML/SFML/issues/875))
    * (Bugfix) [Linux] Fixed Alt+F4 not getting triggered in window mode ([#274](https://github.com/SFML/SFML/issues/274))
    * (Bugfix) [Linux] Fixed Unix joystick stuff ([#838](https://github.com/SFML/SFML/issues/838))
    * (Bugfix) [OS X] Fixed typo in JoystickImpl.cpp to prevent a crash ([#762](https://github.com/SFML/SFML/issues/762), [#765](https://github.com/SFML/SFML/issues/765))
    * (Bugfix) [OS X] Fixed an issue in InputImpl::getSFOpenGLViewFromSFMLWindow ([#782](https://github.com/SFML/SFML/issues/782), [#792](https://github.com/SFML/SFML/issues/792))
  * **Graphics**
    * (Feature) Replaced GLEW with loader generated by glLoadGen ([#779](https://github.com/SFML/SFML/issues/779))
    * (Feature) Added a new constructor to sf::Color that takes an sf::Uint32 ([#722](https://github.com/SFML/SFML/issues/722))
    * (Feature) Updated stb_image to v2.02 ([#777](https://github.com/SFML/SFML/issues/777))
    * (Feature) Updated FreeType to v2.5.5 ([#799](https://github.com/SFML/SFML/issues/799), [#804](https://github.com/SFML/SFML/issues/804))
    * (Feature) Added checks for software OpenGL ([#870](https://github.com/SFML/SFML/issues/870))
    * (Bugfix) Fixed GL_ARB_compatibility not being detected ([#859](https://github.com/SFML/SFML/issues/859))
    * (Bugfix) Fixed pixel format selection ([#862](https://github.com/SFML/SFML/issues/862))
    * (Bugfix) Bumped back the OpenGL version requirement to 1.1 ([#858](https://github.com/SFML/SFML/issues/858))
  * **Audio**
    * (Feature) Dropped libsndfile and started using Vorbis, FLAC and OGG directly ([#604](https://github.com/SFML/SFML/issues/604), [#757](https://github.com/SFML/SFML/issues/757))
    * (Feature) Added a FLAC file to the sound example ([#815](https://github.com/SFML/SFML/issues/815))
    * (Bugfix) Fixed access violation error in the destructor of sf::AudioDevice ([#30](https://github.com/SFML/SFML/issues/30), [#602](https://github.com/SFML/SFML/issues/602))
    * (Bugfix) [OS X] Fixed threading issue with sf::SoundStream and OpenAL ([#541](https://github.com/SFML/SFML/issues/541), [#831](https://github.com/SFML/SFML/issues/831))
  * **Network**
    * (Bugfix) Fixed sf::TcpSocket not handling partial sends properly ([#749](https://github.com/SFML/SFML/issues/749), [#796](https://github.com/SFML/SFML/issues/796))

## SFML 2.2

Also available on the website: http://www.sfml-dev.org/changelog.php#sfml-2.2

  * **General**
    * Support for iOS and Android platform ([#410](https://github.com/SFML/SFML/issues/410), [#440](https://github.com/SFML/SFML/issues/440))
    * Various documentation corrections ([#438](https://github.com/SFML/SFML/issues/438), [#496](https://github.com/SFML/SFML/issues/496), [#497](https://github.com/SFML/SFML/issues/497), [#714](https://github.com/SFML/SFML/issues/714))
    * Fixed support for compilers on Debian FreeBSD ([#380](https://github.com/SFML/SFML/issues/380), [#578](https://github.com/SFML/SFML/issues/578))
    * Added support for Visual Studio 2013 and proper support for the TDM builds ([#482](https://github.com/SFML/SFML/issues/482))
    * Fixed CMake problems related to FindSFML and cached variables ([#637](https://github.com/SFML/SFML/issues/637), [#684](https://github.com/SFML/SFML/issues/684))
    * Switched and enforced LF line endings ([#708](https://github.com/SFML/SFML/issues/708), [#712](https://github.com/SFML/SFML/issues/712))
    * Updated OpenAL to version 1.15.1 (d077210)
    * Made compiler and OS variable names much clearer in CMake files (9b0ed30)
    * Re-enabled RPATH feature (e157e7a)
    * Slight adjustments to the examples ([#737](https://github.com/SFML/SFML/issues/737))
    * [FreeBSD] Various configuration fixes ([#577](https://github.com/SFML/SFML/issues/577), [#578](https://github.com/SFML/SFML/issues/578))
    * [Linux] Updated FindSFML.cmake to add UDev to SFML's dependencies ([#728](https://github.com/SFML/SFML/issues/728), [#729](https://github.com/SFML/SFML/issues/729), [#734](https://github.com/SFML/SFML/issues/734), [#736](https://github.com/SFML/SFML/issues/736))
    * [OS X] Fixed incorrect symlink in freetype.framework ([#519](https://github.com/SFML/SFML/issues/519))
    * [OS X] CMake module for correct dependencies ([#548](https://github.com/SFML/SFML/issues/548))
    * [OS X] Fixed SFML target for Xcode ([#595](https://github.com/SFML/SFML/issues/595), [#596](https://github.com/SFML/SFML/issues/596))
    * [OS X] Updated implementation, mainly reverting to non-ARC ([#601](https://github.com/SFML/SFML/issues/601))
    * [OS X] Fixed memory leaks and dead store ([#615](https://github.com/SFML/SFML/issues/615))
    * [OS X] Improved event handling and performance ([#617](https://github.com/SFML/SFML/issues/617))
    * [OS X] Reduced memory usage ([#672](https://github.com/SFML/SFML/issues/672), [#698](https://github.com/SFML/SFML/issues/698))
    * [OS X] OS X 10.10 support ([#691](https://github.com/SFML/SFML/issues/691), [#699](https://github.com/SFML/SFML/issues/699))
    * [OS X] Improve flexibility of dependencies' locations ([#713](https://github.com/SFML/SFML/issues/713))
    * [Windows] Removed the hack that copied external libraries into SFML static libraries (dbf01a7)
  * **System**
    * (Feature) Added substring and replace functions to sf::String ([#21](https://github.com/SFML/SFML/issues/21), [#355](https://github.com/SFML/SFML/issues/355))
    * (Feature) Added toUtfX to sf::String ([#501](https://github.com/SFML/SFML/issues/501))
    * (Feature) Added fromUtfX functions to set the internal data to a string by converting from another string in a fixed encoding ([#196](https://github.com/SFML/SFML/issues/196))
    * (Feature) Added modulo operator for sf::Time ([#429](https://github.com/SFML/SFML/issues/429), [#430](https://github.com/SFML/SFML/issues/430))
    * (Feature) Added division operator for sf::Time ([#453](https://github.com/SFML/SFML/issues/453))
    * (Bugfix) Ensured a high resolution for sf::sleep ([#439](https://github.com/SFML/SFML/issues/439), [#475](https://github.com/SFML/SFML/issues/475))
    * (Bugfix) [Windows] Fixed stack unalignment by two internal functions ([#412](https://github.com/SFML/SFML/issues/412))
  * **Window**
    * (Feature) Added window methods to request and to check focus ([#518](https://github.com/SFML/SFML/issues/518), [#525](https://github.com/SFML/SFML/issues/525), [#613](https://github.com/SFML/SFML/issues/613), [#723](https://github.com/SFML/SFML/issues/723), [#735](https://github.com/SFML/SFML/issues/735))
    * (Feature) Provide name, manufacturer ID and product ID via sf::Joystick ([#152](https://github.com/SFML/SFML/issues/152), [#528](https://github.com/SFML/SFML/issues/528))
    * (Feature) [FreeBSD] Joystick support ([#477](https://github.com/SFML/SFML/issues/477))
    * (Feature) [OS X] Improved integration with menus and dock actions ([#11](https://github.com/SFML/SFML/issues/11))
    * (Feature) [OS X] Support for OpenGL 3.2 ([#84](https://github.com/SFML/SFML/issues/84))
    * (Feature) [OS X] Improved fullscreen support ([#343](https://github.com/SFML/SFML/issues/343))
    * (Feature) [OS X] Added support for retina displays ([#353](https://github.com/SFML/SFML/issues/353), [#388](https://github.com/SFML/SFML/issues/388))
    * (Feature) [Windows] Removed support for Windows 9x ([#469](https://github.com/SFML/SFML/issues/469))
    * (Feature) [Windows] Fixed typo in Windows keyboard implementation ([#516](https://github.com/SFML/SFML/issues/516))
    * (Bugfix) sf::Window::create() now also resets framerate limit ([#371](https://github.com/SFML/SFML/issues/371))
    * (Bugfix) Fixed OpenGL context leak ([#635](https://github.com/SFML/SFML/issues/635), [#705](https://github.com/SFML/SFML/issues/705))
    * (Bugfix) Fixed various joystick problems (memory leak, accelerometer detected, code refactoring) ([#660](https://github.com/SFML/SFML/issues/660), [#686](https://github.com/SFML/SFML/issues/686), [#742](https://github.com/SFML/SFML/issues/742), [#743](https://github.com/SFML/SFML/issues/743))
    * (Bugfix) Optimized sf::Window::waitEvent a bit, no sleep if events are available at first try (ff555d6)
    * (Bugfix) [Linux] Output error message when XOpenDisplay() fails ([#508](https://github.com/SFML/SFML/issues/508), [#616](https://github.com/SFML/SFML/issues/616))
    * (Bugfix) [Linux] Resize window with setSize when sf::Style::Resize is set ([#466](https://github.com/SFML/SFML/issues/466))
    * (Bugfix) [Linux] Fixed broken key repeat on window recreation ([#564](https://github.com/SFML/SFML/issues/564), [#567](https://github.com/SFML/SFML/issues/567))
    * (Bugfix) [OS X] Fixed KeyReleased not being fired in fullscreen mode ([#465](https://github.com/SFML/SFML/issues/465))
    * (Bugfix) [OS X] Fixed an issue where disconnecting the keyboard would cause a crash ([#467](https://github.com/SFML/SFML/issues/467))
    * (Bugfix) [OS X] Fixed unexpected resizing behavior ([#468](https://github.com/SFML/SFML/issues/468))
    * (Bugfix) [OS X] Improved resizing windows ([#474](https://github.com/SFML/SFML/issues/474))
    * (Bugfix) [OS X] Fixed memory leak with sf::Window::create() ([#484](https://github.com/SFML/SFML/issues/484))
    * (Bugfix) [OS X] Fixed menu shortcuts in fullscreen on OS X ([#527](https://github.com/SFML/SFML/issues/527))
    * (Bugfix) [OS X] Improved cursor hiding ([#703](https://github.com/SFML/SFML/issues/703))
    * (Bugfix) [OS X] Fixed right click not detected with trackpads ([#716](https://github.com/SFML/SFML/issues/716), [#730](https://github.com/SFML/SFML/issues/730))
    * (Bugfix) [Windows] Fixed joystick POV values (ef1d29b)
    * (Bugfix) [Windows] Fixed Unicode inconsistency ([#635](https://github.com/SFML/SFML/issues/635))
    * (Bugfix) [Windows] Fixed Alt+F4 and mouse clicks issues ([#437](https://github.com/SFML/SFML/issues/437), [#457](https://github.com/SFML/SFML/issues/457))
    * (Bugfix) [Windows] Send MouseButtonReleased event when the mouse is outside of the window ([#455](https://github.com/SFML/SFML/issues/455), [#457](https://github.com/SFML/SFML/issues/457))
    * (Bugfix) [Windows] Fixed sf::Joystick wrong registry usage ([#701](https://github.com/SFML/SFML/issues/701), [#702](https://github.com/SFML/SFML/issues/702), [#706](https://github.com/SFML/SFML/issues/706))
  * **Graphics**
    * (Feature) Provide more information about the loaded font in sf::Font ([#164](https://github.com/SFML/SFML/issues/164))
    * (Feature) Implemented a more flexible blending system ([#298](https://github.com/SFML/SFML/issues/298))
    * (Feature) Added strikethrough text style ([#243](https://github.com/SFML/SFML/issues/243), [#362](https://github.com/SFML/SFML/issues/362), [#682](https://github.com/SFML/SFML/issues/682))
    * (Feature) Slight optimization for sf::Text::setString ([#413](https://github.com/SFML/SFML/issues/413))
    * (Feature) Added subtraction operator for sf::Color ([#114](https://github.com/SFML/SFML/issues/114), [#145](https://github.com/SFML/SFML/issues/145))
    * (Feature) Optimized sf::Image::flipVertically/flipHorizontally ([#555](https://github.com/SFML/SFML/issues/555))
    * (Feature) Changed sf::Font measurements from int to float to allow better underline drawing ([#693](https://github.com/SFML/SFML/issues/693))
    * (Bugfix) Improved text quality for small and pixelated fonts ([#228](https://github.com/SFML/SFML/issues/228))
    * (Bugfix) Yet another fix for Intel GPUs with sf::RenderTexture ([#418](https://github.com/SFML/SFML/issues/418))
    * (Bugfix) Removed VTab since it causes issues and doesn't have a use nowadays ([#442](https://github.com/SFML/SFML/issues/442), [#445](https://github.com/SFML/SFML/issues/445), [#460](https://github.com/SFML/SFML/issues/460), [#588](https://github.com/SFML/SFML/issues/588))
    * (Bugfix) Fixed broken BDF and PCF font formats ([#448](https://github.com/SFML/SFML/issues/448))
    * (Bugfix) Fixed compilation issue with newer versions of GCC for sf::Rect ([#458](https://github.com/SFML/SFML/issues/458))
    * (Bugfix) Fixed resetGLStates() not explicitly setting the default polygon mode ([#480](https://github.com/SFML/SFML/issues/480))
    * (Bugfix) Fixed division-by-zero in sf::RectangleShape ([#499](https://github.com/SFML/SFML/issues/499))
    * (Bugfix) Fixed potential memory leak in sf::Font ([#509](https://github.com/SFML/SFML/issues/509))
    * (Bugfix) Updated glext and removed glxext ([#511](https://github.com/SFML/SFML/issues/511), [#583](https://github.com/SFML/SFML/issues/583))
    * (Bugfix) Make sure texture unit 0 is active when resetting sf::RenderTarget states ([#523](https://github.com/SFML/SFML/issues/523), [#591](https://github.com/SFML/SFML/issues/591))
    * (Bugfix) Fixed texture rect computation in fonts ([#669](https://github.com/SFML/SFML/issues/669))
    * (Bugfix) Improved rendering of underlined text ([#593](https://github.com/SFML/SFML/issues/593))
    * (Bugfix) Avoided repeated output of error messages ([#566](https://github.com/SFML/SFML/issues/566))
    * (Bugfix) Fixed text rendered with vertical offset on ascent and font size mismatch ([#576](https://github.com/SFML/SFML/issues/576))
    * (Bugfix) Fixed rounding problem for viewports ([#598](https://github.com/SFML/SFML/issues/598))
    * (Bugfix) Fixed sf::Shader::isAvailable() possibly breaking context management ([#211](https://github.com/SFML/SFML/issues/211), [#603](https://github.com/SFML/SFML/issues/603), [#608](https://github.com/SFML/SFML/issues/608), [#603](https://github.com/SFML/SFML/issues/603))
    * (Bugfix) Fixed sf::Texture::getMaximumSize() possibly breaking context management ([#666](https://github.com/SFML/SFML/issues/666))
    * (Bugfix) Fixed various sf::Text rendering issues ([#692](https://github.com/SFML/SFML/issues/692), [#699](https://github.com/SFML/SFML/issues/699))
    * (Bugfix) The texture matrix is now reset in sf::Texture::bind(NULL) (7c4b058)
    * (Bugfix) [Windows] Fixed DPI scaling causing strange window behavior ([#679](https://github.com/SFML/SFML/issues/679), [#681](https://github.com/SFML/SFML/issues/681), [#688](https://github.com/SFML/SFML/issues/688))
  * **Audio**
    * (Feature) Added support for selecting the audio capture device ([#220](https://github.com/SFML/SFML/issues/220), [#470](https://github.com/SFML/SFML/issues/470))
    * (Feature) Make sf::SoundRecorder processing frequency configurable ([#333](https://github.com/SFML/SFML/issues/333))
    * (Feature) Added up vector to sf::Listener ([#545](https://github.com/SFML/SFML/issues/545))
    * (Bugfix) Prevented sf::SoundStream::setPlayingOffset() from restarting playing even when paused ([#203](https://github.com/SFML/SFML/issues/203), [#592](https://github.com/SFML/SFML/issues/592))
    * (Bugfix) Fixed sf::SoundBuffer contents not being able to be updated when still attached to sounds ([#354](https://github.com/SFML/SFML/issues/354), 367, [#390](https://github.com/SFML/SFML/issues/390), [#589](https://github.com/SFML/SFML/issues/589))
    * (Bugfix) Catch audio format error and prevent division by zero ([#529](https://github.com/SFML/SFML/issues/529))
    * (Bugfix) Fixed sf::SoundBuffer returning wrong duration for sounds containing more than ~4.3 million samples (2ff58ed)
    * (Bugfix) Optimized sf::Listener with a cache (d97e524)
  * **Network**
    * (Feature) Added support for PUT and DELETE in sf::Http ([#257](https://github.com/SFML/SFML/issues/257), [#312](https://github.com/SFML/SFML/issues/312), [#607](https://github.com/SFML/SFML/issues/607))
    * (Feature) Added support for chunked HTTP transfers ([#296](https://github.com/SFML/SFML/issues/296), [#337](https://github.com/SFML/SFML/issues/337))
    * (Feature) Added support for 64-bit integers in sf::Packet ([#710](https://github.com/SFML/SFML/issues/710))
    * (Feature) Made sf::Ftp::sendCommand() public (2c5cab5)
    * (Bugfix) Checked socket descriptor limit ([#153](https://github.com/SFML/SFML/issues/153), [#628](https://github.com/SFML/SFML/issues/628), [#683](https://github.com/SFML/SFML/issues/683))
    * (Bugfix) Fixed sf::TcpSocket::connect()'s switching from blocking to non-blocking mode on immediate connection success ([#221](https://github.com/SFML/SFML/issues/221))
    * (Bugfix) Fixed FTP download and upload file sizes being limited by available RAM ([#565](https://github.com/SFML/SFML/issues/565), [#590](https://github.com/SFML/SFML/issues/590))
    * (Bugfix) Fixed C++11 compiler warnings for sf::Uint8 ([#731](https://github.com/SFML/SFML/issues/731), [#732](https://github.com/SFML/SFML/issues/732))

## SFML 2.1

Also available on the website: http://www.sfml-dev.org/changelog.php#sfml-2.1

  * **General**
    * Updated the Window and OpenGL examples (got rid of GLU and immediate mode)
  * **Window**
    * (Feature) Now using inotify on Linux to avoid constantly polling joystick connections ([#96](https://github.com/SFML/SFML/issues/96))
    * (Feature) Add keypad return, equal and period keys support for OS X
    * (Feature) Improved mouse events on OS X regarding fullscreen mode
    * (Feature) Improved mouse events on OS X ([#213](https://github.com/SFML/SFML/issues/213), [#277](https://github.com/SFML/SFML/issues/277))
    * (Feature) Improved reactivity of setMousePosition on OS X ([#290](https://github.com/SFML/SFML/issues/290))
    * (Feature) Added support for right control key on OS X
    * (Feature) Improved TextEntered for OS X ([#377](https://github.com/SFML/SFML/issues/377))
    * (Feature) Improved the performances of Window::getSize() (the size is now cached)
    * (Feature) Added the WM_CLASS property to SFML windows on Linux
    * (Feature) Fake resize events are no longer sent when the window is moved, on Linux
    * (Feature) Pressing ALT or F10 on Windows no longer steals the focus
    * (Bugfix) Fixed MouseMove event sometimes not generated when holding left button on Windows ([#225](https://github.com/SFML/SFML/issues/225))
    * (Bugfix) Fixed ContextSettings ignored when creating a 3.x/4.x OpenGL context on Linux ([#258](https://github.com/SFML/SFML/issues/258))
    * (Bugfix) Fixed ContextSettings ignored on Linux when creating a window ([#35](https://github.com/SFML/SFML/issues/35))
    * (Bugfix) Fixed windows bigger than the desktop not appearing on Windows ([#215](https://github.com/SFML/SFML/issues/215))
    * (Bugfix) Fixed KeyRelease events sometimes not reported on Linux ([#404](https://github.com/SFML/SFML/issues/404))
    * (Bugfix) Fixed mouse moved event on OS X when dragging the cursor ([#277](https://github.com/SFML/SFML/issues/277))
    * (Bugfix) Fixed KeyRelease event with CMD key pressed ([#381](https://github.com/SFML/SFML/issues/381))
    * (Bugfix) Fixed taskbar bugs on Windows ([#328](https://github.com/SFML/SFML/issues/328), [#69](https://github.com/SFML/SFML/issues/69))
    * (Bugfix) Fixed Window::getPosition() on Linux ([#346](https://github.com/SFML/SFML/issues/346))
    * (Bugfix) Unicode characters outside the BMP (> 0xFFFF) are now correctly handled on Windows ([#366](https://github.com/SFML/SFML/issues/366))
  * **Graphics**
    * (Feature) Checking errors in RenderTarget::pushGLStates() to avoid generating false error messages when user leaves unchecked OpenGL errors ([#340](https://github.com/SFML/SFML/issues/340))
    * (Feature) Optimized Shader::setParameter functions, by using a cache internally ([#316](https://github.com/SFML/SFML/issues/316), [#358](https://github.com/SFML/SFML/issues/358))
    * (Bugfix) Fixed bounding rect of sf::Text ignoring whitespaces ([#216](https://github.com/SFML/SFML/issues/216))
    * (Bugfix) Solved graphics resources not updated or corrupted when loaded in a thread ([#411](https://github.com/SFML/SFML/issues/411))
    * (Bugfix) Fixed white pixel showing on first character of sf::Text ([#414](https://github.com/SFML/SFML/issues/414))
    * (Bugfix) sf::Rect::contains and sf::Rect::intersects now handle rectangles with negative dimensions correctly ([#219](https://github.com/SFML/SFML/issues/219))
    * (Bugfix) Fixed Shape::setTextureRect not working when called before setTexture
  * **Audio**
    * (Feature) loadFromStream functions now explicitly reset the stream (seek(0)) before starting to read ([#349](https://github.com/SFML/SFML/issues/349))
    * (Bugfix) Added a workaround for a bug in the OS X implementation of OpenAL (unsupported channel count no properly detected) ([#201](https://github.com/SFML/SFML/issues/201))
    * (Bugfix) Fixed SoundBuffer::loadFromStream reading past the end of the stream ([#214](https://github.com/SFML/SFML/issues/214))
  * **Network**
    * (Feature) Replaced the deprecated gethostbyname with getaddrinfo ([#47](https://github.com/SFML/SFML/issues/47))
    * (Feature) Minor improvements to sf::Packet operators (now using strlen and wcslen instead of explicit loops) ([#118](https://github.com/SFML/SFML/issues/118))
    * (Bugfix) Fixed non-blocking connection with a sf::TcpSocket on Windows
    * (Bugfix) Fixed TCP packet data corruption in non-blocking mode ([#402](https://github.com/SFML/SFML/issues/402), [#119](https://github.com/SFML/SFML/issues/119))
    * (Bugfix) On Unix systems, a socket disconnection no longer stops the program with signal SIGPIPE ([#72](https://github.com/SFML/SFML/issues/72))

## SFML 2.0

Also available on the website: http://www.sfml-dev.org/changelog.php#sfml-2.0

No changelog available. *Everything changed.*

# Older Releases

See the website for changelogs of older releases: http://www.sfml-dev.org/changelog.php
