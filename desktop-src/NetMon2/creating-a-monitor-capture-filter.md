---
description: A criação de um filtro de captura que funciona com Monitor de Rede é um processo de cinco etapas.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Criando um filtro de captura de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785404"
---
# <a name="creating-a-monitor-capture-filter"></a><span data-ttu-id="7ef80-103">Criando um filtro de captura de monitor</span><span class="sxs-lookup"><span data-stu-id="7ef80-103">Creating a Monitor Capture Filter</span></span>

<span data-ttu-id="7ef80-104">A criação de um filtro de captura que funciona com o Monitor de Rede é um processo de cinco etapas:</span><span class="sxs-lookup"><span data-stu-id="7ef80-104">Creating a capture filter that works with Network Monitor is a five-step process:</span></span>

-   [<span data-ttu-id="7ef80-105">Configurando o filtro ETYPE ou SAP</span><span class="sxs-lookup"><span data-stu-id="7ef80-105">Setting the Etype or SAP Filter</span></span>](writing-etypesap-filter-portion.md)
-   [<span data-ttu-id="7ef80-106">Gravando filtro de endereços de endereço</span><span class="sxs-lookup"><span data-stu-id="7ef80-106">Writing ADDRESSTABLE Filter</span></span>](writing-addresstable-filter-portion.md)
-   [<span data-ttu-id="7ef80-107">Gravando o filtro PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="7ef80-107">Writing the PATTERNMATCH Filter</span></span>](writing-the-patternmatch-filter.md)
-   [<span data-ttu-id="7ef80-108">Recortando um quadro</span><span class="sxs-lookup"><span data-stu-id="7ef80-108">Clipping a Frame</span></span>](clipping-a-frame.md)
-   [<span data-ttu-id="7ef80-109">Implementando o código de filtro de captura</span><span class="sxs-lookup"><span data-stu-id="7ef80-109">Implementing the Capture Filter Code</span></span>](implementing-the-capture-filter-code.md)

<span data-ttu-id="7ef80-110">Um [*filtro de captura*](c.md) é uma série de adições ao blob NPP que seleciona quais quadros são passados de volta para o monitor.</span><span class="sxs-lookup"><span data-stu-id="7ef80-110">A [*capture filter*](c.md) is a series of additions to the NPP BLOB that selects which frames are passed back to the monitor.</span></span> <span data-ttu-id="7ef80-111">Se um monitor não alterar o BLOB NPP, o NPP entrará no modo promíscuo e enviará todo o tráfego de rede para o monitor.</span><span class="sxs-lookup"><span data-stu-id="7ef80-111">If a monitor does not alter the NPP BLOB, then the NPP will go into promiscuous mode and send all network traffic to the monitor.</span></span> <span data-ttu-id="7ef80-112">O NPP será mais eficiente se puder reduzir os dados entregues a um driver, de modo que um monitor deve criar um filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="7ef80-112">The NPP is most efficient if it can reduce the data handed up to a driver, so a monitor should create a capture filter.</span></span> <span data-ttu-id="7ef80-113">Um monitor define seu filtro de captura gravando no BLOB NPP na chamada à função [doconfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="7ef80-113">A monitor sets its capture filter by writing to the NPP BLOB in the call to the [DoConfigure](imonitor-doconfigure.md) function.</span></span> <span data-ttu-id="7ef80-114">Em seguida, o MCSVC chama o NPP com o BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="7ef80-114">The MCSVC then calls the NPP with the NPP BLOB.</span></span> <span data-ttu-id="7ef80-115">Consulte [filtros de captura](capture-filters.md) para obter mais detalhes sobre o filtro de captura, [provedores de pacotes de rede](network-packet-providers.md) em NPPs e [Monitor de rede BLOBs](network-monitor-blobs.md) em funções de BLOB.</span><span class="sxs-lookup"><span data-stu-id="7ef80-115">See [Capture Filters](capture-filters.md) for more details on the capture filter, [Network Packet Providers](network-packet-providers.md) on NPPs, and [Network Monitor Blobs](network-monitor-blobs.md) on BLOB functions.</span></span>

 

 



