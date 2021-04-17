---
title: Elemento TITLE (metarquivo)
description: O elemento TITLE define uma cadeia de texto especificando o título de um elemento ASX ou de entrada.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Elemento de título (metarquivo) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811682"
---
# <a name="title-element-metafile"></a><span data-ttu-id="0389a-104">Elemento TITLE (metarquivo)</span><span class="sxs-lookup"><span data-stu-id="0389a-104">TITLE Element (metafile)</span></span>

<span data-ttu-id="0389a-105">O elemento **title** define uma cadeia de texto especificando o título de um elemento **ASX** ou de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="0389a-105">The **TITLE** element defines a text string specifying the title for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a><span data-ttu-id="0389a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="0389a-106">Attributes</span></span>

<span data-ttu-id="0389a-107">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="0389a-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="0389a-108">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="0389a-108">Parent/Child Elements</span></span>



| <span data-ttu-id="0389a-109">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="0389a-109">Hierarchy</span></span>       | <span data-ttu-id="0389a-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="0389a-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="0389a-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0389a-111">Parent elements</span></span> | <span data-ttu-id="0389a-112">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="0389a-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="0389a-113">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0389a-113">Child elements</span></span>  | <span data-ttu-id="0389a-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0389a-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="0389a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0389a-115">Remarks</span></span>

<span data-ttu-id="0389a-116">Esse elemento define uma cadeia de texto que especifica o título de um elemento **ASX** ou de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="0389a-116">This element defines a text string that specifies the title of an **ASX** or **ENTRY** element.</span></span> <span data-ttu-id="0389a-117">O título é exibido na caixa de diálogo painel de exibição e **Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="0389a-117">The title is displayed in the display panel and **Properties** dialog box.</span></span>

<span data-ttu-id="0389a-118">Quando esse elemento aparece dentro de um elemento **ASX** , o texto é exibido como **Mostrar** informações.</span><span class="sxs-lookup"><span data-stu-id="0389a-118">When this element appears within an **ASX** element, the text is displayed as **Show** information.</span></span> <span data-ttu-id="0389a-119">Quando esse elemento aparece dentro de um elemento de **entrada** , o texto é exibido como informações de **clipe** .</span><span class="sxs-lookup"><span data-stu-id="0389a-119">When this element appears within an **ENTRY** element, the text is displayed as **Clip** information.</span></span>

<span data-ttu-id="0389a-120">Se um elemento **moreinfo** também for usado com o elemento associado (pai), será o texto do título no qual o usuário clica para acessar a URL definida no elemento **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="0389a-120">If a **MOREINFO** element is also used with the associated (parent) element, it is the title text that the user clicks to access the URL defined in the **MOREINFO** element.</span></span>

<span data-ttu-id="0389a-121">Cada elemento de **entrada** e **ASX** pai deve conter no máximo um elemento de **título** filho.</span><span class="sxs-lookup"><span data-stu-id="0389a-121">Each parent **ASX** and **ENTRY** element should contain at most one child **TITLE** element.</span></span> <span data-ttu-id="0389a-122">Vários elementos **title** após o primeiro serão ignorados e não serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="0389a-122">Multiple **TITLE** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="0389a-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0389a-123">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="0389a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0389a-124">Requirements</span></span>



| <span data-ttu-id="0389a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0389a-125">Requirement</span></span> | <span data-ttu-id="0389a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0389a-126">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="0389a-127">Versão</span><span class="sxs-lookup"><span data-stu-id="0389a-127">Version</span></span><br/> | <span data-ttu-id="0389a-128">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0389a-128">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0389a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0389a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0389a-130">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0389a-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0389a-131">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0389a-131">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





