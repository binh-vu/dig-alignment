## images-sample.json

### PyTransforms
#### _ad_crawl_uri_
From column: _ad_url_
>``` python
return getCacheBaseUrl() + "page/"+get_url_hash(getValue("ad_url"))+"/"+getValue("ad_timestamp") + "/processed"
```

#### _image_uri_
From column: _url_
>``` python
return getCacheBaseUrl() + "image/"+get_url_hash(getValue("url"))+"/"+getValue("ad_timestamp") + "/processed"
```

#### _image_snapshot_uri_
From column: _image_uri_
>``` python
return getCacheBaseUrl() + "image/"+get_url_hash(getValue("url"))+"/"+getValue("ad_timestamp") + "/raw"
```


### Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _ad_crawl_uri_ | `uri` | `schema:WebPage1`|
| _image_snapshot_uri_ | `memex:snapshotUri` | `schema:ImageObject1`|
| _image_uri_ | `uri` | `schema:ImageObject1`|
| _importtime_ | `prov:generatedAtTime` | `schema:ImageObject1`|
| _location_ | `memex:cacheUrl` | `schema:ImageObject1`|
| _url_ | `schema:url` | `schema:ImageObject1`|


### Links
| From | Property | To |
|  --- | -------- | ---|
| `schema:WebPage1` | `memex:hasImagePart` | `schema:ImageObject1`|