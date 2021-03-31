---
title: Propriedade SplitButton. MenuGroups
description: Representa um contêiner para um conjunto de itens de menu suspensos em um controle de botão de divisão padrão.
ms.assetid: 6328ad49-037b-4cd5-90f6-b91646e260ee
keywords:
- Faixa de das propriedades do Windows de SplitButton. MenuGroups
topic_type:
- apiref
api_name:
- SplitButton.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8af4639040d6b6302b4d2b5761d750074389a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644640"
---
# <a name="splitbuttonmenugroups-property"></a><span data-ttu-id="3d9f4-104">Propriedade SplitButton. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="3d9f4-104">SplitButton.MenuGroups property</span></span>

<span data-ttu-id="3d9f4-105">Representa um contêiner para um conjunto de itens de menu suspensos em um controle de [botão de divisão](windowsribbon-controls-splitbutton.md) padrão.</span><span class="sxs-lookup"><span data-stu-id="3d9f4-105">Represents a container for a set of drop-down menu items in a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="3d9f4-106">Uso</span><span class="sxs-lookup"><span data-stu-id="3d9f4-106">Usage</span></span>

``` syntax
<SplitButton.MenuGroups>
  child elements
</SplitButton.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="3d9f4-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="3d9f4-107">Attributes</span></span>

<span data-ttu-id="3d9f4-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="3d9f4-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3d9f4-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3d9f4-109">Child elements</span></span>



| <span data-ttu-id="3d9f4-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="3d9f4-110">Element</span></span>                                                         | <span data-ttu-id="3d9f4-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d9f4-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="3d9f4-112">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="3d9f4-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="3d9f4-113">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="3d9f4-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3d9f4-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3d9f4-114">Parent elements</span></span>



| <span data-ttu-id="3d9f4-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="3d9f4-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="3d9f4-116">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="3d9f4-116">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3d9f4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d9f4-117">Remarks</span></span>

<span data-ttu-id="3d9f4-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3d9f4-118">Optional.</span></span>

<span data-ttu-id="3d9f4-119">Pode ocorrer no máximo uma vez para cada [**SplitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="3d9f4-119">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3d9f4-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3d9f4-120">Examples</span></span>

<span data-ttu-id="3d9f4-121">O exemplo a seguir demonstra a marcação básica para o [botão de divisão](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="3d9f4-121">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="3d9f4-122">Esta seção de código mostra as declarações de comando [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. MenuGroups** , com um [**grupo**](windowsribbon-element-group.md) associado que funciona como o contêiner pai para o elemento **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="3d9f4-122">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="3d9f4-123">Esta seção de código mostra as declarações de controle [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="3d9f4-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="3d9f4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d9f4-124">Requirements</span></span>



| <span data-ttu-id="3d9f4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d9f4-125">Requirement</span></span> | <span data-ttu-id="3d9f4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3d9f4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3d9f4-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d9f4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3d9f4-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3d9f4-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3d9f4-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d9f4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3d9f4-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="3d9f4-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d9f4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d9f4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d9f4-132">Controle de botão de divisão</span><span class="sxs-lookup"><span data-stu-id="3d9f4-132">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





