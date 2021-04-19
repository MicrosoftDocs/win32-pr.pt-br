---
title: Propriedade DropDownGallery. MenuLayout
description: Representa um contêiner para layouts de menu suspenso DropDownGallery.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- Faixa de DropDownGallery de propriedades do Windows. MenuLayout
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1b6ad3f07f369dfef90b1e6c52c34793e60520
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764250"
---
# <a name="dropdowngallerymenulayout-property"></a><span data-ttu-id="f9677-104">Propriedade DropDownGallery. MenuLayout</span><span class="sxs-lookup"><span data-stu-id="f9677-104">DropDownGallery.MenuLayout property</span></span>

<span data-ttu-id="f9677-105">Representa um contêiner para layouts de menu suspenso [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="f9677-105">Represents a container for [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="f9677-106">Uso</span><span class="sxs-lookup"><span data-stu-id="f9677-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="f9677-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9677-107">Attributes</span></span>

<span data-ttu-id="f9677-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="f9677-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f9677-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f9677-109">Child elements</span></span>



| <span data-ttu-id="f9677-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9677-110">Element</span></span>                                                                           | <span data-ttu-id="f9677-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9677-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="f9677-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="f9677-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="f9677-113">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="f9677-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="f9677-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="f9677-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="f9677-115">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="f9677-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f9677-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f9677-116">Parent elements</span></span>



| <span data-ttu-id="f9677-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9677-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="f9677-118">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f9677-118">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f9677-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9677-119">Remarks</span></span>

<span data-ttu-id="f9677-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f9677-120">Optional.</span></span>

<span data-ttu-id="f9677-121">Pode ocorrer no máximo uma vez para cada elemento [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="f9677-121">May occur at most once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="f9677-122">Um máximo de um elemento filho ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) é permitido.</span><span class="sxs-lookup"><span data-stu-id="f9677-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f9677-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9677-123">Examples</span></span>

<span data-ttu-id="f9677-124">O exemplo a seguir demonstra a marcação básica para o [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="f9677-124">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="f9677-125">Esta seção de código mostra a declaração de controle **DropDownGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="f9677-125">This section of code shows the **DropDownGallery.MenuLayout** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f9677-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9677-126">Requirements</span></span>



| <span data-ttu-id="f9677-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9677-127">Requirement</span></span> | <span data-ttu-id="f9677-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f9677-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f9677-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9677-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f9677-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f9677-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f9677-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9677-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f9677-132">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f9677-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9677-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9677-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9677-134">**Controle da Galeria suspensa**</span><span class="sxs-lookup"><span data-stu-id="f9677-134">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="f9677-135">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="f9677-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





