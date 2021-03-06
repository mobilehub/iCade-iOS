#iCade-iOS
Project which demonstrates using iCade with iPad.

##Demo
Pair up you iCade, run the project and you're off.

##Usage
To use in your own app, copy the following 3 files from the iCade folder:

* `iCadeReaderView.h`, `iCadeReaderView.m` and `iCadeState.h`

Add an instance of `iCadeReaderView` to your main game view, and call `[iCadeReaderView becomeFirstResponder]`
to ensure it receives the events from the iCade.  You can either read the `iCadeReaderView.iCadeState`
property to determine the current state, or implement the `iCadeEventDelegate` protocol on your target
to receive appropriate notifications.

### Note:
When `applicationWillResignActive:` is called, be sure to

	[iCadeReaderView resignFirstResponder];

When `applicationDidBecomeActive:` do the following to ensure the `iCadeReaderView` receives events again:

	[iCadeReaderView becomeFirstResponder];


##License
Copyright (C) 2011 by Stuart Carnie

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.


