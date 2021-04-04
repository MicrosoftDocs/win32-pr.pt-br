---
description: O \_ esquema de perfil WLAN define os elementos a seguir.
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: Elementos do esquema de WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647351"
---
# <a name="wlan_profile-schema-elements"></a>\_Elementos do esquema do perfil WLAN

O \_ esquema de perfil WLAN define os elementos a seguir. A maioria dos elementos está no namespace `https://www.microsoft.com/networking/WLAN/profile/v1` , com exceção de [**fipsmode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), que está no namespace `https://www.microsoft.com/networking/WLAN/profile/v2` .

A lista a seguir mostra os elementos definidos na ordem em que os elementos aparecem em um perfil. A ordem dos elementos é imposta. Nem todos os elementos estão em todos os perfis, pois alguns elementos são opcionais.

Essa lista não mostra todos os elementos possíveis que podem aparecer em um perfil sem fio, pois os elementos podem ser adicionados em **xs: qualquer** ponto de inserção.

-   [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
    -   [**nome (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)
    -   [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [**Hex (SSID)**](wlan-profileschema-hex-ssid-element.md)
            -   [**nome (SSID)**](wlan-profileschema-name-ssid-element.md)
        -   [**não difusão (SSIDConfig)**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [**Hotspot2 (WLANProfile)**](wlan-profileschema-hotspot2-element.md)
        -   [**Nome_do_domínio (Hotspot2)**](wlan-profileschema-hotspot2-domainname-element.md)
        -   [**NAIRealm (Hotspot2)**](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [**Network3GPP (Hotspot2)**](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [**RoamingConsortium (Hotspot2)**](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [**ConnectionType (WLANProfile)**](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [**ConnectionMode (WLANProfile)**](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [**AutoSwitch (WLANProfile)**](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
        -   [**conectividade (MSM)**](wlan-profileschema-connectivity-msm-element.md)
            -   [**phyType (conectividade)**](wlan-profileschema-phytype-connectivity-element.md)
        -   [**segurança (MSM)**](wlan-profileschema-security-msm-element.md)
            -   [**authEncryption (segurança)**](wlan-profileschema-authencryption-security-element.md)
                -   [**autenticação (authEncryption)**](wlan-profileschema-authentication-authencryption-element.md)
                -   [**criptografia (authEncryption)**](wlan-profileschema-encryption-authencryption-element.md)
                -   [**useOneX (authEncryption)**](wlan-profileschema-useonex-authencryption-element.md)
                -   [**FIPSmode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [**sharedKey (segurança)**](wlan-profileschema-sharedkey-security-element.md)
                -   [**KeyType (sharedKey)**](wlan-profileschema-keytype-sharedkey-element.md)
                -   [**protegido (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)
                -   [**keymaterial (sharedKey)**](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [**KeyIndex (segurança)**](wlan-profileschema-keyindex-security-element.md)
            -   [**PMKCacheMode (segurança)**](wlan-profileschema-pmkcachemode-security-element.md)
            -   [**PMKCacheTTL (segurança)**](wlan-profileschema-pmkcachettl-security-element.md)
            -   [**PMKCacheSize (segurança)**](wlan-profileschema-pmkcachesize-security-element.md)
            -   [**preAuthMode (segurança)**](wlan-profileschema-preauthmode-security-element.md)
            -   [**preAuthThrottle (segurança)**](wlan-profileschema-preauththrottle-security-element.md)
    -   [**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
            -   [**OUI (OUIHeader)**](wlan-profileschema-oui-ouiheader-element.md)
            -   [**tipo (OUIHeader)**](wlan-profileschema-type-ouiheader-element.md)
        -   [**conectividade (IHV)**](wlan-profileschema-connectivity-ihv-element.md)
        -   [**segurança (IHV)**](wlan-profileschema-security-ihv-element.md)
        -   [**useMSOneX (IHV)**](wlan-profileschema-usemsonex-ihv-element.md)

 

 



