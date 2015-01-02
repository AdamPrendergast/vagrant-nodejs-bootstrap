task :gen_keys do
  system "mkdir .ssh"
  system "ssh-keygen -f .ssh/id_rsa -N ''"
  system "cp -a .ssh/id_rsa.pub .ssh/authorized_keys2"
end

task :ssl_win do
    system "curl -o c:/cacert.pem http://curl.haxx.se/ca/cacert.pem"
    system "set SSL_CERT_FILE=c:\cacert.pem"
end

task :install_cookbooks do
    system "berks vendor cookbooks/"
end

task :clean do
  system "rm -r .ssh"
  system "rm -r .kidirtchen"
  system "rm -r cookbooks"
end

task :clean_win do
  system "rmdir /s cookbooks"
end