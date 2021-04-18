---
description: Os NPPs (provedores de pacotes de rede) fornecem interfaces COM que são chamadas por aplicativos NPP e Monitor de Rede.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Interfaces NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753136"
---
# <a name="npp-interfaces"></a><span data-ttu-id="5c96e-103">Interfaces NPP</span><span class="sxs-lookup"><span data-stu-id="5c96e-103">NPP Interfaces</span></span>

<span data-ttu-id="5c96e-104">Os NPPs (provedores de pacotes de rede) fornecem interfaces COM que são chamadas por aplicativos NPP e Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="5c96e-104">Network packet providers (NPPs) provide COM interfaces that are called by NPP applications, and Network Monitor.</span></span> <span data-ttu-id="5c96e-105">Ao chamar [CreateNPPInterface](createnppinterface.md), lembre-se de que cada NPP é representado como um único objeto com em processo.</span><span class="sxs-lookup"><span data-stu-id="5c96e-105">When you call [CreateNPPInterface](createnppinterface.md), remember that each NPP is represented as a single in-process COM object.</span></span> <span data-ttu-id="5c96e-106">Os aplicativos podem criar uma instância de qualquer número de objetos NPP.</span><span class="sxs-lookup"><span data-stu-id="5c96e-106">Applications can instantiate any number of NPP objects.</span></span> <span data-ttu-id="5c96e-107">No entanto, cada objeto instanciado deve usar um — e apenas um — das cinco interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="5c96e-107">However, each instantiated object must use one—and only one—of the five NPP interfaces.</span></span>

<span data-ttu-id="5c96e-108">Observe também que diferentes interfaces NPP fornecem dados de rede em várias formas.</span><span class="sxs-lookup"><span data-stu-id="5c96e-108">Note also that different NPP interfaces provide network data in various forms.</span></span> <span data-ttu-id="5c96e-109">Por exemplo, Monitor de Rede usa a interface **IDelaydC** para capturar o tráfego de rede e salvá-lo em um arquivo de captura; enquanto os monitores usam a interface **IRTC** para capturar o tráfego de rede em tempo real.</span><span class="sxs-lookup"><span data-stu-id="5c96e-109">For example, Network Monitor uses the **IDelaydC** interface to capture network traffic and save it to a capture file; while monitors use the **IRTC** interface to capture real time network traffic.</span></span> <span data-ttu-id="5c96e-110">A tabela a seguir descreve Monitor de Rede interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="5c96e-110">The following table describes Network Monitor NPP interfaces.</span></span>



| <span data-ttu-id="5c96e-111">Interface</span><span class="sxs-lookup"><span data-stu-id="5c96e-111">Interface</span></span>                | <span data-ttu-id="5c96e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c96e-112">Description</span></span>                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c96e-113">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="5c96e-113">IDelaydC</span></span>](idelaydc.md) | <span data-ttu-id="5c96e-114">Captura o tráfego de rede armazenado em um arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="5c96e-114">Captures network traffic that is stored in a capture file.</span></span> <span data-ttu-id="5c96e-115">Essa interface é usada pelos aplicativos Monitor de Rede e NPP.</span><span class="sxs-lookup"><span data-stu-id="5c96e-115">This interface is used by Network Monitor and NPP applications.</span></span>                                          |
| [<span data-ttu-id="5c96e-116">IESP</span><span class="sxs-lookup"><span data-stu-id="5c96e-116">IESP</span></span>](iesp.md)         | <span data-ttu-id="5c96e-117">Captura o tráfego de rede armazenado em um arquivo de captura e fornece estatísticas avançadas em um formato de arquivo ESP especial.</span><span class="sxs-lookup"><span data-stu-id="5c96e-117">Captures network traffic that is stored in a capture file and provides enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="5c96e-118">Essa interface é usada por aplicativos NPP</span><span class="sxs-lookup"><span data-stu-id="5c96e-118">This interface is used by NPP applications</span></span> |
| [<span data-ttu-id="5c96e-119">IRTC</span><span class="sxs-lookup"><span data-stu-id="5c96e-119">IRTC</span></span>](irtc.md)         | <span data-ttu-id="5c96e-120">Captura o tráfego de rede em tempo real e dispara eventos quando eles ocorrem.</span><span class="sxs-lookup"><span data-stu-id="5c96e-120">Captures real time network traffic and triggers events when they occur.</span></span> <span data-ttu-id="5c96e-121">Essa interface é usada por [*monitores*](m.md) e aplicativos NPP.</span><span class="sxs-lookup"><span data-stu-id="5c96e-121">This interface is used by [*monitors*](m.md) and NPP applications.</span></span>     |
| [<span data-ttu-id="5c96e-122">IStats</span><span class="sxs-lookup"><span data-stu-id="5c96e-122">IStats</span></span>](istats.md)     | <span data-ttu-id="5c96e-123">Recupera estatísticas como dados brutos em vez de quadros.</span><span class="sxs-lookup"><span data-stu-id="5c96e-123">Retrieves statistics as raw data rather than frames.</span></span> <span data-ttu-id="5c96e-124">Essa interface é usada por aplicativos NPP, como [*Perfmon*](p.md).</span><span class="sxs-lookup"><span data-stu-id="5c96e-124">This interface is used by NPP applications such as [*Perfmon*](p.md).</span></span>                     |



 

 

 



