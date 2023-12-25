# host-app-no-source-maps
A minimal reproduction of source maps not generating when using NextFederationPlugin

1. cd host-app 
2. npm install
3. npm run build
4. ls -lRas .next | grep map

No source maps are created 