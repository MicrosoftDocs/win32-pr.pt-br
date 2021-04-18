---
title: Propriedade Command. KeyTip
description: Representa o KeyTip de um controle.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Faixa de das propriedades do Windows de Propriedade Command. KeyTip
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788978"
---
# <a name="commandkeytip-property"></a><span data-ttu-id="e7bd7-104">Propriedade Command. KeyTip</span><span class="sxs-lookup"><span data-stu-id="e7bd7-104">Command.Keytip property</span></span>

<span data-ttu-id="e7bd7-105">Representa o KeyTip de um controle.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-105">Represents the keytip for a control.</span></span>

## <a name="usage"></a><span data-ttu-id="e7bd7-106">Uso</span><span class="sxs-lookup"><span data-stu-id="e7bd7-106">Usage</span></span>

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a><span data-ttu-id="e7bd7-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="e7bd7-107">Attributes</span></span>

<span data-ttu-id="e7bd7-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e7bd7-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e7bd7-109">Child elements</span></span>



| <span data-ttu-id="e7bd7-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7bd7-110">Element</span></span>                                                   | <span data-ttu-id="e7bd7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7bd7-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="e7bd7-112">**Strings**</span><span class="sxs-lookup"><span data-stu-id="e7bd7-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="e7bd7-113">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="e7bd7-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e7bd7-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e7bd7-114">Parent elements</span></span>



| <span data-ttu-id="e7bd7-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7bd7-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="e7bd7-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="e7bd7-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e7bd7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7bd7-117">Remarks</span></span>

<span data-ttu-id="e7bd7-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-118">Optional.</span></span>

<span data-ttu-id="e7bd7-119">Pode ocorrer no máximo uma vez para cada elemento de [**comando**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="e7bd7-119">May occur at most once for each [**Command**](windowsribbon-element-command.md) element.</span></span>

<span data-ttu-id="e7bd7-120">**Command. KeyTip** pode conter um valor do tipo *xs: String* restrito a qualquer sequência de caracteres Unicode, incluindo o espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-120">**Command.Keytip** can contain a value of type *xs:string* constrained to any sequence of Unicode characters, including white space.</span></span>

<span data-ttu-id="e7bd7-121">Um **comando. KeyTip** pode começar com um número somente quando associado a um controle dentro de uma [guia](windowsribbon-controls-tab.md) ou na [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="e7bd7-121">A **Command.Keytip** can begin with a number only when associated with a control within a [Tab](windowsribbon-controls-tab.md) or the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="e7bd7-122">Para exibir as dicas de tecla que são válidas para o estado atual da faixa de faixas, pressione e segure a chave ALT.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-122">To display the keytips that are valid for the current state of the ribbon, press and hold the ALT key.</span></span> <span data-ttu-id="e7bd7-123">A captura de tela a seguir mostra o inicial, ou primeiro nível, dicas de teclado que são exibidas no Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-123">The following screen shot shows the initial, or first level, keytips that are displayed in Microsoft Paint for Windows 7.</span></span> <span data-ttu-id="e7bd7-124">Após a seleção de um KeyTip de primeiro nível, somente as keytips de nível de segundo são exibidas.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-124">After a first-level keytip has been selected, only second-level keytips are displayed.</span></span>

![Dicas de primeiro nível no Microsoft Paint para Windows 7](images/properties/ui-pkey-label-keytips.png)

<span data-ttu-id="e7bd7-126">O **comando. KeyTip** atua como o acelerador de teclado para um comando, a menos que esse comando seja exposto por meio de um item de menu.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-126">**Command.Keytip** acts as the keyboard accelerator for a command unless that command is exposed through a menu item.</span></span> <span data-ttu-id="e7bd7-127">Nesse caso, a estrutura ignora o valor de **Command. KeyTip** e, em vez disso, usa um caractere precedido por um e comercial como especificado por [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou o [ \_ \_ rótulo PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="e7bd7-127">In this case, the framework ignores the **Command.Keytip** value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="e7bd7-128">Se nenhum e comercial for especificado pelo **comando Command. LabelTitle** ou UI \_ PKEY \_ , nenhum KeyTip ou acelerador de teclado será exposto.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-128">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="e7bd7-129">Se nenhum valor for fornecido para **Command. KeyTip**, o elemento filho da [**cadeia de caracteres**](windowsribbon-element-string.md) será necessário.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-129">If no value is supplied for **Command.Keytip**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="e7bd7-130">Se **Command. KeyTip** contiver um valor e um elemento filho de [**cadeia**](windowsribbon-element-string.md) de caracteres, a **cadeia de caracteres** terá precedência.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-130">If **Command.Keytip** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="e7bd7-131">Por padrão, as seguintes letras são usadas pela estrutura para gerar automaticamente dicas de Key:</span><span class="sxs-lookup"><span data-stu-id="e7bd7-131">By default, the following letters are used by the framework to automatically generate keytips:</span></span>

-   <span data-ttu-id="e7bd7-132">O **F** é atribuído ao [menu do aplicativo](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="e7bd7-132">**F** is assigned to the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="e7bd7-133">**Y** é atribuído a qualquer comando que não tenha um KeyTip especificado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-133">**Y** is assigned to any command that does not have a keytip specified by the application.</span></span>
-   <span data-ttu-id="e7bd7-134">**Z** é atribuído a cada controle de [grupo](windowsribbon-controls-group.md) e não pode ser personalizado.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-134">**Z** is assigned to each [Group](windowsribbon-controls-group.md) control and cannot be customized.</span></span> <span data-ttu-id="e7bd7-135">Um KeyTip de grupo é exibido somente quando o [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) do controle Especifica uma opção de tamanho de **pop-up** .</span><span class="sxs-lookup"><span data-stu-id="e7bd7-135">A Group keytip is displayed only when the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) for the control specifies a **Popup** size option.</span></span> <span data-ttu-id="e7bd7-136">Para obter mais informações, consulte [Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="e7bd7-136">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

> [!Note]  
> <span data-ttu-id="e7bd7-137">Nenhuma dessas letras é reservada pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-137">None of these letters are reserved by the framework.</span></span> <span data-ttu-id="e7bd7-138">Cada um pode ser atribuído a um ou mais comandos, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-138">Each can be assigned to one or more commands as required.</span></span>

 

<span data-ttu-id="e7bd7-139">A estrutura resolve conflitos de KeyTip das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="e7bd7-139">The framework resolves keytip conflicts in the following ways:</span></span>

-   <span data-ttu-id="e7bd7-140">Se um ou mais controles [guia](windowsribbon-controls-tab.md) estiverem associados ao mesmo KeyTip, um número será acrescentado a cada KeyTip, começando em 1 e aumentando sequencialmente (2, 3,...) para cada controle na ordem de declaração.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-140">If one or more [Tab](windowsribbon-controls-tab.md) controls are associated with the same keytip, a number is appended to each keytip, starting at 1, and increasing sequentially (2, 3,...) for each control in the order of declaration.</span></span> <span data-ttu-id="e7bd7-141">Se qualquer controle de guia for atribuído à letra F como um KeyTip, o [menu do aplicativo](windowsribbon-controls-applicationmenu.md) será atribuído F1 com as dicas de tecla restantes ajustadas conforme descrito.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-141">If any Tab controls are assigned the letter F as a keytip, the [Application Menu](windowsribbon-controls-applicationmenu.md) is assigned F1 with the remaining keytips adjusted as described.</span></span>
-   <span data-ttu-id="e7bd7-142">Quando associado a um único controle dentro de uma [guia](windowsribbon-controls-tab.md), o KeyTip F é válido para o controle e o [menu do aplicativo](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="e7bd7-142">When associated with a single control within a [Tab](windowsribbon-controls-tab.md), the keytip F is valid for both the control and the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="e7bd7-143">O menu do aplicativo padrão KeyTip não é alterado, mas a precedência é dada ao controle na guia ativa.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-143">The default Application Menu keytip is not changed, but precedence is given to the control on the active tab.</span></span>
-   <span data-ttu-id="e7bd7-144">Se um ou mais controles dentro de uma guia estiverem associados ao mesmo KeyTip, a estrutura refatorar automaticamente as dicas de [tecla](windowsribbon-controls-tab.md) desses controles, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-144">If one or more controls within a [Tab](windowsribbon-controls-tab.md) are associated with the same keytip, the framework automatically refactors the keytips of those controls, as described previously.</span></span>

> [!Note]  
> <span data-ttu-id="e7bd7-145">Uma pequena variação na cor do texto é usada para realçar as dicas de atalho Refatorada em uma implementação de faixa de medida padrão.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-145">A slight variation in text color is used to highlight refactored keytips in a standard ribbon implementation.</span></span> <span data-ttu-id="e7bd7-146">Para uma implementação de faixa de faixas não padrão em que a cor da faixa de medida foi personalizada, esse comportamento de estrutura é substituído e todas as keytips são exibidas com a mesma cor do texto.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-146">For a nonstandard ribbon implementation where the ribbon color has been customized, this framework behavior is overridden and all keytips are displayed with the same text color.</span></span> <span data-ttu-id="e7bd7-147">Para obter mais informações, consulte [Personalizando as cores da faixa](ribbon-color.md)de forma.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-147">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>

 

<span data-ttu-id="e7bd7-148">O comprimento máximo é não associado.</span><span class="sxs-lookup"><span data-stu-id="e7bd7-148">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="e7bd7-149">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e7bd7-149">Examples</span></span>

<span data-ttu-id="e7bd7-150">O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command. KeyTip** .</span><span class="sxs-lookup"><span data-stu-id="e7bd7-150">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Keytip** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="e7bd7-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7bd7-151">Requirements</span></span>



| <span data-ttu-id="e7bd7-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7bd7-152">Requirement</span></span> | <span data-ttu-id="e7bd7-153">Valor</span><span class="sxs-lookup"><span data-stu-id="e7bd7-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e7bd7-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bd7-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bd7-155">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7bd7-155">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e7bd7-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bd7-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bd7-157">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="e7bd7-157">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7bd7-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7bd7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bd7-159">\_KeyTip PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="e7bd7-159">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





