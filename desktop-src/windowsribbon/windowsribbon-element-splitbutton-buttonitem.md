---
title: Propriedade SplitButton. ButtonItem
description: Representa um contêiner de botão ou botão de alternância que expõe o comando padrão de um botão de divisão.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Faixa de das propriedades do Windows de SplitButton. ButtonItem
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454829"
---
# <a name="splitbuttonbuttonitem-property"></a><span data-ttu-id="1c52a-104">Propriedade SplitButton. ButtonItem</span><span class="sxs-lookup"><span data-stu-id="1c52a-104">SplitButton.ButtonItem property</span></span>

<span data-ttu-id="1c52a-105">Representa um contêiner de [botão](windowsribbon-controls-button.md) ou [botão de alternância](windowsribbon-controls-togglebutton.md) que expõe o comando padrão de um [botão de divisão](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="1c52a-105">Represents a container for a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) that exposes the default Command of a [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="1c52a-106">Uso</span><span class="sxs-lookup"><span data-stu-id="1c52a-106">Usage</span></span>

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a><span data-ttu-id="1c52a-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="1c52a-107">Attributes</span></span>

<span data-ttu-id="1c52a-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="1c52a-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1c52a-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1c52a-109">Child elements</span></span>



| <span data-ttu-id="1c52a-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="1c52a-110">Element</span></span>                                                               | <span data-ttu-id="1c52a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c52a-111">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="1c52a-112">**Botão**</span><span class="sxs-lookup"><span data-stu-id="1c52a-112">**Button**</span></span>](windowsribbon-element-button.md)<br/>             | <span data-ttu-id="1c52a-113">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="1c52a-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="1c52a-114">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="1c52a-114">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/> | <span data-ttu-id="1c52a-115">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="1c52a-115">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1c52a-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1c52a-116">Parent elements</span></span>



| <span data-ttu-id="1c52a-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="1c52a-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="1c52a-118">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="1c52a-118">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1c52a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c52a-119">Remarks</span></span>

<span data-ttu-id="1c52a-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1c52a-120">Optional.</span></span>

<span data-ttu-id="1c52a-121">Pode ocorrer no máximo uma vez para cada [**SplitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="1c52a-121">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

<span data-ttu-id="1c52a-122">Cada **SplitButton. ButtonItem** pode conter apenas um elemento filho [**Button**](windowsribbon-element-button.md) ou [**ToggleButton**](windowsribbon-element-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="1c52a-122">Each **SplitButton.ButtonItem** can contain only one [**Button**](windowsribbon-element-button.md) or [**ToggleButton**](windowsribbon-element-togglebutton.md) child element.</span></span>

## <a name="examples"></a><span data-ttu-id="1c52a-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1c52a-123">Examples</span></span>

<span data-ttu-id="1c52a-124">O exemplo a seguir demonstra a marcação básica para o [botão de divisão](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="1c52a-124">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="1c52a-125">Esta seção de código mostra as declarações de comando [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. ButtonItem** , com um [**grupo**](windowsribbon-element-group.md) associado que funciona como o contêiner pai para o elemento **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="1c52a-125">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="1c52a-126">Esta seção de código mostra as declarações de controle [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. ButtonItem** .</span><span class="sxs-lookup"><span data-stu-id="1c52a-126">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** control declarations.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1c52a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c52a-127">Requirements</span></span>



| <span data-ttu-id="1c52a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c52a-128">Requirement</span></span> | <span data-ttu-id="1c52a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1c52a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1c52a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c52a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1c52a-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1c52a-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1c52a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c52a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1c52a-133">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="1c52a-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c52a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c52a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c52a-135">Controle de botão de divisão</span><span class="sxs-lookup"><span data-stu-id="1c52a-135">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





