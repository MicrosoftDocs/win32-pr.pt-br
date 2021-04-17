---
description: Demonstra o uso de funções de rede hospedadas sem fio.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Exemplo de rede hospedada sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775680"
---
# <a name="wireless-hosted-network-sample"></a>Exemplo de rede hospedada sem fio

Um exemplo de rede hospedada sem fio que demonstra o uso de funções de rede hospedadas sem fio está incluído no SDK (Software Development Kit) do Microsoft Windows. A versão mais recente do SDK do Windows está disponível no [centro de download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).

Por padrão, o código-fonte do exemplo de rede hospedada sem fio é instalado no seguinte diretório:

**C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ NetDs \\ WLAN**

O exemplo de rede hospedada sem fio está localizado na seguinte pasta:

**WirelessHostedNetwork**

O exemplo de rede hospedada sem fio pode ser compilado no SDK do Windows para o Windows 7. O exemplo de rede hospedada sem fio pode ser executado no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado.

No Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado, o sistema operacional instalará um dispositivo virtual se um adaptador sem fio compatível com a rede hospedada estiver presente no computador. Esse dispositivo virtual normalmente aparece na "pasta Conexões de rede" como "conexão de rede sem fio 2" com um nome de dispositivo "adaptador de miniporta WiFi virtual da Microsoft" se o computador tiver um único adaptador de rede sem fio. Este dispositivo virtual é usado exclusivamente para executar conexões de SoftAP (ponto de acesso de software). O tempo de vida desse dispositivo virtual está vinculado ao adaptador sem fio físico. Se o adaptador sem fio físico estiver desabilitado, esse dispositivo virtual também será removido.

As funções de rede hospedada sem fio são usadas para iniciar e parar a rede hospedada sem fio, definir ou alterar as configurações ou consultar informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a rede hospedada sem fio](about-the-wireless-hosted-network.md)
</dt> <dt>

[Usando rede hospedada e compartilhamento de conexão com a Internet](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



