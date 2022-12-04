# Microfrontend-module-federation

### Summary

1. Create a micro frontend project to implement in a legacy project **changing the webpack configs**
2. Create a react component called **FederationComponent**, so legacy projects have the option **to use** the micro frontend app **without** changing the webpack config


### Common errors in micro frontend and solutions
1. Uncaught TypeError: Cannot read properties of undefined (reading 'init')

**Solution:** Forgot to match the names of the exposed module and where I was importing them


2. Invalid hook call. ➠ Didn’t properly align dependency versions for React in the remote, eslint was upset
host_blahBlahApi__WEBPACK_IMPORTED_MODULE_1___default(...) is not a function

**Solution:** Set publicPath to auto in webpack.config


3. Cannot read properties of undefined (reading 'displayName'). Warning: lazy: Expected the result of a dynamic import() call. Instead received: [object Module] 

**Solution:** Forgot to add an export default <ComponentName> at the bottom of the exposed component page. In my projects usually i dont use export default in nothing, but in microfrontend, your app needs to be exported as default
