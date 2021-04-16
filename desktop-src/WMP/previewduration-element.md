---
title: Elemento PREVIEWDURATION
description: O elemento PREVIEWDURATION define o período de tempo que um clipe é reproduzido no modo de visualização.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Elemento PREVIEWDURATION do Windows Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765240"
---
# <a name="previewduration-element"></a><span data-ttu-id="997ea-104">Elemento PREVIEWDURATION</span><span class="sxs-lookup"><span data-stu-id="997ea-104">PREVIEWDURATION Element</span></span>

<span data-ttu-id="997ea-105">O elemento **PREVIEWDURATION** define o período de tempo que um clipe é reproduzido no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="997ea-105">The **PREVIEWDURATION** element defines the length of time a clip plays in preview mode.</span></span>

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="997ea-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="997ea-106">Attributes</span></span>

<span data-ttu-id="997ea-107">**Valor** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="997ea-107">**VALUE** (required)</span></span>

<span data-ttu-id="997ea-108">Período de tempo (em horas, minutos, segundos e centésimos de segundo) que o clipe reproduz no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="997ea-108">Length of time (in hours, minutes, seconds, and hundredths of a second) that the clip plays in preview mode.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="997ea-109">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="997ea-109">Parent/Child Elements</span></span>



| <span data-ttu-id="997ea-110">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="997ea-110">Hierarchy</span></span>       | <span data-ttu-id="997ea-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="997ea-111">Elements</span></span>                    |
|-----------------|-----------------------------|
| <span data-ttu-id="997ea-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="997ea-112">Parent elements</span></span> | <span data-ttu-id="997ea-113">**ASX**, **entrada**, **referência**</span><span class="sxs-lookup"><span data-stu-id="997ea-113">**ASX**, **ENTRY**, **REF**</span></span> |
| <span data-ttu-id="997ea-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="997ea-114">Child elements</span></span>  | <span data-ttu-id="997ea-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="997ea-115">None</span></span>                        |



 

## <a name="remarks"></a><span data-ttu-id="997ea-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="997ea-116">Remarks</span></span>

<span data-ttu-id="997ea-117">Esse elemento define o período de tempo que um clipe é reproduzido no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="997ea-117">This element defines the length of time that a clip plays in preview mode.</span></span> <span data-ttu-id="997ea-118">Se esse elemento aparecer dentro de um elemento de **entrada** ou um elemento **ref** , ele se aplicará ao clipe definido por esse elemento.</span><span class="sxs-lookup"><span data-stu-id="997ea-118">If this element appears within an **ENTRY** element or a **REF** element, it applies to the clip defined by that element.</span></span> <span data-ttu-id="997ea-119">Se ele aparecer dentro do escopo de um elemento **ASX** , ele se aplicará a todos os clipes no metarquivo.</span><span class="sxs-lookup"><span data-stu-id="997ea-119">If it appears within the scope of an **ASX** element, it applies to every clip in the metafile.</span></span> <span data-ttu-id="997ea-120">Um elemento **PREVIEWDURATION** em um elemento **ref** tem precedência sobre um em um **elemento** de entrada e tem precedência sobre um elemento **PREVIEWDURATION** em um elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="997ea-120">A **PREVIEWDURATION** element in a **REF** element takes precedence over one in an ENTRY **element**, and either takes precedence over a **PREVIEWDURATION** element in an **ASX** element.</span></span> <span data-ttu-id="997ea-121">Se nenhum elemento **PREVIEWDURATION** for definido para um clipe, o tempo de visualização padrão será de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="997ea-121">If no **PREVIEWDURATION** element is defined for a clip, the default preview time is 10 seconds.</span></span>

<span data-ttu-id="997ea-122">Se houver um elemento **StartTime** ou **STARTMARKER** para o clipe, o Windows Media Player renderizará o clipe começando no ponto definido por um desses elementos; caso contrário, ele será renderizado a partir do início do clipe.</span><span class="sxs-lookup"><span data-stu-id="997ea-122">If there is a **STARTTIME** or **STARTMARKER** element for the clip, Windows Media Player renders the clip starting at the point defined by one of these elements; otherwise it renders from the beginning of the clip.</span></span> <span data-ttu-id="997ea-123">O clipe parará normalmente se for menor do que o tempo definido pelo elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="997ea-123">The clip stops normally if it is shorter than the time defined by the **PREVIEWDURATION** element.</span></span>

<span data-ttu-id="997ea-124">O elemento **Duration** substitui um elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="997ea-124">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="997ea-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="997ea-125">Examples</span></span>


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="997ea-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="997ea-126">Requirements</span></span>



| <span data-ttu-id="997ea-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="997ea-127">Requirement</span></span> | <span data-ttu-id="997ea-128">Valor</span><span class="sxs-lookup"><span data-stu-id="997ea-128">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="997ea-129">Versão</span><span class="sxs-lookup"><span data-stu-id="997ea-129">Version</span></span><br/> | <span data-ttu-id="997ea-130">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="997ea-130">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="997ea-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="997ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="997ea-132">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="997ea-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="997ea-133">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="997ea-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





