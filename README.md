# ontap-upgrade-ansible
Sample playbooks for upgrading ONTAP with Ansible

Preparing the Lab On Demand Environment to test this playbook:
  1. run the quick_setup script on the jumphost desktop

  2. Perform the following on cluster1:

    set test
    system node image dev-promoted-update -node cluster1-01
    system node image dev-promoted-update -node cluster1-02
    system services web file-uploads config modify -node * -size 3GB
    
  3. Perform the following on cluster2:
 
    set test
    system node image dev-promoted-update -node cluster2-01
    system services web file-uploads config modify -node * -size 3GB 
    
  4. Monitor job status and wait for successful completion on both clusters

  5. install hfs on jumphost 
      http://rejetto.com/hfs/?f=dl
      
  6. download ONTAP images and add them to hfs
