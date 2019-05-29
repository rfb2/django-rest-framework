# Legacy CoreAPI Schemas Docs

Use of CoreAPI-based schemas were deprecated with the introduction of native OpenAPI-based schema generation in Django REST Framework v3.10.

See the [Version 3.10 Release Announcement](/community/3.10-announcement.md) for more details.

----

You can continue to use CoreAPI schemas by setting the appropriate default schema class:

```python
# In settings.py
REST_FRAMEWORK = {
    'DEFAULT_SCHEMA_CLASS': 'rest_framework.schemas.coreapi.AutoSchema',
}
```

Under-the-hood, any subclass of `coreapi.AutoSchema` here will trigger use of the old CoreAPI schemas.
**Otherwise** you will automatically be opted-in to the new OpenAPI schemas.

All CoreAPI related code will be removed in Django REST Framework v3.12. Switch to OpenAPI schemas by then.

----

For reference this folder contains the old CoreAPI related documentation:

* [Excerpts from _Documenting your API_ topic page](/coreapi/from-documenting-your-api.md).
* [`rest_framework.schemas` API Reference](/coreapi/schemas.md).
* [Tutorial 7: Schemas & client libraries](/coreapi/7-schemas-and-client-libraries.md)