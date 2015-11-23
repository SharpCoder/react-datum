
### ReactDatum.Link

For rendering links like `<a href="...">`.

Example: 
```jsx
var model = new Backbone.Model({
  url: "http://www.zulily.com", 
  name: "Zulily"
})

<ReactDatum.Link attr="url" nameAttr="name"/>
```

The 'attr' prop should return a url from the model and is the href of the link.

Optionally, a 'nameAttr' prop can also be specified to display between the <a></a> tags.  If 'nameAttr' prop is not specified, the children of the link are rendered:
```jsx
// we use an alias to minimize the noise in the JSX below
var Rd = ReactDatum;

// ... and later ...
<Rd.Link attr="url">Go to <Rd.Text attr="name"/> and discover somthing today!</Rd.Link>
```

In this example the link would enclose the rendered contents: "Go to Zulily and ..."

If no nameAttr prop and no children, ReactDatum.Link will render the value of the attr specified (what should be the url of the href):
```jsx
<Rd.Link attr="url"/>
```
renders `<a href="http://www.zulily.com">http://www.zulily.com</a>`  