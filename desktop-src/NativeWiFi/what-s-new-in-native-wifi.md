---
description: Novidades no Wi-Fi nativo
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Novidades no Wi-Fi nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780204"
---
# <a name="whats-new-in-native-wifi"></a>Novidades no Wi-Fi nativo

## <a name="windows-10-version-2004"></a>Windows 10, versão 2004

Consulte [provisionar um perfil de Wi-Fi por meio de um site](prov-wifi-profile-via-website.md).

## <a name="windows-10"></a>Windows 10

O suporte para hotspot 2,0 foi adicionado ao [esquema de \_ perfil WLAN](wlan-profileschema-schema.md). O HotSpot 2,0 permite a conexão automática a serviços de Wi-Fi públicos usando credenciais existentes e associação em redes de provedor de serviços. Os provedores de serviço especificam como as conexões são feitas usando os novos elementos de esquema para descrever quais redes usar e como se autenticar neles. Consulte a documentação do elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) para obter detalhes.

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

Os recursos a seguir foram adicionados às APIs nativas do wifi no Windows 8 e no Windows Server 2012.

Um Wi-Fi recurso direto com base no desenvolvimento do Wi-Fi especificação técnica ponto a ponto v 1.1 pela Aliança de Wi-Fi (consulte [especificações publicadas da Wi-Fi Alliance](https://www.wi-fi.org/)). O objetivo do Wi-Fi especificação técnica ponto a ponto é fornecer uma solução para Wi-Fi conectividade de dispositivo para dispositivo sem a necessidade de um ponto de acesso sem fio (AP sem fio) configurar a conexão ou o uso do mecanismo existente Wi-Fi adhoc (IBSS).

As funções a seguir dão suporte ao recurso direto Wi-Fi.

-   [**\_retorno de \_ \_ chamada completo de sessão aberta WFD \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Os recursos a seguir foram adicionados às APIs nativas do wifi no Windows 7 e no Windows Server 2008 R2.

A rede hospedada sem fio permite que um único adaptador sem fio físico se conecte como um cliente a um ponto de acesso de hardware (AP), ao mesmo tempo que atua como um AP de software, permitindo que outros dispositivos com capacidade de conexão sem fio se conectem a ele.

As funções a seguir dão suporte ao recurso de rede hospedada sem fio.

-   [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

As novas estruturas a seguir funcionam com a rede hospedada sem fio.

-   [**\_configurações de \_ conexão de rede hospedada da \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**\_alteração de \_ \_ estado de par de dados de rede \_ hospedado \_ da WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**\_estado de \_ par de rede hospedada da \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**\_estado de \_ rádio da rede hospedada da \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**\_configurações de \_ segurança de rede hospedada da \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**\_alteração de \_ estado da rede hospedada pela \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**\_status da \_ rede hospedada da WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

As novas enumerações a seguir funcionam com a rede hospedada sem fio.

-   [**\_código de \_ notificação de rede hospedada da \_ WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**\_opcode de \_ rede hospedada da WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**\_estado de \_ \_ autenticação de mesmo nível de rede HOSPEDAda da \_ WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**\_motivo da \_ rede hospedada da WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**\_estado da \_ rede hospedada da WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a rede hospedada sem fio](about-the-wireless-hosted-network.md)
</dt> <dt>

[Usando rede hospedada sem fio e compartilhamento de conexão com a Internet](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



