---
description: A enumeração de tipo principal da linha do tempo \_ \_ especifica o tipo principal de um objeto.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Enumeração de TIMELINE_MAJOR_TYPE (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767666"
---
# <a name="timeline_major_type-enumeration"></a><span data-ttu-id="c5a08-103">\_Enumeração de tipo principal de linha do tempo \_</span><span class="sxs-lookup"><span data-stu-id="c5a08-103">TIMELINE\_MAJOR\_TYPE enumeration</span></span>

> [!Note]  
> <span data-ttu-id="c5a08-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c5a08-104">\[Deprecated.</span></span> <span data-ttu-id="c5a08-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c5a08-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c5a08-106">A `TIMELINE_MAJOR_TYPE` enumeração Especifica o tipo principal de um objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a08-106">The `TIMELINE_MAJOR_TYPE` enumeration specifies the major type of an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a08-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5a08-107">Syntax</span></span>


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c5a08-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="c5a08-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c5a08-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**LINHA de tempo \_ \_ tipo principal \_ composto**</span><span class="sxs-lookup"><span data-stu-id="c5a08-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TIMELINE\_MAJOR\_TYPE\_COMPOSITE**</span></span>
</dt> <dd>

<span data-ttu-id="c5a08-110">Objeto composto.</span><span class="sxs-lookup"><span data-stu-id="c5a08-110">Composite object.</span></span> <span data-ttu-id="c5a08-111">Mantém uma ou mais faixas.</span><span class="sxs-lookup"><span data-stu-id="c5a08-111">Holds one or more tracks.</span></span>

</dd> <dt>

<span data-ttu-id="c5a08-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**LINHA \_ do \_ tipo principal \_ faixa**</span><span class="sxs-lookup"><span data-stu-id="c5a08-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**TIMELINE\_MAJOR\_TYPE\_TRACK**</span></span>
</dt> <dd>

<span data-ttu-id="c5a08-113">Rastrear objeto.</span><span class="sxs-lookup"><span data-stu-id="c5a08-113">Track object.</span></span> <span data-ttu-id="c5a08-114">Contém uma ou mais fontes.</span><span class="sxs-lookup"><span data-stu-id="c5a08-114">Holds one or more sources.</span></span>

</dd> <dt>

<span data-ttu-id="c5a08-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**LINHA de tempo \_ principal \_ tipo \_ fonte**</span><span class="sxs-lookup"><span data-stu-id="c5a08-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**TIMELINE\_MAJOR\_TYPE\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="c5a08-116">Objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="c5a08-116">Source object.</span></span> <span data-ttu-id="c5a08-117">Contém uma referência a uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="c5a08-117">Contains a reference to a media source.</span></span>

</dd> <dt>

<span data-ttu-id="c5a08-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**LINHA do tempo de \_ \_ transição de tipo principal \_**</span><span class="sxs-lookup"><span data-stu-id="c5a08-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TIMELINE\_MAJOR\_TYPE\_TRANSITION**</span></span>
</dt> <dd>

<span data-ttu-id="c5a08-119">Objeto de transição.</span><span class="sxs-lookup"><span data-stu-id="c5a08-119">Transition object.</span></span> <span data-ttu-id="c5a08-120">Define uma transição entre composições, faixas ou fontes.</span><span class="sxs-lookup"><span data-stu-id="c5a08-120">Defines a transition between composites, tracks, or sources.</span></span>

</dd> <dt>

<span data-ttu-id="c5a08-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_efeito de \_ tipo \_ principal de linha do tempo**</span><span class="sxs-lookup"><span data-stu-id="c5a08-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**TIMELINE\_MAJOR\_TYPE\_EFFECT**</span></span>
</dt> <dd>

<span data-ttu-id="c5a08-122">Objeto Effect.</span><span class="sxs-lookup"><span data-stu-id="c5a08-122">Effect object.</span></span> <span data-ttu-id="c5a08-123">Define um efeito de entrada única a ser aplicado a um objeto composto, de faixa ou de origem.</span><span class="sxs-lookup"><span data-stu-id="c5a08-123">Defines a single-input effect to be applied to a composite, track, or source object.</span></span>

</dd> <dt>

<span data-ttu-id="c5a08-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**LINHA \_ do \_ tipo principal \_ grupo**</span><span class="sxs-lookup"><span data-stu-id="c5a08-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**TIMELINE\_MAJOR\_TYPE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="c5a08-125">Objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="c5a08-125">Group object.</span></span> <span data-ttu-id="c5a08-126">Contém uma ou mais faixas de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="c5a08-126">Contains one or more tracks of a given type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5a08-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5a08-127">Requirements</span></span>



| <span data-ttu-id="c5a08-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5a08-128">Requirement</span></span> | <span data-ttu-id="c5a08-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c5a08-129">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a08-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5a08-130">Header</span></span><br/> | <dl> <span data-ttu-id="c5a08-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5a08-131"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5a08-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5a08-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a08-133">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="c5a08-133">**IAMTimeline**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="c5a08-134">**IAMTimelineComp::GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="c5a08-134">**IAMTimelineComp::GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[<span data-ttu-id="c5a08-135">**IAMTimelineObj:: gettimelinetype**</span><span class="sxs-lookup"><span data-stu-id="c5a08-135">**IAMTimelineObj::GetTimelineType**</span></span>](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




