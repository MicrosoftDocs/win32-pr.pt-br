---
description: No Monitor de Rede, o filtro de captura é definido pela estrutura CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: A estrutura CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920992"
---
# <a name="the-capturefilter-structure"></a><span data-ttu-id="6d4d9-103">A estrutura CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="6d4d9-103">The CAPTUREFILTER Structure</span></span>

<span data-ttu-id="6d4d9-104">No Monitor de Rede, o [filtro de captura](capture-filters.md) é definido pela estrutura [**CAPTUREFILTER**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="6d4d9-104">In Network Monitor, the [capture filter](capture-filters.md) is defined by the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span> <span data-ttu-id="6d4d9-105">A ausência ou a combinação de sinalizadores, valores e expressões determina quais quadros serão passados ou descartados pelo driver de Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-105">The absence or combination of flags, values, and expressions determines which frames will be passed on or dropped by the Network Monitor driver.</span></span> <span data-ttu-id="6d4d9-106">A ilustração a seguir mostra as três áreas da análise do filtro de captura: ETYPE/SAP, endereço e correspondência de padrão.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-106">The following illustration shows the three areas of the capture filter analysis: Etype/SAP, address, and pattern match.</span></span>

![três áreas da análise do filtro de captura](images/capfilter.png)

<span data-ttu-id="6d4d9-108">A tabela a seguir lista a função de cada elemento de filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-108">The following table lists the function of each capture filter element.</span></span>



| <span data-ttu-id="6d4d9-109">Elemento Filter</span><span class="sxs-lookup"><span data-stu-id="6d4d9-109">Filter element</span></span>                                       | <span data-ttu-id="6d4d9-110">Ação</span><span class="sxs-lookup"><span data-stu-id="6d4d9-110">Action</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d4d9-111">ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="6d4d9-111">Etype/SAP</span></span>](writing-etypesap-filter-portion.md)     | <span data-ttu-id="6d4d9-112">Avalia as configurações de ETYPE/SAP.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-112">Evaluates Etype/SAP settings.</span></span> <span data-ttu-id="6d4d9-113">A combinação de sinalizadores determina quais tipos de configuração ou valores são incluídos ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-113">The combination of flags determines which setting types or values are included or excluded.</span></span>                                                                                    |
| [<span data-ttu-id="6d4d9-114">Endereço</span><span class="sxs-lookup"><span data-stu-id="6d4d9-114">Address</span></span>](writing-addresstable-filter-portion.md)   | <span data-ttu-id="6d4d9-115">Avalia os endereços de origem e de destino e os pares de endereços.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-115">Evaluates source and destination addresses and address pairs.</span></span> <span data-ttu-id="6d4d9-116">Diferentes combinações de sinalizadores determinam quais valores individuais ou combinações de pares de endereços são incluídos ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-116">Different combinations of flags determine which individual values or combinations of address pairs are included or excluded.</span></span>                   |
| [<span data-ttu-id="6d4d9-117">Correspondência de padrões</span><span class="sxs-lookup"><span data-stu-id="6d4d9-117">Pattern Match</span></span>](writing-the-patternmatch-filter.md) | <span data-ttu-id="6d4d9-118">Define correspondências de padrão complexas dentro de um quadro.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-118">Defines complex pattern matches within a frame.</span></span> <span data-ttu-id="6d4d9-119">Os sinalizadores são fornecidos para diferentes tipos e deslocamentos.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-119">Flags are provided for different types and offsets.</span></span> <span data-ttu-id="6d4d9-120">Você pode combinar correspondências de padrão com instruções lógicos AND ou OR Operator.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-120">You can combine pattern matches with logical AND or OR operator statements.</span></span>                              |
| [<span data-ttu-id="6d4d9-121">Recorte</span><span class="sxs-lookup"><span data-stu-id="6d4d9-121">Clipping</span></span>](clipping-a-frame.md)                     | <span data-ttu-id="6d4d9-122">Corta os quadros de uma maneira especificada por vários valores de byte.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-122">Clips frames in a manner specified by various byte values.</span></span> <span data-ttu-id="6d4d9-123">Você pode usar somente esse elemento para recortar todos os quadros ou usá-los com outros elementos de filtro de captura; por exemplo, para localizar e recortar um único quadro.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-123">You can use only this element to clip all frames or use it with other capture filter elements; for example, to find and then clip a single frame.</span></span> |
| [<span data-ttu-id="6d4d9-124">**Of**</span><span class="sxs-lookup"><span data-stu-id="6d4d9-124">**Trigger**</span></span>](trigger.md)                           | <span data-ttu-id="6d4d9-125">Este elemento de filtro de captura está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-125">This capture filter element is obsolete.</span></span> <span data-ttu-id="6d4d9-126">Os gatilhos não fazem mais parte de um filtro de captura; Agora eles estão contidos em suas próprias marcas de BLOB, que são especificadas separadamente.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-126">Triggers are no longer part of a capture filter; they are now contained in their own BLOB tags, which are specified separately.</span></span>                                     |



 

<span data-ttu-id="6d4d9-127">Um quadro é avaliado em relação a todas as três partes do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-127">A frame is evaluated against all three portions of the capture filter.</span></span> <span data-ttu-id="6d4d9-128">Portanto, um quadro transmitido com êxito deve passar cada elemento.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-128">Therefore, a successfully transmitted frame must pass each element.</span></span> <span data-ttu-id="6d4d9-129">Lembre-se de que o driver Monitor de Rede avalia a ausência de qualquer um dos três elementos como **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="6d4d9-129">Be aware that the Network Monitor driver evaluates the absence of any of the three elements as **TRUE**.</span></span> <span data-ttu-id="6d4d9-130">Por exemplo, o driver avalia a ausência de uma seção ETYPE/SAP como "todos os quadros com qualquer valor de ETYPE/SAP são válidos".</span><span class="sxs-lookup"><span data-stu-id="6d4d9-130">For example, the driver evaluates the absence of an Etype/SAP section as "ALL frames with the ANY Etype/SAP value are valid."</span></span>

 

 



