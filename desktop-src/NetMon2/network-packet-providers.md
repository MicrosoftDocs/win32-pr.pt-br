---
description: Os NPPs (provedores de pacotes de rede) são Monitor de Rede componentes do sistema que coletam o tráfego de rede (quadros) da rede e os transmitem para a interface do usuário do Monitor de Rede e para os aplicativos do NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Provedores de pacotes de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837292"
---
# <a name="network-packet-providers"></a><span data-ttu-id="86b50-103">Provedores de pacotes de rede</span><span class="sxs-lookup"><span data-stu-id="86b50-103">Network Packet Providers</span></span>

<span data-ttu-id="86b50-104">Os NPPs (provedores de pacotes de rede) são Monitor de Rede componentes do sistema que coletam o tráfego de rede (quadros) da rede e os transmitem para a interface do usuário do Monitor de Rede e para os [*aplicativos do NPP*](n.md).</span><span class="sxs-lookup"><span data-stu-id="86b50-104">Network packet providers (NPPs) are Network Monitor system components that collect network traffic (frames) from the network and pass them on to the Network Monitor UI, and [*NPP applications*](n.md).</span></span>

<span data-ttu-id="86b50-105">A ilustração a seguir mostra dois NPPs: o NPP de NDIS fornecido pelo Monitor de Rede e um NPP personalizado.</span><span class="sxs-lookup"><span data-stu-id="86b50-105">The following illustration shows two NPPs: the NDIS NPP provided by Network Monitor and a custom NPP.</span></span>

![NPP NDIS fornecidos pelo monitor de rede e um NPP personalizado](images/npp.png)

<span data-ttu-id="86b50-107">O NPP NDIS fornecido pelo Monitor de Rede é Ndisnpp.dll.</span><span class="sxs-lookup"><span data-stu-id="86b50-107">The NDIS NPP provided by Network Monitor is Ndisnpp.dll.</span></span> <span data-ttu-id="86b50-108">Esse NPP usa o Nmnt.sys (driver de sistema Monitor de Rede) para obter os quadros coletados da rede e várias interfaces COM (chamadas de interfaces NPP) para passar os quadros para a interface do usuário do Monitor de Rede e para os aplicativos NPP, nos quais eles podem ser exibidos e analisados.</span><span class="sxs-lookup"><span data-stu-id="86b50-108">This NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network and several COM interfaces (referred to as the NPP interfaces) to pass the frames on to the Network Monitor UI, and NPP applications, where they can be displayed and analyzed.</span></span>

<span data-ttu-id="86b50-109">Ndisnpp.dll conecta-se à camada [*NDIS*](n.md) para obter seu tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="86b50-109">Ndisnpp.dll connects to the [*NDIS*](n.md) layer to obtain its network traffic.</span></span> <span data-ttu-id="86b50-110">(O NPPs personalizado pode ignorar a camada NDIS e se comunicar diretamente com o hardware de rede.) Lembre-se de que, independentemente de um NPP usar o NDIS, o NPPs pode se conectar a qualquer número de placas de rede e que todas as NPPs devem oferecer suporte às mesmas interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="86b50-110">(Custom NPPs can bypass the NDIS layer and communicate directly with the networking hardware.) Be aware that regardless of whether an NPP uses NDIS, NPPs can connect to any number of network cards and that all NPPs must support the same NPP interfaces.</span></span>

<span data-ttu-id="86b50-111">Antes que um aplicativo possa começar a capturar dados, ele deve:</span><span class="sxs-lookup"><span data-stu-id="86b50-111">Before an application can start to capture data, it must:</span></span>

-   <span data-ttu-id="86b50-112">Selecione a placa de interface de rede (NIC) que conectará o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="86b50-112">Select the network interface card (NIC) that will connect the NPP to the network.</span></span>
-   <span data-ttu-id="86b50-113">Selecione a interface NPP que será usada para capturar os quadros de rede.</span><span class="sxs-lookup"><span data-stu-id="86b50-113">Select the NPP interface that will be used to capture the network frames.</span></span>
-   <span data-ttu-id="86b50-114">Use a interface selecionada para se conectar à NIC.</span><span class="sxs-lookup"><span data-stu-id="86b50-114">Use the selected interface to connect to the NIC.</span></span>

<span data-ttu-id="86b50-115">Para obter mais informações sobre como enumerar e selecionar uma placa de interface de rede, consulte [selecionando uma placa de interface de rede](selecting-a-network-interface-card.md).</span><span class="sxs-lookup"><span data-stu-id="86b50-115">For more information about how to enumerate and select a network interface card, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md).</span></span>

<span data-ttu-id="86b50-116">Para obter mais informações sobre interfaces COM expostas por NPPs, consulte [selecionando uma interface NPP](selecting-an-npp-interface.md).</span><span class="sxs-lookup"><span data-stu-id="86b50-116">For more information about COM interfaces exposed by NPPs, see [Selecting an NPP Interface](selecting-an-npp-interface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86b50-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86b50-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86b50-118">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="86b50-118">**IDelaydC**</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="86b50-119">**IESP**</span><span class="sxs-lookup"><span data-stu-id="86b50-119">**IESP**</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="86b50-120">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="86b50-120">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="86b50-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="86b50-121">**IStats**</span></span>](istats.md)
</dt> </dl>

 

 



