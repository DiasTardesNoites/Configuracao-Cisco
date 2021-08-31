# CONFIGURAÇÕES GERAIS
**Trocar nome do equipamento**
```
>enable
#configure terminal
(config)#hostname <nome>
```

**Configurar um banner**
```
>enable
#configure terminal
(config)#banner motd "<texto>"

M.O.T.D - Message Of The Day
```

**Configurar senha na Console**
```
>enable
#configure terminal
(config)#line console 0
(config-line)#password <senha>
(config-line)#login
```

**Configurar senha na enable**
```
>enable
#configure terminal
(config)#enable secret <senha>
```

**Verificar as configurações que estão rodando no equipamento**
```
>enable
#show running-config
```

**Ativar o serviço de criptografia**
```
>enable
#configure terminal
(config)#service password-encryption
```

**Desfazer configurações no IOS**
```
Colocar "no" na frete do comando
```

**Desativar uma interface**
```
>enable
#configure terminal
(config)#interface <nome>
(config-if)#shutdown

        Exemplo:
            interface FastEthernet 0/2
```

**Desativar várias interfaces de uma vez**
```
>enable
#configure terminal
(config)#interface range <intervalo>
(config-if-range)#shutdown

    Exemplo:
    (config)#interface range f0/1-3
    (config-if-range)#shutdown
```

**Ver o resumo das interfaces**
```
>enable
#show ip interface brief
```

**Salvar as configurações**
```
>enable
#wr

>enable
#copy running-config startup-config
```

**Resetar o equipamento**
```
>enable
#write erase
```

**Colocar IP em uma Interface**
```
>enable
#configure terminal
(config)#interface <nome>
(config-if)#ip address <ip> <mascara>
(config-if)#no shutdown
```

**Colocar descrição em uma interface**
```
>enable
#configure terminal
(config)#interface <nome>
(config)#description <descricao>
```

**Configurar o SSH nas linhas de VTY**
```
>enable
#configure terminal

!Definir o nome do domínio
(config)#ip domain-name <nome-do-domínio>

!Gerar a chave de criptografia
(config)#crypto key generate rsa general-keys modulus <nº-de-bits-da-chave>

!Criar usuário no dispositivo
(config)#username <nome-do-usuário> privilege <1-15> secret <senha>

!Ativar o SSH nas linhas de VTY
(config)#line vty 0 15
(config-line)#transport input ssh
(config-line)#login local
```

**Configurar as VTY para usar TELNET**
```
>enable
#configure terminal
(config)#line vty 0 15
(config-line)#password <senha>
(config-line)#login
```

**Ativar Login Local na Console**
```
>enable
#configure terminal
(config)#line console 0
(config-line)#login local
```

# CONFIGURAÇÕES EXCLUSIVAS PARA O ROTEADOR
**Visualizar tabela de roteamento**
```
>enable
#show ip route
```

**Configurar SubInterfaces no Router**
```
>enable
#configure terminal
(config)#interface <nome-da-subinterface>
        Exemplo: interface g0/0.10
                    Sendo 10 o número da VLAN
(config-subif)#encapsulation dot1q <nº-da-vlan>
(config-subif)#ip address <ip> <máscara>
```

**Inserir IPv6 em uma Interface**
```
>enable
#configure terminal
(config)#interface <nome-da-interface>
(config-if)#ipv6 address <endereço>/<prefixo>
```

**Ativar o Roteamento IPV6**
```
>enable
#configure terminal
(config)#ipv6 unicast-routing
```

**Configurar rota estática**
```
>enable
#configure terminal
(config)#ip route <id-da-rede-de-destino> <máscara-da-rede-de-destino> <ip-do-roteador-que-conhece-a-rede>
```

# CONFIGURAÇÕES EXCLUSIVAS PARA O SWITCH
**Criar uma VLAN**
```
>enable
#configure terminal
(config)#vlan <nº-da-vlan>
(config-vlan)#name <nome-da-vlan>
```

**Colocar uma Interface em uma VLAN (Access)**
```
>enable
#configure terminal
(config)#interface <nome-da-interface>
(config-if)#switchport mode access
(config-if)#switchport access vlan 10
```

**Verificar as VLAN criadas no equipamento**
```
>enable
#show vlan brief
```

**Configurar uma Interface para o Modo Trunk**
```
>enable
#configure terminal
(config)#interface <nome-da-interface>
(config-if)#switchport mode trunk
```

**Configurar VLAN Nativa na Interface Trunk**
```
>enable
#configure terminal
(config)#interface <nome-da-interface>
(config-if)#switchport trunk native vlan <nº-da-vlan-nativa>
```

**Liberar as VLANs na Interface Trunk**
```
>enable
#configure terminal
(config)#interface <nome-da-interface>
(config-if)#switchport trunk allowed vlan <lista de vlans separadas por VÍRGULAS>
        Exemplo: switchport trunk allowed vlan 10,20,30,99
```

**Configurar IP no Switch**
```
>enable
#configure terminal
(config)#interface vlan 90
(config-if)#ip address <endereço> <máscara>
```
