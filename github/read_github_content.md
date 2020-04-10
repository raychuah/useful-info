## Help from StackOverflow

I experimented a bit and found a solution by using a different base64 decoding library as follows:

``` var base64 = require('js-base64').Base64; ```    
``` var contents = base64.decode(res.content); ```

A second solution which I also found to work is specific to how to use the GitHub API. By adding the following to the GitHub API call header, I was also able to get the decoded file contents:

```'accept': 'application/vnd.github.VERSION.raw'```


## Example API request

https://api.github.com/repos/raychuah/useful-info/contents/css/css_name_guide.md
