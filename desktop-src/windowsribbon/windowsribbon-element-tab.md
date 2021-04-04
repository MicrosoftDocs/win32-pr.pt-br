---
title: Elemento Tab
description: Representa um núcleo ou uma guia contextual.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Faixa de das janelas do elemento Tab
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e54abc7e13906ada69c1e10f81878c77c4bf5d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007949"
---
# <a name="tab-element"></a><span data-ttu-id="414a2-104">Elemento Tab</span><span class="sxs-lookup"><span data-stu-id="414a2-104">Tab element</span></span>

<span data-ttu-id="414a2-105">Representa um [núcleo](windowsribbon-controls-tab.md) ou uma guia [contextual](windowsribbon-controls-tabgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="414a2-105">Represents a [core](windowsribbon-controls-tab.md) or [contextual](windowsribbon-controls-tabgroup.md) tab.</span></span>

## <a name="usage"></a><span data-ttu-id="414a2-106">Uso</span><span class="sxs-lookup"><span data-stu-id="414a2-106">Usage</span></span>

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a><span data-ttu-id="414a2-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="414a2-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="414a2-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="414a2-108">Attribute</span></span></th>
<th><span data-ttu-id="414a2-109">Type</span><span class="sxs-lookup"><span data-stu-id="414a2-109">Type</span></span></th>
<th><span data-ttu-id="414a2-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="414a2-110">Required</span></span></th>
<th><span data-ttu-id="414a2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="414a2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="414a2-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="414a2-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="414a2-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="414a2-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="414a2-114">Não</span><span class="sxs-lookup"><span data-stu-id="414a2-114">No</span></span><br/></td>
<td><span data-ttu-id="414a2-115">Válido somente se o <a href="windowsribbon-element-menugroup.md"><strong>MyMenu</strong></a> for o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="414a2-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="414a2-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="414a2-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="414a2-117">Uma cadeia de caracteres que contém uma lista de inteiros separados por vírgulas entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="414a2-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="414a2-118">O espaço em branco é válido e ignorado.</span><span class="sxs-lookup"><span data-stu-id="414a2-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="414a2-119">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="414a2-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="414a2-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="414a2-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="414a2-121">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="414a2-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="414a2-122">Não</span><span class="sxs-lookup"><span data-stu-id="414a2-122">No</span></span><br/></td>
<td><span data-ttu-id="414a2-123">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="414a2-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="414a2-124">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="414a2-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="414a2-125">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="414a2-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="414a2-126">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="414a2-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="414a2-127">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="414a2-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="414a2-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="414a2-128">Child elements</span></span>



| <span data-ttu-id="414a2-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="414a2-129">Element</span></span>                                                                         | <span data-ttu-id="414a2-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="414a2-130">Description</span></span>                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="414a2-131">**Group**</span><span class="sxs-lookup"><span data-stu-id="414a2-131">**Group**</span></span>](windowsribbon-element-group.md)<br/>                         | <span data-ttu-id="414a2-132">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="414a2-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="414a2-133">**Guia. ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="414a2-133">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> | <span data-ttu-id="414a2-134">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="414a2-134">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="414a2-135">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="414a2-135">Parent elements</span></span>



| <span data-ttu-id="414a2-136">Elemento</span><span class="sxs-lookup"><span data-stu-id="414a2-136">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="414a2-137">**Faixa de guia. guias**</span><span class="sxs-lookup"><span data-stu-id="414a2-137">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/> |
| [<span data-ttu-id="414a2-138">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="414a2-138">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="414a2-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="414a2-139">Remarks</span></span>

<span data-ttu-id="414a2-140">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="414a2-140">Required.</span></span>

<span data-ttu-id="414a2-141">Deve ocorrer pelo menos uma vez para cada elemento [**Ribbon. Tabs**](windowsribbon-element-ribbon-tabs.md) ou [**TabGroup**](windowsribbon-element-tabgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="414a2-141">Must occur at least once for each [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) or [**TabGroup**](windowsribbon-element-tabgroup.md) element.</span></span>

<span data-ttu-id="414a2-142">**Guia** dá suporte a [modos de aplicativo](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="414a2-142">**Tab** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="414a2-143">Se [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) estiver presente para o elemento **Tab** , uma entrada para cada elemento [**Group**](windowsribbon-element-group.md) e seu tamanho ideal serão necessários em **ScalingPolicy. IdealSizes**.</span><span class="sxs-lookup"><span data-stu-id="414a2-143">If [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) is present for the **Tab** element, then an entry for each [**Group**](windowsribbon-element-group.md) element and its ideal size is required under **ScalingPolicy.IdealSizes**.</span></span>

## <a name="examples"></a><span data-ttu-id="414a2-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="414a2-144">Examples</span></span>

<span data-ttu-id="414a2-145">O exemplo a seguir demonstra a marcação básica para o elemento **Tab** .</span><span class="sxs-lookup"><span data-stu-id="414a2-145">The following example demonstrates the basic markup for the **Tab** element.</span></span>

<span data-ttu-id="414a2-146">Esta seção de código mostra as declarações de comando de **guia** para uma guia **página inicial** .</span><span class="sxs-lookup"><span data-stu-id="414a2-146">This section of code shows the **Tab** Command declarations for a **Home** tab.</span></span>


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



<span data-ttu-id="414a2-147">Esta seção de código mostra as declarações de controle de **guia** .</span><span class="sxs-lookup"><span data-stu-id="414a2-147">This section of code shows the **Tab** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="414a2-148">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="414a2-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="414a2-149">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="414a2-149">Minimum supported system</span></span><br/> | <span data-ttu-id="414a2-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="414a2-150">Windows 7</span></span> |
| <span data-ttu-id="414a2-151">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="414a2-151">Can be empty</span></span>                        | <span data-ttu-id="414a2-152">Não</span><span class="sxs-lookup"><span data-stu-id="414a2-152">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="414a2-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="414a2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414a2-154">Controle guia</span><span class="sxs-lookup"><span data-stu-id="414a2-154">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> <dt>

[<span data-ttu-id="414a2-155">Controle de grupo de guias</span><span class="sxs-lookup"><span data-stu-id="414a2-155">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="414a2-156">**Setmodos**</span><span class="sxs-lookup"><span data-stu-id="414a2-156">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

