# Compiling Terminus

> WSL is using version 2, the latest Ubuntu 20.04 and
> all commands were ran with Terminus using powershell , then wsl -d Ubuntu for everything after wsl installation.

### Installing WSL envrionment
```
wsl --install -d Ubuntu
wsl -d Ubuntu
```  

```
uname -a
Linux DESKTOP-NHA4S1K 5.10.16.3-microsoft-standard-WSL2 #1 SMP Fri Apr 2 22:23:49 UTC 2021 x86_64 x86_64 x86_64 GNU/Linux

lsb_release -a
Distributor ID: Ubuntu
Description:    Ubuntu 20.04 LTS
Release:        20.04
Codename:       focal
```  
Used this guide to install nodejs 14 (installed version was v14.17.1)
https://computingforgeeks.com/install-node-js-14-on-ubuntu-debian-linux/
(also installed the developer tools and yarn via the same page)  

git cloned and cd'd into the terminus repository. Current tag: 4db4d491877fc441e7ec1fc5a5a456a69373a081  

ran `yarn`  
Output:

```
terminus@DESKTOP-NHA4S1K:~/projects/terminus$ yarn
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
info dmg-license@1.0.8: The platform "linux" is incompatible with this module.
info "dmg-license@1.0.8" is an optional dependency and failed compatibility check. Excluding it from installation.
info iconv-corefoundation@1.1.5: The platform "linux" is incompatible with this module.
info "iconv-corefoundation@1.1.5" is an optional dependency and failed compatibility check. Excluding it from installation.
[3/4] Linking dependencies...
warning " > awesome-typescript-loader@5.2.1" has incorrect peer dependency "typescript@^2.7 || ^3".
warning " > pug-loader@2.4.0" has incorrect peer dependency "pug@^2.0.0".
warning abbrev@1.1.0: Invalid bin field for "abbrev".
warning ansicolors@0.3.2: Invalid bin field for "ansicolors".
warning ansistyles@0.1.3: Invalid bin field for "ansistyles".
warning archy@1.0.0: Invalid bin field for "archy".
warning call-limit@1.1.0: Invalid bin field for "call-limit".
warning bluebird@3.5.0: Invalid bin field for "bluebird".
warning chownr@1.0.1: Invalid bin field for "chownr".
warning cmd-shim@2.0.2: Invalid bin field for "cmd-shim".
warning columnify@1.5.4: Invalid bin field for "columnify".
warning config-chain@1.1.11: Invalid bin field for "config-chain".
warning debuglog@1.0.1: Invalid bin field for "debuglog".
warning detect-indent@5.0.0: Invalid bin field for "detect-indent".
warning dezalgo@1.0.3: Invalid bin field for "dezalgo".
warning editor@1.0.0: Invalid bin field for "editor".
warning fs-vacuum@1.2.10: Invalid bin field for "fs-vacuum".
warning fs-write-stream-atomic@1.0.10: Invalid bin field for "fs-write-stream-atomic".
warning fstream@1.0.11: Invalid bin field for "fstream".
warning graceful-fs@4.1.11: Invalid bin field for "graceful-fs".
warning has-unicode@2.0.1: Invalid bin field for "has-unicode".
warning iferr@0.1.5: Invalid bin field for "iferr".
warning imurmurhash@0.1.4: Invalid bin field for "imurmurhash".
warning inflight@1.0.6: Invalid bin field for "inflight".
warning inherits@2.0.3: Invalid bin field for "inherits".
warning ini@1.3.4: Invalid bin field for "ini".
warning init-package-json@1.10.1: Invalid bin field for "init-package-json".
warning lazy-property@1.0.0: Invalid bin field for "lazy-property".
warning lockfile@1.0.3: Invalid bin field for "lockfile".
warning lodash._baseindexof@3.1.0: Invalid bin field for "lodash._baseindexof".
warning lodash._baseuniq@4.6.0: Invalid bin field for "lodash._baseuniq".
warning lodash._bindcallback@3.0.1: Invalid bin field for "lodash._bindcallback".
warning lodash._cacheindexof@3.0.2: Invalid bin field for "lodash._cacheindexof".
warning lodash._createcache@3.1.2: Invalid bin field for "lodash._createcache".
warning lodash._getnative@3.9.1: Invalid bin field for "lodash._getnative".
warning lodash.clonedeep@4.5.0: Invalid bin field for "lodash.clonedeep".
warning lodash.restparam@3.6.1: Invalid bin field for "lodash.restparam".
warning lodash.union@4.6.0: Invalid bin field for "lodash.union".
warning lodash.uniq@4.5.0: Invalid bin field for "lodash.uniq".
warning lodash.without@4.4.0: Invalid bin field for "lodash.without".
warning mississippi@1.3.0: Invalid bin field for "mississippi".
warning move-concurrently@1.0.1: Invalid bin field for "move-concurrently".
warning npm-cache-filename@1.0.2: Invalid bin field for "npm-cache-filename".
warning npm-install-checks@3.0.0: Invalid bin field for "npm-install-checks".
warning once@1.4.0: Invalid bin field for "once".
warning osenv@0.1.4: Invalid bin field for "osenv".
warning path-is-inside@1.0.2: Invalid bin field for "path-is-inside".
warning promise-inflight@1.0.1: Invalid bin field for "promise-inflight".
warning read@1.0.7: Invalid bin field for "read".
warning read-cmd-shim@1.0.1: Invalid bin field for "read-cmd-shim".
warning read-installed@4.0.3: Invalid bin field for "read-installed".
warning readdir-scoped-modules@1.0.2: Invalid bin field for "readdir-scoped-modules".
warning retry@0.10.1: Invalid bin field for "retry".
warning sha@2.0.1: Invalid bin field for "sha".
warning slide@1.1.6: Invalid bin field for "slide".
warning sorted-object@2.0.1: Invalid bin field for "sorted-object".
warning sorted-union-stream@2.1.3: Invalid bin field for "sorted-union-stream".
warning tar@2.2.1: Invalid bin field for "tar".
warning text-table@0.2.0: Invalid bin field for "text-table".
warning uid-number@0.0.6: Invalid bin field for "uid-number".
warning umask@1.1.0: Invalid bin field for "umask".
warning unique-filename@1.1.0: Invalid bin field for "unique-filename".
warning unpipe@1.0.0: Invalid bin field for "unpipe".
warning validate-npm-package-license@3.0.1: Invalid bin field for "validate-npm-package-license".
warning validate-npm-package-name@3.0.0: Invalid bin field for "validate-npm-package-name".
warning wrappy@1.0.2: Invalid bin field for "wrappy".
[4/4] Building fresh packages...
$ node ./scripts/install-deps.js
info deps app
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
info macos-native-processlist@2.0.0: The platform "linux" is incompatible with this module.
info "macos-native-processlist@2.0.0" is an optional dependency and failed compatibility check. Excluding it from installation.
info windows-blurbehind@1.0.1: The platform "linux" is incompatible with this module.
info "windows-blurbehind@1.0.1" is an optional dependency and failed compatibility check. Excluding it from installation.
info windows-native-registry@3.0.0: The platform "linux" is incompatible with this module.
info "windows-native-registry@3.0.0" is an optional dependency and failed compatibility check. Excluding it from installation.
info windows-process-tree@0.3.0: The platform "linux" is incompatible with this module.
info "windows-process-tree@0.3.0" is an optional dependency and failed compatibility check. Excluding it from installation.
[3/4] Linking dependencies...
warning " > @angular/common@12.0.0" has incorrect peer dependency "rxjs@^6.5.3".
warning " > @angular/core@12.0.0" has incorrect peer dependency "rxjs@^6.5.3".
warning " > @angular/forms@12.0.0" has incorrect peer dependency "rxjs@^6.5.3".
warning " > @electron/remote@1.2.0" has unmet peer dependency "electron@>= 10.0.0-beta.1".
warning " > @ng-bootstrap/ng-bootstrap@9.1.1" has incorrect peer dependency "@angular/common@^11.0.0".
warning " > @ng-bootstrap/ng-bootstrap@9.1.1" has incorrect peer dependency "@angular/core@^11.0.0".
warning " > @ng-bootstrap/ng-bootstrap@9.1.1" has incorrect peer dependency "@angular/forms@^11.0.0".
warning " > @ng-bootstrap/ng-bootstrap@9.1.1" has unmet peer dependency "@angular/localize@^11.0.0".
warning " > @ng-bootstrap/ng-bootstrap@9.1.1" has incorrect peer dependency "rxjs@^6.5.5".
warning " > electron-promise-ipc@2.2.4" has unmet peer dependency "electron@>= 9.1.2".
[4/4] Rebuilding all packages...
error /home/terminus/projects/terminus/app/node_modules/fontmanager-redux: Command failed.
Exit code: 1
Command: node-gyp rebuild
Arguments:
Directory: /home/terminus/projects/terminus/app/node_modules/fontmanager-redux
Output:
gyp info it worked if it ends with ok
gyp info using node-gyp@5.1.0
gyp info using node@14.17.1 | linux | x64
gyp info find Python using Python version 3.8.2 found at "/usr/bin/python3"
gyp http GET https://nodejs.org/download/release/v14.17.1/node-v14.17.1-headers.tar.gz
gyp http 200 https://nodejs.org/download/release/v14.17.1/node-v14.17.1-headers.tar.gz
gyp http GET https://nodejs.org/download/release/v14.17.1/SHASUMS256.txt
gyp http 200 https://nodejs.org/download/release/v14.17.1/SHASUMS256.txt
gyp info spawn /usr/bin/python3
gyp info spawn args [
gyp info spawn args   '/usr/lib/node_modules/npm/node_modules/node-gyp/gyp/gyp_main.py',
gyp info spawn args   'binding.gyp',
gyp info spawn args   '-f',
gyp info spawn args   'make',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/projects/terminus/app/node_modules/fontmanager-redux/build/config.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/usr/lib/node_modules/npm/node_modules/node-gyp/addon.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/.cache/node-gyp/14.17.1/include/node/common.gypi',
gyp info spawn args   '-Dlibrary=shared_library',
gyp info spawn args   '-Dvisibility=default',
gyp info spawn args   '-Dnode_root_dir=/home/terminus/.cache/node-gyp/14.17.1',
gyp info spawn args   '-Dnode_gyp_dir=/usr/lib/node_modules/npm/node_modules/node-gyp',
gyp info spawn args   '-Dnode_lib_file=/home/terminus/.cache/node-gyp/14.17.1/<(target_arch)/node.lib',
gyp info spawn args   '-Dmodule_root_dir=/home/terminus/projects/terminus/app/node_modules/fontmanager-redux',
gyp info spawn args   '-Dnode_engine=v8',
gyp info spawn args   '--depth=.',
gyp info spawn args   '--no-parallel',
gyp info spawn args   '--generator-output',
gyp info spawn args   'build',
gyp info spawn args   '-Goutput_dir=.'
gyp info spawn args ]
gyp info spawn make
gyp info spawn args [ 'BUILDTYPE=Release', '-C', 'build' ]
make: Entering directory '/home/terminus/projects/terminus/app/node_modules/fontmanager-redux/build'
  CXX(target) Release/obj.target/fontmanager/src/FontManager.o
  CXX(target) Release/obj.target/fontmanager/src/FontManagerLinux.o
../src/FontManagerLinux.cc:1:10: fatal error: fontconfig/fontconfig.h: No such file or directory
    1 | #include <fontconfig/fontconfig.h>
      |          ^~~~~~~~~~~~~~~~~~~~~~~~~
compilation terminated.
make: *** [fontmanager.target.mk:110: Release/obj.target/fontmanager/src/FontManagerLinux.o] Error 1
make: Leaving directory '/home/terminus/projects/terminus/app/node_modules/fontmanager-redux/build'
gyp ERR! build error
gyp ERR! stack Error: `make` failed with exit code: 2
gyp ERR! stack     at ChildProcess.onExit (/usr/lib/node_modules/npm/node_modules/node-gyp/lib/build.js:194:23)
gyp ERR! stack     at ChildProcess.emit (events.js:375:28)
gyp ERR! stack     at Process.ChildProcess._handle.onexit (internal/child_process.js:277:12)
gyp ERR! System Linux 5.10.16.3-microsoft-standard-WSL2
gyp ERR! command "/usr/bin/node" "/usr/lib/node_modules/npm/node_modules/node-gyp/bin/node-gyp.js" "rebuild"
gyp ERR! cwd /home/terminus/projects/terminus/app/node_modules/fontmanager-redux
gyp ERR! node -v v14.17.1
gyp ERR! node-gyp -v v5.1.0
gyp ERR! not ok
info Visit https://yarnpkg.com/en/docs/cli/install for documentation about this command.
yarn install v1.22.5
warning package.json: No license field
warning No license field
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 4.35s.
info deps terminus-core
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
warning " > bootstrap@4.5.3" has unmet peer dependency "jquery@1.9.1 - 3".
warning " > bootstrap@4.5.3" has unmet peer dependency "popper.js@^1.16.1".
warning " > ng2-dnd@5.0.2" has unmet peer dependency "@angular/core@^4.0.0 || ^5.0.0".
warning " > ng2-dnd@5.0.2" has unmet peer dependency "@angular/forms@^4.0.0 || ^5.0.0".
warning " > ngx-perfect-scrollbar@10.1.1" has unmet peer dependency "@angular/common@>=9.0.0".
warning " > ngx-perfect-scrollbar@10.1.1" has unmet peer dependency "@angular/core@>=9.0.0".
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 4.80s.
info deps terminus-settings
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 2.59s.
info deps terminus-terminal
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 4.23s.
info deps terminus-electron
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
warning " > electron-promise-ipc@2.2.4" has unmet peer dependency "electron@>= 9.1.2".
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 2.21s.
info deps terminus-local
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 1.99s.
info deps terminus-web
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
warning " > bootstrap@4.6.0" has unmet peer dependency "jquery@1.9.1 - 3".
warning " > bootstrap@4.6.0" has unmet peer dependency "popper.js@^1.16.1".
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 4.41s.
info deps terminus-community-color-schemes
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 0.06s.
info deps terminus-plugin-manager
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 0.63s.
info deps terminus-ssh
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Rebuilding all packages...
warning Error running install script for optional dependency: "/home/terminus/projects/terminus/terminus-ssh/node_modules/cpu-features: Command failed.
Exit code: 1
Command: node-gyp rebuild
Arguments:
Directory: /home/terminus/projects/terminus/terminus-ssh/node_modules/cpu-features
Output:
gyp info it worked if it ends with ok
gyp info using node-gyp@5.1.0
gyp info using node@14.17.1 | linux | x64
gyp info find Python using Python version 3.8.2 found at \"/usr/bin/python3\"
gyp info spawn /usr/bin/python3
gyp info spawn args [
gyp info spawn args   '/usr/lib/node_modules/npm/node_modules/node-gyp/gyp/gyp_main.py',
gyp info spawn args   'binding.gyp',
gyp info spawn args   '-f',
gyp info spawn args   'make',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/projects/terminus/terminus-ssh/node_modules/cpu-features/build/config.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/usr/lib/node_modules/npm/node_modules/node-gyp/addon.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/.cache/node-gyp/14.17.1/include/node/common.gypi',
gyp info spawn args   '-Dlibrary=shared_library',
gyp info spawn args   '-Dvisibility=default',
gyp info spawn args   '-Dnode_root_dir=/home/terminus/.cache/node-gyp/14.17.1',
gyp info spawn args   '-Dnode_gyp_dir=/usr/lib/node_modules/npm/node_modules/node-gyp',
gyp info spawn args   '-Dnode_lib_file=/home/terminus/.cache/node-gyp/14.17.1/<(target_arch)/node.lib',
gyp info spawn args   '-Dmodule_root_dir=/home/terminus/projects/terminus/terminus-ssh/node_modules/cpu-features',
gyp info spawn args   '-Dnode_engine=v8',
gyp info spawn args   '--depth=.',
gyp info spawn args   '--no-parallel',
gyp info spawn args   '--generator-output',
gyp info spawn args   'build',
gyp info spawn args   '-Goutput_dir=.'
gyp info spawn args ]
gyp info spawn make
gyp info spawn args [ 'BUILDTYPE=Release', '-C', 'build' ]
make: Entering directory '/home/terminus/projects/terminus/terminus-ssh/node_modules/cpu-features/build'
  ACTION Configuring dependencies /home/terminus/projects/terminus/terminus-ssh/node_modules/cpu-features/deps/cpu_features/build/Makefile
/bin/sh: 1: cmake: not found
make: *** [config_deps.target.mk:13: /home/terminus/projects/terminus/terminus-ssh/node_modules/cpu-features/deps/cpu_features/build/Makefile] Error 127
make: Leaving directory '/home/terminus/projects/terminus/terminus-ssh/node_modules/cpu-features/build'
gyp ERR! build error
gyp ERR! stack Error: `make` failed with exit code: 2
gyp ERR! stack     at ChildProcess.onExit (/usr/lib/node_modules/npm/node_modules/node-gyp/lib/build.js:194:23)
gyp ERR! stack     at ChildProcess.emit (events.js:375:28)
gyp ERR! stack     at Process.ChildProcess._handle.onexit (internal/child_process.js:277:12)
gyp ERR! System Linux 5.10.16.3-microsoft-standard-WSL2
gyp ERR! command \"/usr/bin/node\" \"/usr/lib/node_modules/npm/node_modules/node-gyp/bin/node-gyp.js\" \"rebuild\"
gyp ERR! cwd /home/terminus/projects/terminus/terminus-ssh/node_modules/cpu-features
gyp ERR! node -v v14.17.1
gyp ERR! node-gyp -v v5.1.0
gyp ERR! not ok"
info This module is OPTIONAL, you can safely ignore this error
success Saved lockfile.
$ run-script-os
yarn run v1.22.5
$ exit
Done in 0.06s.
Done in 6.37s.
info deps terminus-serial
yarn install v1.22.5
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Rebuilding all packages...
success Saved lockfile.
Done in 1.34s.
Done in 157.53s.
```  
Ran build-native.js
`./scripts/build-native.js`  
Output: 

```
Building against Electron 13.1.4
Rebuilding app/bindings
gyp info find Python using Python version 3.8.2 found at "/usr/bin/python3"
gyp http GET https://www.electronjs.org/headers/v13.1.4/node-v13.1.4-headers.tar.gz
gyp http 200 https://www.electronjs.org/headers/v13.1.4/node-v13.1.4-headers.tar.gz
gyp http GET https://www.electronjs.org/headers/v13.1.4/SHASUMS256.txt
gyp http 200 https://www.electronjs.org/headers/v13.1.4/SHASUMS256.txt
gyp info spawn /usr/bin/python3
gyp info spawn args [
gyp info spawn args   '/home/terminus/projects/terminus/node_modules/node-gyp/gyp/gyp_main.py',
gyp info spawn args   'binding.gyp',
gyp info spawn args   '-f',
gyp info spawn args   'make',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/projects/terminus/app/node_modules/@serialport/bindings/build/config.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/projects/terminus/node_modules/node-gyp/addon.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/.electron-gyp/13.1.4/include/node/common.gypi',
gyp info spawn args   '-Dlibrary=shared_library',
gyp info spawn args   '-Dvisibility=default',
gyp info spawn args   '-Dnode_root_dir=/home/terminus/.electron-gyp/13.1.4',
gyp info spawn args   '-Dnode_gyp_dir=/home/terminus/projects/terminus/node_modules/node-gyp',
gyp info spawn args   '-Dnode_lib_file=/home/terminus/.electron-gyp/13.1.4/<(target_arch)/node.lib',
gyp info spawn args   '-Dmodule_root_dir=/home/terminus/projects/terminus/app/node_modules/@serialport/bindings',
gyp info spawn args   '-Dnode_engine=v8',
gyp info spawn args   '--depth=.',
gyp info spawn args   '--no-parallel',
gyp info spawn args   '--generator-output',
gyp info spawn args   'build',
gyp info spawn args   '-Goutput_dir=.'
gyp info spawn args ]
gyp info spawn make
gyp info spawn args [ 'BUILDTYPE=Release', '-C', 'build' ]
make: Entering directory '/home/terminus/projects/terminus/app/node_modules/@serialport/bindings/build'
  CXX(target) Release/obj.target/bindings/src/serialport.o
In file included from /home/terminus/.electron-gyp/13.1.4/include/node/node.h:67,
                 from ../../../nan/nan.h:56,
                 from ../src/./serialport.h:13,
                 from ../src/serialport.cpp:1:
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:1670:79: warning: ‘using ResolveCallback = class v8::MaybeLocal<v8::Module> (*)(class v8::Local<v8::Context>, class v8::Local<v8::String>, class v8::Local<v8::Module>)’ is deprecated: Use ResolveModuleCallback [-Wdeprecated-declarations]
 1670 |                                                       ResolveCallback callback);
      |                                                                               ^
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:1652:9: note: declared here
 1652 |   using ResolveCallback V8_DEPRECATE_SOON("Use ResolveModuleCallback") =
      |         ^~~~~~~~~~~~~~~
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:8652:51: warning: ‘using HostImportModuleDynamicallyCallback = class v8::MaybeLocal<v8::Promise> (*)(class v8::Local<v8::Context>, class v8::Local<v8::ScriptOrModule>, class v8::Local<v8::String>)’ is deprecated: Use HostImportModuleDynamicallyWithImportAssertionsCallback instead [-Wdeprecated-declarations]
 8652 |       HostImportModuleDynamicallyCallback callback);
      |                                                   ^
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:7291:7: note: declared here
 7291 | using HostImportModuleDynamicallyCallback V8_DEPRECATE_SOON(
      |       ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
../src/serialport.cpp: In function ‘Nan::NAN_METHOD_RETURN_TYPE Open(Nan::NAN_METHOD_ARGS_TYPE)’:
../src/serialport.cpp:78:69: warning: cast between incompatible function types from ‘void (*)(uv_work_t*)’ {aka ‘void (*)(uv_work_s*)’} to ‘uv_after_work_cb’ {aka ‘void (*)(uv_work_s*, int)’} [-Wcast-function-type]
   78 |   uv_queue_work(uv_default_loop(), req, EIO_Open, (uv_after_work_cb)EIO_AfterOpen);
      |                                                                     ^~~~~~~~~~~~~
../src/serialport.cpp: In function ‘Nan::NAN_METHOD_RETURN_TYPE Update(Nan::NAN_METHOD_ARGS_TYPE)’:
../src/serialport.cpp:135:71: warning: cast between incompatible function types from ‘void (*)(uv_work_t*)’ {aka ‘void (*)(uv_work_s*)’} to ‘uv_after_work_cb’ {aka ‘void (*)(uv_work_s*, int)’} [-Wcast-function-type]
  135 |   uv_queue_work(uv_default_loop(), req, EIO_Update, (uv_after_work_cb)EIO_AfterUpdate);
      |                                                                       ^~~~~~~~~~~~~~~
../src/serialport.cpp: In function ‘Nan::NAN_METHOD_RETURN_TYPE Close(Nan::NAN_METHOD_ARGS_TYPE)’:
../src/serialport.cpp:175:70: warning: cast between incompatible function types from ‘void (*)(uv_work_t*)’ {aka ‘void (*)(uv_work_s*)’} to ‘uv_after_work_cb’ {aka ‘void (*)(uv_work_s*, int)’} [-Wcast-function-type]
  175 |   uv_queue_work(uv_default_loop(), req, EIO_Close, (uv_after_work_cb)EIO_AfterClose);
      |                                                                      ^~~~~~~~~~~~~~
../src/serialport.cpp: In function ‘Nan::NAN_METHOD_RETURN_TYPE Flush(Nan::NAN_METHOD_ARGS_TYPE)’:
../src/serialport.cpp:215:70: warning: cast between incompatible function types from ‘void (*)(uv_work_t*)’ {aka ‘void (*)(uv_work_s*)’} to ‘uv_after_work_cb’ {aka ‘void (*)(uv_work_s*, int)’} [-Wcast-function-type]
  215 |   uv_queue_work(uv_default_loop(), req, EIO_Flush, (uv_after_work_cb)EIO_AfterFlush);
      |                                                                      ^~~~~~~~~~~~~~
../src/serialport.cpp: In function ‘Nan::NAN_METHOD_RETURN_TYPE Set(Nan::NAN_METHOD_ARGS_TYPE)’:
../src/serialport.cpp:271:68: warning: cast between incompatible function types from ‘void (*)(uv_work_t*)’ {aka ‘void (*)(uv_work_s*)’} to ‘uv_after_work_cb’ {aka ‘void (*)(uv_work_s*, int)’} [-Wcast-function-type]
  271 |   uv_queue_work(uv_default_loop(), req, EIO_Set, (uv_after_work_cb)EIO_AfterSet);
      |                                                                    ^~~~~~~~~~~~
../src/serialport.cpp: In function ‘Nan::NAN_METHOD_RETURN_TYPE Get(Nan::NAN_METHOD_ARGS_TYPE)’:
../src/serialport.cpp:316:68: warning: cast between incompatible function types from ‘void (*)(uv_work_t*)’ {aka ‘void (*)(uv_work_s*)’} to ‘uv_after_work_cb’ {aka ‘void (*)(uv_work_s*, int)’} [-Wcast-function-type]
  316 |   uv_queue_work(uv_default_loop(), req, EIO_Get, (uv_after_work_cb)EIO_AfterGet);
      |                                                                    ^~~~~~~~~~~~
../src/serialport.cpp: In function ‘Nan::NAN_METHOD_RETURN_TYPE GetBaudRate(Nan::NAN_METHOD_ARGS_TYPE)’:
../src/serialport.cpp:366:76: warning: cast between incompatible function types from ‘void (*)(uv_work_t*)’ {aka ‘void (*)(uv_work_s*)’} to ‘uv_after_work_cb’ {aka ‘void (*)(uv_work_s*, int)’} [-Wcast-function-type]
  366 |   uv_queue_work(uv_default_loop(), req, EIO_GetBaudRate, (uv_after_work_cb)EIO_AfterGetBaudRate);
      |                                                                            ^~~~~~~~~~~~~~~~~~~~
../src/serialport.cpp: In function ‘Nan::NAN_METHOD_RETURN_TYPE Drain(Nan::NAN_METHOD_ARGS_TYPE)’:
../src/serialport.cpp:412:70: warning: cast between incompatible function types from ‘void (*)(uv_work_t*)’ {aka ‘void (*)(uv_work_s*)’} to ‘uv_after_work_cb’ {aka ‘void (*)(uv_work_s*, int)’} [-Wcast-function-type]
  412 |   uv_queue_work(uv_default_loop(), req, EIO_Drain, (uv_after_work_cb)EIO_AfterDrain);
      |                                                                      ^~~~~~~~~~~~~~
../src/serialport.cpp: At global scope:
../src/serialport.cpp:433:28: warning: unnecessary parentheses in declaration of ‘ToParityEnum’ [-Wparentheses]
  433 | SerialPortParity NAN_INLINE(ToParityEnum(const v8::Local<v8::String>& v8str)) {
      |                            ^
../src/serialport.cpp:452:30: warning: unnecessary parentheses in declaration of ‘ToStopBitEnum’ [-Wparentheses]
  452 | SerialPortStopBits NAN_INLINE(ToStopBitEnum(double stopBits)) {
      |                              ^
In file included from ../../../nan/nan.h:56,
                 from ../src/./serialport.h:13,
                 from ../src/serialport.cpp:1:
/home/terminus/.electron-gyp/13.1.4/include/node/node.h:770:43: warning: cast between incompatible function types from ‘void (*)(Nan::ADDON_REGISTER_FUNCTION_ARGS_TYPE)’ {aka ‘void (*)(v8::Local<v8::Object>)’} to ‘node::addon_register_func’ {aka ‘void (*)(v8::Local<v8::Object>, v8::Local<v8::Value>, void*)’} [-Wcast-function-type]
  770 |       (node::addon_register_func) (regfunc),                          \
      |                                           ^
/home/terminus/.electron-gyp/13.1.4/include/node/node.h:804:3: note: in expansion of macro ‘NODE_MODULE_X’
  804 |   NODE_MODULE_X(modname, regfunc, NULL, 0)  // NOLINT (readability/null_usage)
      |   ^~~~~~~~~~~~~
../src/serialport.cpp:486:1: note: in expansion of macro ‘NODE_MODULE’
  486 | NODE_MODULE(serialport, init);
      | ^~~~~~~~~~~
  CXX(target) Release/obj.target/bindings/src/serialport_unix.o
In file included from /home/terminus/.electron-gyp/13.1.4/include/node/node.h:67,
                 from ../../../nan/nan.h:56,
                 from ../src/serialport.h:13,
                 from ../src/serialport_unix.cpp:2:
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:1670:79: warning: ‘using ResolveCallback = class v8::MaybeLocal<v8::Module> (*)(class v8::Local<v8::Context>, class v8::Local<v8::String>, class v8::Local<v8::Module>)’ is deprecated: Use ResolveModuleCallback [-Wdeprecated-declarations]
 1670 |                                                       ResolveCallback callback);
      |                                                                               ^
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:1652:9: note: declared here
 1652 |   using ResolveCallback V8_DEPRECATE_SOON("Use ResolveModuleCallback") =
      |         ^~~~~~~~~~~~~~~
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:8652:51: warning: ‘using HostImportModuleDynamicallyCallback = class v8::MaybeLocal<v8::Promise> (*)(class v8::Local<v8::Context>, class v8::Local<v8::ScriptOrModule>, class v8::Local<v8::String>)’ is deprecated: Use HostImportModuleDynamicallyWithImportAssertionsCallback instead [-Wdeprecated-declarations]
 8652 |       HostImportModuleDynamicallyCallback callback);
      |                                                   ^
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:7291:7: note: declared here
 7291 | using HostImportModuleDynamicallyCallback V8_DEPRECATE_SOON(
      |       ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
../src/serialport_unix.cpp: In function ‘int setup(int, OpenBaton*)’:
../src/serialport_unix.cpp:176:82: warning: ‘%s’ directive output may be truncated writing up to 1023 bytes into a region of size 1005 [-Wformat-truncation=]
  176 |     snprintf(data->errorString, sizeof(data->errorString), "Error %s Cannot open %s", strerror(errno), data->path);
      |                                                                                  ^~
In file included from /usr/include/stdio.h:867,
                 from ../src/serialport.h:10,
                 from ../src/serialport_unix.cpp:2:
/usr/include/x86_64-linux-gnu/bits/stdio2.h:67:35: note: ‘__builtin___snprintf_chk’ output 20 or more bytes (assuming 1043) into a destination of size 1024
   67 |   return __builtin___snprintf_chk (__s, __n, __USE_FORTIFY_LEVEL - 1,
      |          ~~~~~~~~~~~~~~~~~~~~~~~~~^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
   68 |        __bos (__s), __fmt, __va_arg_pack ());
      |        ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
../src/serialport_unix.cpp: In function ‘void EIO_Open(uv_work_t*)’:
../src/serialport_unix.cpp:86:84: warning: ‘%s’ directive output may be truncated writing up to 1023 bytes into a region of size 1003 [-Wformat-truncation=]
   86 |     snprintf(data->errorString, sizeof(data->errorString), "Error: %s, cannot open %s", strerror(errno), data->path);
      |                                                                                    ^~
In file included from /usr/include/stdio.h:867,
                 from ../src/serialport.h:10,
                 from ../src/serialport_unix.cpp:2:
/usr/include/x86_64-linux-gnu/bits/stdio2.h:67:35: note: ‘__builtin___snprintf_chk’ output 22 or more bytes (assuming 1045) into a destination of size 1024
   67 |   return __builtin___snprintf_chk (__s, __n, __USE_FORTIFY_LEVEL - 1,
      |          ~~~~~~~~~~~~~~~~~~~~~~~~~^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
   68 |        __bos (__s), __fmt, __va_arg_pack ());
      |        ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  CXX(target) Release/obj.target/bindings/src/poller.o
In file included from /home/terminus/.electron-gyp/13.1.4/include/node/node.h:67,
                 from ../../../nan/nan.h:56,
                 from ../src/poller.cpp:1:
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:1670:79: warning: ‘using ResolveCallback = class v8::MaybeLocal<v8::Module> (*)(class v8::Local<v8::Context>, class v8::Local<v8::String>, class v8::Local<v8::Module>)’ is deprecated: Use ResolveModuleCallback [-Wdeprecated-declarations]
 1670 |                                                       ResolveCallback callback);
      |                                                                               ^
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:1652:9: note: declared here
 1652 |   using ResolveCallback V8_DEPRECATE_SOON("Use ResolveModuleCallback") =
      |         ^~~~~~~~~~~~~~~
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:8652:51: warning: ‘using HostImportModuleDynamicallyCallback = class v8::MaybeLocal<v8::Promise> (*)(class v8::Local<v8::Context>, class v8::Local<v8::ScriptOrModule>, class v8::Local<v8::String>)’ is deprecated: Use HostImportModuleDynamicallyWithImportAssertionsCallback instead [-Wdeprecated-declarations]
 8652 |       HostImportModuleDynamicallyCallback callback);
      |                                                   ^
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:7291:7: note: declared here
 7291 | using HostImportModuleDynamicallyCallback V8_DEPRECATE_SOON(
      |       ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  CXX(target) Release/obj.target/bindings/src/serialport_linux.o
  SOLINK_MODULE(target) Release/obj.target/bindings.node
  COPY Release/bindings.node
make: Leaving directory '/home/terminus/projects/terminus/app/node_modules/@serialport/bindings/build'
Rebuilding app/node-pty
gyp info find Python using Python version 3.8.2 found at "/usr/bin/python3"
gyp info spawn /usr/bin/python3
gyp info spawn args [
gyp info spawn args   '/home/terminus/projects/terminus/node_modules/node-gyp/gyp/gyp_main.py',
gyp info spawn args   'binding.gyp',
gyp info spawn args   '-f',
gyp info spawn args   'make',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/projects/terminus/app/node_modules/@terminus-term/node-pty/build/config.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/projects/terminus/node_modules/node-gyp/addon.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/.electron-gyp/13.1.4/include/node/common.gypi',
gyp info spawn args   '-Dlibrary=shared_library',
gyp info spawn args   '-Dvisibility=default',
gyp info spawn args   '-Dnode_root_dir=/home/terminus/.electron-gyp/13.1.4',
gyp info spawn args   '-Dnode_gyp_dir=/home/terminus/projects/terminus/node_modules/node-gyp',
gyp info spawn args   '-Dnode_lib_file=/home/terminus/.electron-gyp/13.1.4/<(target_arch)/node.lib',
gyp info spawn args   '-Dmodule_root_dir=/home/terminus/projects/terminus/app/node_modules/@terminus-term/node-pty',
gyp info spawn args   '-Dnode_engine=v8',
gyp info spawn args   '--depth=.',
gyp info spawn args   '--no-parallel',
gyp info spawn args   '--generator-output',
gyp info spawn args   'build',
gyp info spawn args   '-Goutput_dir=.'
gyp info spawn args ]
gyp info spawn make
gyp info spawn args [ 'BUILDTYPE=Release', '-C', 'build' ]
make: Entering directory '/home/terminus/projects/terminus/app/node_modules/@terminus-term/node-pty/build'
  CXX(target) Release/obj.target/pty/src/unix/pty.o
In file included from /home/terminus/.electron-gyp/13.1.4/include/node/node.h:67,
                 from ../../../nan/nan.h:56,
                 from ../src/unix/pty.cc:20:
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:1670:79: warning: ‘using ResolveCallback = class v8::MaybeLocal<v8::Module> (*)(class v8::Local<v8::Context>, class v8::Local<v8::String>, class v8::Local<v8::Module>)’ is deprecated: Use ResolveModuleCallback [-Wdeprecated-declarations]
 1670 |                                                       ResolveCallback callback);
      |                                                                               ^
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:1652:9: note: declared here
 1652 |   using ResolveCallback V8_DEPRECATE_SOON("Use ResolveModuleCallback") =
      |         ^~~~~~~~~~~~~~~
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:8652:51: warning: ‘using HostImportModuleDynamicallyCallback = class v8::MaybeLocal<v8::Promise> (*)(class v8::Local<v8::Context>, class v8::Local<v8::ScriptOrModule>, class v8::Local<v8::String>)’ is deprecated: Use HostImportModuleDynamicallyWithImportAssertionsCallback instead [-Wdeprecated-declarations]
 8652 |       HostImportModuleDynamicallyCallback callback);
      |                                                   ^
/home/terminus/.electron-gyp/13.1.4/include/node/v8.h:7291:7: note: declared here
 7291 | using HostImportModuleDynamicallyCallback V8_DEPRECATE_SOON(
      |       ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
../src/unix/pty.cc: In function ‘void pty_after_waitpid(uv_async_t*)’:
../src/unix/pty.cc:512:43: warning: ‘void* memset(void*, int, size_t)’ writing to an object of type ‘class Nan::Persistent<v8::Function>’ with no trivial copy-assignment [-Wclass-memaccess]
  512 |   memset(&baton->cb, -1, sizeof(baton->cb));
      |                                           ^
In file included from ../../../nan/nan.h:405,
                 from ../src/unix/pty.cc:20:
../../../nan/nan_persistent_12_inl.h:12:40: note: ‘class Nan::Persistent<v8::Function>’ declared here
   12 | template<typename T, typename M> class Persistent :
      |                                        ^~~~~~~~~~
In file included from ../../../nan/nan.h:56,
                 from ../src/unix/pty.cc:20:
../src/unix/pty.cc: At global scope:
/home/terminus/.electron-gyp/13.1.4/include/node/node.h:770:43: warning: cast between incompatible function types from ‘void (*)(Nan::ADDON_REGISTER_FUNCTION_ARGS_TYPE)’ {aka ‘void (*)(v8::Local<v8::Object>)’} to ‘node::addon_register_func’ {aka ‘void (*)(v8::Local<v8::Object>, v8::Local<v8::Value>, void*)’} [-Wcast-function-type]
  770 |       (node::addon_register_func) (regfunc),                          \
      |                                           ^
/home/terminus/.electron-gyp/13.1.4/include/node/node.h:804:3: note: in expansion of macro ‘NODE_MODULE_X’
  804 |   NODE_MODULE_X(modname, regfunc, NULL, 0)  // NOLINT (readability/null_usage)
      |   ^~~~~~~~~~~~~
../src/unix/pty.cc:734:1: note: in expansion of macro ‘NODE_MODULE’
  734 | NODE_MODULE(pty, init)
      | ^~~~~~~~~~~
  SOLINK_MODULE(target) Release/obj.target/pty.node
  COPY Release/pty.node
make: Leaving directory '/home/terminus/projects/terminus/app/node_modules/@terminus-term/node-pty/build'
Rebuilding app/fontmanager-redux
gyp info find Python using Python version 3.8.2 found at "/usr/bin/python3"
gyp info spawn /usr/bin/python3
gyp info spawn args [
gyp info spawn args   '/home/terminus/projects/terminus/node_modules/node-gyp/gyp/gyp_main.py',
gyp info spawn args   'binding.gyp',
gyp info spawn args   '-f',
gyp info spawn args   'make',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/projects/terminus/app/node_modules/fontmanager-redux/build/config.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/projects/terminus/node_modules/node-gyp/addon.gypi',
gyp info spawn args   '-I',
gyp info spawn args   '/home/terminus/.electron-gyp/13.1.4/include/node/common.gypi',
gyp info spawn args   '-Dlibrary=shared_library',
gyp info spawn args   '-Dvisibility=default',
gyp info spawn args   '-Dnode_root_dir=/home/terminus/.electron-gyp/13.1.4',
gyp info spawn args   '-Dnode_gyp_dir=/home/terminus/projects/terminus/node_modules/node-gyp',
gyp info spawn args   '-Dnode_lib_file=/home/terminus/.electron-gyp/13.1.4/<(target_arch)/node.lib',
gyp info spawn args   '-Dmodule_root_dir=/home/terminus/projects/terminus/app/node_modules/fontmanager-redux',
gyp info spawn args   '-Dnode_engine=v8',
gyp info spawn args   '--depth=.',
gyp info spawn args   '--no-parallel',
gyp info spawn args   '--generator-output',
gyp info spawn args   'build',
gyp info spawn args   '-Goutput_dir=.'
gyp info spawn args ]
gyp info spawn make
gyp info spawn args [ 'BUILDTYPE=Release', '-C', 'build' ]
make: Entering directory '/home/terminus/projects/terminus/app/node_modules/fontmanager-redux/build'
  CXX(target) Release/obj.target/fontmanager/src/FontManager.o
  CXX(target) Release/obj.target/fontmanager/src/FontManagerLinux.o
../src/FontManagerLinux.cc:1:10: fatal error: fontconfig/fontconfig.h: No such file or directory
    1 | #include <fontconfig/fontconfig.h>
      |          ^~~~~~~~~~~~~~~~~~~~~~~~~
compilation terminated.
make: *** [fontmanager.target.mk:116: Release/obj.target/fontmanager/src/FontManagerLinux.o] Error 1
make: Leaving directory '/home/terminus/projects/terminus/app/node_modules/fontmanager-redux/build'
Error: node-gyp failed to rebuild '/home/terminus/projects/terminus/app/node_modules/fontmanager-redux'.
Error: `make` failed with exit code: 2


    at ModuleRebuilder.rebuildNodeGypModule (/home/terminus/projects/terminus/node_modules/electron-rebuild/lib/src/module-rebuilder.js:193:19)
    at processTicksAndRejections (internal/process/task_queues.js:95:5)
    at async Rebuilder.rebuildModuleAt (/home/terminus/projects/terminus/node_modules/electron-rebuild/lib/src/rebuild.js:190:9)
    at async Rebuilder.rebuild (/home/terminus/projects/terminus/node_modules/electron-rebuild/lib/src/rebuild.js:152:17)
```  
