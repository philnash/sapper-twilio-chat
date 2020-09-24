# Twilio Chat on Sapper with Rollup

This is a test repo to show that things aren't working when you try to use Twilio Chat with Sapper and Rollup.

## Running this example

Clone the repo and change into the new directory:

```
git clone https://github.com/philnash/sapper-twilio-chat.git
cd sapper-twilio-chat
```

Install the dependencies:

```
npm install
```

Try to run the development server:

```
npm run dev
```

Check out the results:

```
> TODO@0.0.1 dev /Users/pnash/projects/sapper-twilio-chat
> sapper dev

✔ server (847ms)
✗ client
Cannot read property 'imports' of undefined
✔ service worker (21ms)
> Listening on http://localhost:3000
```

## The problem

```
✗ client
Cannot read property 'imports' of undefined
```

This results in the failure to build the index route and the app is broken.

I have tried to debug, but I'm not sure where to start. The build error doesn't give a file location.

Changing the import of the `twilio-chat` library to `import Chat from "twilio-chat/dist/twilio-chat"` does seem to work, but this is not the intended way to use the library and makes for debugging with the library more difficult.

## Please help!

Thank you!
