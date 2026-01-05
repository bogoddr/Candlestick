TODO
- get npm install working on node 20
- resolve critical security issues with npm audit
- remove PORT=3006 in package.json (needed this on my machine specifically)
- add tauri back
- test tauri builds
- regression test entire app
- confirm engine unit tests passing (engine should not be affected by the node upgrade, but still check.)
- update package.json scripts
- update engine build documentation

Notes

"14": "^3.1.6", -- what is this? https://www.npmjs.com/package/14

"fs": "0.0.1-security", -- what is this? https://www.npmjs.com/package/fs

https://www.npmjs.com/package/node-sass
node-sass "^4.9.4", -> ^9.0

https://stackoverflow.com/questions/69692842/error-message-error0308010cdigital-envelope-routinesunsupported

https://github.com/facebook/create-react-app
create-react-app is deprecated. 
ill try to get it to the last maintenance release hoping it supports react 16 https://github.com/facebook/create-react-app/releases/tag/v5.0.1
stuff like vite seems to be the modern replacement. https://www.reddit.com/r/reactjs/comments/12x6k9x/it_looks_like_createreactapp_is_dead_what_should/
https://v1.tauri.app/v1/guides/getting-started/setup/vite/
