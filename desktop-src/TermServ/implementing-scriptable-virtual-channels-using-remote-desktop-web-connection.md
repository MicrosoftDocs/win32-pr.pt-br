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
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a><span data-ttu-id="450e4-103">Implementando canais virtuais programáveis usando o Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="450e4-103">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>

<span data-ttu-id="450e4-104">Os exemplos de procedimento e código a seguir mostram as etapas para implementar canais virtuais programáveis com Conexão Web de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="450e4-104">The following procedure and code examples show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span> <span data-ttu-id="450e4-105">Os exemplos foram escritos em Visual Basic Scripting Edition e presumem que o Área de Trabalho Remota controle ActiveX se chama "MsRdpClient".</span><span class="sxs-lookup"><span data-stu-id="450e4-105">The examples were written in Visual Basic Scripting Edition and assume that the Remote Desktop ActiveX control is named "MsRdpClient".</span></span>

<span data-ttu-id="450e4-106">**Para criar e implantar canais virtuais programáveis**</span><span class="sxs-lookup"><span data-stu-id="450e4-106">**To create and deploy scriptable virtual channels**</span></span>

1.  <span data-ttu-id="450e4-107">Implante o lado do servidor do aplicativo e verifique se ele está em execução no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="450e4-107">Deploy the server side of the application and make sure it is running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="450e4-108">Para obter informações sobre a implantação de aplicativos de canais virtuais no servidor, consulte [virtual Channel Server Application](virtual-channel-server-application.md).</span><span class="sxs-lookup"><span data-stu-id="450e4-108">For information about deploying virtual channels applications on the server, see [Virtual Channel Server Application](virtual-channel-server-application.md).</span></span>
2.  <span data-ttu-id="450e4-109">No script do cliente, chame [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md), passando uma cadeia de caracteres que contém uma lista separada por vírgulas de nomes de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="450e4-109">In your client script, call [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md), passing a string that contains a comma-separated list of virtual channel names.</span></span>

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    <span data-ttu-id="450e4-110">Para obter informações sobre restrições de nomenclatura de canal virtual, consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md).</span><span class="sxs-lookup"><span data-stu-id="450e4-110">For information about virtual channel naming restrictions, see [Virtual Channel Client Registration](virtual-channel-client-registration.md).</span></span>

3.  <span data-ttu-id="450e4-111">Chame [**IMsTscAx:: Connect**](imstscax-connect.md) para criar sua conexão de serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="450e4-111">Call [**IMsTscAx::Connect**](imstscax-connect.md) to create your Remote Desktop Services connection.</span></span>

    ```VB
    MsRdpClient.connect
    ```

    

4.  <span data-ttu-id="450e4-112">Use o método [**IMsTscAx:: SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) para enviar dados ao servidor, passando uma cadeia de caracteres que contém o nome do canal virtual e uma segunda cadeia de caracteres que contém os dados a serem passados.</span><span class="sxs-lookup"><span data-stu-id="450e4-112">Use the [**IMsTscAx::SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) method to send data to the server, passing a string that contains the virtual channel name and a second string that contains the data to be passed.</span></span>

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  <span data-ttu-id="450e4-113">Receba dados do servidor no evento [**IMsTscAxEvents:: OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) .</span><span class="sxs-lookup"><span data-stu-id="450e4-113">Receive data from the server on the [**IMsTscAxEvents::OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) event.</span></span>

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




