 function check_email_password()
    {
        $mailbox_email = trim($_POST['jiveshdoshi@gmail.com']);
        $mailbox_password = trim($_POST['']);
        $mb = imap_open('{imap.gmail.com:993/imap/ssl}INBOX',$mailbox_email,$mailbox_password) or die(json_encode(array('success'=>false,'massage'=>'Password is false.','error'=>imap_last_error())));
        echo json_encode(array('success'=>true,'massage'=>'Password is true.'));


        
