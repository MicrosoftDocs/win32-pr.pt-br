---
description: A enumeração de sinalizadores de pesquisa do DEXTERF \_ Track \_ \_ especifica as condições de limite em uma pesquisa de um objeto na linha do tempo.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Enumeração de DEXTERF_TRACK_SEARCH_FLAGS (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750279"
---
# <a name="dexterf_track_search_flags-enumeration"></a><span data-ttu-id="aff67-103">\_Enumeração de \_ sinalizadores de pesquisa do DEXTERF Track \_</span><span class="sxs-lookup"><span data-stu-id="aff67-103">DEXTERF\_TRACK\_SEARCH\_FLAGS enumeration</span></span>

> [!Note]  
> <span data-ttu-id="aff67-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="aff67-104">\[Deprecated.</span></span> <span data-ttu-id="aff67-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aff67-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aff67-106">A `DEXTERF_TRACK_SEARCH_FLAGS` enumeração Especifica as condições de limite em uma pesquisa de um objeto na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="aff67-106">The `DEXTERF_TRACK_SEARCH_FLAGS` enumeration specifies the boundary conditions on a search for an object in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff67-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aff67-107">Syntax</span></span>


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="aff67-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="aff67-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aff67-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**limite de DEXTERF \_**</span><span class="sxs-lookup"><span data-stu-id="aff67-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DEXTERF\_BOUNDING**</span></span>
</dt> <dd>

<span data-ttu-id="aff67-110">Procure um objeto que abranja o tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="aff67-110">Search for an object that spans the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="aff67-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ exatamente \_ em**</span><span class="sxs-lookup"><span data-stu-id="aff67-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF\_EXACTLY\_AT**</span></span>
</dt> <dd>

<span data-ttu-id="aff67-112">Pesquisar um objeto que inicia exatamente na hora especificada.</span><span class="sxs-lookup"><span data-stu-id="aff67-112">Search for an object that starts exactly at the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="aff67-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**\_encaminhamentos de DEXTERF**</span><span class="sxs-lookup"><span data-stu-id="aff67-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF\_FORWARDS**</span></span>
</dt> <dd>

<span data-ttu-id="aff67-114">Pesquisar um objeto que inicia na hora especificada ou posteriormente.</span><span class="sxs-lookup"><span data-stu-id="aff67-114">Search for an object that starts at the specified time or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aff67-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="aff67-115">Remarks</span></span>

<span data-ttu-id="aff67-116">Essas condições de limite são resumidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aff67-116">These boundary conditions are summarized in the following table.</span></span>



| <span data-ttu-id="aff67-117">Valor de enumeração</span><span class="sxs-lookup"><span data-stu-id="aff67-117">Enumeration value</span></span>    | <span data-ttu-id="aff67-118">Condição de limite</span><span class="sxs-lookup"><span data-stu-id="aff67-118">Boundary condition</span></span>                        |
|----------------------|-------------------------------------------|
| <span data-ttu-id="aff67-119">limite de DEXTERF \_</span><span class="sxs-lookup"><span data-stu-id="aff67-119">DEXTERF\_BOUNDING</span></span>    | <span data-ttu-id="aff67-120">Iniciar <= tempo de > do TimeStop</span><span class="sxs-lookup"><span data-stu-id="aff67-120">Start <= TimeStop > Time</span></span><br/> |
| <span data-ttu-id="aff67-121">DEXTERF \_ exatamente \_ em</span><span class="sxs-lookup"><span data-stu-id="aff67-121">DEXTERF\_EXACTLY\_AT</span></span> | <span data-ttu-id="aff67-122">Início = = hora</span><span class="sxs-lookup"><span data-stu-id="aff67-122">Start == Time</span></span>                             |
| <span data-ttu-id="aff67-123">\_encaminhamentos de DEXTERF</span><span class="sxs-lookup"><span data-stu-id="aff67-123">DEXTERF\_FORWARDS</span></span>    | <span data-ttu-id="aff67-124">Iniciar >= hora</span><span class="sxs-lookup"><span data-stu-id="aff67-124">Start >= Time</span></span>                          |



 

-   <span data-ttu-id="aff67-125">Início: hora de início do objeto recuperado.</span><span class="sxs-lookup"><span data-stu-id="aff67-125">Start: start time of the retrieved object.</span></span>
-   <span data-ttu-id="aff67-126">Stop: hora de parada do objeto recuperado.</span><span class="sxs-lookup"><span data-stu-id="aff67-126">Stop: stop time of the retrieved object.</span></span>
-   <span data-ttu-id="aff67-127">Hora: tempo de pesquisa especificado.</span><span class="sxs-lookup"><span data-stu-id="aff67-127">Time: specified search time.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff67-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aff67-128">Requirements</span></span>



| <span data-ttu-id="aff67-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="aff67-129">Requirement</span></span> | <span data-ttu-id="aff67-130">Valor</span><span class="sxs-lookup"><span data-stu-id="aff67-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aff67-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aff67-131">Header</span></span><br/> | <dl> <span data-ttu-id="aff67-132"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff67-132"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff67-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="aff67-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff67-134">**IAMTimelineTrack::GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="aff67-134">**IAMTimelineTrack::GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




