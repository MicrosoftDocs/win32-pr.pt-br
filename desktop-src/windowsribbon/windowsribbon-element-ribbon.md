---
title: Elemento Ribbon
description: Representa o controle de faixa de opções na Exibição da Faixa de Opções.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Faixa de Opções do elemento Ribbon do Windows
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a743fc354dfea73c525884ec5ffe1f9471f3752
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444997"
---
# <a name="ribbon-element"></a><span data-ttu-id="07f0d-104">Elemento Ribbon</span><span class="sxs-lookup"><span data-stu-id="07f0d-104">Ribbon element</span></span>

<span data-ttu-id="07f0d-105">Representa o controle de faixa de opções na Exibição da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="07f0d-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="07f0d-106">Uso</span><span class="sxs-lookup"><span data-stu-id="07f0d-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="07f0d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="07f0d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07f0d-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="07f0d-108">Attribute</span></span></th>
<th><span data-ttu-id="07f0d-109">Type</span><span class="sxs-lookup"><span data-stu-id="07f0d-109">Type</span></span></th>
<th><span data-ttu-id="07f0d-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="07f0d-110">Required</span></span></th>
<th><span data-ttu-id="07f0d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="07f0d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07f0d-112"><strong>GroupSpacing</strong></span><span class="sxs-lookup"><span data-stu-id="07f0d-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="07f0d-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="07f0d-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="07f0d-114">Não</span><span class="sxs-lookup"><span data-stu-id="07f0d-114">No</span></span><br/></td>
<td><span data-ttu-id="07f0d-115"><dt><span></span><span></span><strong></strong> (Pequeno)</span><span class="sxs-lookup"><span data-stu-id="07f0d-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="07f0d-116">Padrão.</span><span class="sxs-lookup"><span data-stu-id="07f0d-116">Default.</span></span> <br/> </dd> <span data-ttu-id="07f0d-117"><dt><span></span><span></span><strong></strong> (Médio)</span><span class="sxs-lookup"><span data-stu-id="07f0d-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="07f0d-118"><dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="07f0d-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07f0d-119"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="07f0d-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="07f0d-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="07f0d-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="07f0d-121">Não</span><span class="sxs-lookup"><span data-stu-id="07f0d-121">No</span></span><br/></td>
<td><span data-ttu-id="07f0d-122">Usado para anotar o elemento de comando.</span><span class="sxs-lookup"><span data-stu-id="07f0d-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="07f0d-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="07f0d-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="07f0d-124">Qualquer sequência de zero ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="07f0d-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="07f0d-125">O comprimento máximo não ébounded.</span><span class="sxs-lookup"><span data-stu-id="07f0d-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="07f0d-126">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="07f0d-126">Child elements</span></span>



| <span data-ttu-id="07f0d-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="07f0d-127">Element</span></span>                                                                                         | <span data-ttu-id="07f0d-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="07f0d-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="07f0d-129">**Ribbon.ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="07f0d-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="07f0d-130">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="07f0d-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="07f0d-131">**Ribbon.ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="07f0d-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="07f0d-132">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="07f0d-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="07f0d-133">**Ribbon.HelpButton**</span><span class="sxs-lookup"><span data-stu-id="07f0d-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="07f0d-134">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="07f0d-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="07f0d-135">**Ribbon.QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="07f0d-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="07f0d-136">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="07f0d-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="07f0d-137">**Ribbon.SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="07f0d-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="07f0d-138">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="07f0d-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="07f0d-139">**Ribbon.Tabs**</span><span class="sxs-lookup"><span data-stu-id="07f0d-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="07f0d-140">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="07f0d-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="07f0d-141">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="07f0d-141">Parent elements</span></span>



| <span data-ttu-id="07f0d-142">Elemento</span><span class="sxs-lookup"><span data-stu-id="07f0d-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="07f0d-143">**Application.Views**</span><span class="sxs-lookup"><span data-stu-id="07f0d-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="07f0d-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="07f0d-144">Remarks</span></span>

<span data-ttu-id="07f0d-145">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="07f0d-145">Required.</span></span>

<span data-ttu-id="07f0d-146">Deve ocorrer exatamente uma vez para cada [**elemento Application.Views.**](windowsribbon-element-application-views.md)</span><span class="sxs-lookup"><span data-stu-id="07f0d-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="07f0d-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="07f0d-147">Examples</span></span>

<span data-ttu-id="07f0d-148">O exemplo a seguir demonstra a marcação básica para uma **Exibição** da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="07f0d-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="07f0d-149">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="07f0d-149">Element information</span></span>




* <span data-ttu-id="07f0d-150">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="07f0d-150">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="07f0d-151">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="07f0d-151">**Can be empty**: No</span></span>



 

 





