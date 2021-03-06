## Introduction to Textual

Textual is a highly modified version of the open source project known as [LimeChat](https://github.com/psychs/limechat) created by Satoshi Nakagawa. Much of the app uses the open standard of [WebKit](http://webkit.org/) which makes customization easy through the use of CSS 3 and HTML 5. [Plugins](http://www.codeux.com/textual/help/Writing-Plugins.kb) written in Objective-C and [scripts](http://www.codeux.com/textual/help/Writing-Scripts.kb) made with AppleScript (and other languages) are also supported.

## Supporting Textual

Please do not abuse the power to build Textual in order to freely distribute it to hundreds of users. The copy of Textual in the Mac App Store helps fund the project. Therefore, what is asked, is asked out of respect so that the project can continue to thrive.

## Note Regarding Support

Please be aware that while it is within your right to compile Textual, **we will not provide support for the building process as it encourages use of potentially unstable code**. However, once built, [basic support](http://www.codeux.com/textual/help/Support.kb) for easy to answer questions related to the use of the application is still available.

## Note Regarding Code Signing

**It is HIGHLY DISCOURAGED to turn off code signing.** Certain features rely on the fact that Textual is properly signed and is within a sandboxed environment. 

For example, Textual uses security scoped bookmarks issued by the kernel to access certain resources outside of its sandbox. These bookmarks rely on the kernel knowing whether the copy of Textual that you are running is the same assigned to the bookmark. The kernel makes its judgements using identity defined by the certificate used for code signing. Therefore, if disabled, certain features such as logging to disk will never work because Textual wont be able to save the bookmark to the specified logging location.

Another example is that Textual may have difficulties accessing passwords when not code signed. This is a result of the OS X keychain internals relying on the trust defined by process of code signing.

## Building Textual

The latest version of Textual requires two things to be built. One is a valid (does not need to be issued by Apple) code signing certificate. The second is an installation of Xcode 6.1 or newer on OS X Yosemite. **Building on OS X Mavericks and earlier is not possible.**

If you are an Apple registered developer, then obtaining a signing certificate is not very difficult. However, if you are not, a self-signed certificate for "code signing" will do fine. The steps to produce one of these self-signed certificates is very simple to find using Google.

Once you have your code signing certificate, **do not modify the Build Settings of Textual through Xcode**. Instead,    modify the file at the path: **Resources ➜ Build Configurations ➜ Code Signing Identity.xcconfig** — The contents of this file define the name of the certificate which will be used for code signing.

After defining your code signing certificate, build Textual using the "Standard Release" build scheme.

## Original Limechat License

The source code of Limechat did not fall under its current GPL license at the time that the source code was forked in 2010. Its original license, at the time of the fork, is displayed below:

<pre>
The New BSD License

Copyright (c) 2008 - 2010 Satoshi Nakagawa < psychs AT limechat DOT net >
All rights reserved. 

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions
are met:
1. Redistributions of source code must retain the above copyright
   notice, this list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in the
   documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE AUTHOR AND CONTRIBUTORS ``AS IS'' AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
ARE DISCLAIMED.  IN NO EVENT SHALL THE AUTHOR OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS
OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
SUCH DAMAGE.
</pre>

## License for content originating from Textual

Textual has indirectly incorporated work from several open source projects. Acknowledgement of these can be found in the respective files that were contributed including licensing information for distribution.

Work that originated from the authors of Textual and were not contributed by other open source projects or from Limechat itself fall under the following license:

<pre>
Copyright (c) 2010 — 2014 Codeux Software, LLC & respective contributors.
      Please see Acknowledgements.pdf for additional information.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions
are met:

   * Redistributions of source code must retain the above copyright
     notice, this list of conditions and the following disclaimer.
   * Redistributions in binary form must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.
   * Neither the name of Textual and/or "Codeux Software, LLC", nor the 
     names of its contributors may be used to endorse or promote products 
     derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE AUTHOR AND CONTRIBUTORS ``AS IS'' AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
ARE DISCLAIMED. IN NO EVENT SHALL THE AUTHOR OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS
OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
SUCH DAMAGE.
</pre>
