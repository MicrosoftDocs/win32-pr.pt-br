---
title: Elemento AUTHOR
description: O elemento autor contém o nome do autor de um metarquivo de mídia do Windows ou clipe de mídia.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Elemento de autor Windows Media Player
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784921"
---
# <a name="author-element"></a><span data-ttu-id="97b86-104">Elemento AUTHOR</span><span class="sxs-lookup"><span data-stu-id="97b86-104">AUTHOR Element</span></span>

<span data-ttu-id="97b86-105">O elemento **autor** contém o nome do autor de um metarquivo de mídia do Windows ou clipe de mídia.</span><span class="sxs-lookup"><span data-stu-id="97b86-105">The **AUTHOR** element contains the name of the author of a Windows Media metafile or media clip.</span></span>

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a><span data-ttu-id="97b86-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="97b86-106">Attributes</span></span>

<span data-ttu-id="97b86-107">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="97b86-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="97b86-108">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="97b86-108">Parent/Child Elements</span></span>



| <span data-ttu-id="97b86-109">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="97b86-109">Hierarchy</span></span>       | <span data-ttu-id="97b86-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="97b86-110">Element</span></span>            |
|-----------------|--------------------|
| <span data-ttu-id="97b86-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="97b86-111">Parent elements</span></span> | <span data-ttu-id="97b86-112">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="97b86-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="97b86-113">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="97b86-113">Child elements</span></span>  | <span data-ttu-id="97b86-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="97b86-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="97b86-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="97b86-115">Remarks</span></span>

<span data-ttu-id="97b86-116">Esse elemento contém uma cadeia de texto que representa o nome do autor de um metarquivo de mídia do Windows ou clipe de mídia.</span><span class="sxs-lookup"><span data-stu-id="97b86-116">This element contains a text string representing the name of the author of a Windows Media metafile or media clip.</span></span> <span data-ttu-id="97b86-117">Você pode usar o elemento **Author** dentro do elemento **ASX** e dentro de elementos de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="97b86-117">You can use the **AUTHOR** element within the **ASX** element and within **ENTRY** elements.</span></span>

<span data-ttu-id="97b86-118">Se esse elemento aparecer no elemento **ASX** , o texto será exibido como **Mostrar** informações.</span><span class="sxs-lookup"><span data-stu-id="97b86-118">If this element appears in the **ASX** element, the text is displayed as **Show** information.</span></span>

<span data-ttu-id="97b86-119">Se esse elemento aparecer em um elemento de **entrada** , o texto será exibido como o autor do clipe.</span><span class="sxs-lookup"><span data-stu-id="97b86-119">If this element appears in an **ENTRY** element, the text is displayed as the clip author.</span></span>

<span data-ttu-id="97b86-120">Cada elemento de **entrada** e **ASX** pai deve conter no máximo um elemento de **autor** filho.</span><span class="sxs-lookup"><span data-stu-id="97b86-120">Each parent **ASX** and **ENTRY** element should contain at most one child **AUTHOR** element.</span></span> <span data-ttu-id="97b86-121">Vários elementos de **autor** após o primeiro serão ignorados e não serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="97b86-121">Multiple **AUTHOR** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="97b86-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97b86-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="97b86-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97b86-123">Requirements</span></span>



| <span data-ttu-id="97b86-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="97b86-124">Requirement</span></span> | <span data-ttu-id="97b86-125">Valor</span><span class="sxs-lookup"><span data-stu-id="97b86-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="97b86-126">Versão</span><span class="sxs-lookup"><span data-stu-id="97b86-126">Version</span></span><br/> | <span data-ttu-id="97b86-127">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="97b86-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97b86-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="97b86-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b86-129">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="97b86-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="97b86-130">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="97b86-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





