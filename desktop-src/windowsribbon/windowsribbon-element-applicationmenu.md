---
title: Elemento ApplicationMenu
description: Representa o menu do aplicativo. | Elemento ApplicationMenu
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- Faixa de ApplicationMenu do elemento do Windows
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e535fbcc09a404ad7dd5a4019438f4513f5c77c6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443047"
---
# <a name="applicationmenu-element"></a><span data-ttu-id="f98af-105">Elemento ApplicationMenu</span><span class="sxs-lookup"><span data-stu-id="f98af-105">ApplicationMenu element</span></span>

<span data-ttu-id="f98af-106">Representa o [menu do aplicativo](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="f98af-106">Represents the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="f98af-107">Uso</span><span class="sxs-lookup"><span data-stu-id="f98af-107">Usage</span></span>

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="f98af-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f98af-108">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f98af-109">Atributo</span><span class="sxs-lookup"><span data-stu-id="f98af-109">Attribute</span></span></th>
<th><span data-ttu-id="f98af-110">Type</span><span class="sxs-lookup"><span data-stu-id="f98af-110">Type</span></span></th>
<th><span data-ttu-id="f98af-111">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f98af-111">Required</span></span></th>
<th><span data-ttu-id="f98af-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f98af-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f98af-113"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="f98af-113"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="f98af-114">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="f98af-114">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="f98af-115">Não</span><span class="sxs-lookup"><span data-stu-id="f98af-115">No</span></span><br/></td>
<td><span data-ttu-id="f98af-116">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f98af-116">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="f98af-117">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="f98af-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f98af-118">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="f98af-118">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="f98af-119">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="f98af-119">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="f98af-120">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f98af-120">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f98af-121">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f98af-121">Child elements</span></span>



| <span data-ttu-id="f98af-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="f98af-122">Element</span></span>                                                                                             | <span data-ttu-id="f98af-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="f98af-123">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f98af-124">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="f98af-124">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> | <span data-ttu-id="f98af-125">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="f98af-125">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="f98af-126">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="f98af-126">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                     | <span data-ttu-id="f98af-127">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="f98af-127">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f98af-128">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f98af-128">Parent elements</span></span>



| <span data-ttu-id="f98af-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="f98af-129">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f98af-130">**Ribbon. ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="f98af-130">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f98af-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="f98af-131">Remarks</span></span>

<span data-ttu-id="f98af-132">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f98af-132">Required.</span></span>

<span data-ttu-id="f98af-133">Deve ocorrer exatamente uma vez para cada [**Ribbon. ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="f98af-133">Must occur exactly once for each [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span></span>

<span data-ttu-id="f98af-134">Os elementos filho do elemento **ApplicationMenu** devem ocorrer na ordem especificada:</span><span class="sxs-lookup"><span data-stu-id="f98af-134">The child elements of the **ApplicationMenu** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="f98af-135">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="f98af-135">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)
2.  [<span data-ttu-id="f98af-136">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="f98af-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)

## <a name="examples"></a><span data-ttu-id="f98af-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f98af-137">Examples</span></span>

<span data-ttu-id="f98af-138">O exemplo a seguir demonstra a marcação básica para o [menu do aplicativo](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="f98af-138">The following example demonstrates the basic markup for the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

<span data-ttu-id="f98af-139">Esta seção de código mostra as declarações de comando **ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="f98af-139">This section of code shows the **ApplicationMenu** Command declarations.</span></span>


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



<span data-ttu-id="f98af-140">Esta seção de código mostra as declarações de controle **ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="f98af-140">This section of code shows the **ApplicationMenu** control declarations.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a><span data-ttu-id="f98af-141">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f98af-141">Element information</span></span>

* <span data-ttu-id="f98af-142">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="f98af-142">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="f98af-143">**Pode estar vazio**: não</span><span class="sxs-lookup"><span data-stu-id="f98af-143">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="f98af-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="f98af-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98af-145">Controle de menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="f98af-145">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





