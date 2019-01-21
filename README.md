# downloadr
A Go executable to use a config and download file from given url based on some ignore criteria (when API does not exist &amp; HTTP status codes are not useable)


This was created becuase I use  http://wttr.in to get the current weather as an image.
This is then used to display weather in my conky. (My Conky config I shall upload later but it based on GreenAppleDesktop conky theme)
However every now and then, they return an image which says API requests exceeded or Too many requests, which looks very bad in my conky :)
So the Json config file can have sha512 hashes that should be ignored for that URL.

The config file looks like this (at least for now) (a Json Array) :
```json
[
	{
		"url": "http://wttr.in/pune_0tqp0.png",
		"output": "pune.png",
		"ignoreHashes": [
			"f0f5c334a45344d4c858e3d9100847d20464ef9176525d88c93db7781730bcfeecfa463bf908d929508f65014401ec67eeb1d8578957240c17b4c598a40eb038",
			"776103f2dfe7639b73779d5e632282c99423d3044ad4a53a372d41b7a2fa2d3e60c8d8ea57089cddda628e3286ae16011b128dccfecf5143aa15c730c4905071",
			"8b9039da91b5ba49f108dbb30273fa75f62dd1560d4e2610f93e01507d860c4574c5cdbba2ae1a334517219ef61da0e59e5eb113ef51abe4edd1dda1db3cf8d3",
			"cf83e1357eefb8bdf1542850d66d8007d620e4050b5715dc83f4a921d36ce9ce47d0d13c5d85f2b0ff8318d2877eec2f63b931bd47417a81a538327af927da3e"
		]
	},
	{
		"url": "http://wttr.in/munich_0tqp0.png",
		"output": "munich.png",
		"ignoreHashes": [
			"f0f5c334a45344d4c858e3d9100847d20464ef9176525d88c93db7781730bcfeecfa463bf908d929508f65014401ec67eeb1d8578957240c17b4c598a40eb038",
			"776103f2dfe7639b73779d5e632282c99423d3044ad4a53a372d41b7a2fa2d3e60c8d8ea57089cddda628e3286ae16011b128dccfecf5143aa15c730c4905071",
			"8b9039da91b5ba49f108dbb30273fa75f62dd1560d4e2610f93e01507d860c4574c5cdbba2ae1a334517219ef61da0e59e5eb113ef51abe4edd1dda1db3cf8d3",
			"cf83e1357eefb8bdf1542850d66d8007d620e4050b5715dc83f4a921d36ce9ce47d0d13c5d85f2b0ff8318d2877eec2f63b931bd47417a81a538327af927da3e"
		]
	}
]
```

The Program can be run with -h -help to see the options.
Latest version can be downloaded from the releases :)

Suggesstions are welcome as Bug / Feature requests and PRs of course :)
