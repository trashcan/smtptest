Using this script
=================

This script connects to a mail server and attempts to authenticate and deliver a message to a recipient.

./smtptest host[:port] username password recipient

It will print the commands sent by the script and any responses by the server. If you run into any issues, let me know.

Example output
==============

    $  ./smtptest.php mail.<snip>.com:587 <snip> <snip> <snip>
    Connecting to mail.<snip>.com:587...
    Connected.
    >> EHLO dssh.codero.com
    << 250-69-64-82-122.phx.dedicated.codero.com
    >> AUTH LOGIN
    << 250-AUTH=LOGIN CRAM-MD5 PLAIN
    << 250-AUTH LOGIN CRAM-MD5 PLAIN
    << 250-STARTTLS
    << 250-PIPELINING
    << 250 8BITMIME
    << 334 VXNlcm5hbWU6
    >> <snip>
    << 334 UGFzc3dvcmQ6
    >> <snip>
    << 235 go ahead
    >> MAIL FROM: <snip>
    << 250 ok
    >> RCPT TO: <snip>
    << 250 ok
    >> DATA
    << 354 go ahead
    >> Subject: test message
    
    This is a test message. Please disregard.
    .
    << 250 ok 1375388751 qp 26627
    Message sent succesfully.

