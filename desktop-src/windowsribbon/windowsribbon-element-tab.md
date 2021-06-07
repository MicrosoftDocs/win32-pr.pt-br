---
title: Elemento Tab
description: Representa uma guia principal ou contextual.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Faixa de Opções do Windows do elemento Tab
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 410326961df84f6ae62d3c43bee3e651c9533066
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443877"
---
# <a name="tab-element"></a><span data-ttu-id="189b6-104">Elemento Tab</span><span class="sxs-lookup"><span data-stu-id="189b6-104">Tab element</span></span>

<span data-ttu-id="189b6-105">Representa uma [guia principal](windowsribbon-controls-tab.md) [ou contextual.](windowsribbon-controls-tabgroup.md)</span><span class="sxs-lookup"><span data-stu-id="189b6-105">Represents a [core](windowsribbon-controls-tab.md) or [contextual](windowsribbon-controls-tabgroup.md) tab.</span></span>

## <a name="usage"></a><span data-ttu-id="189b6-106">Uso</span><span class="sxs-lookup"><span data-stu-id="189b6-106">Usage</span></span>

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a><span data-ttu-id="189b6-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="189b6-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="189b6-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="189b6-108">Attribute</span></span></th>
<th><span data-ttu-id="189b6-109">Type</span><span class="sxs-lookup"><span data-stu-id="189b6-109">Type</span></span></th>
<th><span data-ttu-id="189b6-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="189b6-110">Required</span></span></th>
<th><span data-ttu-id="189b6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="189b6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="189b6-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="189b6-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="189b6-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="189b6-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="189b6-114">Não</span><span class="sxs-lookup"><span data-stu-id="189b6-114">No</span></span><br/></td>
<td><span data-ttu-id="189b6-115">Válido somente se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> for o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="189b6-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="189b6-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="189b6-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="189b6-117">Uma cadeia de caracteres que contém uma lista separada por vírgulas de inteiros entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="189b6-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="189b6-118">O espaço em branco é válido e ignorado.</span><span class="sxs-lookup"><span data-stu-id="189b6-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="189b6-119">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="189b6-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="189b6-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="189b6-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="189b6-121">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="189b6-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="189b6-122">Não</span><span class="sxs-lookup"><span data-stu-id="189b6-122">No</span></span><br/></td>
<td><span data-ttu-id="189b6-123">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="189b6-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="189b6-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="189b6-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="189b6-125">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="189b6-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="189b6-126">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="189b6-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="189b6-127">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="189b6-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="189b6-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="189b6-128">Child elements</span></span>



| <span data-ttu-id="189b6-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="189b6-129">Element</span></span>                                                                         | <span data-ttu-id="189b6-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="189b6-130">Description</span></span>                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="189b6-131">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="189b6-131">**Group**</span></span>](windowsribbon-element-group.md)<br/>                         | <span data-ttu-id="189b6-132">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="189b6-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="189b6-133">**Tab.ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="189b6-133">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> | <span data-ttu-id="189b6-134">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="189b6-134">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="189b6-135">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="189b6-135">Parent elements</span></span>



| <span data-ttu-id="189b6-136">Elemento</span><span class="sxs-lookup"><span data-stu-id="189b6-136">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="189b6-137">**Ribbon.Tabs**</span><span class="sxs-lookup"><span data-stu-id="189b6-137">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/> |
| [<span data-ttu-id="189b6-138">**Tabgroup**</span><span class="sxs-lookup"><span data-stu-id="189b6-138">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="189b6-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="189b6-139">Remarks</span></span>

<span data-ttu-id="189b6-140">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="189b6-140">Required.</span></span>

<span data-ttu-id="189b6-141">Deve ocorrer pelo menos uma vez para cada [**elemento Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) ou [**TabGroup.**](windowsribbon-element-tabgroup.md)</span><span class="sxs-lookup"><span data-stu-id="189b6-141">Must occur at least once for each [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) or [**TabGroup**](windowsribbon-element-tabgroup.md) element.</span></span>

<span data-ttu-id="189b6-142">**A guia** dá suporte [aos modos de aplicativo](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="189b6-142">**Tab** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="189b6-143">Se [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) estiver presente para o elemento **Tab,** uma entrada para cada elemento [**Group**](windowsribbon-element-group.md) e seu tamanho ideal será necessária em **ScalingPolicy.IdealSizes**.</span><span class="sxs-lookup"><span data-stu-id="189b6-143">If [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) is present for the **Tab** element, then an entry for each [**Group**](windowsribbon-element-group.md) element and its ideal size is required under **ScalingPolicy.IdealSizes**.</span></span>

## <a name="examples"></a><span data-ttu-id="189b6-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="189b6-144">Examples</span></span>

<span data-ttu-id="189b6-145">O exemplo a seguir demonstra a marcação básica para o **elemento Tab.**</span><span class="sxs-lookup"><span data-stu-id="189b6-145">The following example demonstrates the basic markup for the **Tab** element.</span></span>

<span data-ttu-id="189b6-146">Esta seção de código mostra as declarações **comando tab** para uma **guia** Página Início.</span><span class="sxs-lookup"><span data-stu-id="189b6-146">This section of code shows the **Tab** Command declarations for a **Home** tab.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



<span data-ttu-id="189b6-147">Esta seção de código mostra as **declarações de controle** Tab.</span><span class="sxs-lookup"><span data-stu-id="189b6-147">This section of code shows the **Tab** control declarations.</span></span>


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a><span data-ttu-id="189b6-148">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="189b6-148">Element information</span></span>

- <span data-ttu-id="189b6-149">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="189b6-149">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="189b6-150">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="189b6-150">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="189b6-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="189b6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="189b6-152">Controle guia</span><span class="sxs-lookup"><span data-stu-id="189b6-152">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> <dt>

[<span data-ttu-id="189b6-153">Controle De grupo de guias</span><span class="sxs-lookup"><span data-stu-id="189b6-153">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="189b6-154">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="189b6-154">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

