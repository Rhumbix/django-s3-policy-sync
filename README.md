django-s3-policy-sync
==========================

If your Django project relies on S3, for instance, file storage in S3, S3 policies can be a pain to manage.

django-s3-policy-sync provides a solution to put S3 policies under source control.

# Install django-s3-policy-sync

```bash
$ pip django-s3-policy-sync
```

# Set up django-s3-policy-sync

## Add ```s3_policy_sync.middleware.S3PolicySyncMiddleware``` to your ```MIDDLEWARE_CLASSES```.

For example:

```
MIDDLEWARE_CLASSES = (
    ...,
    's3_policy_sync.middleware.S3PolicySyncMiddleware',
    ...,
)
```

## Configure 2 variables ```S3_POLICY_DIR``` and  ```S3_BUCKETS```

For example:

```
S3_POLICY_DIR = os.path.join(BASE_DIR, 'settings', 's3_policies')
S3_BUCKETS = (S3_MEDIA_BUCKET, S3_PRIVATE_BUCKET)
```


# Enjoy!

Email me with any questions: [kenneth.jiang@gmail.com](kenneth.jiang@gmail.com).
