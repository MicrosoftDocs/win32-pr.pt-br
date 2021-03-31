---
title: Propriedade SplitButtonGallery. MenuGroups
description: Representa um contêiner para um conjunto de itens de menu suspenso em um controle SplitButtonGallery.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- Faixa de SplitButtonGallery de propriedades do Windows. MenuGroups
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72176e7d7e79b076c3a7cf4d1fd847aa4f4e0561
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085543"
---
# <a name="splitbuttongallerymenugroups-property"></a><span data-ttu-id="7df47-104">Propriedade SplitButtonGallery. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="7df47-104">SplitButtonGallery.MenuGroups property</span></span>

<span data-ttu-id="7df47-105">Representa um contêiner para um conjunto de itens de menu suspenso em um controle [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="7df47-105">Represents a container for a set of drop-down menu items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="7df47-106">Uso</span><span class="sxs-lookup"><span data-stu-id="7df47-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="7df47-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="7df47-107">Attributes</span></span>

<span data-ttu-id="7df47-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="7df47-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7df47-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7df47-109">Child elements</span></span>



| <span data-ttu-id="7df47-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="7df47-110">Element</span></span>                                                         | <span data-ttu-id="7df47-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7df47-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="7df47-112">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="7df47-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="7df47-113">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="7df47-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="7df47-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7df47-114">Parent elements</span></span>



| <span data-ttu-id="7df47-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="7df47-115">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="7df47-116">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="7df47-116">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7df47-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7df47-117">Remarks</span></span>

<span data-ttu-id="7df47-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7df47-118">Required.</span></span>

<span data-ttu-id="7df47-119">Deve ocorrer exatamente uma vez para cada elemento [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="7df47-119">Must occur exactly once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="7df47-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7df47-120">Examples</span></span>

<span data-ttu-id="7df47-121">O exemplo a seguir demonstra a marcação básica para o elemento **SplitButtonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="7df47-121">The following example demonstrates the basic markup for the **SplitButtonGallery.MenuGroups** element.</span></span>

<span data-ttu-id="7df47-122">Esta seção de código mostra a declaração de controle **SplitButtonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="7df47-122">This section of code shows the **SplitButtonGallery.MenuGroups** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7df47-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df47-123">Requirements</span></span>



| <span data-ttu-id="7df47-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df47-124">Requirement</span></span> | <span data-ttu-id="7df47-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7df47-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7df47-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df47-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7df47-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7df47-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7df47-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df47-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7df47-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="7df47-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7df47-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7df47-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df47-131">Controle da Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="7df47-131">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="7df47-132">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="7df47-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





