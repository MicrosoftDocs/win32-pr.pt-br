---
title: Elemento ENTRYREF
description: O elemento ENTRYREF aponta para os elementos de entrada em um metarquivo externo.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Elemento ENTRYREF do Windows Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789557"
---
# <a name="entryref-element"></a><span data-ttu-id="46fdf-104">Elemento ENTRYREF</span><span class="sxs-lookup"><span data-stu-id="46fdf-104">ENTRYREF Element</span></span>

<span data-ttu-id="46fdf-105">O elemento **ENTRYREF** aponta para os elementos de **entrada** em um metarquivo externo.</span><span class="sxs-lookup"><span data-stu-id="46fdf-105">The **ENTRYREF** element points to the **ENTRY** elements in an external metafile.</span></span>

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="46fdf-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="46fdf-106">Attributes</span></span>

<span data-ttu-id="46fdf-107">**Href** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="46fdf-107">**HREF** (required)</span></span>

<span data-ttu-id="46fdf-108">URL para um metarquivo referenciado.</span><span class="sxs-lookup"><span data-stu-id="46fdf-108">URL to a referenced metafile.</span></span>

<span data-ttu-id="46fdf-109">**CLIENTBIND**</span><span class="sxs-lookup"><span data-stu-id="46fdf-109">**CLIENTBIND**</span></span>

<span data-ttu-id="46fdf-110">Não há mais suporte para este atributo.</span><span class="sxs-lookup"><span data-stu-id="46fdf-110">This attribute is no longer supported.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="46fdf-111">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="46fdf-111">Parent/Child Elements</span></span>



| <span data-ttu-id="46fdf-112">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="46fdf-112">Hierarchy</span></span>       | <span data-ttu-id="46fdf-113">Elementos</span><span class="sxs-lookup"><span data-stu-id="46fdf-113">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="46fdf-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="46fdf-114">Parent elements</span></span> | <span data-ttu-id="46fdf-115">**ASX**, **evento**, **repetir**</span><span class="sxs-lookup"><span data-stu-id="46fdf-115">**ASX**, **EVENT**, **REPEAT**</span></span> |
| <span data-ttu-id="46fdf-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="46fdf-116">Child elements</span></span>  | <span data-ttu-id="46fdf-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="46fdf-117">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="46fdf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="46fdf-118">Remarks</span></span>

<span data-ttu-id="46fdf-119">Esse elemento aponta para o conteúdo de um metarquivo externo.</span><span class="sxs-lookup"><span data-stu-id="46fdf-119">This element points to the contents of an external metafile.</span></span> <span data-ttu-id="46fdf-120">O Windows Media Player processa os elementos de **entrada** do metarquivo referenciado como se eles estivessem incluídos no metarquivo primário na posição do elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="46fdf-120">Windows Media Player processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="46fdf-121">No entanto, ele ignora todos os elementos de **entrada** no metarquivo referenciado que têm o atributo **SKIPIFREF** definido como Sim.</span><span class="sxs-lookup"><span data-stu-id="46fdf-121">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="46fdf-122">O Windows Media Player 7,0, 7,1 e Windows Media Player para Windows XP ignoram todos os elementos **ENTRYREF** no metarquivo referenciado.</span><span class="sxs-lookup"><span data-stu-id="46fdf-122">Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="46fdf-123">Portanto, os metaarquivos só podem ser aninhados em um nível profundo ao usar essas versões do Player.</span><span class="sxs-lookup"><span data-stu-id="46fdf-123">Thus, metafiles can only be nested one level deep when using these versions of the Player.</span></span> <span data-ttu-id="46fdf-124">O Windows Media Player também ignora o elemento **ASX** no arquivo referenciado junto com seus atributos.</span><span class="sxs-lookup"><span data-stu-id="46fdf-124">Windows Media Player also ignores the **ASX** element in the referenced file along with its attributes.</span></span> <span data-ttu-id="46fdf-125">O Windows Media Player 9 Series ou posterior dá suporte ao aninhamento de metaarquivos de até cinco níveis de profundidade.</span><span class="sxs-lookup"><span data-stu-id="46fdf-125">Windows Media Player 9 Series or later supports nesting metafiles up to five levels deep.</span></span>

<span data-ttu-id="46fdf-126">A URL especificada no atributo **href** torna-se a URL base para quaisquer URLs relativas no metarquivo externo.</span><span class="sxs-lookup"><span data-stu-id="46fdf-126">The URL specified in the **HREF** attribute becomes the base URL for any relative URLs in the external metafile.</span></span> <span data-ttu-id="46fdf-127">Essa URL é usada quando uma entrada do metarquivo externo está sendo executada e o usuário a adiciona à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="46fdf-127">This URL is used when an entry from the external metafile is playing and the user adds it to the library.</span></span>

## <a name="examples"></a><span data-ttu-id="46fdf-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46fdf-128">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="46fdf-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46fdf-129">Requirements</span></span>



| <span data-ttu-id="46fdf-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="46fdf-130">Requirement</span></span> | <span data-ttu-id="46fdf-131">Valor</span><span class="sxs-lookup"><span data-stu-id="46fdf-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="46fdf-132">Versão</span><span class="sxs-lookup"><span data-stu-id="46fdf-132">Version</span></span><br/> | <span data-ttu-id="46fdf-133">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="46fdf-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46fdf-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="46fdf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46fdf-135">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="46fdf-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="46fdf-136">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="46fdf-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





