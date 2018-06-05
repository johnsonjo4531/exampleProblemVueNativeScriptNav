# exampleProblemVueNativeScriptNav

vue nativescript problem with loading the same component twice.

The `Nav` component in `@/components/Nav.vue` is trying to be used in page A and page B which are both in their respective files in `@/components/{A,B}.vue`. The Nav component however is not defined in both pages but only one. You can create the nav as a mixin to get around this, but you would hopefully just be able to use the same component twice.
