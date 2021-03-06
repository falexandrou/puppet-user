puppet-user
===========

A simple Puppet module to manage standalone Unix user accounts and ssh keys.
 
If you have a small or temporary environment where running LDAP auth is overkill, this module does the job nicely.

### Usage

Create the account:

<pre>
user::account { 'fred':
  email    => 'f@fredtronic.com',
  uid      => 666
}
</pre>
 
Create the ~/.ssh subdirectory and 'authorized_keys' file:
 
<pre>
user::sshkey { 'fred':
  key     => 'AAAAB3N...',
  type    => 'ssh-rsa'
}
</pre>
 
Refer to <code> manifests/{account,sshkey}.pp</code> for all resource types
