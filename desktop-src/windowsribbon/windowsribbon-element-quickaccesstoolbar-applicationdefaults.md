---
title: Propriedade QuickAccessToolbar. ApplicationDefaults
description: Representa um contêiner para comandos padrão na barra de ferramentas de acesso rápido (QAT).
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- Faixa de QuickAccessToolbar de propriedades do Windows. ApplicationDefaults
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 084ea334441cb0cf545adaa3d1016f7d02da1b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764488"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a><span data-ttu-id="81308-104">Propriedade QuickAccessToolbar. ApplicationDefaults</span><span class="sxs-lookup"><span data-stu-id="81308-104">QuickAccessToolbar.ApplicationDefaults property</span></span>

<span data-ttu-id="81308-105">Representa um contêiner para comandos padrão na [barra de ferramentas de acesso rápido (qat)](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="81308-105">Represents a container for default Commands in the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

## <a name="usage"></a><span data-ttu-id="81308-106">Uso</span><span class="sxs-lookup"><span data-stu-id="81308-106">Usage</span></span>

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a><span data-ttu-id="81308-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="81308-107">Attributes</span></span>

<span data-ttu-id="81308-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="81308-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="81308-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="81308-109">Child elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="81308-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="81308-110">Element</span></span></th>
<th><span data-ttu-id="81308-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="81308-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81308-112"><a href="windowsribbon-element-button.md"><strong>Botão</strong></a></span><span class="sxs-lookup"><span data-stu-id="81308-112"><a href="windowsribbon-element-button.md"><strong>Button</strong></a></span></span><br/></td>
<td><span data-ttu-id="81308-113">Deve ocorrer pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="81308-113">Must occur at least once.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81308-114"><a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a></span><span class="sxs-lookup"><span data-stu-id="81308-114"><a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a></span></span><br/></td>
<td><span data-ttu-id="81308-115">Deve ocorrer pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="81308-115">Must occur at least once.</span></span><br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81308-116"><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a></span><span class="sxs-lookup"><span data-stu-id="81308-116"><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a></span></span><br/></td>
<td><span data-ttu-id="81308-117">Deve ocorrer pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="81308-117">Must occur at least once.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81308-118">Windows 8 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="81308-118">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81308-119"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="81308-119"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>
<td><span data-ttu-id="81308-120">Deve ocorrer pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="81308-120">Must occur at least once.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81308-121">Windows 8 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="81308-121">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81308-122"><a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="81308-122"><a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a></span></span><br/></td>
<td><span data-ttu-id="81308-123">Deve ocorrer pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="81308-123">Must occur at least once.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81308-124">Windows 8 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="81308-124">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81308-125"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="81308-125"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>
<td><span data-ttu-id="81308-126">Deve ocorrer pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="81308-126">Must occur at least once.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81308-127">Windows 8 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="81308-127">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81308-128"><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="81308-128"><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="81308-129">Deve ocorrer pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="81308-129">Must occur at least once.</span></span><br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="parent-elements"></a><span data-ttu-id="81308-130">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="81308-130">Parent elements</span></span>



| <span data-ttu-id="81308-131">Elemento</span><span class="sxs-lookup"><span data-stu-id="81308-131">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="81308-132">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="81308-132">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="81308-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="81308-133">Remarks</span></span>

<span data-ttu-id="81308-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="81308-134">Optional.</span></span>

<span data-ttu-id="81308-135">Pode ocorrer no máximo uma vez para cada [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="81308-135">May occur at most once for each [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="81308-136">Um mínimo de um elemento filho deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="81308-136">A minimum of one child element must be specified.</span></span>

<span data-ttu-id="81308-137">Um máximo de 20 elementos filho pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="81308-137">A maximum of 20 child elements can be specified.</span></span>

## <a name="examples"></a><span data-ttu-id="81308-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="81308-138">Examples</span></span>

<span data-ttu-id="81308-139">O exemplo a seguir demonstra a marcação básica para o [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="81308-139">The following example demonstrates the basic markup for the [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="81308-140">Esta seção de código mostra a declaração de controle **QuickAccessToolbar. ApplicationDefaults** .</span><span class="sxs-lookup"><span data-stu-id="81308-140">This section of code shows the **QuickAccessToolbar.ApplicationDefaults** control declaration.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a><span data-ttu-id="81308-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81308-141">Requirements</span></span>



| <span data-ttu-id="81308-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="81308-142">Requirement</span></span> | <span data-ttu-id="81308-143">Valor</span><span class="sxs-lookup"><span data-stu-id="81308-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="81308-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81308-144">Minimum supported client</span></span><br/> | <span data-ttu-id="81308-145">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="81308-145">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="81308-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81308-146">Minimum supported server</span></span><br/> | <span data-ttu-id="81308-147">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="81308-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81308-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="81308-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81308-149">Controle da barra de ferramentas de acesso rápido</span><span class="sxs-lookup"><span data-stu-id="81308-149">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





