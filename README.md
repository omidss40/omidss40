{
    "dns": {
        "disable_cache": false,
        "disable_expire": false,
        "final": "dns-remote",
        "rules": [
            {1
                "domain_suffix": [
                    "ir",
                    "firefox.com"
                ],
                "server": "dns-direct"
            },
            {
                "disable_cache": true,
                "domain_suffix": [
                    "app-measurement.com",
                    "crashlytics.com",
                    "google-analytics.com",
                    "appcenter.ms",
                    "firebase.io"
                ],
                "geosite": "category-ads-all",
                "server": "dns-block"
            },
            {
                "disable_cache": true,
                "domain_suffix": [
                    ".arpa.",
                    ".arpa"
                ],
                "server": "dns-block"
            }
        ],
        "servers": [
            {
                "address": "https://1.1.1.1/dns-query",
                "address_resolver": "dns-direct",
                "address_strategy": "prefer_ipv4",
                "strategy": "ipv4_only",
                "tag": "dns-remote"
            },
            {
                "address": "local",
                "detour": "Direct",
                "tag": "dns-direct"
            },
            {
                "address": "rcode://success",
                "tag": "dns-block"
            }
        ],
        "strategy": "ipv4_only"
    },
    "experimental": {
        "clash_api": {
            "cache_file": "cache.db",
            "default_mode": "rule",
            "external_controller": "127.0.0.1:9090",
            "external_ui": "dashboard",
            "secret": "",
            "store_selected": true
        }
    },
    "inbounds": [
        {
            "domain_strategy": "prefer_ipv4",
            "listen": "::",
            "listen_port": 2080,
            "sniff": true,
            "tag": "mixed-in",
            "type": "mixed"
        }
    ],
    "log": {
        "level": "info"
    },
    "outbounds": [
        {
            "outbounds": [
                "Best Latency",
                "SSH1",
                "SSH2",
                "SSH3",
                "SSH4",
                "SSH5",
                "SSH6",
                "SSH7",
                "SSH8",
                "SSH9",
                "SSH10"
            ],
            "tag": "Select Manually",
            "type": "selector"
        },
        {
            "interval": "1m0s",
            "outbounds": [
                "SSH1",
                "SSH2",
                "SSH3",
                "SSH4",
                "SSH5",
                "SSH6",
                "SSH7",
                "SSH8",
                "SSH9",
                "SSH10"
            ],
            "tag": "Best Latency",
            "type": "urltest",
            "url": "https://detectportal.firefox.com/success.txt"
        },
        {
            "domain_strategy": "",
            "password": "xLo3xj",
            "server": "103.229.28.29",
            "server_port": 8000,
            "tag": "SSH1",
            "type": "nl1",
            "user": "n4W3SX"
        },
        {
            "domain_strategy": "",
            "password": "CHoNSJ",
            "server": "45.147.31.173",
            "server_port": 8000,
            "tag": "SSH2",
            "type": "sshnl2",
            "user": "beHWTa"
        },
        {
            "domain_strategy": "",
            "password": "2P7MuX",
            "server": "103.229.28.132",
            "server_port": 8000,
            "tag": "SSH3",
            "type": "sshnl3",
            "user": "JuYHwf"
        },
        {
            "domain_strategy": "",
            "password": "uCq8hW",
            "server": "45.142.30.14",
            "server_port": 8000,
            "tag": "SSH4",
            "type": "sshnl4",
            "user": "7aBP2b"
        },
        {
            "domain_strategy": "",
            "password": "KoXPtc",
            "server": "103.229.28.11",
            "server_port": 8000,
            "tag": "SSH5",
            "type": "sshnl5",
            "user": "1BgdLE"
        },
        {
            "domain_strategy": "",
            "password": "VZC1ty",
            "server": "103.229.28.56",
            "server_port": 8000,
            "tag": "SSH6",
            "type": "sshnl6",
            "user": "mfaGKE"
        },
        {
            "domain_strategy": "",
            "password": "8uWmwk",
            "server": "103.229.28.68",
            "server_port": 8000,
            "tag": "SSH7",
            "type": "sshnl7",
            "user": "wJvd4H"
        },
        {
            "domain_strategy": "",
            "password": "oJMZrT",
            "server": "45.85.163.59",
            "server_port": 8000,
            "tag": "SSH8",
            "type": "sshnl8",
            "user": "4BNvpC"
        },
        {
            "domain_strategy": "",
            "password": "Kq0eGn",
            "server": "45.94.39.203",
            "server_port": 8000,
            "tag": "SSH9",
            "type": "sshnl9",
            "user": "cArUrU"
        },
        {
            "domain_strategy": "",
            "password": "Nt8v9L",
            "server": "185.202.0.69",
            "server_port": 8000,
            "tag": "SSH10",
            "type": "sshrussia",
            "user": "UmumW3"
        },
        {
            "tag": "Direct",
            "type": "direct"
        },
        {
            "tag": "Bypass",
            "type": "direct"
        },
        {
            "tag": "Block",
            "type": "block"
        },
        {
            "tag": "DNS-Out",
            "type": "dns"
        }
    ],
    "route": {
        "auto_detect_interface": true,
        "final": "Select Manually",
        "geoip": {
            "download_detour": "Direct",
            "path": "geoip.db"
        },
        "geosite": {
            "download_detour": "Direct",
            "path": "geosite.db"
        },
        "rules": [
            {
                "outbound": "DNS-Out",
                "port": 53
            },
            {
                "inbound": "dns-in",
                "outbound": "DNS-Out"
            },
            {
                "geoip": "private",
                "outbound": "Bypass"
            },
            {
                "geosite": "category-ads-all",
                "outbound": "Block"
            },
            {
                "domain_suffix": [
                    "appcenter.ms",
                    "app-measurement.com",
                    "firebase.io",
                    "crashlytics.com",
                    "google-analytics.com"
                ],
                "outbound": "Block"
            },
            {
                "geoip": "ir",
                "outbound": "Bypass"
            },
            {
                "domain_suffix": "ir",
                "outbound": "Bypass"
            },
            {
                "ip_cidr": [
                    "224.0.0.0/3",
                    "ff00::/8"
                ],
                "outbound": "Block",
                "source_ip_cidr": [
                    "224.0.0.0/3",
                    "ff00::/8"
                ]
            }
        ]
    }
}
