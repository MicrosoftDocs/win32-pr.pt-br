---
description: Devido às diferenças de arquitetura subjacentes no sistema operacional, o Windows XP com Service Pack 3 (SP3) e a API de LAN sem fio para Windows XP com Service Pack 2 (SP2) dão suporte apenas a um subconjunto dos elementos descritos no \_ esquema do perfil WLAN e material de referência do esquema Onex.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilidade de perfis sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505923"
---
# <a name="wireless-profile-compatibility"></a>Compatibilidade de perfis sem fio

Devido às diferenças de arquitetura subjacentes no sistema operacional, o Windows XP com Service Pack 3 (SP3) e a API de LAN sem fio para Windows XP com Service Pack 2 (SP2) dão suporte apenas a um subconjunto dos elementos descritos no [ \_ esquema do perfil WLAN](wlan-profileschema-schema.md) e material de referência do [esquema Onex](onexschema-schema.md) .

Todos os perfis que estão em conformidade com os requisitos do Windows XP com SP3 e da API de LAN sem fio para Windows XP com SP2 também podem ser usados no Windows Vista e no Windows Server 2008.

## <a name="wlan_profile-support"></a>\_Suporte a perfis WLAN

Os seguintes elementos de perfil de WLAN \_ não têm suporte no Windows XP com SP3 ou API de LAN sem fio para Windows XP com SP2:

-   conectividade (IHV)
-   IHV (WLANProfile)
-   OUI (OUIHeader)
-   phyType (conectividade)
-   PMKCacheMode (segurança)
-   PMKCacheSize (segurança)
-   PMKCacheTTL (segurança)
-   preAuthMode (segurança)
-   preAuthThrottle (segurança)
-   segurança (IHV)
-   tipo (OUIHeader)
-   useMSOneX (IHV)

A tabela a seguir mostra os \_ elementos de perfil de WLAN com valores restritos para o Windows XP com SP3 e a API de LAN sem fio para Windows XP com SP2:



| Elemento                                                                               | Constraint                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**nome (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)             | O elemento Name é ignorado quando o perfil é salvo no repositório de perfis. O nome do perfil é derivado automaticamente do SSID da rede. Para perfis de rede de infraestrutura, o nome do perfil é o SSID da rede. Para perfis de rede ad hoc, o nome do perfil é o SSID da rede ad hoc seguida por `-adhoc` . |
| [**protegido (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)       | Deve ter um valor de FALSE.                                                                                                                                                                                                                                                                                                                                      |
| [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | Restrito a um elemento [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) filho.                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>Suporte a OneX

Somente o elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) tem suporte no Windows XP com SP3 e na API de LAN sem fio para Windows XP com SP2. Outros elementos OneX, se presentes em um perfil, serão ignorados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API Wi-Fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Suporte nativo à API WiFi no Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



