---
title: Elemento HelpButton
description: Representa o controle do botão de ajuda.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- Faixa de HelpButton do elemento do Windows
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "105763793"
---
# <a name="helpbutton-element"></a><span data-ttu-id="085e4-104">Elemento HelpButton</span><span class="sxs-lookup"><span data-stu-id="085e4-104">HelpButton element</span></span>

<span data-ttu-id="085e4-105">Representa o controle do [botão de ajuda](windowsribbon-controls-helpbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="085e4-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="085e4-106">Uso</span><span class="sxs-lookup"><span data-stu-id="085e4-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="085e4-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="085e4-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="085e4-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="085e4-108">Attribute</span></span></th>
<th><span data-ttu-id="085e4-109">Type</span><span class="sxs-lookup"><span data-stu-id="085e4-109">Type</span></span></th>
<th><span data-ttu-id="085e4-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="085e4-110">Required</span></span></th>
<th><span data-ttu-id="085e4-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="085e4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="085e4-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="085e4-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="085e4-113">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="085e4-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="085e4-114">Não</span><span class="sxs-lookup"><span data-stu-id="085e4-114">No</span></span><br/></td>
<td><span data-ttu-id="085e4-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="085e4-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="085e4-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="085e4-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="085e4-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="085e4-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="085e4-118">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="085e4-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="085e4-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="085e4-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="085e4-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="085e4-120">Child elements</span></span>

<span data-ttu-id="085e4-121">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="085e4-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="085e4-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="085e4-122">Parent elements</span></span>



| <span data-ttu-id="085e4-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="085e4-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="085e4-124">**Ribbon. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="085e4-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="085e4-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="085e4-125">Remarks</span></span>

<span data-ttu-id="085e4-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="085e4-126">Optional.</span></span>

<span data-ttu-id="085e4-127">Pode ocorrer no máximo uma vez para cada [**Ribbon. HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="085e4-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="085e4-128">Inicia uma caixa de diálogo de ajuda do aplicativo quando clicado.</span><span class="sxs-lookup"><span data-stu-id="085e4-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="085e4-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="085e4-129">Examples</span></span>

<span data-ttu-id="085e4-130">O exemplo a seguir demonstra a marcação básica necessária para implementar um controle do [botão de ajuda](windowsribbon-controls-helpbutton.md) da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="085e4-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="085e4-131">Esta seção de código mostra a declaração de comando **HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="085e4-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="085e4-132">Esta seção de código mostra a declaração de controle **HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="085e4-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="085e4-133">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="085e4-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="085e4-134">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="085e4-134">Minimum supported system</span></span><br/> | <span data-ttu-id="085e4-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="085e4-135">Windows 7</span></span> |
| <span data-ttu-id="085e4-136">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="085e4-136">Can be empty</span></span>                        | <span data-ttu-id="085e4-137">Sim</span><span class="sxs-lookup"><span data-stu-id="085e4-137">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="085e4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="085e4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="085e4-139">Controle do botão ajuda</span><span class="sxs-lookup"><span data-stu-id="085e4-139">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





