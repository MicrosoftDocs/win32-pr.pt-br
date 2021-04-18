---
description: Este documento descreve o design e o uso das classes base do MSP. O uso dessas classes não é necessário, mas a maioria dos desenvolvedores vai perceber que simplificam a tarefa de criar um MSP baseado em DirectShow para TAPI 3S New MSPI.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Classes base TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780589"
---
# <a name="tapi-3-msp-base-classes"></a><span data-ttu-id="9fd54-104">Classes base TAPI 3 MSP</span><span class="sxs-lookup"><span data-stu-id="9fd54-104">TAPI 3 MSP Base Classes</span></span>

<span data-ttu-id="9fd54-105">Este documento descreve o design e o uso das classes base do MSP.</span><span class="sxs-lookup"><span data-stu-id="9fd54-105">This document describes the design and use of the MSP Base Classes.</span></span> <span data-ttu-id="9fd54-106">O uso dessas classes não é necessário, mas a maioria dos desenvolvedores vai perceber que simplificam a tarefa de criar um MSP baseado em DirectShow para a nova MSPI da TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="9fd54-106">Use of these classes is not required, but most developers will find they simplify the task of building a DirectShow-based MSP for TAPI 3's new MSPI.</span></span>

<span data-ttu-id="9fd54-107">O código-fonte para as classes base MSP pode ser encontrado no diretório de exemplos do SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="9fd54-107">Source code for the MSP base classes can be found in the Samples directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="9fd54-108">Presume-se familiaridade com COM, ATL, DirectShow e C++.</span><span class="sxs-lookup"><span data-stu-id="9fd54-108">Familiarity with COM, ATL, DirectShow, and C++ is assumed.</span></span> <span data-ttu-id="9fd54-109">O leitor também deve conhecer o material geral em [sobre o MSP (provedor de serviços de mídia)](about-the-media-service-provider-msp-.md) e na [MSPI (interface do provedor de serviços de mídia)](media-service-provider-interface-mspi-.md).</span><span class="sxs-lookup"><span data-stu-id="9fd54-109">The reader must also know the general material in [About the Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) and in [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md).</span></span>

<span data-ttu-id="9fd54-110">O ATL 2,1 é necessário para o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9fd54-110">ATL 2.1 is required for Windows 2000.</span></span> <span data-ttu-id="9fd54-111">A partir do Windows XP, tanto o ATL 2,1 quanto o 3,0 serão compilados.</span><span class="sxs-lookup"><span data-stu-id="9fd54-111">Starting with Windows XP, both ATL 2.1 and 3.0 will compile.</span></span>

<span data-ttu-id="9fd54-112">Bibliotecas de classe base MSP (disponíveis no SDK):</span><span class="sxs-lookup"><span data-stu-id="9fd54-112">MSP Base Class Libraries (available in the SDK):</span></span>

-   <span data-ttu-id="9fd54-113">Mspbase. lib</span><span class="sxs-lookup"><span data-stu-id="9fd54-113">Mspbase.lib</span></span>
-   <span data-ttu-id="9fd54-114">Mspid. lib</span><span class="sxs-lookup"><span data-stu-id="9fd54-114">Mspid.lib</span></span>
-   <span data-ttu-id="9fd54-115">Strmbase. lib</span><span class="sxs-lookup"><span data-stu-id="9fd54-115">Strmbase.lib</span></span>
-   <span data-ttu-id="9fd54-116">Tmuid. lib</span><span class="sxs-lookup"><span data-stu-id="9fd54-116">Tmuid.lib</span></span>
    > [!Note]  
    > <span data-ttu-id="9fd54-117">A vinculação dinâmica em vez de estática deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="9fd54-117">Dynamic rather than static linking should be used.</span></span>

     

<span data-ttu-id="9fd54-118">Arquivos de cabeçalho de classe base MSP (disponíveis no SDK):</span><span class="sxs-lookup"><span data-stu-id="9fd54-118">MSP Base Class Header Files (available in the SDK):</span></span>

-   <span data-ttu-id="9fd54-119">Mspaddr. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-119">Mspaddr.h</span></span>
-   <span data-ttu-id="9fd54-120">Mspbase. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-120">Mspbase.h</span></span>
-   <span data-ttu-id="9fd54-121">Mspcall. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-121">Mspcall.h</span></span>
-   <span data-ttu-id="9fd54-122">Msplog. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-122">Msplog.h</span></span>
-   <span data-ttu-id="9fd54-123">Mspstrm. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-123">Mspstrm.h</span></span>
-   <span data-ttu-id="9fd54-124">Mspterm. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-124">Mspterm.h</span></span>
-   <span data-ttu-id="9fd54-125">Mspthrd. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-125">Mspthrd.h</span></span>
-   <span data-ttu-id="9fd54-126">Msptmac. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-126">Msptmac.h</span></span>
-   <span data-ttu-id="9fd54-127">Msptmvc. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-127">Msptmvc.h</span></span>
-   <span data-ttu-id="9fd54-128">Msptrmvc. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-128">Msptrmvc.h</span></span>
-   <span data-ttu-id="9fd54-129">Msptrmac. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-129">Msptrmac.h</span></span>
-   <span data-ttu-id="9fd54-130">Msptrmar. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-130">Msptrmar.h</span></span>
-   <span data-ttu-id="9fd54-131">Msputils. h</span><span class="sxs-lookup"><span data-stu-id="9fd54-131">Msputils.h</span></span>

<span data-ttu-id="9fd54-132">Arquivos de origem da classe base MSP (disponível nas amostras do SDK):</span><span class="sxs-lookup"><span data-stu-id="9fd54-132">MSP Base Class Source Files (available in the SDK Samples):</span></span>

-   <span data-ttu-id="9fd54-133">Mspaddr. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-133">Mspaddr.cpp</span></span>
-   <span data-ttu-id="9fd54-134">Mspcall. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-134">Mspcall.cpp</span></span>
-   <span data-ttu-id="9fd54-135">Msplog. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-135">Msplog.cpp</span></span>
-   <span data-ttu-id="9fd54-136">Mspstrm. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-136">Mspstrm.cpp</span></span>
-   <span data-ttu-id="9fd54-137">Mspterm. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-137">Mspterm.cpp</span></span>
-   <span data-ttu-id="9fd54-138">Mspthrd. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-138">Mspthrd.cpp</span></span>
-   <span data-ttu-id="9fd54-139">Msptrmac. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-139">Msptrmac.cpp</span></span>
-   <span data-ttu-id="9fd54-140">Msptrmar. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-140">Msptrmar.cpp</span></span>
-   <span data-ttu-id="9fd54-141">Msptrmvc. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-141">Msptrmvc.cpp</span></span>
-   <span data-ttu-id="9fd54-142">Msputils. cpp</span><span class="sxs-lookup"><span data-stu-id="9fd54-142">Msputils.cpp</span></span>

 

 



