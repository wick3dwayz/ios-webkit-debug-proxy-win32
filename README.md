> **⚠️ No longer maintained**
>
> This project is no longer maintained. Windows support was introduced with [google/ios-webkit-debug-proxy#193](https://github.com/google/ios-webkit-debug-proxy/pull/193) in the original repo. You can find the latest binaries on the releases page of [google/ios-webkit-debug-proxy](https://github.com/google/ios-webkit-debug-proxy/releases).

iOS WebKit Debug Proxy Win32
============================

Win32 port of [ios-webkit-debug-proxy](https://github.com/google/ios-webkit-debug-proxy).

The ios-webkit-debug-proxy allows developers to inspect MobileSafari and UIWebViews on real and simulated iOS devices via the [Chrome DevTools UI](https://developer.chrome.com/docs/devtools/) and [WebKit Remote Debugging Protocol](https://webkit.org/blog/1620/webkit-remote-debugging/).  DevTools requests are translated into Apple's [Remote Web Inspector service](https://developer.apple.com/safari/tools/) calls.

For more info please refer to the original [README](https://github.com/google/ios-webkit-debug-proxy/blob/master/README.md).


Binaries
--------

Get the latest MSVC build from SourceForge:
- [Release build](http://sourceforge.net/projects/ios-webkit-debug-proxy-win32/files/ios-webkit-debug-proxy-win32.zip/download)
- [Debug build](http://sourceforge.net/projects/ios-webkit-debug-proxy-win32/files/ios-webkit-debug-proxy-win32-debug.zip/download)

MinGW32 builds (since the latest libimobiledevice libraries do not officially support MSVC):
- [MinGW32 Build](http://sourceforge.net/projects/ios-webkit-debug-proxy-win32/files/test-builds/ios-webkit-debug-proxy-mingw32.zip/download)
- [x64 Build](https://sourceforge.net/projects/ios-webkit-debug-proxy-win32/files/ios-webkit-debug-proxy-win64.zip/download)

Why a Win32 port?
-----------------

While you can use virtual machine software to compile and run the original ios-webkit-debug-proxy and forward USB/ports, having a native Windows port provides a much better developer experience.


Prerequisites
-------------

- **iTunes** must be installed (after installation you can safely remove iTunes from Programs and Features — just leave **Apple Mobile Device Support** and **Apple Application Support** installed)
- Visual Studio 2012 or 2013 (for MSVC builds)


Notes
-----

- The project compilation was tested with VS2012 and VS2013 only
- If you want to debug using Safari DevTools on Windows you may find [webkit-webinspector](https://github.com/artygus/webkit-webinspector) useful


Troubleshooting
---------------

| Symptom | Solution |
|---------|----------|
| `connect: No error` message | Check that the **Apple Mobile Device** service is running |
| Pages appear in device list but DevTools window is blank | Click the shield icon in the address bar and choose **"Load unsafe script"** |


Third Party Libraries
---------------------

Library | License | Project Link
------- | ------- | ----
libiconv\* | LGPL | https://www.gnu.org/software/libiconv/
libxml2\* | MIT | https://xmlsoft.org
openssl\* | OpenSSL | https://www.openssl.org
pcre\* | BSD | https://www.pcre.org
zlib\* | zlib | https://www.zlib.net
getopt | BSD | https://www.gnu.org/software/libc/ (win32 port: https://www.opensource.apple.com)
libimobiledevice | LGPL 2.1 | https://libimobiledevice.org (win32 port: https://github.com/MCE-KobyBo/libimobiledevice)
usbmuxd | LGPL 2.1 | https://libimobiledevice.org (win32 port: https://github.com/MCE-KobyBo/usbmuxd)
libplist | LGPL 2.1 | https://libimobiledevice.org (win32 port: https://github.com/MCE-KobyBo/libplist)


\* win32 binaries provided by https://gnuwin32.sourceforge.net
