---
title: Elemento Ribbon
description: Representa o controle da faixa de faixas na exibição da faixa de faixas.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Faixa de Ribbon do Windows do elemento Ribbon
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76ce73735d05b3d8c8cfa686f53570fd08ae6f1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105761639"
---
# <a name="ribbon-element"></a><span data-ttu-id="65512-104">Elemento Ribbon</span><span class="sxs-lookup"><span data-stu-id="65512-104">Ribbon element</span></span>

<span data-ttu-id="65512-105">Representa o controle da faixa de faixas na exibição da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="65512-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="65512-106">Uso</span><span class="sxs-lookup"><span data-stu-id="65512-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="65512-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="65512-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65512-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="65512-108">Attribute</span></span></th>
<th><span data-ttu-id="65512-109">Type</span><span class="sxs-lookup"><span data-stu-id="65512-109">Type</span></span></th>
<th><span data-ttu-id="65512-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="65512-110">Required</span></span></th>
<th><span data-ttu-id="65512-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="65512-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65512-112"><strong>GroupSpacing</strong></span><span class="sxs-lookup"><span data-stu-id="65512-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="65512-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="65512-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="65512-114">Não</span><span class="sxs-lookup"><span data-stu-id="65512-114">No</span></span><br/></td>
<td><span data-ttu-id="65512-115"><dt><span></span><span></span><strong></strong> Menores</span><span class="sxs-lookup"><span data-stu-id="65512-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="65512-116">Padrão.</span><span class="sxs-lookup"><span data-stu-id="65512-116">Default.</span></span> <br/> </dd> <span data-ttu-id="65512-117"><dt><span></span><span></span><strong></strong> Médio</span><span class="sxs-lookup"><span data-stu-id="65512-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="65512-118"><dt><span></span><span></span><strong></strong> Vários</span><span class="sxs-lookup"><span data-stu-id="65512-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65512-119"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="65512-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="65512-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="65512-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="65512-121">Não</span><span class="sxs-lookup"><span data-stu-id="65512-121">No</span></span><br/></td>
<td><span data-ttu-id="65512-122">Usado para anotar o elemento Command.</span><span class="sxs-lookup"><span data-stu-id="65512-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="65512-123">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="65512-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="65512-124">Qualquer sequência de zero ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="65512-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="65512-125">O comprimento máximo é não associado.</span><span class="sxs-lookup"><span data-stu-id="65512-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="65512-126">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="65512-126">Child elements</span></span>



| <span data-ttu-id="65512-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="65512-127">Element</span></span>                                                                                         | <span data-ttu-id="65512-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="65512-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="65512-129">**Ribbon. ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="65512-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="65512-130">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="65512-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="65512-131">**Ribbon. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="65512-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="65512-132">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="65512-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="65512-133">**Ribbon. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="65512-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="65512-134">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="65512-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="65512-135">**Ribbon. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="65512-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="65512-136">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="65512-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="65512-137">**Ribbon. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="65512-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="65512-138">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="65512-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="65512-139">**Faixa de guia. guias**</span><span class="sxs-lookup"><span data-stu-id="65512-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="65512-140">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="65512-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="65512-141">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="65512-141">Parent elements</span></span>



| <span data-ttu-id="65512-142">Elemento</span><span class="sxs-lookup"><span data-stu-id="65512-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="65512-143">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="65512-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="65512-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="65512-144">Remarks</span></span>

<span data-ttu-id="65512-145">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="65512-145">Required.</span></span>

<span data-ttu-id="65512-146">Deve ocorrer exatamente uma vez para cada elemento [**Application. views**](windowsribbon-element-application-views.md) .</span><span class="sxs-lookup"><span data-stu-id="65512-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="65512-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65512-147">Examples</span></span>

<span data-ttu-id="65512-148">O exemplo a seguir demonstra a marcação básica para um modo de exibição de **faixa** de opções.</span><span class="sxs-lookup"><span data-stu-id="65512-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a><span data-ttu-id="65512-149">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="65512-149">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="65512-150">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65512-150">Minimum supported system</span></span><br/> | <span data-ttu-id="65512-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="65512-151">Windows 7</span></span> |
| <span data-ttu-id="65512-152">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="65512-152">Can be empty</span></span>                        | <span data-ttu-id="65512-153">Não</span><span class="sxs-lookup"><span data-stu-id="65512-153">No</span></span>        |



 

 





