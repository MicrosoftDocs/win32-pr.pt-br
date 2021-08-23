---
description: Há suporte para um subconjunto da funcionalidade da API Wifi Nativa no Windows XP com Service Pack 2 (SP2) e Windows XP com Service Pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Suporte nativo à API Wifi no Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc284ed24a6aa6ddb266b410a6233c15e063bf909aa9c82f0afa3dc070c9289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685306"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>Suporte nativo à API Wifi no Windows XP

Há suporte para um subconjunto da funcionalidade da API Wifi Nativa no Windows XP com Service Pack 2 (SP2) e Windows XP com Service Pack 3 (SP3). Essa funcionalidade está incluída no Windows XP com SP3 por padrão. No Windows XP com SP2, essa funcionalidade pode ser adicionada aplicando um hotfix, que é conhecido como API de LAN sem fio para Windows XP com Service Pack 2 (SP2). Para obter mais informações ou para baixar o hotfix, consulte "Os desenvolvedores não podem criar programas cliente sem fio que gerenciam perfis sem fio e conexões pelo serviço de Configuração Sem Fio Zero no Microsoft Windows XP Service Pack 2 (SP2)" na Base de Dados de Conhecimento de Ajuda e Suporte em [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .

Devido às diferenças de arquitetura subjacentes Windows XP, a API Wifi Nativa no tem algumas limitações. Aqui está uma lista de limitações:

-   No máximo um SSID pode ser associado a um perfil.
-   As redes de infraestrutura sempre aparecem antes das redes ad hoc na lista de perfis.
-   Os nomes de perfil são derivados do SSID e não podem ser definidos pelo usuário como uma cadeia de caracteres arbitrária.
-   Não há suporte para tipos PHY.
-   Não há suporte para o cache de PMK (chave mestra emparelhada).
-   Não há suporte para funções de extensibilidade de IHV (fornecedor independente de hardware).
-   Não há suporte para permissões de perfil.
-   Somente a conexão acm de notificação wlan concluída e as notificações \_ \_ de \_ \_ \_ \_ notificação wlan acm \_ desconectadas estão disponíveis.
-   Não há suporte para definições de configuração global 802.1X e EAPOL.

As funções a seguir têm suporte do Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:

-   [**RETORNO DE CHAMADA \_ DE \_ NOTIFICAÇÃO WLAN**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
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

[Sobre Wifi nativo](about-native-wifi.md)
</dt> </dl>

 

 
