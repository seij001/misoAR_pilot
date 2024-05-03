# misoAR_pilot


# Instrunctions for data access

1. Find the log in info for Empatica CareLab Portal
URL: https://carelab.empatica.com/

Install the Amazon CLI and use the commands below:

2. Configure security keys


`aws configure`

`AWS Access Key ID [None]: <PASTE ID>`

`AWS Secret Access Key [None]: <PASTE Key>`

`Default region name [None]: <LEAVE_EMPTY>`

`Default output format [None]: <LEAVE_EMPTY>`

3. Provide the access URL


`export ACCESS_URL=<PASTE access URL>`

4. Provide local path you want to save files


`export LOCAL_PATH=<insert a local path here>`

5. If you want to preview available files, use the list command


`aws s3 ls ${ACCESS_URL} --recursive`

6. Use the copy command, recursively copying files available for your organization (or copy the specific file you want to download)


`aws s3 cp ${ACCESS_URL} ${LOCAL_PATH} --recursive`