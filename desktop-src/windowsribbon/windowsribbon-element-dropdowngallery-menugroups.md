---
title: Propriedade DropDownGallery. MenuGroups
description: Representa um contêiner para um conjunto de itens de menu suspensos em um controle de galeria de Drop-Down.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- Faixa de DropDownGallery de propriedades do Windows. MenuGroups
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788776"
---
# <a name="dropdowngallerymenugroups-property"></a><span data-ttu-id="086a5-104">Propriedade DropDownGallery. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="086a5-104">DropDownGallery.MenuGroups property</span></span>

<span data-ttu-id="086a5-105">Representa um contêiner para um conjunto de itens de menu suspensos em um controle de [Galeria suspensa](windowsribbon-controls-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="086a5-105">Represents a container for a set of drop-down menu items in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="086a5-106">Uso</span><span class="sxs-lookup"><span data-stu-id="086a5-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="086a5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="086a5-107">Attributes</span></span>

<span data-ttu-id="086a5-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="086a5-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="086a5-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="086a5-109">Child elements</span></span>



| <span data-ttu-id="086a5-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="086a5-110">Element</span></span>                                                         | <span data-ttu-id="086a5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="086a5-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="086a5-112">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="086a5-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="086a5-113">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="086a5-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="086a5-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="086a5-114">Parent elements</span></span>



| <span data-ttu-id="086a5-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="086a5-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="086a5-116">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="086a5-116">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="086a5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="086a5-117">Remarks</span></span>

<span data-ttu-id="086a5-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="086a5-118">Required.</span></span>

<span data-ttu-id="086a5-119">Deve ocorrer exatamente uma vez para cada elemento [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="086a5-119">Must occur exactly once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="086a5-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="086a5-120">Examples</span></span>

<span data-ttu-id="086a5-121">O exemplo a seguir demonstra a marcação básica para o elemento **DropDownGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="086a5-121">The following example demonstrates the basic markup for the **DropDownGallery.MenuGroups** element.</span></span>

<span data-ttu-id="086a5-122">Esta seção de código mostra a declaração de controle **DropDownGallery. MenuGroups** em um espaço de comando da [Galeria suspensa](windowsribbon-controls-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="086a5-122">This section of code shows the **DropDownGallery.MenuGroups** control declaration in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) Command Space.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="086a5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="086a5-123">Requirements</span></span>



| <span data-ttu-id="086a5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="086a5-124">Requirement</span></span> | <span data-ttu-id="086a5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="086a5-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="086a5-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="086a5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="086a5-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="086a5-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="086a5-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="086a5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="086a5-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="086a5-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="086a5-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="086a5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="086a5-131">**Controle da Galeria suspensa**</span><span class="sxs-lookup"><span data-stu-id="086a5-131">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="086a5-132">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="086a5-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





