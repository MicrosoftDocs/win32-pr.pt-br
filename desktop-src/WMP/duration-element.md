---
title: Elemento DURATION
description: O elemento DURATION define o período de tempo durante o qual o Windows Media Player processará a entrada da playlist associada.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Elemento DURATION do Windows Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796433"
---
# <a name="duration-element"></a><span data-ttu-id="df56f-104">Elemento DURATION</span><span class="sxs-lookup"><span data-stu-id="df56f-104">DURATION Element</span></span>

<span data-ttu-id="df56f-105">O elemento **Duration** define o período de tempo durante o qual o Windows Media Player processará a entrada da playlist associada.</span><span class="sxs-lookup"><span data-stu-id="df56f-105">The **DURATION** element defines the length of time Windows Media Player will render the associated playlist entry.</span></span>

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="df56f-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="df56f-106">Attributes</span></span>

<span data-ttu-id="df56f-107">**Valor** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="df56f-107">**VALUE** (required)</span></span>

<span data-ttu-id="df56f-108">O período de tempo, em horas, minutos, segundos e centésimos de segundo, que uma entrada é renderizada pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="df56f-108">The length of time, in hours, minutes, seconds, and hundredths of a second, that an entry is rendered by Windows Media Player.</span></span> <span data-ttu-id="df56f-109">O valor padrão é o comprimento total da entrada.</span><span class="sxs-lookup"><span data-stu-id="df56f-109">The default value is the entire length of the entry.</span></span> <span data-ttu-id="df56f-110">Se a entrada for um arquivo gráfico, um valor de duração deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="df56f-110">If the entry is a graphic file, a duration value must be specified.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="df56f-111">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="df56f-111">Parent/Child Elements</span></span>



| <span data-ttu-id="df56f-112">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="df56f-112">Hierarchy</span></span>       | <span data-ttu-id="df56f-113">Elementos</span><span class="sxs-lookup"><span data-stu-id="df56f-113">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="df56f-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="df56f-114">Parent elements</span></span> | <span data-ttu-id="df56f-115">**entrada**, **ref**</span><span class="sxs-lookup"><span data-stu-id="df56f-115">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="df56f-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="df56f-116">Child elements</span></span>  | <span data-ttu-id="df56f-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="df56f-117">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="df56f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="df56f-118">Remarks</span></span>

<span data-ttu-id="df56f-119">Esse elemento define o período de tempo que um fluxo deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="df56f-119">This element defines the length of time a stream is to be rendered.</span></span> <span data-ttu-id="df56f-120">Se o atributo de **valor** exceder o comprimento do fluxo de conteúdo, o fluxo será encerrado em seu ponto de extremidade normal.</span><span class="sxs-lookup"><span data-stu-id="df56f-120">If the **VALUE** attribute exceeds the length of the content stream, the stream terminates at its normal end-point.</span></span>

<span data-ttu-id="df56f-121">Esse elemento pode aparecer em um elemento **ref** ou dentro de um elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="df56f-121">This element can appear either within a **REF** element or within an **ENTRY** element.</span></span> <span data-ttu-id="df56f-122">No entanto, um elemento **Duration** definido dentro de um elemento **ref** substitui um que aparece dentro do elemento de **entrada** pai do elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="df56f-122">However, a **DURATION** element defined within a **REF** element overrides one that appears within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="df56f-123">O elemento **Duration** substitui um elemento **PREVIEWDURATION** .</span><span class="sxs-lookup"><span data-stu-id="df56f-123">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="df56f-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df56f-124">Examples</span></span>


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a><span data-ttu-id="df56f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df56f-125">Requirements</span></span>



| <span data-ttu-id="df56f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="df56f-126">Requirement</span></span> | <span data-ttu-id="df56f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="df56f-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="df56f-128">Versão</span><span class="sxs-lookup"><span data-stu-id="df56f-128">Version</span></span><br/> | <span data-ttu-id="df56f-129">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="df56f-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df56f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="df56f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df56f-131">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="df56f-131">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="df56f-132">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="df56f-132">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





