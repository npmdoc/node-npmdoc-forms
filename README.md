# api documentation for  [forms (v1.3.0)](https://github.com/caolan/forms#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-forms.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-forms) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-forms.svg)](https://travis-ci.org/npmdoc/node-npmdoc-forms)
#### An easy way to create, parse, and validate forms

[![NPM](https://nodei.co/npm/forms.png?downloads=true)](https://www.npmjs.com/package/forms)

[![apidoc](https://npmdoc.github.io/node-npmdoc-forms/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-forms_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-forms/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-forms/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-forms/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Caolan McMahon"
    },
    "bugs": {
        "url": "https://github.com/caolan/forms/issues"
    },
    "contributors": [
        {
            "name": "Caolan McMahon",
            "email": "caolan.mcmahon@gmail.com"
        },
        {
            "name": "Jordan Harband",
            "email": "ljharb@gmail.com",
            "url": "http://ljharb.codes"
        }
    ],
    "dependencies": {
        "async": "^2.1.2",
        "formidable": "^1.0.17",
        "is": "^3.2.0",
        "object-keys": "^1.0.11",
        "object.assign": "^4.0.4",
        "qs": "^6.3.0",
        "string.prototype.trim": "^1.1.2"
    },
    "description": "An easy way to create, parse, and validate forms",
    "devDependencies": {
        "@ljharb/eslint-config": "^8.0.0",
        "covert": "^1.1.0",
        "eslint": "^3.10.2",
        "evalmd": "^0.0.17",
        "jscs": "^3.0.7",
        "nsp": "^2.6.2",
        "tape": "^4.6.2",
        "tape-dom": "^0.0.12",
        "testling": "^1.7.1"
    },
    "directories": {},
    "dist": {
        "shasum": "8a3a32361724b2fd33bea2a7881ea0ec7d0a0e07",
        "tarball": "https://registry.npmjs.org/forms/-/forms-1.3.0.tgz"
    },
    "engines": {
        "node": ">= 0.4"
    },
    "gitHead": "78d8d3a5818d0586d8f54a9eecb09dd8ff4534f2",
    "homepage": "https://github.com/caolan/forms#readme",
    "license": "MIT",
    "licenses": [
        {
            "type": "MIT",
            "url": "https://github.com/caolan/forms/raw/master/LICENSE"
        }
    ],
    "main": "./index",
    "maintainers": [
        {
            "name": "caolan",
            "email": "caolan@caolanmcmahon.com"
        },
        {
            "name": "ljharb",
            "email": "ljharb@gmail.com"
        }
    ],
    "name": "forms",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/caolan/forms.git"
    },
    "scripts": {
        "coverage": "covert test/*.js",
        "coverage-quiet": "covert --quiet test/*.js",
        "eslint": "eslint test/*.js lib/*.js example/simple.js example/complex.js",
        "jscs": "jscs test/*.js lib/*.js example/simple.js example/complex.js",
        "lint": "npm run jscs && npm run eslint && evalmd *.md",
        "posttest": "npm run security",
        "pretest": "npm run lint",
        "security": "nsp check",
        "test": "npm run tests-only",
        "test-browser": "testling",
        "tests-only": "tape test/*.js"
    },
    "testling": {
        "files": "test-browser.js",
        "browsers": [
            "iexplore/6..latest",
            "firefox/3..10",
            "firefox/15..latest",
            "firefox/nightly",
            "chrome/4..10",
            "chrome/23..latest",
            "chrome/canary",
            "opera/10..latest",
            "opera/next",
            "safari/5.0.5..latest",
            "ipad/6.0..latest",
            "iphone/6.0..latest",
            "android-browser/4.2"
        ]
    },
    "version": "1.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module forms](#apidoc.module.forms)
1.  [function <span class="apidocSignatureSpan">forms.</span>create (fields, options)](#apidoc.element.forms.create)
1.  [function <span class="apidocSignatureSpan">forms.</span>tag (tagName, attrsMap, content, contentIsEscaped)](#apidoc.element.forms.tag)
1.  object <span class="apidocSignatureSpan">forms.</span>fields
1.  object <span class="apidocSignatureSpan">forms.</span>render
1.  object <span class="apidocSignatureSpan">forms.</span>validators
1.  object <span class="apidocSignatureSpan">forms.</span>widgets

#### [module forms.fields](#apidoc.module.forms.fields)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>array (opt)](#apidoc.element.forms.fields.array)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>boolean (opt)](#apidoc.element.forms.fields.boolean)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>date (opt)](#apidoc.element.forms.fields.date)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>email (opt)](#apidoc.element.forms.fields.email)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>number (opt)](#apidoc.element.forms.fields.number)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>object (fields, opts)](#apidoc.element.forms.fields.object)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>password (opt)](#apidoc.element.forms.fields.password)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>string (options)](#apidoc.element.forms.fields.string)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>tel (opt)](#apidoc.element.forms.fields.tel)
1.  [function <span class="apidocSignatureSpan">forms.fields.</span>url (opt)](#apidoc.element.forms.fields.url)

#### [module forms.render](#apidoc.module.forms.render)
1.  [function <span class="apidocSignatureSpan">forms.render.</span>div (name, field, options)](#apidoc.element.forms.render.div)
1.  [function <span class="apidocSignatureSpan">forms.render.</span>li (name, field, options)](#apidoc.element.forms.render.li)
1.  [function <span class="apidocSignatureSpan">forms.render.</span>p (name, field, options)](#apidoc.element.forms.render.p)
1.  [function <span class="apidocSignatureSpan">forms.render.</span>table (name, field, options)](#apidoc.element.forms.render.table)

#### [module forms.tag](#apidoc.module.forms.tag)
1.  [function <span class="apidocSignatureSpan">forms.</span>tag (tagName, attrsMap, content, contentIsEscaped)](#apidoc.element.forms.tag.tag)
1.  [function <span class="apidocSignatureSpan">forms.tag.</span>attrs (a)](#apidoc.element.forms.tag.attrs)

#### [module forms.validators](#apidoc.module.forms.validators)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>alphanumeric (message)](#apidoc.element.forms.validators.alphanumeric)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>color (message)](#apidoc.element.forms.validators.color)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>date (message)](#apidoc.element.forms.validators.date)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>digits (message)](#apidoc.element.forms.validators.digits)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>email (message)](#apidoc.element.forms.validators.email)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>integer (message)](#apidoc.element.forms.validators.integer)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>matchField (match_field, message)](#apidoc.element.forms.validators.matchField)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>matchValue (valueGetter, message)](#apidoc.element.forms.validators.matchValue)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>max (val, message)](#apidoc.element.forms.validators.max)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>maxlength (val, message)](#apidoc.element.forms.validators.maxlength)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>min (val, message)](#apidoc.element.forms.validators.min)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>minlength (val, message)](#apidoc.element.forms.validators.minlength)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>range (min, max, message)](#apidoc.element.forms.validators.range)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>rangelength (min, max, message)](#apidoc.element.forms.validators.rangelength)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>regexp (regex, message)](#apidoc.element.forms.validators.regexp)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>required (message)](#apidoc.element.forms.validators.required)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>requiresFieldIfEmpty (alternate_field, message)](#apidoc.element.forms.validators.requiresFieldIfEmpty)
1.  [function <span class="apidocSignatureSpan">forms.validators.</span>url (include_localhost, message)](#apidoc.element.forms.validators.url)

#### [module forms.widgets](#apidoc.module.forms.widgets)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>checkbox (options)](#apidoc.element.forms.widgets.checkbox)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>color (opts)](#apidoc.element.forms.widgets.color)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>date (opt)](#apidoc.element.forms.widgets.date)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>email (opts)](#apidoc.element.forms.widgets.email)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>hidden (opts)](#apidoc.element.forms.widgets.hidden)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>label (options)](#apidoc.element.forms.widgets.label)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>multipleCheckbox (options)](#apidoc.element.forms.widgets.multipleCheckbox)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>multipleRadio (options)](#apidoc.element.forms.widgets.multipleRadio)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>multipleSelect (options)](#apidoc.element.forms.widgets.multipleSelect)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>number (opts)](#apidoc.element.forms.widgets.number)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>password (opt)](#apidoc.element.forms.widgets.password)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>select (options)](#apidoc.element.forms.widgets.select)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>tel (opts)](#apidoc.element.forms.widgets.tel)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>text (opts)](#apidoc.element.forms.widgets.text)
1.  [function <span class="apidocSignatureSpan">forms.widgets.</span>textarea (options)](#apidoc.element.forms.widgets.textarea)



# <a name="apidoc.module.forms"></a>[module forms](#apidoc.module.forms)

#### <a name="apidoc.element.forms.create"></a>[function <span class="apidocSignatureSpan">forms.</span>create (fields, options)](#apidoc.element.forms.create)
- description and source-code
```javascript
create = function (fields, options) {
    var opts = assign({}, options);

    var validatePastFirstError = !!opts.validatePastFirstError;

    keys(fields).forEach(function (k) {
        // if it's not a field object, create an object field.
        if (!is.fn(fields[k].toHTML) && is.object(fields[k])) {
            fields[k] = exports.fields.object(fields[k], opts);
        }
        fields[k].name = k;
    });
    var f = {
        fields: fields,
        bind: function (data) {
            var b = {
                toHTML: f.toHTML,
                fields: {}
            };
            keys(f.fields).forEach(function (k) {
                if (data != null || f.fields[k].required) {
                    b.fields[k] = f.fields[k].bind((data || {})[k]);
                }
            });
            b.data = keys(b.fields).reduce(function (a, k) {
                a[k] = b.fields[k].data;
                return a;
            }, {});
            b.validate = function () {
                var callback = arguments.length > 1 ? arguments[1] : arguments[0];

                async.forEach(keys(b.fields), function (k, asyncCallback) {
                    b.fields[k].validate(b, function (err, bound_field) {
                        b.fields[k] = bound_field;
                        asyncCallback(validatePastFirstError ? null : err);
                    });
                }, function (err) {
                    callback(err, b);
                });
            };
            b.isValid = function () {
                var form = this;
                return keys(form.fields).every(function (k) {
                    var field = form.fields[k];
                    if (is.fn(field.isValid)) { return field.isValid(); }
                    return field.error === null || typeof field.error === 'undefined';
                });
            };
            return b;
        },
        handle: function (obj, callbacks) {
            if (typeof obj === 'undefined' || obj === null || (is.object(obj) && is.empty(obj))) {
                (callbacks.empty || callbacks.other)(f, callbacks);
            } else if (obj instanceof http.IncomingMessage) {
                if (obj.method === 'GET') {
                    var qs = parse(obj.url, { parseArrays: false }).query;
                    f.handle(querystring.parse(qs), callbacks);
                } else if (obj.method === 'POST' || obj.method === 'PUT') {
                    // If the app is using bodyDecoder for connect or express,
                    // it has already put all the POST data into request.body.
                    if (obj.body) {
                        f.handle(obj.body, callbacks);
                    } else {
                        var form = new formidable.IncomingForm();
                        form.parse(obj, function (err, originalFields/* , files*/) {
                            if (err) { throw err; }
                            var parsedFields = querystring.parse(querystring.stringify(originalFields));
                            f.handle(parsedFields, callbacks);
                        });
                    }
                } else {
                    throw new Error('Cannot handle request method: ' + obj.method);
                }
            } else if (is.object(obj)) {
                f.bind(obj).validate(function (err, field) {
                    if (field.isValid()) {
                        (callbacks.success || callbacks.other)(field, callbacks);
                    } else {
                        (callbacks.error || callbacks.other)(field, callbacks);
                    }
                });
            } else {
                throw new Error('Cannot handle type: ' + typeof obj);
            }
        },
        toHTML: function () {
            var form = this;

            var iterator = arguments.length > 1 ? arguments[1] : arguments[0];
            var name = arguments.length > 1 ? arguments[0] : void 0;

            return keys(form.fields).reduce(function (html, k) {
                var kname = is.string(name) ? name + '[' + k + ']' : k;
                re ...
```
- example usage
```shell
...
Creating an example registration form:

'''javascript
var forms = require('forms');
var fields = forms.fields;
var validators = forms.validators;

var reg_form = forms.create({
username: fields.string({ required: true }),
password: fields.password({ required: validators.required('You definitely want a password') }),
confirm:  fields.password({
    required: validators.required('don\'t you know your own password?'),
    validators: [validators.matchField('password')]
}),
email: fields.email()
...
```

#### <a name="apidoc.element.forms.tag"></a>[function <span class="apidocSignatureSpan">forms.</span>tag (tagName, attrsMap, content, contentIsEscaped)](#apidoc.element.forms.tag)
- description and source-code
```javascript
function tag(tagName, attrsMap, content, contentIsEscaped) {
    var safeTagName = htmlEscape(tagName);
    var attrsHTML = !is.array(attrsMap) ? attrs(attrsMap) : attrsMap.reduce(function (html, map) {
        return html + attrs(map);
    }, '');
    var safeContent = contentIsEscaped ? content : htmlEscape(content);
    return '<' + safeTagName + attrsHTML + (isSelfClosing(safeTagName) ? ' />' : '>' + safeContent + '</' + safeTagName + '>');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.forms.fields"></a>[module forms.fields](#apidoc.module.forms.fields)

#### <a name="apidoc.element.forms.fields.array"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>array (opt)](#apidoc.element.forms.fields.array)
- description and source-code
```javascript
array = function (opt) {
    var opts = assign({}, opt);
    var f = exports.string(opts);
    f.parse = function (raw_data) {
        if (typeof raw_data === 'undefined') { return []; }
        return is.array(raw_data) ? raw_data : [raw_data];
    };
    return f;
}
```
- example usage
```shell
...
var keys = require('object-keys');

// generates a string for common HTML tag attributes
var attrs = function attrs(a) {
if (typeof a.id === 'boolean') {
    a.id = a.id ? 'id_' + a.name : null;
}
if (is.array(a.classes) && a.classes.length > 0) {
    a['class'] = htmlEscape(a.classes.join(' '));
}
a.classes = null;
var pairs = [];
keys(a).forEach(function (field) {
    var value = a[field];
    if (typeof value === 'boolean') {
...
```

#### <a name="apidoc.element.forms.fields.boolean"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>boolean (opt)](#apidoc.element.forms.fields.boolean)
- description and source-code
```javascript
boolean = function (opt) {
    var opts = assign({}, opt);
    var f = exports.string(opts);

    f.widget = opts.widget || forms.widgets.checkbox(opts.attrs || {});
    f.parse = function (raw_data) {
        return !!raw_data;
    };
    return f;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.fields.date"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>date (opt)](#apidoc.element.forms.fields.date)
- description and source-code
```javascript
date = function (opt) {
    var opts = assign({}, opt);
    var f = exports.string(opts);
    if (f.validators) {
        f.validators.unshift(forms.validators.date());
    } else {
        f.validators = [forms.validators.date()];
    }
    return f;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.fields.email"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>email (opt)](#apidoc.element.forms.fields.email)
- description and source-code
```javascript
email = function (opt) {
    var opts = assign({}, opt);
    if (!opts.widget) { opts.widget = forms.widgets.email(opts.attrs || {}); }
    var f = exports.string(opts);
    if (f.validators) {
        f.validators.unshift(forms.validators.email());
    } else {
        f.validators = [forms.validators.email()];
    }
    return f;
}
```
- example usage
```shell
...
var reg_form = forms.create({
    username: fields.string({ required: true }),
    password: fields.password({ required: validators.required('You definitely want a password') }),
    confirm:  fields.password({
        required: validators.required('don\'t you know your own password?'),
        validators: [validators.matchField('password')]
    }),
    email: fields.email()
});
'''

Rendering a HTML representation of the form:

'''javascript
reg_form.toHTML();
...
```

#### <a name="apidoc.element.forms.fields.number"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>number (opt)](#apidoc.element.forms.fields.number)
- description and source-code
```javascript
number = function (opt) {
    var opts = assign({}, opt);
    var f = exports.string(opts);

    f.parse = function (raw_data) {
        if (raw_data === null || raw_data === '') {
            return NaN;
        }
        return Number(raw_data);
    };
    return f;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.fields.object"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>object (fields, opts)](#apidoc.element.forms.fields.object)
- description and source-code
```javascript
object = function (fields, opts) {
    return forms.create(fields || {}, opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.fields.password"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>password (opt)](#apidoc.element.forms.fields.password)
- description and source-code
```javascript
password = function (opt) {
    var opts = assign({}, opt);
    var f = exports.string(opts);
    f.widget = opts.widget || forms.widgets.password(opts.attrs || {});
    return f;
}
```
- example usage
```shell
...
'''javascript
var forms = require('forms');
var fields = forms.fields;
var validators = forms.validators;

var reg_form = forms.create({
    username: fields.string({ required: true }),
    password: fields.password({ required: validators.required('You definitely want a password') }),
    confirm:  fields.password({
        required: validators.required('don\'t you know your own password?'),
        validators: [validators.matchField('password')]
    }),
    email: fields.email()
});
'''
...
```

#### <a name="apidoc.element.forms.fields.string"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>string (options)](#apidoc.element.forms.fields.string)
- description and source-code
```javascript
string = function (options) {
    var opt = options || {};

    var f = assign({}, opt);
    f.widget = f.widget || forms.widgets.text(opt.attrs || {});

    f.parse = function (raw_data) {
        if (typeof raw_data !== 'undefined' && raw_data !== null) {
            return String(raw_data);
        }
        return '';
    };
    f.bind = function (raw_data) {
        var b = assign({}, f); // clone field object:
        b.value = raw_data;
        b.data = b.parse(raw_data);
        b.validate = function (form, callback) {
            var forceValidation = (b.validators || []).some(function (validator) {
                return validator.forceValidation;
            });
            if (!forceValidation && (raw_data === '' || raw_data === null || typeof raw_data === 'undefined')) {
                // don't validate empty fields, but check if required
                if (b.required) {
                    var validator = is.fn(b.required) ? b.required : validators.required();
                    validator(form, b, function (v_err) {
                        b.error = v_err ? String(v_err) : null;
                        callback(v_err, b);
                    });
                } else {
                    process.nextTick(function () { callback(null, b); });
                }
            } else {
                async.forEachSeries(b.validators || [], function (v, asyncCallback) {
                    if (!b.error) {
                        v(form, b, function (v_err) {
                            b.error = v_err ? String(v_err) : null;
                            asyncCallback(null);
                        });
                    } else {
                        asyncCallback(null);
                    }
                }, function (err) {
                    callback(err, b);
                });
            }
        };
        return b;
    };
    f.errorHTML = function () {
        var classes = typeof this.cssClasses !== 'undefined' ? coerceArray(this.cssClasses.error) : [];
        return this.error ? tag('p', { classes: ['error_msg'].concat(classes) }, this.error) : '';
    };
    f.labelText = function (name) {
        var text = this.label;
        if (!text && name) {
            text = name.charAt(0).toUpperCase() + name.slice(1).replace(nameSeparatorRegExp, ' ').replace(/([a-z])([A-Z])/g, function
 (match, firstLetter, secondLetter) {
                return firstLetter + ' ' + secondLetter.toLowerCase();
            });
        }
        return text || '';
    };
    f.labelHTML = function (name, id) {
        if (this.widget.type === 'hidden') { return ''; }
        var forID = id === false ? false : (id || 'id_' + name);
        return forms.widgets.label({
            classes: typeof this.cssClasses !== 'undefined' ? coerceArray(this.cssClasses.label) : [],
            content: this.labelText(name, id)
        }).toHTML(forID, f);
    };
    f.classes = function () {
        var r = ['field'];
        if (this.error) { r.push('error'); }
        if (this.required) { r.push('required'); }
        if (typeof this.cssClasses !== 'undefined') {
            r = r.concat(coerceArray(this.cssClasses.field));
        }
        return r;
    };
    f.toHTML = function (name, iterator) {
        return (iterator || forms.render.div)(name || this.name, this, opt);
    };

    return f;
}
```
- example usage
```shell
...

'''javascript
var forms = require('forms');
var fields = forms.fields;
var validators = forms.validators;

var reg_form = forms.create({
    username: fields.string({ required: true }),
    password: fields.password({ required: validators.required('You definitely want a password') }),
    confirm:  fields.password({
        required: validators.required('don\'t you know your own password?'),
        validators: [validators.matchField('password')]
    }),
    email: fields.email()
});
...
```

#### <a name="apidoc.element.forms.fields.tel"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>tel (opt)](#apidoc.element.forms.fields.tel)
- description and source-code
```javascript
tel = function (opt) {
    var opts = assign({}, opt);
    if (!opts.widget) { opts.widget = forms.widgets.tel(opts.attrs || {}); }
    return exports.string(opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.fields.url"></a>[function <span class="apidocSignatureSpan">forms.fields.</span>url (opt)](#apidoc.element.forms.fields.url)
- description and source-code
```javascript
url = function (opt) {
    var opts = assign({}, opt);
    var f = exports.string(opts);
    if (f.validators) {
        f.validators.unshift(forms.validators.url());
    } else {
        f.validators = [forms.validators.url()];
    }
    return f;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.forms.render"></a>[module forms.render](#apidoc.module.forms.render)

#### <a name="apidoc.element.forms.render.div"></a>[function <span class="apidocSignatureSpan">forms.render.</span>div (name, field, options)](#apidoc.element.forms.render.div)
- description and source-code
```javascript
div = function (name, field, options) {
    var opt = options || {};
    var wrappedContent = [];
    var errorHTML = opt.hideError ? '' : field.errorHTML();
    if (field.widget.type === 'multipleCheckbox' || field.widget.type === 'multipleRadio') {
        var fieldsetAttrs = { classes: [] };
        if (opt.fieldsetClasses) {
            fieldsetAttrs.classes = fieldsetAttrs.classes.concat(opt.fieldsetClasses);
        }
        var legendAttrs = { classes: [] };
        if (opt.legendClasses) {
            legendAttrs.classes = legendAttrs.classes.concat(opt.legendClasses);
        }

        var fieldset = tag('fieldset', fieldsetAttrs, [
            tag('legend', legendAttrs, field.labelText(name)),
            opt.errorAfterField ? '' : errorHTML,
            field.widget.toHTML(name, field),
            opt.errorAfterField ? errorHTML : ''
        ].join(''), true);
        wrappedContent.push(fieldset);
    } else {
        var fieldHTMLs = [field.labelHTML(name, field.id), field.widget.toHTML(name, field)];
        if (opt.labelAfterField) {
            fieldHTMLs.reverse();
        }
        if (opt.errorAfterField) {
            fieldHTMLs.push(errorHTML);
        } else {
            fieldHTMLs.unshift(errorHTML);
        }
        wrappedContent = wrappedContent.concat(fieldHTMLs);
    }
    return tag(tagName, { classes: field.classes() }, wrappedContent.join(''), true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.render.li"></a>[function <span class="apidocSignatureSpan">forms.render.</span>li (name, field, options)](#apidoc.element.forms.render.li)
- description and source-code
```javascript
li = function (name, field, options) {
    var opt = options || {};
    var wrappedContent = [];
    var errorHTML = opt.hideError ? '' : field.errorHTML();
    if (field.widget.type === 'multipleCheckbox' || field.widget.type === 'multipleRadio') {
        var fieldsetAttrs = { classes: [] };
        if (opt.fieldsetClasses) {
            fieldsetAttrs.classes = fieldsetAttrs.classes.concat(opt.fieldsetClasses);
        }
        var legendAttrs = { classes: [] };
        if (opt.legendClasses) {
            legendAttrs.classes = legendAttrs.classes.concat(opt.legendClasses);
        }

        var fieldset = tag('fieldset', fieldsetAttrs, [
            tag('legend', legendAttrs, field.labelText(name)),
            opt.errorAfterField ? '' : errorHTML,
            field.widget.toHTML(name, field),
            opt.errorAfterField ? errorHTML : ''
        ].join(''), true);
        wrappedContent.push(fieldset);
    } else {
        var fieldHTMLs = [field.labelHTML(name, field.id), field.widget.toHTML(name, field)];
        if (opt.labelAfterField) {
            fieldHTMLs.reverse();
        }
        if (opt.errorAfterField) {
            fieldHTMLs.push(errorHTML);
        } else {
            fieldHTMLs.unshift(errorHTML);
        }
        wrappedContent = wrappedContent.concat(fieldHTMLs);
    }
    return tag(tagName, { classes: field.classes() }, wrappedContent.join(''), true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.render.p"></a>[function <span class="apidocSignatureSpan">forms.render.</span>p (name, field, options)](#apidoc.element.forms.render.p)
- description and source-code
```javascript
p = function (name, field, options) {
    var opt = options || {};
    var wrappedContent = [];
    var errorHTML = opt.hideError ? '' : field.errorHTML();
    if (field.widget.type === 'multipleCheckbox' || field.widget.type === 'multipleRadio') {
        var fieldsetAttrs = { classes: [] };
        if (opt.fieldsetClasses) {
            fieldsetAttrs.classes = fieldsetAttrs.classes.concat(opt.fieldsetClasses);
        }
        var legendAttrs = { classes: [] };
        if (opt.legendClasses) {
            legendAttrs.classes = legendAttrs.classes.concat(opt.legendClasses);
        }

        var fieldset = tag('fieldset', fieldsetAttrs, [
            tag('legend', legendAttrs, field.labelText(name)),
            opt.errorAfterField ? '' : errorHTML,
            field.widget.toHTML(name, field),
            opt.errorAfterField ? errorHTML : ''
        ].join(''), true);
        wrappedContent.push(fieldset);
    } else {
        var fieldHTMLs = [field.labelHTML(name, field.id), field.widget.toHTML(name, field)];
        if (opt.labelAfterField) {
            fieldHTMLs.reverse();
        }
        if (opt.errorAfterField) {
            fieldHTMLs.push(errorHTML);
        } else {
            fieldHTMLs.unshift(errorHTML);
        }
        wrappedContent = wrappedContent.concat(fieldHTMLs);
    }
    return tag(tagName, { classes: field.classes() }, wrappedContent.join(''), true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.render.table"></a>[function <span class="apidocSignatureSpan">forms.render.</span>table (name, field, options)](#apidoc.element.forms.render.table)
- description and source-code
```javascript
table = function (name, field, options) {
    var opt = options || {};

    var th = tag('th', {}, field.labelHTML(name, field.id), true);

    var tdContent = field.widget.toHTML(name, field);

    if (!opt.hideError) {
        var errorHTML = field.errorHTML();
        if (opt.errorAfterField) {
            tdContent += errorHTML;
        } else {
            tdContent = errorHTML + tdContent;
        }
    }

    var td = tag('td', {}, tdContent, true);

    return tag('tr', { classes: field.classes() }, th + td, true);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.forms.tag"></a>[module forms.tag](#apidoc.module.forms.tag)

#### <a name="apidoc.element.forms.tag.tag"></a>[function <span class="apidocSignatureSpan">forms.</span>tag (tagName, attrsMap, content, contentIsEscaped)](#apidoc.element.forms.tag.tag)
- description and source-code
```javascript
function tag(tagName, attrsMap, content, contentIsEscaped) {
    var safeTagName = htmlEscape(tagName);
    var attrsHTML = !is.array(attrsMap) ? attrs(attrsMap) : attrsMap.reduce(function (html, map) {
        return html + attrs(map);
    }, '');
    var safeContent = contentIsEscaped ? content : htmlEscape(content);
    return '<' + safeTagName + attrsHTML + (isSelfClosing(safeTagName) ? ' />' : '>' + safeContent + '</' + safeTagName + '>');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.tag.attrs"></a>[function <span class="apidocSignatureSpan">forms.tag.</span>attrs (a)](#apidoc.element.forms.tag.attrs)
- description and source-code
```javascript
function attrs(a) {
    if (typeof a.id === 'boolean') {
        a.id = a.id ? 'id_' + a.name : null;
    }
    if (is.array(a.classes) && a.classes.length > 0) {
        a['class'] = htmlEscape(a.classes.join(' '));
    }
    a.classes = null;
    var pairs = [];
    keys(a).forEach(function (field) {
        var value = a[field];
        if (typeof value === 'boolean') {
            value = value ? field : null;
        } else if (typeof value === 'number' && isNaN(value)) {
            value = null;
        }
        if (typeof value !== 'undefined' && value !== null) {
            pairs.push(htmlEscape(field) + '="' + htmlEscape(value) + '"');
        }
    });
    return pairs.length > 0 ? ' ' + pairs.join(' ') : '';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.forms.validators"></a>[module forms.validators](#apidoc.module.forms.validators)

#### <a name="apidoc.element.forms.validators.alphanumeric"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>alphanumeric (message)](#apidoc.element.forms.validators.alphanumeric)
- description and source-code
```javascript
alphanumeric = function (message) {
    return exports.regexp(/^[a-zA-Z0-9]*$/, message || 'Letters and numbers only.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.color"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>color (message)](#apidoc.element.forms.validators.color)
- description and source-code
```javascript
color = function (message) {
    var msg = message || 'Inputs of type "color" require hex notation, e.g. #FFF or #ABC123.';
    var re = /^#([0-9A-F]{8}|[0-9A-F]{6}|[0-9A-F]{3})$/i;
    return function (form, field, callback) {
        if (re.test(field.data)) {
            callback();
        } else {
            callback(msg);
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.date"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>date (message)](#apidoc.element.forms.validators.date)
- description and source-code
```javascript
date = function (message) {
    var msg = message || 'Inputs of type "date" must be valid dates in the format "yyyy-mm-dd"';
    var numberRegex = /^[0-9]+$/,
        invalidDate = new Date('z');
    return function (form, field, callback) {
        var parts = field.data ? field.data.split('-') : [];
        var allNumbers = parts.every(function (part) { return numberRegex.test(part); });
        var date = allNumbers && parts.length === 3 ? new Date(parts[0], parts[1] - 1, parts[2]) : invalidDate;
        if (!isNaN(date.getTime())) {
            callback();
        } else {
            callback(msg);
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.digits"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>digits (message)](#apidoc.element.forms.validators.digits)
- description and source-code
```javascript
digits = function (message) {
    return exports.regexp(/^\d+$/, message || 'Numbers only.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.email"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>email (message)](#apidoc.element.forms.validators.email)
- description and source-code
```javascript
email = function (message) {
    var msg = message || 'Please enter a valid email address.';
    // regular expression by Scott Gonzalez:
    // http://projects.scottsplayground.com/email_address_validation/
    // eslint-disable-next-line no-control-regex, no-useless-escape
    return exports.regexp(/^((([a-z]|\d|[!#\$%&'\*\+\-\/=\?\^_'{\|}~]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])+(\.([a-z]|\d|[!#\$%&'\*\+\-\/=\?\^_'{\|}~]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])+)*)|((\x22)((((\x20|\x09)*(\x0d\x0a))?(\x20|\x09)+)?(([\x01-\x08\x0b\x0c\x0e-\x1f\x7f]|\x21|[\x23-\x5b]|[\x5d-\x7e]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(\\([\x01-\x09\x0b\x0c\x0d-\x7f]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF]))))*(((\x20|\x09)*(\x0d\x0a))?(\x20|\x09)+)?(\x22)))@((([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.)+(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.?$/i, msg);
}
```
- example usage
```shell
...
var reg_form = forms.create({
    username: fields.string({ required: true }),
    password: fields.password({ required: validators.required('You definitely want a password') }),
    confirm:  fields.password({
        required: validators.required('don\'t you know your own password?'),
        validators: [validators.matchField('password')]
    }),
    email: fields.email()
});
'''

Rendering a HTML representation of the form:

'''javascript
reg_form.toHTML();
...
```

#### <a name="apidoc.element.forms.validators.integer"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>integer (message)](#apidoc.element.forms.validators.integer)
- description and source-code
```javascript
integer = function (message) {
    return exports.regexp(/^-?\d+$/, message || 'Please enter an integer value.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.matchField"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>matchField (match_field, message)](#apidoc.element.forms.validators.matchField)
- description and source-code
```javascript
matchField = function (match_field, message) {
    var msg = message || 'Does not match %s.';
    return function (form, field, callback) {
        if (form.fields[match_field].data !== field.data) {
            callback(format(msg, match_field));
        } else {
            callback();
        }
    };
}
```
- example usage
```shell
...
var validators = forms.validators;

var reg_form = forms.create({
    username: fields.string({ required: true }),
    password: fields.password({ required: validators.required('You definitely want a password') }),
    confirm:  fields.password({
        required: validators.required('don\'t you know your own password?'),
        validators: [validators.matchField('password')]
    }),
    email: fields.email()
});
'''

Rendering a HTML representation of the form:
...
```

#### <a name="apidoc.element.forms.validators.matchValue"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>matchValue (valueGetter, message)](#apidoc.element.forms.validators.matchValue)
- description and source-code
```javascript
matchValue = function (valueGetter, message) {
    if (!is.fn(valueGetter)) {
        throw new TypeError('valueGetter must be a function');
    }
    var msg = message || '%s does not match expected value: "%s"';
    return function (form, field, callback) {
        var expected = valueGetter();
        if (field.data !== expected) {
            callback(format(msg, formatFieldName(field), expected));
        } else {
            callback();
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.max"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>max (val, message)](#apidoc.element.forms.validators.max)
- description and source-code
```javascript
max = function (val, message) {
    var msg = message || 'Please enter a value less than or equal to %s.';
    return function (form, field, callback) {
        if (field.data <= val) {
            callback();
        } else {
            callback(format(msg, val));
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.maxlength"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>maxlength (val, message)](#apidoc.element.forms.validators.maxlength)
- description and source-code
```javascript
maxlength = function (val, message) {
    var msg = message || 'Please enter no more than %s characters.';
    return function (form, field, callback) {
        if (field.data.length <= val) {
            callback();
        } else {
            callback(format(msg, val));
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.min"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>min (val, message)](#apidoc.element.forms.validators.min)
- description and source-code
```javascript
min = function (val, message) {
    var msg = message || 'Please enter a value greater than or equal to %s.';
    return function (form, field, callback) {
        if (field.data >= val) {
            callback();
        } else {
            callback(format(msg, val));
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.minlength"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>minlength (val, message)](#apidoc.element.forms.validators.minlength)
- description and source-code
```javascript
minlength = function (val, message) {
    var msg = message || 'Please enter at least %s characters.';
    return function (form, field, callback) {
        if (field.data.length >= val) {
            callback();
        } else {
            callback(format(msg, val));
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.range"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>range (min, max, message)](#apidoc.element.forms.validators.range)
- description and source-code
```javascript
range = function (min, max, message) {
    var msg = message || 'Please enter a value between %s and %s.';
    return function (form, field, callback) {
        if (field.data >= min && field.data <= max) {
            callback();
        } else {
            callback(format(msg, min, max));
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.rangelength"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>rangelength (min, max, message)](#apidoc.element.forms.validators.rangelength)
- description and source-code
```javascript
rangelength = function (min, max, message) {
    var msg = message || 'Please enter a value between %s and %s characters long.';
    return function (form, field, callback) {
        if (field.data.length >= min && field.data.length <= max) {
            callback();
        } else {
            callback(format(msg, min, max));
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.regexp"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>regexp (regex, message)](#apidoc.element.forms.validators.regexp)
- description and source-code
```javascript
regexp = function (regex, message) {
    var msg = message || 'Invalid format.';
    var re = new RegExp(regex);
    return function (form, field, callback) {
        if (re.test(field.data)) {
            callback();
        } else {
            callback(msg);
        }
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.required"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>required (message)](#apidoc.element.forms.validators.required)
- description and source-code
```javascript
required = function (message) {
    var msg = message || '%s is required.';
    return function (form, field, callback) {
        if (trim(field.data || '').length === 0) {
            callback(format(msg, formatFieldName(field)));
        } else {
            callback();
        }
    };
}
```
- example usage
```shell
...
'''javascript
var forms = require('forms');
var fields = forms.fields;
var validators = forms.validators;

var reg_form = forms.create({
    username: fields.string({ required: true }),
    password: fields.password({ required: validators.required('You definitely want a password') }),
    confirm:  fields.password({
        required: validators.required('don\'t you know your own password?'),
        validators: [validators.matchField('password')]
    }),
    email: fields.email()
});
'''
...
```

#### <a name="apidoc.element.forms.validators.requiresFieldIfEmpty"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>requiresFieldIfEmpty (alternate_field, message)](#apidoc.element.forms.validators.requiresFieldIfEmpty)
- description and source-code
```javascript
requiresFieldIfEmpty = function (alternate_field, message) {
    var msg = message || 'One of %s or %s is required.';
    var validator = function (form, field, callback) {
        var alternateBlank = trim(form.fields[alternate_field].data || '').length === 0;
        var fieldBlank = trim(field.data || '').length === 0;
        if (alternateBlank && fieldBlank) {
            callback(format(msg, formatFieldName(field), alternate_field));
        } else {
            callback();
        }
    };
    validator.forceValidation = true;
    return validator;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.validators.url"></a>[function <span class="apidocSignatureSpan">forms.validators.</span>url (include_localhost, message)](#apidoc.element.forms.validators.url)
- description and source-code
```javascript
url = function (include_localhost, message) {
    var msg = message || 'Please enter a valid URL.';
    // regular expression by Scott Gonzalez:
    // http://projects.scottsplayground.com/iri/
    // eslint-disable-next-line no-control-regex, no-useless-escape
    var external_regex = /^(https?|ftp):\/\/(((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:)*@)?(((\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5])\.(\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5])\.(\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5])\.(\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5]))|((([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.)+(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.?)(:\d*)?)(\/((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)+(\/(([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)*)*)?)?(\?((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)|[\uE000-\uF8FF]|\/|\?)*)?(#((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)|\/|\?)*)?$/i;
    // eslint-disable-next-line no-useless-escape
    var with_localhost_regex = /^(https?|ftp):\/\/(localhost|((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:)*@)?(((\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5])\.(\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5])\.(\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5])\.(\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5]))|((([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.)+(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.?)(:\d*)?)(\/((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)+(\/(([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)*)*)?)?(\?((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)|[\uE000-\uF8FF]|\/|\?)*)?(#((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)|\/|\?)*)?$/i;
    return exports.regexp(include_localhost ? with_localhost_regex : external_regex, msg);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.forms.widgets"></a>[module forms.widgets](#apidoc.module.forms.widgets)

#### <a name="apidoc.element.forms.widgets.checkbox"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>checkbox (options)](#apidoc.element.forms.widgets.checkbox)
- description and source-code
```javascript
checkbox = function (options) {
    var opt = options || {};
    var w = {
        classes: opt.classes,
        type: 'checkbox'
    };
    var userAttrs = getUserAttrs(opt);
    w.toHTML = function (name, field) {
        var f = field || {};
        var attrs = {
            type: 'checkbox',
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes,
            checked: !!f.value,
            value: 'on'
        };
        return tag('input', [attrs, userAttrs, w.attrs || {}]);
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.color"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>color (opts)](#apidoc.element.forms.widgets.color)
- description and source-code
```javascript
color = function (opts) {
    var opt = opts || {};
    var userAttrs = getUserAttrs(opt);
    var w = {
        classes: opt.classes,
        type: type,
        formatValue: function (value) {
            return (value || value === 0) ? value : null;
        }
    };
    w.toHTML = function (name, field) {
        var f = field || {};
        var attrs = {
            type: type,
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes,
            value: w.formatValue(f.value)
        };
        return tag('input', [attrs, userAttrs, w.attrs || {}]);
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.date"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>date (opt)](#apidoc.element.forms.widgets.date)
- description and source-code
```javascript
date = function (opt) {
    var w = dateWidget(opt);
    w.formatValue = function (value) {
        if (!value) {
            return null;
        }

        var date = is.date(value) ? value : new Date(value);

        if (isNaN(date.getTime())) {
            return null;
        }

        return date.toISOString().slice(0, 10);
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.email"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>email (opts)](#apidoc.element.forms.widgets.email)
- description and source-code
```javascript
email = function (opts) {
    var opt = opts || {};
    var userAttrs = getUserAttrs(opt);
    var w = {
        classes: opt.classes,
        type: type,
        formatValue: function (value) {
            return (value || value === 0) ? value : null;
        }
    };
    w.toHTML = function (name, field) {
        var f = field || {};
        var attrs = {
            type: type,
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes,
            value: w.formatValue(f.value)
        };
        return tag('input', [attrs, userAttrs, w.attrs || {}]);
    };
    return w;
}
```
- example usage
```shell
...
var reg_form = forms.create({
    username: fields.string({ required: true }),
    password: fields.password({ required: validators.required('You definitely want a password') }),
    confirm:  fields.password({
        required: validators.required('don\'t you know your own password?'),
        validators: [validators.matchField('password')]
    }),
    email: fields.email()
});
'''

Rendering a HTML representation of the form:

'''javascript
reg_form.toHTML();
...
```

#### <a name="apidoc.element.forms.widgets.hidden"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>hidden (opts)](#apidoc.element.forms.widgets.hidden)
- description and source-code
```javascript
hidden = function (opts) {
    var opt = opts || {};
    var userAttrs = getUserAttrs(opt);
    var w = {
        classes: opt.classes,
        type: type,
        formatValue: function (value) {
            return (value || value === 0) ? value : null;
        }
    };
    w.toHTML = function (name, field) {
        var f = field || {};
        var attrs = {
            type: type,
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes,
            value: w.formatValue(f.value)
        };
        return tag('input', [attrs, userAttrs, w.attrs || {}]);
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.label"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>label (options)](#apidoc.element.forms.widgets.label)
- description and source-code
```javascript
label = function (options) {
    var opt = options || {};
    var w = { classes: opt.classes || [] };
    var userAttrs = getUserAttrs(opt);
    w.toHTML = function (forID) {
        var attrs = {
            'for': forID,
            classes: w.classes
        };
        return tag('label', [attrs, userAttrs, w.attrs || {}], opt.content);
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.multipleCheckbox"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>multipleCheckbox (options)](#apidoc.element.forms.widgets.multipleCheckbox)
- description and source-code
```javascript
multipleCheckbox = function (options) {
    var opt = options || {};
    var w = {
        classes: opt.classes,
        labelClasses: opt.labelClasses,
        type: 'multipleCheckbox'
    };
    var userAttrs = getUserAttrs(opt);
    w.toHTML = function (name, field) {
        var f = field || {};
        var choices = unifyChoices(f.choices, 0);
        return renderChoices(choices, function (choice) {
            // input element
            var id = f.id === false ? false : (f.id ? f.id + '_' + choice.value : 'id_' + name + '_' + choice.value);
            var checked = isSelected(f.value, choice.value);

            var attrs = {
                type: 'checkbox',
                name: name,
                id: id,
                classes: w.classes,
                value: choice.value,
                checked: !!checked
            };
            var inputHTML = tag('input', [attrs, userAttrs, w.attrs || {}]);

            // label element
            var labelHTML = tag('label', { 'for': id, classes: w.labelClasses }, choice.label);

            return inputHTML + labelHTML;
        });
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.multipleRadio"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>multipleRadio (options)](#apidoc.element.forms.widgets.multipleRadio)
- description and source-code
```javascript
multipleRadio = function (options) {
    var opt = options || {};
    var w = {
        classes: opt.classes,
        labelClasses: opt.labelClasses,
        type: 'multipleRadio'
    };
    var userAttrs = getUserAttrs(opt);
    w.toHTML = function (name, field) {
        var f = field || {};
        var choices = unifyChoices(f.choices, 0);
        return renderChoices(choices, function (choice) {
            // input element
            var id = f.id === false ? false : (f.id ? f.id + '_' + choice.value : 'id_' + name + '_' + choice.value);
            var checked = isSelected(f.value, choice.value);
            var attrs = {
                type: 'radio',
                name: name,
                id: id,
                classes: w.classes,
                value: choice.value,
                checked: !!checked
            };
            var inputHTML = tag('input', [attrs, userAttrs, w.attrs || {}]);
            // label element
            var labelHTML = tag('label', { 'for': id, classes: w.labelClasses }, choice.label);

            return inputHTML + labelHTML;
        });
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.multipleSelect"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>multipleSelect (options)](#apidoc.element.forms.widgets.multipleSelect)
- description and source-code
```javascript
multipleSelect = function (options) {
    var opt = options || {};
    var w = {
        classes: opt.classes,
        type: isMultiple ? 'multipleSelect' : 'select'
    };
    var userAttrs = getUserAttrs(opt);
    w.toHTML = function (name, field) {
        var f = field || {};
        var choices = unifyChoices(f.choices, 1);
        var optionsHTML = renderChoices(choices, function render(choice) {
            if (choice.isNested) {
                return tag('optgroup', { label: choice.label }, renderChoices(choice.choices, render), true);
            } else {
                return tag('option', { value: choice.value, selected: !!isSelected(f.value, choice.value) }, choice.label);
            }
        });
        var attrs = {
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes
        };
        if (isMultiple) {
            attrs.multiple = true;
        }
        return tag('select', [attrs, userAttrs, w.attrs || {}], optionsHTML, true);
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.number"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>number (opts)](#apidoc.element.forms.widgets.number)
- description and source-code
```javascript
number = function (opts) {
    var opt = opts || {};
    var userAttrs = getUserAttrs(opt);
    var w = {
        classes: opt.classes,
        type: type,
        formatValue: function (value) {
            return (value || value === 0) ? value : null;
        }
    };
    w.toHTML = function (name, field) {
        var f = field || {};
        var attrs = {
            type: type,
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes,
            value: w.formatValue(f.value)
        };
        return tag('input', [attrs, userAttrs, w.attrs || {}]);
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.password"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>password (opt)](#apidoc.element.forms.widgets.password)
- description and source-code
```javascript
password = function (opt) {
    var w = passwordWidget(opt);
    w.formatValue = passwordFormatValue;
    return w;
}
```
- example usage
```shell
...
'''javascript
var forms = require('forms');
var fields = forms.fields;
var validators = forms.validators;

var reg_form = forms.create({
    username: fields.string({ required: true }),
    password: fields.password({ required: validators.required('You definitely want a password') }),
    confirm:  fields.password({
        required: validators.required('don\'t you know your own password?'),
        validators: [validators.matchField('password')]
    }),
    email: fields.email()
});
'''
...
```

#### <a name="apidoc.element.forms.widgets.select"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>select (options)](#apidoc.element.forms.widgets.select)
- description and source-code
```javascript
select = function (options) {
    var opt = options || {};
    var w = {
        classes: opt.classes,
        type: isMultiple ? 'multipleSelect' : 'select'
    };
    var userAttrs = getUserAttrs(opt);
    w.toHTML = function (name, field) {
        var f = field || {};
        var choices = unifyChoices(f.choices, 1);
        var optionsHTML = renderChoices(choices, function render(choice) {
            if (choice.isNested) {
                return tag('optgroup', { label: choice.label }, renderChoices(choice.choices, render), true);
            } else {
                return tag('option', { value: choice.value, selected: !!isSelected(f.value, choice.value) }, choice.label);
            }
        });
        var attrs = {
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes
        };
        if (isMultiple) {
            attrs.multiple = true;
        }
        return tag('select', [attrs, userAttrs, w.attrs || {}], optionsHTML, true);
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.tel"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>tel (opts)](#apidoc.element.forms.widgets.tel)
- description and source-code
```javascript
tel = function (opts) {
    var opt = opts || {};
    var userAttrs = getUserAttrs(opt);
    var w = {
        classes: opt.classes,
        type: type,
        formatValue: function (value) {
            return (value || value === 0) ? value : null;
        }
    };
    w.toHTML = function (name, field) {
        var f = field || {};
        var attrs = {
            type: type,
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes,
            value: w.formatValue(f.value)
        };
        return tag('input', [attrs, userAttrs, w.attrs || {}]);
    };
    return w;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.forms.widgets.text"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>text (opts)](#apidoc.element.forms.widgets.text)
- description and source-code
```javascript
text = function (opts) {
    var opt = opts || {};
    var userAttrs = getUserAttrs(opt);
    var w = {
        classes: opt.classes,
        type: type,
        formatValue: function (value) {
            return (value || value === 0) ? value : null;
        }
    };
    w.toHTML = function (name, field) {
        var f = field || {};
        var attrs = {
            type: type,
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes,
            value: w.formatValue(f.value)
        };
        return tag('input', [attrs, userAttrs, w.attrs || {}]);
    };
    return w;
}
```
- example usage
```shell
...

'''javascript
var widgets = require('forms').widgets;

var my_form = forms.create({
title: fields.string({
    required: true,
    widget: widgets.text({ classes: ['input-with-feedback'] }),
    errorAfterField: true,
    cssClasses: {
        label: ['control-label col col-lg-3']
    }
}),
description: fields.string({
    errorAfterField: true,
...
```

#### <a name="apidoc.element.forms.widgets.textarea"></a>[function <span class="apidocSignatureSpan">forms.widgets.</span>textarea (options)](#apidoc.element.forms.widgets.textarea)
- description and source-code
```javascript
textarea = function (options) {
    var opt = options || {};
    var w = {
        classes: opt.classes,
        type: 'textarea'
    };
    var userAttrs = getUserAttrs(opt);
    w.toHTML = function (name, field) {
        var f = field || {};
        var attrs = {
            name: name,
            id: f.id === false ? false : (f.id || true),
            classes: w.classes,
            rows: opt.rows || null,
            cols: opt.cols || null
        };
        return tag('textarea', [attrs, userAttrs, w.attrs || {}], f.value || '');
    };
    return w;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
