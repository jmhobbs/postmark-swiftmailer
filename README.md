This is a fork of http://code.google.com/p/postmark-swiftmailer

It hasn't changed in a while, and I needed one of these, so I forked it and brought it over to github.

# Usge

    require_once '/path/to/swift-mailer/lib/swift_required.php';
    require_once '/path/to/postmark_swiftmailer.php';
    
    $transport = Swift_PostmarkTransport::newInstance('YOUR-POSTMARK-API-KEY')
    $mailer = Swift_Mailer::newInstance($transport);
    $message = Swift_Message::newInstance('Wonderful Subject')
                 ->setFrom(array('sender@mydomain.com' => 'John Doe'))
                 ->setTo(array('receiver@otherdomain.org' => 'Jane Doe'))
                 ->setBody('Here is the message itself');
    
    $mailer->send($message);

# License - New BSD

	Copyright (c) 2010, Øystein Riiser Gundersen <oysteinrg@gmail.com>
	All rights reserved.

	Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

	Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
	Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
	THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
