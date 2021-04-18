---
title: Elemento ABSTRACT
description: O elemento ABSTRACT contém texto que descreve o elemento ASX, BANNER ou ENTRY associado.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Elemento ABSTRATO Windows Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781065"
---
# <a name="abstract-element"></a><span data-ttu-id="8e492-104">Elemento ABSTRACT</span><span class="sxs-lookup"><span data-stu-id="8e492-104">ABSTRACT Element</span></span>

<span data-ttu-id="8e492-105">O elemento **abstract** contém texto que descreve o elemento **ASX**, **banner** ou **entry** associado.</span><span class="sxs-lookup"><span data-stu-id="8e492-105">The **ABSTRACT** element contains text that describes the associated **ASX**, **BANNER**, or **ENTRY** element.</span></span>

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a><span data-ttu-id="8e492-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e492-106">Attributes</span></span>

<span data-ttu-id="8e492-107">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="8e492-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="8e492-108">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="8e492-108">Parent/Child Elements</span></span>



| <span data-ttu-id="8e492-109">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="8e492-109">Hierarchy</span></span> | <span data-ttu-id="8e492-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="8e492-110">Elements</span></span>                       |
|-----------|--------------------------------|
| <span data-ttu-id="8e492-111">Pai</span><span class="sxs-lookup"><span data-stu-id="8e492-111">Parent</span></span>    | <span data-ttu-id="8e492-112">**ASX**, **entrada**, **faixa**</span><span class="sxs-lookup"><span data-stu-id="8e492-112">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="8e492-113">Filho</span><span class="sxs-lookup"><span data-stu-id="8e492-113">Child</span></span>     | <span data-ttu-id="8e492-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8e492-114">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="8e492-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e492-115">Remarks</span></span>

<span data-ttu-id="8e492-116">Se esse elemento aparecer em um elemento **ASX** , o texto será exibido como uma dica de ferramenta quando o mouse passar sobre o título mostrar.</span><span class="sxs-lookup"><span data-stu-id="8e492-116">If this element appears within an **ASX** element, the text displays as a ToolTip when the mouse hovers over the show title.</span></span>

<span data-ttu-id="8e492-117">Se esse elemento aparecer dentro de um elemento de **entrada** , o texto será exibido como uma dica de ferramenta quando o mouse passar sobre o título do clipe.</span><span class="sxs-lookup"><span data-stu-id="8e492-117">If this element appears within an **ENTRY** element, the text displays as a ToolTip when the mouse hovers over the clip title.</span></span>

<span data-ttu-id="8e492-118">Se esse elemento aparecer dentro de um elemento de **faixa** , o texto será exibido como uma dica de ferramenta para o gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="8e492-118">If this element appears within a **BANNER** element, the text displays as a ToolTip for the banner graphic.</span></span>

<span data-ttu-id="8e492-119">Use apenas um elemento **abstract** por escopo.</span><span class="sxs-lookup"><span data-stu-id="8e492-119">Use only one **ABSTRACT** element per scope.</span></span> <span data-ttu-id="8e492-120">Somente o primeiro elemento **abstract** dentro do escopo de outro elemento é usado quando um arquivo de metarquivo é processado.</span><span class="sxs-lookup"><span data-stu-id="8e492-120">Only the first **ABSTRACT** element within the scope of another element is used when a metafile file is processed.</span></span> <span data-ttu-id="8e492-121">Quaisquer elementos **abstratos** subsequentes nesse escopo são ignorados.</span><span class="sxs-lookup"><span data-stu-id="8e492-121">Any subsequent **ABSTRACT** elements in that scope are ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="8e492-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e492-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="8e492-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e492-123">Requirements</span></span>



| <span data-ttu-id="8e492-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e492-124">Requirement</span></span> | <span data-ttu-id="8e492-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8e492-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="8e492-126">Versão</span><span class="sxs-lookup"><span data-stu-id="8e492-126">Version</span></span><br/> | <span data-ttu-id="8e492-127">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8e492-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e492-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e492-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e492-129">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8e492-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8e492-130">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8e492-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





