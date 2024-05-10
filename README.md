# face-recognition-rest-api
This is a demo API built to demonstrate how to use face-api.js with nodejs, express and mongodb

More details about this can be found on the blog [here](https://medium.com/@rakesh_openai/build-face-recognition-as-a-rest-api-use-it-from-mobile-web-iot-etc-981c627cf15a) .


https://github.com/tensorflow/tfjs/issues/8064


when running this command: "node-gyp configure --verbose" in "node_modules@tensorflow\tfjs-node",
i get the following error:
gyp: Undefined variable module_name in binding.gyp while trying to load binding.gyp
gyp ERR! configure error
gyp ERR! stack Error: gyp failed with exit code: 1
gyp ERR! stack at ChildProcess. (C:\Users\ASUS\AppData\Roaming\nvm\v20.9.0\node_modules\node-gyp\lib\configure.js:270:18)
gyp ERR! stack at ChildProcess.emit (node:events:514:28)
gyp ERR! stack at ChildProcess._handle.onexit (node:internal/child_process:294:12)
gyp ERR! System Windows_NT 10.0.22621
gyp ERR! command "C:\Program Files\nodejs\node.exe" "C:\Program Files\nodejs\node_modules\node-gyp\bin\node-gyp.js" "configure" "--verbose"
gyp ERR! cwd C:\Users\ASUS\Desktop\tensorFlow\node_modules@tensorflow\tfjs-node
gyp ERR! node -v v20.9.0
gyp ERR! node-gyp -v v10.0.0
gyp ERR! not ok

any thoughts on how to fix this?


Thank you for bringing this issue to our attention, I see you're using the Node.js v20.9.0 version so could you please give it try by downgrading to Node.js v18.16.1 with python 3.8 or python 3.9 and try with npm install --save-exact @tensorflow/tfjs-node@3.18.0 

I believe you're referring this official documentation , TensorFlow.js Node.js bindings Windows troubleshooting., node-gyp on Windows

In general you'll have to follow below steps to install @tensorflow/tfjs-node on Windows system:

Edit the path user or system variable, ensure that the path to python is added to the path variable.
Install Visual Studio community edition with desktop development with C++ Link
Install visual studio build tools with the help of Visual Studio Installer
Ensure that node-gyp is available: npm install -g node-gyp
Install tfjs-node: npm install --save-exact @tensorflow/tfjs-node@3.18.0
After following above instructions If issue still persists please let us know with error log after running node-gyp configure --verbose command. Thank you.


https://github.com/vladmandic/face-api

