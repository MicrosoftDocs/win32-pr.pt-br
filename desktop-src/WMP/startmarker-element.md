---
title: Elemento STARTMARKER
description: O elemento STARTMARKER especifica um marcador do qual o Windows Media Player começará a renderizar o fluxo.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Elemento STARTMARKER do Windows Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761156"
---
# <a name="startmarker-element"></a><span data-ttu-id="dfd49-104">Elemento STARTMARKER</span><span class="sxs-lookup"><span data-stu-id="dfd49-104">STARTMARKER Element</span></span>

<span data-ttu-id="dfd49-105">O elemento **STARTMARKER** especifica um marcador do qual o Windows Media Player começará a renderizar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="dfd49-105">The **STARTMARKER** element specifies a marker from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="dfd49-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="dfd49-106">Attributes</span></span>

<span data-ttu-id="dfd49-107">**AUTOMÁTICA**</span><span class="sxs-lookup"><span data-stu-id="dfd49-107">**NUMBER**</span></span>

<span data-ttu-id="dfd49-108">O número de um marcador numérico no índice.</span><span class="sxs-lookup"><span data-stu-id="dfd49-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="dfd49-109">O valor padrão é o início do conteúdo sob demanda ou a posição atual em um fluxo em tempo real.</span><span class="sxs-lookup"><span data-stu-id="dfd49-109">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

<span data-ttu-id="dfd49-110">**NOME**</span><span class="sxs-lookup"><span data-stu-id="dfd49-110">**NAME**</span></span>

<span data-ttu-id="dfd49-111">O nome de um marcador nomeado no índice.</span><span class="sxs-lookup"><span data-stu-id="dfd49-111">The name of a named marker in the index.</span></span> <span data-ttu-id="dfd49-112">O valor padrão é o início do conteúdo sob demanda ou a posição atual em um fluxo em tempo real.</span><span class="sxs-lookup"><span data-stu-id="dfd49-112">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="dfd49-113">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="dfd49-113">Parent/Child Elements</span></span>



| <span data-ttu-id="dfd49-114">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="dfd49-114">Hierarchy</span></span>       | <span data-ttu-id="dfd49-115">Elementos</span><span class="sxs-lookup"><span data-stu-id="dfd49-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="dfd49-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="dfd49-116">Parent elements</span></span> | <span data-ttu-id="dfd49-117">**entrada**, **ref**</span><span class="sxs-lookup"><span data-stu-id="dfd49-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="dfd49-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="dfd49-118">Child elements</span></span>  | <span data-ttu-id="dfd49-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfd49-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="dfd49-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfd49-120">Remarks</span></span>

<span data-ttu-id="dfd49-121">Esse elemento Especifica o marcador do qual o Windows Media Player deve começar a renderizar o fluxo definido na **entrada** pai ou no elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="dfd49-121">This element specifies the marker from which Windows Media Player is to start rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="dfd49-122">**Observação**</span><span class="sxs-lookup"><span data-stu-id="dfd49-122">**Note**</span></span>

<span data-ttu-id="dfd49-123">Use esse elemento com o atributo **Number** ou **Name** , mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="dfd49-123">Use this element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="dfd49-124">Um **elemento STARTMARKER** definido em um elemento **ref** tem precedência sobre um elemento **STARTMARKER** definido dentro do elemento de **entrada** pai do elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="dfd49-124">A **STARTMARKER** element defined within a **REF** element takes precedence over a **STARTMARKER** element defined within the **REF** element's parent **ENTRY** element.</span></span> <span data-ttu-id="dfd49-125">Um elemento **STARTMARKER** também tem precedência sobre um elemento **StartTime** .</span><span class="sxs-lookup"><span data-stu-id="dfd49-125">A **STARTMARKER** element also takes precedence over a **STARTTIME** element.</span></span>

<span data-ttu-id="dfd49-126">Se o marcador especificado por um elemento **STARTMARKER** ocorrer posteriormente no fluxo do que o marcador definido por um elemento de **marca de fim** , nenhum conteúdo será reproduzido, mas nenhum erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="dfd49-126">If the marker specified by a **STARTMARKER** element occurs later in the stream than the marker defined by an **ENDMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="dfd49-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dfd49-127">Examples</span></span>


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
```



## <a name="requirements"></a><span data-ttu-id="dfd49-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfd49-128">Requirements</span></span>



| <span data-ttu-id="dfd49-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfd49-129">Requirement</span></span> | <span data-ttu-id="dfd49-130">Valor</span><span class="sxs-lookup"><span data-stu-id="dfd49-130">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="dfd49-131">Versão</span><span class="sxs-lookup"><span data-stu-id="dfd49-131">Version</span></span><br/> | <span data-ttu-id="dfd49-132">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="dfd49-132">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dfd49-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfd49-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd49-134">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="dfd49-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="dfd49-135">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="dfd49-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





