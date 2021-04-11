---
title: Criando assinaturas de evento de hardware
description: Em computadores que têm um BMC (Baseboard Management Controller) instalado, os eventos de hardware são gerados e registrados no SEL (log de eventos do sistema), que é o armazenamento de eventos do BMC armazenado na memória não volátil.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5f904e74d1f29b0666c9cb02b13689a0633bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294320"
---
# <a name="creating-hardware-event-subscriptions"></a><span data-ttu-id="10d65-103">Criando assinaturas de evento de hardware</span><span class="sxs-lookup"><span data-stu-id="10d65-103">Creating Hardware Event Subscriptions</span></span>

<span data-ttu-id="10d65-104">Em computadores que têm um BMC (Baseboard Management Controller) instalado, os eventos de hardware são gerados e registrados no SEL (log de eventos do sistema), que é o armazenamento de eventos do BMC armazenado na memória não volátil.</span><span class="sxs-lookup"><span data-stu-id="10d65-104">On computers that have a Baseboard Management Controller (BMC) installed, hardware events are raised and logged in the System event log (SEL), which is the BMC event store that is stored in nonvolatile memory.</span></span> <span data-ttu-id="10d65-105">Para ler esses eventos de hardware no Windows Server 2008 usando o Visualizador de Eventos, você deve criar uma assinatura para os eventos.</span><span class="sxs-lookup"><span data-stu-id="10d65-105">To read these hardware events on Windows Server 2008 using the Event Viewer, you must create a subscription to the events.</span></span> <span data-ttu-id="10d65-106">As assinaturas de evento de hardware só funcionarão no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="10d65-106">The hardware event subscriptions will only work on Windows Server 2008.</span></span>

<span data-ttu-id="10d65-107">O procedimento a seguir define como criar a assinatura de evento do SEL para recuperar os eventos de hardware:</span><span class="sxs-lookup"><span data-stu-id="10d65-107">The following procedure defines how to create the SEL event subscription to retrieve the hardware events:</span></span>

1.  <span data-ttu-id="10d65-108">Salve o XML a seguir em um arquivo. XML (neste exemplo, o arquivo é denominado Wsmanselrg.xml).</span><span class="sxs-lookup"><span data-stu-id="10d65-108">Save the following XML in an .xml file (in this example the file is named Wsmanselrg.xml).</span></span> <span data-ttu-id="10d65-109">Esse XML define a assinatura.</span><span class="sxs-lookup"><span data-stu-id="10d65-109">This XML defines the subscription.</span></span>

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  <span data-ttu-id="10d65-110">Crie uma assinatura de evento executando o seguinte comando em uma janela de prompt de comando (o programa Wecutil.exe está localizado no diretório% SYSTEMROOT% \\ System32):</span><span class="sxs-lookup"><span data-stu-id="10d65-110">Create an event subscription by executing the following command in a command prompt window (the Wecutil.exe program is located in the %SYSTEMROOT%\\System32 directory.):</span></span>

    <span data-ttu-id="10d65-111">**Wecutil cs** *<path> \\wsmanselrg.xml*</span><span class="sxs-lookup"><span data-stu-id="10d65-111">**Wecutil cs** *<path>\\wsmanselrg.xml*</span></span>

3.  <span data-ttu-id="10d65-112">Verifique se a assinatura está ativa executando o seguinte comando em uma janela de prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="10d65-112">Ensure that the subscription is active by executing the following command in a command prompt window:</span></span>

    <span data-ttu-id="10d65-113">**Wecutil gr** *wsmanselrg*</span><span class="sxs-lookup"><span data-stu-id="10d65-113">**Wecutil gr** *wsmanselrg*</span></span>

<span data-ttu-id="10d65-114">O BMC é um microcontrolador conectado localmente a um servidor.</span><span class="sxs-lookup"><span data-stu-id="10d65-114">The BMC is a microcontroller attached locally to a server.</span></span> <span data-ttu-id="10d65-115">BMCs têm sensores que monitoram o estado físico do servidor e uma conexão de rede separada que pode se comunicar pela rede, mesmo que o servidor esteja offline.</span><span class="sxs-lookup"><span data-stu-id="10d65-115">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="10d65-116">Você tem acesso aos dados do BMC por meio do provedor WMI da IPMI (interface de gerenciamento de plataforma inteligente).</span><span class="sxs-lookup"><span data-stu-id="10d65-116">You have access to BMC data through the Intelligent Platform Management Interface (IPMI) WMI Provider.</span></span> <span data-ttu-id="10d65-117">Para obter mais informações sobre o provedor IPMI, consulte [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="10d65-117">For more information about the IPMI provider, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

<span data-ttu-id="10d65-118">O computador deve ter o BMC e o provedor IPMI instalados para que a assinatura de evento funcione.</span><span class="sxs-lookup"><span data-stu-id="10d65-118">The computer must have the BMC and the IPMI provider installed for the event subscription to work.</span></span> <span data-ttu-id="10d65-119">Para computadores em execução no Windows Server 2008, o provedor IPMI é instalado por padrão.</span><span class="sxs-lookup"><span data-stu-id="10d65-119">For computers running on Windows Server 2008, the IPMI provider is installed by default.</span></span> <span data-ttu-id="10d65-120">Se o BMC não estiver disponível, o driver IPMI não poderá ser instalado e o status do tempo de execução da assinatura sempre exibirá um erro (falha genérica 0x8004001-WMI).</span><span class="sxs-lookup"><span data-stu-id="10d65-120">If the BMC is not available, then IPMI driver cannot be installed and the subscription runtime status will always display an error (0x8004001 - WMI Generic Failure).</span></span>

 

 