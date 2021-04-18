---
title: Elemento COPYRIGHT (msfeeds. h)
description: O elemento de direitos AUTORais define uma cadeia de caracteres de texto especificando as informações de direitos autorais de um elemento ASX ou de entrada.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Elemento de direitos AUTORais Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810570"
---
# <a name="copyright-element"></a><span data-ttu-id="5f5d8-104">Elemento de direitos AUTORais</span><span class="sxs-lookup"><span data-stu-id="5f5d8-104">COPYRIGHT Element</span></span>

<span data-ttu-id="5f5d8-105">O elemento de **direitos autorais** define uma cadeia de caracteres de texto especificando as informações de direitos autorais de um elemento **ASX** ou de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="5f5d8-105">The **COPYRIGHT** element defines a text string specifying the copyright information for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a><span data-ttu-id="5f5d8-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f5d8-106">Attributes</span></span>

<span data-ttu-id="5f5d8-107">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="5f5d8-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="5f5d8-108">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="5f5d8-108">Parent/Child Elements</span></span>



| <span data-ttu-id="5f5d8-109">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="5f5d8-109">Hierarchy</span></span>       | <span data-ttu-id="5f5d8-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="5f5d8-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="5f5d8-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5f5d8-111">Parent elements</span></span> | <span data-ttu-id="5f5d8-112">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="5f5d8-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="5f5d8-113">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5f5d8-113">Child elements</span></span>  | <span data-ttu-id="5f5d8-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5f5d8-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="5f5d8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f5d8-115">Remarks</span></span>

<span data-ttu-id="5f5d8-116">Esse elemento define uma cadeia de texto que especifica as informações de direitos autorais de um elemento **ASX** ou de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="5f5d8-116">This element defines a text string that specifies the copyright information for an **ASX** or **ENTRY** element.</span></span>

<span data-ttu-id="5f5d8-117">Quando esse elemento aparece dentro de um elemento **ASX** , a cadeia de caracteres de direitos autorais é exibida apenas como **Mostrar** informações.</span><span class="sxs-lookup"><span data-stu-id="5f5d8-117">When this element appears within an **ASX** element, the copyright string is displayed only as **Show** information.</span></span> <span data-ttu-id="5f5d8-118">Quando esse elemento aparece dentro de um elemento de **entrada** , o texto é exibido como informações de clipe.</span><span class="sxs-lookup"><span data-stu-id="5f5d8-118">When this element appears within an **ENTRY** element, the text is displayed as clip information.</span></span> <span data-ttu-id="5f5d8-119">Cada elemento de **entrada** e **ASX** pai deve conter no máximo um elemento de **direitos autorais** filho.</span><span class="sxs-lookup"><span data-stu-id="5f5d8-119">Each parent **ASX** and **ENTRY** element should contain at most one child **COPYRIGHT** element.</span></span> <span data-ttu-id="5f5d8-120">Vários elementos de **direitos autorais** após o primeiro serão ignorados e não serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="5f5d8-120">Multiple **COPYRIGHT** elements after the first will be ignored and will not be displayed.</span></span>

<span data-ttu-id="5f5d8-121">Os caracteres de símbolos de registro de direitos autorais e marcas comerciais (ou) podem não ser exibidos corretamente se o metarquivo não for codificado usando o esquema de codificação UTF-8.</span><span class="sxs-lookup"><span data-stu-id="5f5d8-121">The characters for copyright and trademark registration symbols (   or   ) may not display properly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="5f5d8-122">Nesse caso, para exibir qualquer um desses símbolos corretamente para todos os usuários, você pode usar os equivalentes ASCII (c) e (R) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5f5d8-122">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (R) instead.</span></span>

<span data-ttu-id="5f5d8-123">Se o metarquivo for codificado usando UTF-8, os símbolos de direitos autorais e marcas comerciais serão exibidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f5d8-123">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="5f5d8-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5f5d8-124">Examples</span></span>


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a><span data-ttu-id="5f5d8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f5d8-125">Requirements</span></span>



| <span data-ttu-id="5f5d8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f5d8-126">Requirement</span></span> | <span data-ttu-id="5f5d8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5f5d8-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5d8-128">Versão</span><span class="sxs-lookup"><span data-stu-id="5f5d8-128">Version</span></span><br/> | <span data-ttu-id="5f5d8-129">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5f5d8-129">Windows Media Player version 7.0 or later</span></span><br/>                                 |
| <span data-ttu-id="5f5d8-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f5d8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5f5d8-131"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f5d8-131"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f5d8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f5d8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f5d8-133">**Adicionando caracteres de direitos autorais a metaarquivos**</span><span class="sxs-lookup"><span data-stu-id="5f5d8-133">**Adding Copyright Characters to Metafiles**</span></span>](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[<span data-ttu-id="5f5d8-134">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5f5d8-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="5f5d8-135">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5f5d8-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





