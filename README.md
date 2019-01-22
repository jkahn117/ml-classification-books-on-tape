# ml-classification-books-on-tape




## Training Data

1. Download audio books from http://www.openculture.com/freeaudiobooks
2. Selected:
    * Charles Dickens *Great Expectations*: http://www.archive.org/download/great_expectations_mfs_0812_librivox/great_expectations_mfs_0812_librivox_64kb_mp3.zip
    * Jane Austen *Sense & Sensibility*: http://www.archive.org/download/0_sense_and_sensibility_librivox/0_sense_and_sensibility_librivox_64kb_mp3.zip
3. Upload to Amazon S3



## SageMaker Execution Role Policy

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:PutObject",
                "s3:GetObject",
                "s3:ListBucket",
                "s3:DeleteObject"
            ],
            "Resource": "arn:aws:s3:::*"
        },
        {
            "Effect": "Allow",
            "Action": [
                "s3:GetObject",
                "s3:ListBucket"
            ],
            "Resource": "arn:aws:s3:::ml-classification-books-on-tape"
        },
        {
            "Effect": "Allow",
            "Action": "transcribe:StartTranscriptionJob",
            "Resource": "*"
        }
    ]
}
```