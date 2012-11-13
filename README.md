# sparkartTags

jQuery plugin for creating a simple tag input.

SparkartTags converts a simple text input into a dynamic tag input. Tags can be typed in and completed with either the `enter` or `,` key. Tags created with this input are added to the parent `<input>` as a comma separated list.

## Usage

In order to use sparkartTags you'll need to include jQuery and the jquery.sparkartTags.js file ( the jquery.sparkartTags.css file is highly recommended, but still optional ).

**A basic tag input**

```html
<input id="tags" type="text" value="javascript,jquery" />
<script>
	$('#tags').sparkartTags();
</script>
```

Existing values for the input will be converted into tags automatically.

**A customized tag input**

```html
<input id="tags" type="text" value="javascript,jquery" />
<script>
	$('#tags').sparkartTags({
		value: 'ruby,rails',
		placeholder: 'Add a language'
	});
</script>
```

If `value` is manually specified, it will override the value of the input.

**A tag input with auto-suggest**

```html
<input id="tags" type="text" />
<script>
	var languages = ['javascript','ruby','python','php'];
	$('#tags').sparkartTags({
		suggest: {
			source: languages
		}
	});
</script>
```

You must include the [sparkartSuggest](https://github.com/SparkartGroupInc/sparkartSuggest) plugin to use `suggest`.

## Configuration

* **value** - *(string)* - A comma separated list of tags to include when the plugin first loads. Overrides the value of the input `sparkartTags` is called on.
* **placeholder** - *(string)* - The value of the placeholder for the tag input. Defaults to "add a tag".
* **suggest** - *(object)* - A configuration object for the [sparkartSuggest](https://github.com/SparkartGroupInc/sparkartSuggest) plugin. The plugin must be included in order for this to work.

## License

MIT License.

----------

Copyright © 2012 Sparkart Group, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.