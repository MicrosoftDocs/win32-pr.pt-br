---
title: Propriedade InRibbonGallery. MenuLayout
description: Representa um contêiner para layouts de menu suspenso da Galeria de In-Ribbon.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Faixa de InRibbonGallery de propriedades do Windows. MenuLayout
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008952"
---
# <a name="inribbongallerymenulayout-property"></a><span data-ttu-id="d1d8c-104">Propriedade InRibbonGallery. MenuLayout</span><span class="sxs-lookup"><span data-stu-id="d1d8c-104">InRibbonGallery.MenuLayout property</span></span>

<span data-ttu-id="d1d8c-105">Representa um contêiner para layouts de menu suspenso [da Galeria de faixa de](windowsribbon-controls-inribbongallery.md) opção.</span><span class="sxs-lookup"><span data-stu-id="d1d8c-105">Represents a container for [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="d1d8c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="d1d8c-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="d1d8c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d1d8c-107">Attributes</span></span>

<span data-ttu-id="d1d8c-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="d1d8c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d1d8c-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d1d8c-109">Child elements</span></span>



| <span data-ttu-id="d1d8c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="d1d8c-110">Element</span></span>                                                                           | <span data-ttu-id="d1d8c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1d8c-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="d1d8c-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="d1d8c-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="d1d8c-113">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="d1d8c-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="d1d8c-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="d1d8c-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="d1d8c-115">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="d1d8c-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d1d8c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d1d8c-116">Parent elements</span></span>



| <span data-ttu-id="d1d8c-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="d1d8c-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="d1d8c-118">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="d1d8c-118">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d1d8c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1d8c-119">Remarks</span></span>

<span data-ttu-id="d1d8c-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d1d8c-120">Optional.</span></span>

<span data-ttu-id="d1d8c-121">Pode ocorrer no máximo uma vez para cada elemento [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d8c-121">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="d1d8c-122">Um máximo de um elemento filho ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) é permitido.</span><span class="sxs-lookup"><span data-stu-id="d1d8c-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d1d8c-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1d8c-123">Examples</span></span>

<span data-ttu-id="d1d8c-124">O exemplo a seguir demonstra a marcação básica para a [Galeria na faixa de](windowsribbon-controls-inribbongallery.md)opções.</span><span class="sxs-lookup"><span data-stu-id="d1d8c-124">The following example demonstrates the basic markup for the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="d1d8c-125">Esta seção de código mostra a declaração de controle **InRibbonGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="d1d8c-125">This section of code shows the **InRibbonGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="d1d8c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1d8c-126">Requirements</span></span>



| <span data-ttu-id="d1d8c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d8c-127">Requirement</span></span> | <span data-ttu-id="d1d8c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d1d8c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1d8c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d8c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d8c-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d1d8c-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d1d8c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d8c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d8c-132">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d1d8c-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1d8c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1d8c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d8c-134">Controle da Galeria de faixa de bits</span><span class="sxs-lookup"><span data-stu-id="d1d8c-134">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="d1d8c-135">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="d1d8c-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





