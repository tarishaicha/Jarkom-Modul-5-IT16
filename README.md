# Jarkom-Modul-5-IT16

## Nama Anggota Kelompok
| Nama | NRP | Github |
|---------------------------|------------|--------|
|Tarisha Syira Mazaya Putri | 5027211061 | https://github.com/tarishaicha |
|Evan Darya Kusuma | 5027211069 | https://github.com/shinjitakeru00 |

## Topologi VLSM
berikut adalah topologi untuk VLSM yang kami gunakan
![image](https://github.com/tarishaicha/Jarkom-Modul-5-IT16/assets/102363994/0eba28c4-1545-41a1-8ae6-dcb1c62868c7)

## Pembagian Rute dan Subnet VLSM
berikut adalah pembagian rute dan subnet yang dibuat
![image](https://github.com/tarishaicha/Jarkom-Modul-5-IT16/assets/102363994/b0ff530b-74fe-4140-8b16-4cffb2e9b6a1)

## Pembagian IP VLSM
berikut adalah hasil pembagian IP kami
![image](https://github.com/tarishaicha/Jarkom-Modul-5-IT16/assets/102363994/4e9f2649-18d8-4880-ab32-3a1a8179ea3c)

## Persiapan

### Subnetting
berikut adalah subnetting pada GNS

#### Aura
```
# config for eth0
#iface eth0 inet dhcp
auto eth0
iface eth0 inet static
    address 192.168.122.2
    netmask 255.255.255.252
    gateway 192.168.122.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

# config for eth1 ke
auto eth1
iface eth1 inet static
    address 192.241.14.133
    netmask 255.255.255.252

# config for eth2
auto eth2
iface eth2 inet static
    address 192.241.14.129
    netmask 255.255.255.252
```

#### Fern
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.3
    netmask 255.255.255.128
    gateway 192.241.14.1

# config for eth1
auto eth1
iface eth1 inet static
    address 192.241.14.145
    netmask 255.255.255.252

# config for eth2
auto eth2
iface eth2 inet static
    address 192.241.14.149
    netmask 255.255.255.252
```

#### Frieren
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.134
    netmask 255.255.255.252
    gateway 192.241.14.133
    
# config for eth1
auto eth1
iface eth1 inet static
    address 192.241.14.137
    netmask 255.255.255.252

# config for eth2
auto eth2
iface eth2 inet static
    address 192.241.14.141
    netmask 255.255.255.252
```

#### Globe-Forest
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.134
    netmask 255.255.255.252
    gateway 192.241.14.133
    
# config for eth1
auto eth1
iface eth1 inet static
    address 192.241.14.137
    netmask 255.255.255.252

# config for eth2
auto eth2
iface eth2 inet static
    address 192.241.14.141
    netmask 255.255.255.252
```

#### Heiter
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.130
    netmask 255.255.255.252
    gateway 192.241.14.129

# config for eth1
auto eth1
iface eth1 inet static
    address 192.241.0.1
    netmask 255.255.248.0

# config for eth2
auto eth2
iface eth2 inet static
    address 192.241.8.1
    netmask 255.255.252.0
```

#### Himmel
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.142
    netmask 255.255.255.252
    gateway 192.241.14.141

# config for eth1
auto eth1
iface eth1 inet static
    address 192.241.12.1
    netmask 255.255.254.0

# config for eth2
auto eth2
iface eth2 inet static
    address 192.241.14.1
    netmask 255.255.255.128
```

#### Laub Hills
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.138
    netmask 255.255.255.252
    gateway 192.241.14.137
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

#### Revolte
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.150
    netmask 255.255.255.252
    gateway 192.241.14.149
```

#### Richter
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.146
    netmask 255.255.255.252
    gateway 192.241.14.145
```

#### Schwer Mountain
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.2
    netmask 255.255.255.128
    gateway 192.241.14.1

auto eth0
iface eth0 inet dhcp
    gateway 192.241.14.1
```

#### Sein
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.8.2
    netmask 255.255.252.0
    gateway 192.241.8.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

#### Stark
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.14.138
    netmask 255.255.255.252
    gateway 192.241.14.137
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

#### Turk Region
```
# config for eth0
auto eth0
iface eth0 inet static
    address 192.241.0.2
    netmask 255.255.248.0
    gateway 192.241.0.1

auto eth0
iface eth0 inet dhcp
    gateway 192.241.0.1
```


### Routing
Berikut adalah routing dari kelompok kami

```
#AURA
# A9 Heiter eth0
route add -net 192.241.0.0 netmask 255.255.248.0 gw 192.241.14.130
# A10 Heiter eth0
route add -net 192.241.8.0 netmask 255.255.252.0 gw 192.241.14.130
# A6 Frieren eth0
route add -net 192.241.14.136 netmask 255.255.255.252 gw 192.241.14.134
# A4 Frieren eth0
route add -net 192.241.12.0 netmask 255.255.254.0 gw 192.241.14.134
# A3 Frieren eth0
route add -net 192.241.14.0 netmask 255.255.255.128 gw 192.241.14.134
# A2 Frieren eth0
route add -net 192.241.14.144 netmask 255.255.255.252 gw 192.241.14.134
# A1 Frieren eth0
route add -net 192.241.14.148 netmask 255.255.255.252 gw 192.241.14.134

#HEITER
# Heiter Aura eth2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.241.14.129
# A8
iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 192.241.14.128/30 --to-source 192.168.122.2

#FRIEREN
# Frieren Aura eth1
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.241.14.133
# A4 Himmel eth0
route add -net 192.241.12.0 netmask 255.255.254.0 gw 192.241.14.142
# A3 Himmel eth0
route add -net 192.241.14.0 netmask 255.255.255.128 gw 192.241.14.142
# A2 Himmel eth0
route add -net 192.241.14.144 netmask 255.255.255.252 gw 192.241.14.142
# A1 Himmel eth0
route add -net 192.241.14.148 netmask 255.255.255.252 gw 192.241.14.142
# A9 Aura eth1
route add -net 192.241.0.0 netmask 255.255.248.0 gw 192.241.14.133
# A10 Aura eth1
route add -net 192.241.8.0 netmask 255.255.248.0 gw 192.241.14.133
# A7
iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 192.241.14.132/30 --to-source 192.168.122.2

#HIMMEL
# Himmel Frieren eth2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.241.14.141
# A2 Fern eth0
route add -net 192.241.14.144 netmask 255.255.255.252 gw 192.241.14.3
# A1 Fern eth0
route add -net 192.241.14.148 netmask 255.255.255.252 gw 192.241.14.3
# A5
iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 192.241.14.140/30 --to-source 192.168.122.2

#FERN
# Fern Himmel eth2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.241.14.1
# A3
iptables -t nat -A POSTROUTING -o eth0 -j SNAT -s 192.241.14.0/25 --to-source 192.168.122.2
```

### Konfigurasi DNS
untuk konfig DNS kami menggunakan Script ini
```

echo "nameserver 192.168.122.1" >/etc/resolv.conf

apt update
apt install bind9 dnsutils -y

# Backup existing file
cp /etc/bind/named.conf.options /etc/bind/named.conf.options/bak

# Configuration data
echo 'options {
    listen-on-v6 { none; };
    directory "/var/cache/bind";

    # Forwarders
    forwarders {
        192.168.122.1;
    };

    # If there is no answer from the forwarders, dont attempt to resolve recursively
    forward only;

    dnssec-validation no;

    auth-nxdomain no;    # conform to RFC1035
    allow-query { any; };
};' >/etc/bind/named.conf.options

service bind9 restart
service bind9 status
```

### Setup DHCP Server dan Relay
#### DHCP Server
```

echo "nameserver 192.168.122.1" >/etc/resolv.conf

apt update
apt install isc-dhcp-server rsyslog -y

Konfigurasi yang akan dimasukkan ke dalam file
echo "# Defaults for isc-dhcp-server (sourced by /etc/init.d/isc-dhcp-server)
# Path to dhcpd's config file (default: /etc/dhcp/dhcpd.conf).
#DHCPDv4_CONF=/etc/dhcp/dhcpd.conf
#DHCPDv6_CONF=/etc/dhcp/dhcpd6.conf
# Path to dhcpd's PID file (default: /var/run/dhcpd.pid).
#DHCPDv4_PID=/var/run/dhcpd.pid
#DHCPDv6_PID=/var/run/dhcpd6.pid
# Additional options to start dhcpd with.
#       Don't use options -cf or -pf here; use DHCPD_CONF/ DHCPD_PID instead
#OPTIONS=\"\"
# On what interfaces should the DHCP server (dhcpd) serve DHCP requests?
#       Separate multiple interfaces with spaces, e.g. \"eth0 eth1\".
INTERFACESv4=\"eth0\"
INTERFACESv6=\"\"" >/etc/default/isc-dhcp-server

echo "# Subnet A10 Grobe Forest
subnet 192.241.8.0 netmask 255.255.252.0 {
    range 192.241.8.3 192.241.11.254;
    option routers 192.241.8.1;
    option broadcast-address 192.241.11.255;
    option domain-name-servers 192.241.14.146;
    default-lease-time 720;
    max-lease-time 5760;
}

# Subnet A9 Turk Region
subnet 192.241.0.0 netmask 255.255.248.0 {
    range 192.241.0.1 192.241.7.254;
    option routers 192.241.0.1;
    option broadcast-address 192.241.7.255;
    option domain-name-servers 192.241.14.146;
    default-lease-time 720;
    max-lease-time 5760;
}

# Subnet A8
subnet 192.241.14.128 netmask 255.255.255.252 {
}

# Subnet A7
subnet 192.241.14.132 netmask 255.255.255.252 {
}

# Subnet A6
subnet 192.241.14.136 netmask 255.255.255.252 {
}

# Subnet A5
subnet 192.241.14.140 netmask 255.255.255.252 {
}

# Subnet A4 Laub Hills
subnet 192.241.12.0 netmask 255.255.254.0 {
    range 192.241.12.2 192.241.13.254;
    option routers 192.241.12.1;
    option broadcast-address 192.241.13.255;
    option domain-name-servers 192.241.14.146;
    default-lease-time 720;
    max-lease-time 5760;
}

# Subnet A3 Schwer Mountains
subnet 192.241.14.0 netmask 255.255.255.128 {
    range 192.241.14.2 192.241.14.126;
    option routers 192.241.14.1;
    option broadcast-address 192.241.14.127;
    option domain-name-servers 192.241.14.146;
    default-lease-time 720;
    max-lease-time 5760;
}

# Subnet A2
subnet 192.241.14.144 netmask 255.255.255.252 {
}

# Subnet A1
subnet 192.241.14.148 netmask 255.255.255.252 {
}
" >/etc/dhcp/dhcpd.conf

rm /var/run/dhcpd.pid

service isc-dhcp-server restart
service rsyslog start

service isc-dhcp-server status
```

#### DHCP Relay
```
apt update

apt-get install isc-dhcp-relay rsyslog -y

echo "# Defaults for isc-dhcp-relay initscript
# sourced by /etc/init.d/isc-dhcp-relay
# installed at /etc/default/isc-dhcp-relay by the maintainer scripts

#
# This is a POSIX shell fragment
#

# What servers should the DHCP relay forward requests to?
SERVERS=\"192.241.14.150\"

# On what interfaces should the DHCP relay (dhrelay) serve DHCP requests?
INTERFACES=\"eth0 eth1 eth2\"

# Additional options that are passed to the DHCP relay daemon?
OPTIONS=\"\"" >/etc/default/isc-dhcp-relay

service rsyslog start

# sed -i 's/#net.ipv4.ip_forward=1/net.ipv4.ip_forward=1/g' /etc/sysctl.conf

service isc-dhcp-relay restart
service isc-dhcp-relay status
```

## Soal 1
