[![Continuous Integration - FastAPI](https://github.com/BigDataIA-Spring2023-Team-04/Assignment-2/actions/workflows/fastapi.yml/badge.svg?branch=lokesh)](https://github.com/BigDataIA-Spring2023-Team-04/Assignment-2/actions/workflows/fastapi.yml)
[![Continuous Integration - UnitTesting](https://github.com/BigDataIA-Spring2023-Team-04/Assignment-2/actions/workflows/pytest.yml/badge.svg?branch=lokesh)](https://github.com/BigDataIA-Spring2023-Team-04/Assignment-2/actions/workflows/pytest.yml)

/get_goes_url (POST): Given a filename, the endpoint generates the S3 URL for the corresponding file hosted on the GOES-18 S3 bucket. If the file is not found, an HTTP 404 error is returned. This endpoint also checks for the file format and raises an HTTP 400 error if the format is incorrect.

/get_nexrad_url (POST): Given a filename, the endpoint generates the S3 URL for the corresponding file hosted on the NEXRAD level 2 S3 bucket. If the file is not found, an HTTP 404 error is returned. This endpoint also checks for the file format and raises an HTTP 400 error if the format is incorrect.

/get_goes_url_parameters (POST): Given the year, day of year, and hour of a GOES-18 satellite file, the endpoint generates a list of URLs for all files matching the specified parameters. This endpoint returns an HTTP 404 error if the directory specified by the parameters is not found.

/get_nexrad_url_parameters (POST): Given the year, month, day, and station ID of a NEXRAD level 2 file, the endpoint generates a list of URLs for all files matching the specified parameters. This endpoint returns an HTTP 404 error if the directory specified by the parameters is not found.

/get_unique_years_geos (GET): Returns a list of all unique years for which GOES-18 satellite files are available in the database.

/get_unique_days_geos (GET): Given a year, returns a list of all unique days of the year for which GOES-18 satellite files are available in the database.

/get_unique_hours_geos (GET): Given a year and day of year, returns a list of all unique hours of the day for which GOES-18 satellite files are available in the database.

/get_file_names_geos (GET): Given a year, day of year, and hour, returns a list of all file names matching the specified parameters for the GOES-18 satellite.

/get_unique_years_nexrad (GET): Returns a list of all unique years for which NEXRAD level 2 files are available in the database.

/get_unique_months_nexrad (GET): Given a year, returns a list of all unique months of the year for which NEXRAD level 2 files are available in the database.

/get_unique_days_nexrad (GET): Given a year and month, returns a list of all unique days of the month for which NEXRAD level 2 files are available in the database.

/get_unique_stations_nexrad (GET): Given a year, month, and day, returns a list of all unique station IDs for which NEXRAD level 2 files are available in the database.

/get_file_names_nexrad (GET): Given a year, month, day, and station ID, returns a list of all file names matching the specified parameters for the NEXRAD level 2 files.

/download_and_upload_s3_file (POST): Downloads a file from a specified S3 bucket and uploads it to another specified S3 bucket. If the file already exists in the destination bucket, the function returns a download URL for the existing file. Otherwise, it uploads the file and returns
