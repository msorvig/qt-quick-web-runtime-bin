The Qt Quick Web Runtime Binary Distribution
============================================

The Qt Quick Web Runtime provides a JavaScript API for interpreting
QML and running Qt Quick in the browser. It is currently implemented
using Native Client (NaCl). This limits support to the Chrome browser.

Distribution
--------------------------------------------
The runtime binary distribution is LGPL-licensed and consists of
the following files:

    LICENSE                 LGPLv3 licence text
    qtquickruntime.js       Runtime public API
    qtloader.js             Qt loader API and implementation
    qtquickruntime.pexe     Runtime implementation + static Qt (Quick) build.
    qtquickruntime.nmf      NaCl manifest file
    qml/*                   qmldir files

In addition, this repository has an usage example:

    example.html
    example.png

Using
--------------------------------------------
Create the runtime object, create a DOM element, and set the source:

    var runtime = new QtQuickRuntime()
    var element = runtime.createElement()
    runtime.setSource(source)

See qtquickruntime.js for API documentation.

Source Code
--------------------------------------------
The qt-quick-web-runtime repository contains BSD-licensed sources:

    github.com/msorvig/qt-quick-web-runtime

If you are a Qt commercial license holder you can build your own binary using
your commercially licensed Qt, the BSD licensed Qt for NaCl port, and the BSD
licensed runtime.
