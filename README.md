# hello-world

This is my first Dotnet Core sample project runs on docker/linux.

When use ASPDOTNET Core to serve restful api, you will meet error like "error:2006D002:BIO routines:BIO_new_file:system lib".
It's caused by certificates in /etc/pki/tls/certs/* are readonly for root user.
You need to run
# chmod +r /etc/pki/tls/certs/*
to fix such issue.
