# About the polyfill

The polyfill maps the Web Authentication API on top of the Microsoft Edge preliminary implementation. The polyfill is up-to-date with the [5th W3C working draft of the Web Authentication API specification](http://www.w3.org/TR/2017/WD-webauthn-20170505/). 

The Microsoft Edge preliminary implementation is available on all Windows 10 computers that have been updated to the Windows Anniversary Update. You can check the version number by clicking Setting->System->About and check if the OS build is above or equal to 14393. 

## Limitation

This implementation inherits its limitations on parameter values from the Edge implementation.

Notes on limitations:
The polyfill only works if the user has created a PIN (and optionally Hello gestures) for themselves in Settings->Accounts->Sign-in options. Otherwise, a error will be thrown.

create:
- Few parameters are ignored: challenge, timeout, rpId, excludeList, and authenticatorSelection.
- The returned signature is different between the current Web Authentication API and the polyfill.

get:
- Few parameters are ignored: parameters, timeout, and rpId.
- The returned signature is different between the current Web Authentication API and the polyfill.


## Contributing 

If you found a bug with the polyfill, open an issue and we will see how we can do that!
If you want to collaborate just make sure your code passes the ESLint and JSCS rules we've set up!

### Git workflow

1. Fork this project and [set up a remote](https://help.github.com/articles/configuring-a-remote-for-a-fork/) to file pull requests 
against later. 
2. Create a feature branch for your new fixes off of the master branch.
3. Before creating a pull request, make sure your feature branch is up to date with the latest changes to MicrosoftEdge/webauthn-polyfill/master (the 
remote you set up).
4. Create a pull request against MicrosoftEdge/webauthn-polyfill/master with the changes from your branch. Title with the name of your fixes. 
Mention @molant and optionally @melanierichards (for front-end/design review) in the comments so we're aware of your PR.
5. Push any changes based on feedback to your feature branch. This will update the PR with the most recent changes.

## Code of Conduct
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
