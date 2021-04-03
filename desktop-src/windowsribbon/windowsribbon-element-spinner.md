---
title: Elemento Spinner
description: Representa um controle giratório.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Faixa de medida do elemento Spinner do Windows
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b1f9727dc7fbad8be24c15f0b1f551b021294dd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104007049"
---
# <a name="spinner-element"></a><span data-ttu-id="569b4-104">Elemento Spinner</span><span class="sxs-lookup"><span data-stu-id="569b4-104">Spinner element</span></span>

<span data-ttu-id="569b4-105">Representa um controle [giratório](windowsribbon-controls-spinner.md) .</span><span class="sxs-lookup"><span data-stu-id="569b4-105">Represents a [Spinner](windowsribbon-controls-spinner.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="569b4-106">Uso</span><span class="sxs-lookup"><span data-stu-id="569b4-106">Usage</span></span>

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="569b4-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="569b4-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="569b4-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="569b4-108">Attribute</span></span></th>
<th><span data-ttu-id="569b4-109">Type</span><span class="sxs-lookup"><span data-stu-id="569b4-109">Type</span></span></th>
<th><span data-ttu-id="569b4-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="569b4-110">Required</span></span></th>
<th><span data-ttu-id="569b4-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="569b4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="569b4-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="569b4-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="569b4-113">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="569b4-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="569b4-114">Não</span><span class="sxs-lookup"><span data-stu-id="569b4-114">No</span></span><br/></td>
<td><span data-ttu-id="569b4-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="569b4-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="569b4-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="569b4-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="569b4-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="569b4-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="569b4-118">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="569b4-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="569b4-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="569b4-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="569b4-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="569b4-120">Child elements</span></span>

<span data-ttu-id="569b4-121">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="569b4-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="569b4-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="569b4-122">Parent elements</span></span>



| <span data-ttu-id="569b4-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="569b4-123">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="569b4-124">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="569b4-124">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="569b4-125">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="569b4-125">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="569b4-126">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="569b4-126">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="569b4-127">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="569b4-127">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="569b4-128">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="569b4-128">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="569b4-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="569b4-129">Remarks</span></span>

<span data-ttu-id="569b4-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="569b4-130">Optional.</span></span>

<span data-ttu-id="569b4-131">Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md) ou [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="569b4-131">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="569b4-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="569b4-132">Examples</span></span>

<span data-ttu-id="569b4-133">O exemplo a seguir demonstra a marcação básica para o [controle giratório](windowsribbon-controls-spinner.md).</span><span class="sxs-lookup"><span data-stu-id="569b4-133">The following example demonstrates the basic markup for the [Spinner](windowsribbon-controls-spinner.md).</span></span>

<span data-ttu-id="569b4-134">Esta seção de código mostra as declarações de comando **Spinner** , com um elemento [**Group**](windowsribbon-element-group.md) que funciona como o contêiner pai para o elemento **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="569b4-134">This section of code shows the **Spinner** Command declarations, with a [**Group**](windowsribbon-element-group.md) element that functions as the parent container for the **Spinner** element.</span></span>


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



<span data-ttu-id="569b4-135">Esta seção de código mostra as declarações de controle **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="569b4-135">This section of code shows the **Spinner** control declarations.</span></span>


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="569b4-136">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="569b4-136">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="569b4-137">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="569b4-137">Minimum supported system</span></span><br/> | <span data-ttu-id="569b4-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="569b4-138">Windows 7</span></span> |
| <span data-ttu-id="569b4-139">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="569b4-139">Can be empty</span></span>                        | <span data-ttu-id="569b4-140">Sim</span><span class="sxs-lookup"><span data-stu-id="569b4-140">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="569b4-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="569b4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="569b4-142">Controle Spinner</span><span class="sxs-lookup"><span data-stu-id="569b4-142">Spinner control</span></span>](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





