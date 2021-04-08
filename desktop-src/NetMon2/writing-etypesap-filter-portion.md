---
description: A parte ETYPE/SAP do filtro de captura notifica o driver de Monitor de Rede para aceitar quadros que têm uma combinação específica de ETYPEs e SAPs (pontos de acesso de serviço).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Gravando a parte do filtro ETYPE/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922322"
---
# <a name="writing-etypesap-filter-portion"></a><span data-ttu-id="c9d8b-103">Gravando a parte do filtro ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="c9d8b-103">Writing Etype/SAP Filter Portion</span></span>

<span data-ttu-id="c9d8b-104">A parte ETYPE/SAP do filtro de captura notifica o driver de Monitor de Rede para aceitar quadros que têm uma combinação específica de ETYPEs e SAPS ( [*pontos de acesso de serviço*](s.md) ).</span><span class="sxs-lookup"><span data-stu-id="c9d8b-104">The Etype/SAP portion of the capture filter notifies the Network Monitor driver to accept frames that have a specific combination of Etypes and [*service access points*](s.md) (SAPs).</span></span> <span data-ttu-id="c9d8b-105">Os ETYPEs e SAPs são maneiras de os protocolos de nível inferior, como Ethernet, LLC e snap, indicam qual protocolo os segue.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-105">Etypes and SAPs are both ways that low-level protocols such as Ethernet, LLC, and Snap indicate which protocol follows them.</span></span> <span data-ttu-id="c9d8b-106">Especificamente:</span><span class="sxs-lookup"><span data-stu-id="c9d8b-106">Specifically:</span></span>

-   <span data-ttu-id="c9d8b-107">Ethernet especifica um ETYPE</span><span class="sxs-lookup"><span data-stu-id="c9d8b-107">Ethernet specifies an Etype</span></span>
-   <span data-ttu-id="c9d8b-108">O LLC especifica um SAP</span><span class="sxs-lookup"><span data-stu-id="c9d8b-108">LLC specifies a SAP</span></span>
-   <span data-ttu-id="c9d8b-109">Snap especifica um ETYPE</span><span class="sxs-lookup"><span data-stu-id="c9d8b-109">Snap specifies an Etype</span></span>

## <a name="etypesap-capture-filter-flags"></a><span data-ttu-id="c9d8b-110">Sinalizadores de filtro de captura de ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="c9d8b-110">Etype/SAP Capture Filter Flags</span></span>

<span data-ttu-id="c9d8b-111">Use as informações a seguir para definir os sinalizadores no membro **FilterFlags** da estrutura [**CAPTUREFILTER**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="c9d8b-111">Use the following information to set the flags in the **FilterFlags** member of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="c9d8b-112">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="c9d8b-112">Flag</span></span>                                         | <span data-ttu-id="c9d8b-113">Significado</span><span class="sxs-lookup"><span data-stu-id="c9d8b-113">Meaning</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d8b-114">\_os sinalizadores CAPTUREFILTER \_ incluem \_ todos os \_ SAPs</span><span class="sxs-lookup"><span data-stu-id="c9d8b-114">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_SAPS</span></span>   | <span data-ttu-id="c9d8b-115">Passa todos os valores SAP e notifica o driver de que todos os valores SAP são válidos.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-115">Passes all SAP values and notifies the driver that all SAP values are valid.</span></span> <span data-ttu-id="c9d8b-116">Se combinado com quaisquer valores no membro **lpSapTable** , esse sinalizador notificará o driver de que todos os valores SAP, exceto aqueles no **lpSapTable** , são válidos.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-116">If combined with any values in the **lpSapTable** member, this flag notifies the driver that all SAP values except those in the **lpSapTable** are valid.</span></span><br/>           |
| <span data-ttu-id="c9d8b-117">\_os sinalizadores CAPTUREFILTER \_ incluem \_ todos os \_ ETYPES</span><span class="sxs-lookup"><span data-stu-id="c9d8b-117">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_ETYPES</span></span> | <span data-ttu-id="c9d8b-118">Passa todos os valores de ETYPE e notifica o driver de que todos os valores de ETYPE são válidos.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-118">Passes all Etype values and notifies the driver that all Etype values are valid.</span></span> <span data-ttu-id="c9d8b-119">Se combinado com quaisquer valores no membro **lpEtypeTable** , esse sinalizador notificará o driver de que todos os valores de ETYPE, exceto aqueles no **lpEtypeTable** , são válidos.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-119">If combined with any values in the **lpEtypeTable** member, this flag notifies the driver that all Etype values except those in the **lpEtypeTable** are valid.</span></span><br/> |
| <span data-ttu-id="c9d8b-120">CAPTUREFILTER \_ sinalizadores \_ \_ somente locais</span><span class="sxs-lookup"><span data-stu-id="c9d8b-120">CAPTUREFILTER\_ FLAGS\_LOCAL\_ONLY</span></span>           | <span data-ttu-id="c9d8b-121">A definição desse sinalizador não definirá uma NIC para o modo P.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-121">Setting this flag will not set a NIC to P-Mode.</span></span> <span data-ttu-id="c9d8b-122">Você verá apenas o tráfego local (todos os quadros no computador local).</span><span class="sxs-lookup"><span data-stu-id="c9d8b-122">You will only see local traffic (any frames to the local machine).</span></span>                                                                                                                                          |
| <span data-ttu-id="c9d8b-123">CAPTUREFILTER \_ sinalizadores de \_ manutenção \_ brutos</span><span class="sxs-lookup"><span data-stu-id="c9d8b-123">CAPTUREFILTER\_ FLAGS\_KEEP\_RAW</span></span>             | <span data-ttu-id="c9d8b-124">Mantém os quadros MAC SMT e token ring.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-124">Keeps SMT and Token Ring MAC frames.</span></span>                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a><span data-ttu-id="c9d8b-125">Configurações do filtro de captura do ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="c9d8b-125">Etype/SAP Capture Filter Settings</span></span>

<span data-ttu-id="c9d8b-126">Use as informações a seguir para definir os membros **lpSapTable** e **LpEtypeTable** da estrutura [**CAPTUREFILTER**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="c9d8b-126">Use the following information to set the **lpSapTable** and **lpEtypeTable** members of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="c9d8b-127">Configuração</span><span class="sxs-lookup"><span data-stu-id="c9d8b-127">Setting</span></span>          | <span data-ttu-id="c9d8b-128">Significado</span><span class="sxs-lookup"><span data-stu-id="c9d8b-128">Meaning</span></span>                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d8b-129">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="c9d8b-129">**lpSapTable**</span></span>   | <span data-ttu-id="c9d8b-130">Lista os valores SAP que você deseja que o driver passe.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-130">Lists the SAP values that you want the driver to pass.</span></span> <span data-ttu-id="c9d8b-131">Essa lista informa o driver de Monitor de Rede para validar qualquer quadro que contenha uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-131">This list tells the Network Monitor driver to validate any frame that contains a match.</span></span> <span data-ttu-id="c9d8b-132">Se CAPTUREFILTER \_ flags \_ incluir \_ todos os \_ SAPs for definido, isso se tornará uma lista de exceção (se for encontrada, não passará).</span><span class="sxs-lookup"><span data-stu-id="c9d8b-132">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (if found, do not pass).</span></span>           |
| <span data-ttu-id="c9d8b-133">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="c9d8b-133">**lpEtypeTable**</span></span> | <span data-ttu-id="c9d8b-134">Lista os valores de ETYPE que você deseja que o driver de Monitor de Rede passe.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-134">Lists the Etype values that you want the Network Monitor driver to pass.</span></span> <span data-ttu-id="c9d8b-135">Essa lista só informa ao driver para validar qualquer quadro que contenha uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="c9d8b-135">This list alone tells the driver to validate any frame that contains a match.</span></span> <span data-ttu-id="c9d8b-136">Se \_ os sinalizadores CAPTUREFILTERs \_ incluírem \_ todos os \_ ETYPES forem definidos, isso se tornará uma lista de exceção (se for encontrada, não passará).</span><span class="sxs-lookup"><span data-stu-id="c9d8b-136">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (if found, do not pass).</span></span> |



 

 

 




