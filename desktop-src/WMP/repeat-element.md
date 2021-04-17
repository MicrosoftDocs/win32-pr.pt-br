---
title: Elemento REPEAT
description: O elemento REPEAT define o número de vezes que o Windows Media Player repete um ou mais elementos de entrada ou ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- REPETIR elemento Windows Media Player
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752595"
---
# <a name="repeat-element"></a><span data-ttu-id="024fe-104">Elemento REPEAT</span><span class="sxs-lookup"><span data-stu-id="024fe-104">REPEAT Element</span></span>

<span data-ttu-id="024fe-105">O elemento **REPEAT** define o número de vezes que o Windows Media Player repete um ou mais elementos de **entrada** ou **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="024fe-105">The **REPEAT** element defines the number of times Windows Media Player repeats one or more **ENTRY** or **ENTRYREF** elements.</span></span>

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a><span data-ttu-id="024fe-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="024fe-106">Attributes</span></span>

<span data-ttu-id="024fe-107">**COUNT**</span><span class="sxs-lookup"><span data-stu-id="024fe-107">**COUNT**</span></span>

<span data-ttu-id="024fe-108">Inteiro que representa o número de vezes que o Windows Media Player repete a **entrada** e os elementos **ENTRYREF** dentro desse escopo do elemento.</span><span class="sxs-lookup"><span data-stu-id="024fe-108">Integer representing the number of times Windows Media Player repeats the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="024fe-109">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="024fe-109">Parent/Child Elements</span></span>



| <span data-ttu-id="024fe-110">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="024fe-110">Hierarchy</span></span>       | <span data-ttu-id="024fe-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="024fe-111">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="024fe-112">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="024fe-112">Parent elements</span></span> | <span data-ttu-id="024fe-113">**ASX**</span><span class="sxs-lookup"><span data-stu-id="024fe-113">**ASX**</span></span>                 |
| <span data-ttu-id="024fe-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="024fe-114">Child elements</span></span>  | <span data-ttu-id="024fe-115">**entrada**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="024fe-115">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="024fe-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="024fe-116">Remarks</span></span>

<span data-ttu-id="024fe-117">Esse elemento define o número de vezes que o Windows Media Player se repete ou faz um loop pelos clipes definidos pelos elementos **entry** e **ENTRYREF** dentro desse escopo do elemento.</span><span class="sxs-lookup"><span data-stu-id="024fe-117">This element defines the number of times Windows Media Player repeats, or loops through, the clips defined by the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span> <span data-ttu-id="024fe-118">Somente o primeiro elemento **REPEAT** em um metarquivo é válido; os elementos **repetidos** subsequentes são ignorados.</span><span class="sxs-lookup"><span data-stu-id="024fe-118">Only the first **REPEAT** element in a metafile is valid; subsequent **REPEAT** elements are ignored.</span></span>

<span data-ttu-id="024fe-119">Se nenhum atributo **Count** for definido, o conteúdo na **entrada** associada e nos elementos **ENTRYREF** repetirá um número infinito de vezes.</span><span class="sxs-lookup"><span data-stu-id="024fe-119">If no **COUNT** attribute is defined, the content in the associated **ENTRY** and **ENTRYREF** elements repeats an infinite number of times.</span></span> <span data-ttu-id="024fe-120">Um valor de zero faz com que o Windows Media Player ignore o elemento **REPEAT** e reproduza o conteúdo uma vez.</span><span class="sxs-lookup"><span data-stu-id="024fe-120">A value of zero causes Windows Media Player to ignore the **REPEAT** element and play the content once.</span></span>

## <a name="examples"></a><span data-ttu-id="024fe-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="024fe-121">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="024fe-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="024fe-122">Requirements</span></span>



| <span data-ttu-id="024fe-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="024fe-123">Requirement</span></span> | <span data-ttu-id="024fe-124">Valor</span><span class="sxs-lookup"><span data-stu-id="024fe-124">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="024fe-125">Versão</span><span class="sxs-lookup"><span data-stu-id="024fe-125">Version</span></span><br/> | <span data-ttu-id="024fe-126">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="024fe-126">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="024fe-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="024fe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024fe-128">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="024fe-128">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="024fe-129">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="024fe-129">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





