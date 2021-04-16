---
description: A figura a seguir mostra a relação entre monitores e outros componentes da arquitetura de Monitor de Rede.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Arquitetura do monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567852"
---
# <a name="monitor-architecture"></a><span data-ttu-id="2c80e-103">Arquitetura do monitor</span><span class="sxs-lookup"><span data-stu-id="2c80e-103">Monitor Architecture</span></span>

<span data-ttu-id="2c80e-104">A figura a seguir mostra a relação entre [*monitores*](m.md) e outros componentes da arquitetura de monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="2c80e-104">The following figure shows the relationship between [*monitors*](m.md) and other components of the Network Monitor architecture.</span></span>

![relação entre monitores e outros componentes do monitor de rede](images/nmarch2.png)

<span data-ttu-id="2c80e-106">O tráfego de rede é coletado (como quadros individuais) do driver NDIS.</span><span class="sxs-lookup"><span data-stu-id="2c80e-106">The network traffic is collected (as individual frames) from the NDIS driver.</span></span> <span data-ttu-id="2c80e-107">O driver de Monitor de Rede (Nmnt.sys), em seguida, roteia os quadros para um NPP (provedor de pacotes de rede) que, por sua vez, captura os dados em modo em tempo real.</span><span class="sxs-lookup"><span data-stu-id="2c80e-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which in turn captures the data in real-time mode.</span></span> <span data-ttu-id="2c80e-108">O NPP é uma coleção de interfaces COM usadas para capturar dados.</span><span class="sxs-lookup"><span data-stu-id="2c80e-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="2c80e-109">Nesse caso, a interface [**IRTC**](irtc.md) é usada para executar uma captura em tempo real.</span><span class="sxs-lookup"><span data-stu-id="2c80e-109">In this case, the [**IRTC**](irtc.md) interface is used to perform a real-time capture.</span></span>

> [!Note]  
> <span data-ttu-id="2c80e-110">O NPP é usado para capturas atrasadas e em tempo real.</span><span class="sxs-lookup"><span data-stu-id="2c80e-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="2c80e-111">Para capturas atrasadas usadas por especialistas e analisadores, a interface [**IDelaydC**](idelaydc.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="2c80e-111">For delayed captures used by experts and parsers, the [**IDelaydC**](idelaydc.md) interface is used.</span></span>

 

<span data-ttu-id="2c80e-112">Em seguida, o monitor examina os dados capturados no modo em tempo real, detectando condições de rede específicas e gerando eventos conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="2c80e-112">The monitor then examines the captured data in real-time mode, detecting specific network conditions and generating events as required.</span></span>

<span data-ttu-id="2c80e-113">Três outros componentes são usados por aplicativos de monitor: a ferramenta de controle de monitor, o serviço de controle de monitor (MCSVC) e o Visualizador de Eventos:</span><span class="sxs-lookup"><span data-stu-id="2c80e-113">Three other components are used by monitor applications: the Monitor Control Tool, the Monitor Control Service (MCSVC), and the Event Viewer:</span></span>

-   <span data-ttu-id="2c80e-114">A ferramenta de controle de monitor é usada para gerenciar seus aplicativos de monitor.</span><span class="sxs-lookup"><span data-stu-id="2c80e-114">The Monitor Control Tool is used to manage your monitor applications.</span></span> <span data-ttu-id="2c80e-115">Isso inclui a configuração e a execução de todos os seus aplicativos de monitor.</span><span class="sxs-lookup"><span data-stu-id="2c80e-115">This includes configuring and running all your monitor applications.</span></span>
-   <span data-ttu-id="2c80e-116">O serviço de controle de monitor (MCSVC) dispara eventos, fornece um link de comunicações para o WMI para exibição de eventos e coordena o processamento de operações de monitor.</span><span class="sxs-lookup"><span data-stu-id="2c80e-116">The Monitor Control Service (MCSVC) fires events, provides a communications link to WMI for event viewing, and coordinates the processing of monitor operations.</span></span>
-   <span data-ttu-id="2c80e-117">O Visualizador de Eventos exibe os eventos acionados pelo serviço de controle de monitor.</span><span class="sxs-lookup"><span data-stu-id="2c80e-117">The Event Viewer displays the events fired by the Monitor Control Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c80e-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c80e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c80e-119">**IMonitor**</span><span class="sxs-lookup"><span data-stu-id="2c80e-119">**IMonitor**</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="2c80e-120">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="2c80e-120">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="2c80e-121">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="2c80e-121">**IRTC**</span></span>](irtc.md)
</dt> </dl>

 

 



