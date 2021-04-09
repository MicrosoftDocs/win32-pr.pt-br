---
title: Propriedade InRibbonGallery. MenuGroups
description: Representa um contêiner para o conjunto de itens de menu suspenso de um controle da Galeria de In-Ribbon.
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- Faixa de InRibbonGallery de propriedades do Windows. MenuGroups
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447b66dada74b1a9b909b3030e080198143b12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009428"
---
# <a name="inribbongallerymenugroups-property"></a><span data-ttu-id="ffa75-104">Propriedade InRibbonGallery. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="ffa75-104">InRibbonGallery.MenuGroups property</span></span>

<span data-ttu-id="ffa75-105">Representa um contêiner para o conjunto de itens de menu suspenso de um controle [da Galeria de faixas](windowsribbon-controls-inribbongallery.md) de uma.</span><span class="sxs-lookup"><span data-stu-id="ffa75-105">Represents a container for the set of drop-down menu items of an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="ffa75-106">Uso</span><span class="sxs-lookup"><span data-stu-id="ffa75-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="ffa75-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ffa75-107">Attributes</span></span>

<span data-ttu-id="ffa75-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="ffa75-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ffa75-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ffa75-109">Child elements</span></span>



| <span data-ttu-id="ffa75-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ffa75-110">Element</span></span>                                                         | <span data-ttu-id="ffa75-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ffa75-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="ffa75-112">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="ffa75-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="ffa75-113">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="ffa75-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ffa75-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ffa75-114">Parent elements</span></span>



| <span data-ttu-id="ffa75-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="ffa75-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="ffa75-116">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="ffa75-116">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ffa75-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffa75-117">Remarks</span></span>

<span data-ttu-id="ffa75-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ffa75-118">Optional.</span></span>

<span data-ttu-id="ffa75-119">Pode ocorrer no máximo uma vez para cada elemento [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ffa75-119">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="ffa75-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ffa75-120">Examples</span></span>

<span data-ttu-id="ffa75-121">O exemplo a seguir demonstra a marcação básica para um controle [da galeria na faixa de](windowsribbon-controls-inribbongallery.md) opções.</span><span class="sxs-lookup"><span data-stu-id="ffa75-121">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

<span data-ttu-id="ffa75-122">Esta seção de código mostra a declaração de controle **InRibbonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="ffa75-122">This section of code shows the **InRibbonGallery.MenuGroups** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ffa75-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffa75-123">Requirements</span></span>



| <span data-ttu-id="ffa75-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffa75-124">Requirement</span></span> | <span data-ttu-id="ffa75-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ffa75-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ffa75-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffa75-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa75-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ffa75-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ffa75-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffa75-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa75-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ffa75-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ffa75-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffa75-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa75-131">Controle da Galeria de faixa de bits</span><span class="sxs-lookup"><span data-stu-id="ffa75-131">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="ffa75-132">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="ffa75-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="ffa75-133">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="ffa75-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





