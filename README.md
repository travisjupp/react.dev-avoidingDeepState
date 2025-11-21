# react.dev-avoidingDeepState

Created with CodeSandbox

Updating nested state involves making copies of objects all the way up from the
part that changed. Deleting a deeply nested place would involve copying its
entire parent place chain. Such code can be very verbose.

If the state is too nested to update easily, consider making it “flat”. Here is
one way you can restructure this data. Instead of a tree-like structure where
each place has an array of its child places, you can have each place hold an
array of its child place IDs. Then store a mapping from each place ID to the
corresponding place.

Forked from: https://react.dev/learn/choosing-the-state-structure#avoid-deeply-nested-state
