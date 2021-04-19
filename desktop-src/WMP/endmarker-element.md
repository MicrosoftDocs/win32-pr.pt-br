---
title: Elemento endmarcer
description: O elemento endmarcer especifica um marcador no qual o Windows Media Player irá parar de renderizar o fluxo.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Elemento de marca de fim do Windows Media Player
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811109"
---
# <a name="endmarker-element"></a><span data-ttu-id="b684f-104">Elemento endmarcer</span><span class="sxs-lookup"><span data-stu-id="b684f-104">ENDMARKER Element</span></span>

<span data-ttu-id="b684f-105">O elemento **ENDmarcer** especifica um marcador no qual o Windows Media Player irá parar de renderizar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="b684f-105">The **ENDMARKER** element specifies a marker at which Windows Media Player will stop rendering the stream.</span></span>

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="b684f-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b684f-106">Attributes</span></span>

<span data-ttu-id="b684f-107">**AUTOMÁTICA**</span><span class="sxs-lookup"><span data-stu-id="b684f-107">**NUMBER**</span></span>

<span data-ttu-id="b684f-108">O número de um marcador numérico no índice.</span><span class="sxs-lookup"><span data-stu-id="b684f-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="b684f-109">O valor padrão é o final do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b684f-109">The default value is the end of the content.</span></span>

<span data-ttu-id="b684f-110">**NOME**</span><span class="sxs-lookup"><span data-stu-id="b684f-110">**NAME**</span></span>

<span data-ttu-id="b684f-111">O nome de um marcador nomeado no índice.</span><span class="sxs-lookup"><span data-stu-id="b684f-111">The name of a named marker in the index.</span></span> <span data-ttu-id="b684f-112">O valor padrão é o final do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b684f-112">The default value is the end of the content.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b684f-113">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="b684f-113">Parent/Child Elements</span></span>



| <span data-ttu-id="b684f-114">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="b684f-114">Hierarchy</span></span>       | <span data-ttu-id="b684f-115">Elementos</span><span class="sxs-lookup"><span data-stu-id="b684f-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="b684f-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b684f-116">Parent elements</span></span> | <span data-ttu-id="b684f-117">**entrada**, **ref**</span><span class="sxs-lookup"><span data-stu-id="b684f-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="b684f-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b684f-118">Child elements</span></span>  | <span data-ttu-id="b684f-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b684f-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="b684f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b684f-120">Remarks</span></span>

<span data-ttu-id="b684f-121">Esse elemento Especifica o marcador em que o Windows Media Player deve parar de renderizar o fluxo definido na **entrada** pai ou no elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="b684f-121">This element specifies the marker where Windows Media Player is to stop rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="b684f-122">Observação</span><span class="sxs-lookup"><span data-stu-id="b684f-122">Note</span></span>

<span data-ttu-id="b684f-123">Use o elemento **ENDmarcer** com o atributo **Number** ou **Name** , mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="b684f-123">Use the **ENDMARKER** element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="b684f-124">No modo de visualização, atingir um marcador final interrompe a visualização, mesmo que o tempo especificado pelo elemento **PREVIEWDURATION** não tenha decorrido.</span><span class="sxs-lookup"><span data-stu-id="b684f-124">In preview mode, reaching an end marker stops the preview, even if the time specified by the **PREVIEWDURATION** element has not elapsed.</span></span> <span data-ttu-id="b684f-125">O elemento **ENDmarcer** também tem precedência sobre o elemento **Duration** .</span><span class="sxs-lookup"><span data-stu-id="b684f-125">The **ENDMARKER** element also takes precedence over the **DURATION** element.</span></span>

<span data-ttu-id="b684f-126">Um elemento de **marca de fim** definido em um elemento **ref** tem PREcedência sobre um **marca de fim** definido dentro do elemento de **entrada** pai do elemento **ref** .</span><span class="sxs-lookup"><span data-stu-id="b684f-126">An **ENDMARKER** element defined within a **REF** element takes precedence over an **ENDMARKER** defined within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="b684f-127">Se o marcador especificado por um elemento de **marca de fim** ocorrer anteriormente no fluxo do que o marcador definido por um elemento **STARTMARKER** , nenhum conteúdo será reproduzido, mas nenhum erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="b684f-127">If the marker specified by an **ENDMARKER** element occurs earlier in the stream than the marker defined by a **STARTMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="b684f-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b684f-128">Examples</span></span>


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

```



## <a name="requirements"></a><span data-ttu-id="b684f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b684f-129">Requirements</span></span>



| <span data-ttu-id="b684f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b684f-130">Requirement</span></span> | <span data-ttu-id="b684f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b684f-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="b684f-132">Versão</span><span class="sxs-lookup"><span data-stu-id="b684f-132">Version</span></span><br/> | <span data-ttu-id="b684f-133">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b684f-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b684f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b684f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b684f-135">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b684f-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b684f-136">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b684f-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





