---
title: Propriedade SplitButtonGallery. MenuLayout
description: Representa um contêiner para layouts de menu suspenso da Galeria de botões de divisão.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- Faixa de SplitButtonGallery de propriedades do Windows. MenuLayout
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04428c14b5e47795da47e5c03970610cd08a6e8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782692"
---
# <a name="splitbuttongallerymenulayout-property"></a><span data-ttu-id="2b7ae-104">Propriedade SplitButtonGallery. MenuLayout</span><span class="sxs-lookup"><span data-stu-id="2b7ae-104">SplitButtonGallery.MenuLayout property</span></span>

<span data-ttu-id="2b7ae-105">Representa um contêiner para layouts de menu suspenso da [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="2b7ae-105">Represents a container for [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="2b7ae-106">Uso</span><span class="sxs-lookup"><span data-stu-id="2b7ae-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="2b7ae-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2b7ae-107">Attributes</span></span>

<span data-ttu-id="2b7ae-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2b7ae-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2b7ae-109">Child elements</span></span>



| <span data-ttu-id="2b7ae-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="2b7ae-110">Element</span></span>                                                                           | <span data-ttu-id="2b7ae-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b7ae-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="2b7ae-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="2b7ae-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="2b7ae-113">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="2b7ae-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="2b7ae-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="2b7ae-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="2b7ae-115">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="2b7ae-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2b7ae-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2b7ae-116">Parent elements</span></span>



| <span data-ttu-id="2b7ae-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="2b7ae-117">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="2b7ae-118">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="2b7ae-118">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2b7ae-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b7ae-119">Remarks</span></span>

<span data-ttu-id="2b7ae-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-120">Optional.</span></span>

<span data-ttu-id="2b7ae-121">Pode ocorrer no máximo uma vez para cada elemento [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="2b7ae-121">May occur at most once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="2b7ae-122">Um máximo de um elemento filho ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) é permitido.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2b7ae-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2b7ae-123">Examples</span></span>

<span data-ttu-id="2b7ae-124">O exemplo a seguir demonstra a marcação básica para a [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="2b7ae-124">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="2b7ae-125">Esta seção de código mostra a declaração de controle **SplitButtonGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="2b7ae-125">This section of code shows the **SplitButtonGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="2b7ae-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b7ae-126">Requirements</span></span>



| <span data-ttu-id="2b7ae-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b7ae-127">Requirement</span></span> | <span data-ttu-id="2b7ae-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2b7ae-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2b7ae-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b7ae-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2b7ae-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2b7ae-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2b7ae-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b7ae-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2b7ae-132">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="2b7ae-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b7ae-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b7ae-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7ae-134">Controle da Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="2b7ae-134">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="2b7ae-135">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="2b7ae-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





