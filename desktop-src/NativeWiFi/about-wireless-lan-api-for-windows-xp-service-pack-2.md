---
description: Há suporte para um subconjunto da funcionalidade nativa da API WiFi no Windows XP com Service Pack 2 (SP2) e no Windows XP com Service Pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Suporte nativo à API WiFi no Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296851"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>Suporte nativo à API WiFi no Windows XP

Há suporte para um subconjunto da funcionalidade nativa da API WiFi no Windows XP com Service Pack 2 (SP2) e no Windows XP com Service Pack 3 (SP3). Por padrão, essa funcionalidade está incluída no Windows XP com SP3. No Windows XP com SP2, essa funcionalidade pode ser adicionada aplicando-se um hotfix, que é conhecido como API de LAN sem fio para Windows XP com Service Pack 2 (SP2). Para obter mais informações ou baixar o hotfix, consulte "os desenvolvedores não podem criar programas de cliente sem fio que gerenciam perfis e conexões sem fio por meio do serviço de configuração zero sem fio no Microsoft Windows XP Service Pack 2 (SP2)" na base de dados de conhecimento de ajuda e suporte em [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .

Devido a diferenças arquitetônicas subjacentes no Windows XP, a API Wi-Fi nativa no tem algumas limitações. Aqui está uma lista de limitações:

-   No máximo um SSID pode ser associado a um perfil.
-   As redes de infraestrutura sempre aparecem antes das redes ad hoc na lista de perfis.
-   Os nomes de perfil são derivados do SSID e não podem ser definidos pelo usuário para uma cadeia de caracteres arbitrária.
-   Não há suporte para tipos PHY.
-   Não há suporte para o cache de PMK (chave mestra de paridade).
-   Não há suporte para funções de extensibilidade de fornecedor de hardware independente (IHV).
-   Não há suporte para permissões de perfil.
-   Somente a conexão do ACM de notificação da WLAN \_ \_ \_ \_ foi concluída e as notificações de notificação de WLAN \_ \_ ACM \_ desconectadas estão disponíveis.
-   Não há suporte para definições de configuração global 802.1 X e EAPOL.

As funções a seguir têm suporte do Windows XP com SP3 e da API de LAN sem fio para Windows XP com SP2:

-   [**retorno de chamada de \_ notificação de WLAN \_**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [**WlanAllocateMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [**WlanFreeMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [**WlanGetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [**WlanOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [**WlanSetProfileEapXmlUserData**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [**WlanSetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [**WlanSetProfilePosition**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[Sobre WiFi nativo](about-native-wifi.md)
</dt> </dl>

 

 
