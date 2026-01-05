## TODO

[x] get npm install working on node 20
[] test build on windows
[] resolve critical security issues with npm audit
  - update gh-pages deployment scripts (needed if we want to fix https://github.com/advisories/GHSA-8mmm-9v2q-x3f9 -- low risk for us, but it would be great to get the "critical" warnings to go away during npm install)
  - critical issue - https://github.com/advisories/GHSA-fjxv-7rqg-78g4
[] remove PORT=3006 in package.json (needed this on my machine specifically)
[] add tauri back
[] test tauri builds
[] regression test entire app
[] confirm engine unit tests passing (engine should not be affected by the node upgrade, but still check.)
[] update package.json scripts
[] update engine build documentation
[] update README

## Notes

- I temporarily removed Tauri and related configuration to simplify the migration from node 14 to 20, which is currently supported: https://nodejs.org/en/about/previous-releases
- I removed electon and unused/outdated native+desktop build config + files
- removed both of these unused dependencies:
  - "14": "^3.1.6"
  - "fs": "0.0.1-security
- bumped 
- bumped node-sass "^4.9.4", -> ^9.0 -- needed for node 20 support https://www.npmjs.com/package/node-sass

https://stackoverflow.com/questions/69692842/error-message-error0308010cdigital-envelope-routinesunsupported

https://github.com/facebook/create-react-app
create-react-app is deprecated. 
ill try to get it to the last maintenance release hoping it supports react 16 https://github.com/facebook/create-react-app/releases/tag/v5.0.1
stuff like vite seems to be the modern replacement. https://www.reddit.com/r/reactjs/comments/12x6k9x/it_looks_like_createreactapp_is_dead_what_should/
https://v1.tauri.app/v1/guides/getting-started/setup/vite/

https://stackoverflow.com/questions/59820954/syntaxerror-unknown-namespace-tags-are-not-supported-by-default
.svgrrc.js -- fixes SVG imports as JSX to work with react-scripts 5.0.1

https://www.typescriptlang.org/tsconfig/#baseUrl
jsconfig.json -- react-scripts 5.0.1 breaks importing from "Editor/" which used to work because paths implicitly started with src/
This fixes that issue without having to update every single import in the project.
