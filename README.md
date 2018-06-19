# pluck-value-from-yaml
pluck one value from yaml with bash cli

      # read svc_rheltowerrw's passwd from the ansible vault without running a playbook
      myPass=$(ansible-vault view /etc/ansible/NetworkVars/passwords.yml | sed -n '/svc_rheltowerrw:/,/password/p' | tail -1 | sed 's/^.*password: //')
      echo 'password='$myPass >> /root/secret.txt

