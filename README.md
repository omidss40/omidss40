{
  "dns": {
    "servers": [
      {
        "tag": "google",
        "address": "tls://8.8.8.8"
      },
      {
        "tag": "local",
        "address": "223.5.5.5",
        "detour": "direct"
      },
      {
        "tag": "block",
        "address": "rcode://success"
      }
    ],
    "rules": [
      {
        "geosite": "category-ads-all",
        "server": "block",
        "disable_cache": true
      },
      {
        "outbound": "any",
        "server": "local"
      },
      {
        "geosite": "cn",
        "server": "local"
      }
    ],
        "strategy": "ipv4_only"
    },
    "experimental": {
        "clash_api": {
            "external_controller": "127.0.0.1:9090",
            "secret": "",
            "store_selected": true
        }
    },
    "inbounds": [
        {
            "auto_route": true,
            "domain_strategy": "ipv4_only",
            "endpoint_independent_nat": true,
            "inet4_address": "172.19.0.1/30",
            "mtu": 9000,
            "sniff": true,
            "sniff_override_destination": true,
            "strict_route": true,
            "type": "tun"
        },
        {
            "domain_strategy": "ipv4_only",
            "listen": "127.0.0.1",
            "listen_port": 2333,
            "sniff": true,
            "sniff_override_destination": true,
            "tag": "socks-in",
            "type": "socks",
            "users": []
        },
        {
            "domain_strategy": "ipv4_only",
            "listen": "127.0.0.1",
            "listen_port": 2334,
            "sniff": true,
            "sniff_override_destination": true,
            "tag": "mixed-in",
            "type": "mixed",
            "users": []
        }
    ],
    "log": {},
    "outbounds": [
        {
            "tag": "hello",
            "type": "selector",
            "default": "urltest",
            "outbounds": [
                "urltest",
                "1",
                "2",
                "3",
                "4",
                "5",
                "6",
                "7",
                "8",
                "9",
                "10",
                "11",
                "12",
                "13",
                "14",
                "15"
            ]
        },

    {
  "type": "http",
  "tag": "1",
  "server": "103.229.28.29",
  "server_port": 8000,
  "username": "n4W3SX",
  "password": "xLo3xj",
  "path": "",
  "headers": {},
  "tls": {  "enabled": true,
  "disable_sni": false,
  "server_name": "telewebion.com",
  "insecure": true}

},

    {
  "type": "http",
  "tag": "2",
  "server": "45.147.31.173",
  "server_port": 8000,
  "username": "beHWTa",
  "password": "CHoNSJ",
  "path": "",
  "headers": {},
  "tls": {  "enabled": true,
  "disable_sni": false,
  "server_name": "telewebion.com",
  "insecure": true}

},

    {
  "type": "http",
  "tag": "3",
  "server": "185.242.246.198",
  "server_port": 8000,
  "username": "rdZTLc",
  "password": "cSgL9e",
  "path": "",
  "headers": {},
  "tls": {  "enabled": true,
  "disable_sni": false,
  "server_name": "telewebion.com",
  "insecure": true}

},
        {
          "type": "http",
          "tag": "4",
          "server": "103.229.28.132",
          "server_port": 8000,
          "username": "JuYHwf",
          "password": "2P7MuX",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "5",
          "server": "45.142.30.14",
          "server_port": 8000,
          "username": "7aBP2b",
          "password": "uCq8hW",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "6",
          "server": "103.229.28.11",
          "server_port": 8000,
          "username": "1BgdLE",
          "password": "KoXPtc",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "7",
          "server": "103.229.28.56",
          "server_port": 8000,
          "username": "mfaGKE",
          "password": "VZC1ty",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "8",
          "server": "103.229.28.68",
          "server_port": 8000,
          "username": "wJvd4H",
          "password": "8uWmwk",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "9",
          "server": "45.85.163.59",
          "server_port": 8000,
          "username": "4BNvpC",
          "password": "oJMZrT",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "10",
          "server": "45.94.39.203",
          "server_port": 8000,
          "username": "cArUrU",
          "password": "Kq0eGn",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "11",
          "server": "45.133.222.224",
          "server_port": 8000,
          "username": "0efVNH",
          "password": "bsrGCW",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "12",
          "server": "147.45.85.207",
          "server_port": 8000,
          "username": "CUhZcy",
          "password": "8PK2TA",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "13",
          "server": "45.93.213.249",
          "server_port": 8000,
          "username": "edBEDG",
          "password": "6wyruh",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

            {
          "type": "http",
          "tag": "14",
          "server": "196.18.1.92",
          "server_port": 8000,
          "username": "8Wymdy",
          "password": "kFSMwQ",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },

        {
          "type": "http",
          "tag": "15",
          "server": "38.154.88.44",
          "server_port": 8000,
          "username": "UMbS8u",
          "password": "7XjKUz",
          "path": "",
          "headers": {},
          "tls": {  "enabled": true,
          "disable_sni": false,
          "server_name": "telewebion.com",
          "insecure": true}

        },
        {
                    "tag": "direct",
                    "type": "direct"
                },
                {
                    "tag": "block",
                    "type": "block"
                },
                {
                    "tag": "dns-out",
                    "type": "dns"
                },
                {
                    "tag": "urltest",
                    "type": "urltest",
                    "outbounds": [

                        "1",
                        "2",
                        "3",
                        "4",
                        "5",
                        "6",
                        "7",
                        "8",
                        "9",
                        "10",
                        "11",
                        "12",
                        "13",
                        "14",
                        "15"

                    ]
                }
            ],
            "route": {
                "auto_detect_interface": true,
                "rules": [
                    {
                        "geosite": "category-ads-all",
                        "outbound": "block"
                    },
                    {
                        "outbound": "dns-out",
                        "protocol": "dns"
                    },
                    {
                        "clash_mode": "direct",
                        "outbound": "direct"
                    },
                    {
                        "clash_mode": "global",
                        "outbound": "hello"
                    },
                    {
                        "geoip": [
                            "cn",
                            "private"
                        ],
                        "outbound": "direct"
                    },
                    {
                        "geosite": "geolocation-!cn",
                        "outbound": "hello1"
                    },
                    {
                        "geosite": "cn",
                        "outbound": "direct"
                    }
                ]
            }
        }
