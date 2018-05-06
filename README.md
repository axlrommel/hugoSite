# hugoSite
Static Template Hugo

Install Hugo
`brew hugo`

Get hugo theme
https://themes.gohugo.io/hugo-split-theme/

start hugo server

`hugo server`

get static files

`hugo`

Deploy to S3:
Instructions here
https://medium.com/@sbuckpesch/setup-aws-s3-static-website-hosting-using-ssl-acm-34d41d32e394


To note:
- create certs only in region1
- create certs for rommelvillagomez.com and *.rommelvillagomez.com
- in CloudFront/origins don't take the default S3 value but the one from S3 directly
- create Alias repo in Route 53 pointing to Cloud Front
- everywhere else use rommelvillagomez.com only
- make S3 public folder
- in S3 change meta of index.html to Cache-Control: max-age=0 so all files are refreshed automatically
- in Cloudfront add to invalidations * so all files are not cached but refreshed
