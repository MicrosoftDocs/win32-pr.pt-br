---
description: Devido às diferenças de arquitetura subjacentes no sistema operacional, o Windows XP com Service Pack 3 (SP3) e a API de LAN Sem Fio para Windows XP com Service Pack 2 (SP2) suportam apenas um subconjunto dos elementos descritos no material de referência esquema de perfil WLAN e \_ esquema OneX.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilidade de perfil sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36db0ecea6f85341d904603c99308ec10e79cee20d7567160cd3beee3b13c35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684566"
---
# <a name="wireless-profile-compatibility"></a>Compatibilidade de perfil sem fio

Devido às diferenças de arquitetura subjacentes no sistema operacional, o Windows XP com Service Pack 3 (SP3) e a API de LAN Sem Fio para Windows XP com Service Pack 2 (SP2) suportam apenas um subconjunto dos elementos descritos no material de referência esquema de perfil [WLAN \_ ](wlan-profileschema-schema.md) e [esquema OneX.](onexschema-schema.md)

Todos os perfis que estão em conformidade com Windows XP com SP3 e API de LAN sem fio para o Windows XP com requisitos sp2 também podem ser usados no Windows Vista e Windows Server 2008.

## <a name="wlan_profile-support"></a>Suporte ao perfil \_ WLAN

Os seguintes elementos de perfil WLAN não têm suporte no Windows XP com SP3 ou API de LAN sem \_ fio para Windows XP com SP2:

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
-   type (OUIHeader)
-   useMSOneX (IHV)

A tabela a seguir mostra elementos de perfil WLAN com valores restritos para Windows XP com SP3 e API de LAN sem fio \_ para Windows XP com SP2:



| Elemento                                                                               | Constraint                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**name (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)             | O elemento name é ignorado quando o perfil é salvo no armazenamento de perfil. O nome do perfil é derivado automaticamente do SSID da rede. Para perfis de rede de infraestrutura, o nome do perfil é o SSID da rede. Para perfis de rede ad hoc, o nome do perfil é o SSID da rede ad hoc seguida por `-adhoc` . |
| [**protected (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)       | Deve ter um valor false.                                                                                                                                                                                                                                                                                                                                      |
| [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | Restrito a um elemento [**SSID filho (SSIDConfig).**](wlan-profileschema-ssid-ssidconfig-element.md)                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>Suporte do OneX

Somente o [**elemento EAPConfig**](onexschema-eapconfig-onex-element.md) tem suporte no Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2. Outros elementos OneX, se presentes em um perfil, serão ignorados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API wi-fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Suporte nativo à API Wifi no Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



