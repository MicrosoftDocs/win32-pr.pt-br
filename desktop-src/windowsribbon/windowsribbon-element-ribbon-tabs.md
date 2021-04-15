---
title: Propriedade Ribbon. Tabs
description: Representa um contêiner para todas as guias de núcleo em uma faixa de faixas.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Faixa de das propriedades do Windows da faixa de guia. Tabs
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454713"
---
# <a name="ribbontabs-property"></a><span data-ttu-id="62edc-104">Propriedade Ribbon. Tabs</span><span class="sxs-lookup"><span data-stu-id="62edc-104">Ribbon.Tabs property</span></span>

<span data-ttu-id="62edc-105">Representa um contêiner para todas as guias de núcleo em uma faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="62edc-105">Represents a container for all core tabs in a Ribbon.</span></span>

## <a name="usage"></a><span data-ttu-id="62edc-106">Uso</span><span class="sxs-lookup"><span data-stu-id="62edc-106">Usage</span></span>

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a><span data-ttu-id="62edc-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="62edc-107">Attributes</span></span>

<span data-ttu-id="62edc-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="62edc-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="62edc-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="62edc-109">Child elements</span></span>



| <span data-ttu-id="62edc-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="62edc-110">Element</span></span>                                             | <span data-ttu-id="62edc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="62edc-111">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="62edc-112">**Tab**</span><span class="sxs-lookup"><span data-stu-id="62edc-112">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="62edc-113">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="62edc-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="62edc-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="62edc-114">Parent elements</span></span>



| <span data-ttu-id="62edc-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="62edc-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="62edc-116">**Faixa de opções**</span><span class="sxs-lookup"><span data-stu-id="62edc-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="62edc-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="62edc-117">Remarks</span></span>

<span data-ttu-id="62edc-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="62edc-118">Required.</span></span>

<span data-ttu-id="62edc-119">Pode ocorrer uma ou mais vezes para cada [**faixa de faixas**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="62edc-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="62edc-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62edc-120">Examples</span></span>

<span data-ttu-id="62edc-121">O exemplo a seguir demonstra a marcação básica para um elemento **Ribbon. Tabs** com uma declaração de [**guia**](windowsribbon-element-tab.md) **página inicial** .</span><span class="sxs-lookup"><span data-stu-id="62edc-121">The following example demonstrates the basic markup for a **Ribbon.Tabs** element with a **Home** [**Tab**](windowsribbon-element-tab.md) declaration.</span></span>


```C++
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
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
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



## <a name="requirements"></a><span data-ttu-id="62edc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62edc-122">Requirements</span></span>



| <span data-ttu-id="62edc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="62edc-123">Requirement</span></span> | <span data-ttu-id="62edc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="62edc-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="62edc-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62edc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="62edc-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="62edc-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="62edc-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62edc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="62edc-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="62edc-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62edc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="62edc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62edc-130">**Ribbon. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="62edc-130">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





