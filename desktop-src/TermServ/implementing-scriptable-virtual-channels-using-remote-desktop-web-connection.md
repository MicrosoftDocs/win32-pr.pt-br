---
title: Implementando canais virtuais programáveis usando o Conexão Web de Área de Trabalho Remota
description: Exemplos de código que mostram as etapas para implementar canais virtuais programáveis com Conexão Web de Área de Trabalho Remota.
ms.assetid: a482b84d-96b6-4f42-8841-7039a1882789
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a36f685de01312a93df67deb6be16ce031794c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636474"
---
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a>Implementando canais virtuais programáveis usando o Conexão Web de Área de Trabalho Remota

Os exemplos de procedimento e código a seguir mostram as etapas para implementar canais virtuais programáveis com Conexão Web de Área de Trabalho Remota. Os exemplos foram escritos em Visual Basic Scripting Edition e presumem que o Área de Trabalho Remota controle ActiveX se chama "MsRdpClient".

**Para criar e implantar canais virtuais programáveis**

1.  Implante o lado do servidor do aplicativo e verifique se ele está em execução no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Para obter informações sobre a implantação de aplicativos de canais virtuais no servidor, consulte [virtual Channel Server Application](virtual-channel-server-application.md).
2.  No script do cliente, chame [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md), passando uma cadeia de caracteres que contém uma lista separada por vírgulas de nomes de canal virtual.

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    Para obter informações sobre restrições de nomenclatura de canal virtual, consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md).

3.  Chame [**IMsTscAx:: Connect**](imstscax-connect.md) para criar sua conexão de serviços de área de trabalho remota.

    ```VB
    MsRdpClient.connect
    ```

    

4.  Use o método [**IMsTscAx:: SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) para enviar dados ao servidor, passando uma cadeia de caracteres que contém o nome do canal virtual e uma segunda cadeia de caracteres que contém os dados a serem passados.

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  Receba dados do servidor no evento [**IMsTscAxEvents:: OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) .

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




