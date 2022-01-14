# Heartbeat engineering exercise (frontend, react)

## Rules

1. Try this exercise in **2 hours**. 🕙

2. There are no right or wrong answers. Most likely you won't have time to finish all the tasks. We are looking for:

   1. Code quality ✅
   2. Structure ✅
   3. Functionality ✅
   4. Architectural decisions (e.g. _why have you used this package?_) ✅

3. This is a real world situation. You are allowed to use the internet, use every library you want, call a friend...  
   **But don't:**
   - code with someone else
   - use a previous version of this exercise (if you have completed it before)

# Tasks

## Task 1

There is a basic search component `patients_search.tsx`. It allows a user to type a query and have the results return to the parent component.

It's a little janky though, sometimes it doesn't search for the correct query.

### Add a test

Add a test for this component. Feel free to use whichever testing library you think is best.

### Refactor and add a feature

Now that we have a useful test for this component. Please refactor this component to remove the peculiar behaviour when searching for something.

Add a loading spinner (feel free to use anything) to provide the user with some visual feedback while it is waiting for a network request to complete.

## Task 2

Error handling is a little old fashioned. Currently the errors are handled in the components and just popped up via an `alert`:

```
// patients_search.tsx
loadPatients(sq).then(ps => onResults(ps)).catch(err => alert(err))
```

We would like a nice "toast" component to show to the user when an error is encountered. There is a base component to use in the `src/toast/toast.tsx`. And in the `App.tsx` file, there is an example usage of this component commented out.

## License

See [LICENSE](LICENSE) file.
