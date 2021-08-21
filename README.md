# USERS ROLE
Ruolo per creare o cancellare utenti sul sistema.

## Creazione

Il ruolo crea utenti nel sistema. Permetti di associare gruppi aggiuntivi rispetto al gruppo base.
Il gruppo base viene scelto come da impostazioni di sistema. L'UID viene gestito dal sistema.


Esempio di vars da usare nei playbook:

``` yaml
vars:
      users_list:
          - username: sindria
            groups: ["group1", "group2", ... "]
            authorized_keys: |
                ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx8crAHG/a9QBD4zO0ZHIjdRXy+ySKviXVCMIJ3/NMIAAzDyIsPKToUJmIApHHHF1/hBllqzBSkPEMwgFbXjyqTeVPHF8V0iq41n0kgbulJG sindria@cicd
```

## Cancellazione

Il ruolo cancella utenti gli utenti di sistema e le loro home specificando il nome utente in una lista.

**NON TESTATO**

Esempio di vars da usare nei playbook:

``` yaml
vars:
      delusers_list:
          - username: sindria
```
