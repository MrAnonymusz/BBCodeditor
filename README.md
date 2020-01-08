# BBCodeditor - 1.0
_**Warning!** I'm not a professional javascript developer so this project may have some bugs and probably it will take time to fix them on my own._

# Installation
1. You must include in your page the necessary file(s) of [jQuery](https://jquery.com/) and [Bootstrap](https://getbootstrap.com/) *These files must be included in the header tag*
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.4.1/css/bootstrap.css">

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.4.1/js/bootstrap.min.js"></script>
``` 
2. Add the following code to your header tag *(before it closes)*
```html
<head>
  <!-- ... -->
  <link rel="stylesheet" href="../dist/jquery.editor.css">
   <link rel="stylesheet" href="../dist/inc/pickr/themes/monolith.min.css">
</head>
```
3. Add the code to your body tag *(in the bottom of it)*
```html
<!-- Editor -->
<script src="../dist/inc/pickr/pickr.es5.min.js"></script>
<script src="../dist/inc/inputmask/jquery.inputmask.js"></script>
<script src="../dist/lang/en_EN.js"></script>
<script src="../dist/icons/font-awesome-5.js"></script>
<script src="../dist/jquery.editor.js"></script>
<!-- Editor -->
```

# Usage
Create a div in your body tag add an id to it and call the bbcodeditor function.
##### Example:
```html
<div class="example-editor"></div>
```
And now add to the body tag after the *jquery.editor.js* file the following html *(javascript)* code:
```html
<script>
$(function() {
  $('#example-editor').bbcodeditor({
    defaultValue: "", // This option must be included whenever the editor is called (it can be left empty) !important
    content_class: "example-editor-content" // This "option" is optional but you must call it if you want the get the value of the content area (editor)
  });
});
</script>
```
### Documentation
**_For the documentation please check the documentation.html in the examples folder!_**

# Default Options
```javascript
{
  lang: 'en-EN',
  icons: 'font-awesome-5',
  height: 200,
  minHeight: 100,
  maxHeight: 400,
  button_class: 'btn btn-primary',
  content_class: '', 
  includedButtons: [
  ['bold', 'italic', 'underline'], ['strikethrough', 'supperscript', 'subscript'], ['font-name', 'font-size', 'color'], ['unordered-list', 'ordered-list', 'align'], ['link', 'image', 'media'], ['misc', 'advcode', 'table']
  ],
  advcodeLanguages: ['General Code', 'HTML', 'CSS', 'Javascript', 'PHP', 'XML', 'JSON', 'SQL', 'Ruby', 'Python', 'Java', 'C', 'C#', 'C++', 'Lua', 'Markdown', 'Yaml'],
  enableTextareaResize: true,
  colorPickerDefaultColor: '#3498DB',
  colorPickerSwatches: [
    'rgba(52, 152, 219, 1)',
    'rgba(46, 204, 113, 1)',
    'rgba(26, 188, 156, 1)',
    'rgba(234, 76, 136, 1)',
    'rgba(155, 89, 182, 1)',
    'rgba(241, 196, 15, 1)',
    'rgba(243, 156, 18, 1)',
    'rgba(231, 76, 60, 1)',
    'rgba(236, 240, 241, 1)',
    'rgba(189, 195, 199, 1)',
    'rgba(149, 165, 166, 1)',
    'rgba(127, 140, 141, 1)',
    'rgba(52, 73, 94, 1)',
    'rgba(44, 62, 80, 1)'
  ],
  enableImageUpload: false,
  imageUploadUrl: "",
  imageUploadType: "POST",
  uploadFileName: "filename",
  uploadFile: "bbcodeditor-image-upload",
  uploadFileTokenName: "_token",
  uploadFileToken: "",
  includedMiscItems: ['h1', 'h2', 'h3', 'h4', 'h5', 'h6', 'blockquote', 'code', 'linebreak'],
  previewRequestUrl: "",
  previewRequestType: "GET",
  customRequestToken: false,
  previewRequestTokenName: "_token",
  previewRequestToken: ""
}
```

### The Following Plugins Were Used

1. [Inputmask](http://robinherbots.github.io/Inputmask) by [RobinHerbots](https://github.com/RobinHerbots)
2. [Pickr](https://github.com/Simonwep/pickr) by [Simonwep](https://github.com/Simonwep)
3. [PrismJS](https://github.com/PrismLibrary/Prism) by [PrismLibrary](https://github.com/PrismLibrary)
