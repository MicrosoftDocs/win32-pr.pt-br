---
title: Propriedade Application. views
description: Representa um contêiner para cada exibição de estrutura da faixa de forma, especificamente a faixa de e ContextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Faixa de vista da propriedade Application. views Windows
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764121"
---
# <a name="applicationviews-property"></a><span data-ttu-id="24aae-104">Propriedade Application. views</span><span class="sxs-lookup"><span data-stu-id="24aae-104">Application.Views property</span></span>

<span data-ttu-id="24aae-105">Representa um contêiner para cada exibição de estrutura da faixa de forma, especificamente a [**faixa**](windowsribbon-element-ribbon.md) de e [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="24aae-105">Represents a container for each Ribbon framework View, specifically the [**Ribbon**](windowsribbon-element-ribbon.md) and the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="usage"></a><span data-ttu-id="24aae-106">Uso</span><span class="sxs-lookup"><span data-stu-id="24aae-106">Usage</span></span>

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a><span data-ttu-id="24aae-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="24aae-107">Attributes</span></span>

<span data-ttu-id="24aae-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="24aae-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="24aae-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="24aae-109">Child elements</span></span>



| <span data-ttu-id="24aae-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="24aae-110">Element</span></span>                                                               | <span data-ttu-id="24aae-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="24aae-111">Description</span></span>                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="24aae-112">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="24aae-112">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> | <span data-ttu-id="24aae-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="24aae-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="24aae-114">**Faixa de opções**</span><span class="sxs-lookup"><span data-stu-id="24aae-114">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/>             | <span data-ttu-id="24aae-115">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="24aae-115">Must occur exactly once</span></span><br/> <br/>     |



## <a name="parent-elements"></a><span data-ttu-id="24aae-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="24aae-116">Parent elements</span></span>



| <span data-ttu-id="24aae-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="24aae-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="24aae-118">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="24aae-118">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="24aae-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="24aae-119">Remarks</span></span>

<span data-ttu-id="24aae-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="24aae-120">Required.</span></span>

<span data-ttu-id="24aae-121">Deve ocorrer exatamente uma vez para cada elemento de [**aplicativo**](windowsribbon-element-application.md) .</span><span class="sxs-lookup"><span data-stu-id="24aae-121">Must occur exactly once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="24aae-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24aae-122">Examples</span></span>

<span data-ttu-id="24aae-123">O exemplo a seguir mostra um elemento **Application. views** que contém um manifesto de controles de faixa de opções, cada um com uma referência a um comando declarado no elemento [**Application. paracommands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="24aae-123">The following example shows an **Application.Views** element that contains a manifest of Ribbon controls, each with a reference to a Command declared in the [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a><span data-ttu-id="24aae-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24aae-124">Requirements</span></span>



| <span data-ttu-id="24aae-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="24aae-125">Requirement</span></span> | <span data-ttu-id="24aae-126">Valor</span><span class="sxs-lookup"><span data-stu-id="24aae-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="24aae-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24aae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="24aae-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="24aae-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="24aae-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24aae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="24aae-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="24aae-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24aae-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="24aae-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24aae-132">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="24aae-132">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





