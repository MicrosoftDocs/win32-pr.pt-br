---
title: Propriedade Command. LabelTitle
description: Representa um título de rótulo.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Faixa de das propriedades do Windows de Propriedade Command. LabelTitle
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499678"
---
# <a name="commandlabeltitle-property"></a><span data-ttu-id="f6ec2-104">Propriedade Command. LabelTitle</span><span class="sxs-lookup"><span data-stu-id="f6ec2-104">Command.LabelTitle property</span></span>

<span data-ttu-id="f6ec2-105">Representa um título de rótulo.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-105">Represents a label title.</span></span>

## <a name="usage"></a><span data-ttu-id="f6ec2-106">Uso</span><span class="sxs-lookup"><span data-stu-id="f6ec2-106">Usage</span></span>

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a><span data-ttu-id="f6ec2-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="f6ec2-107">Attributes</span></span>

<span data-ttu-id="f6ec2-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f6ec2-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f6ec2-109">Child elements</span></span>



| <span data-ttu-id="f6ec2-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6ec2-110">Element</span></span>                                                   | <span data-ttu-id="f6ec2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6ec2-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="f6ec2-112">**String**</span><span class="sxs-lookup"><span data-stu-id="f6ec2-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="f6ec2-113">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="f6ec2-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f6ec2-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f6ec2-114">Parent elements</span></span>



| <span data-ttu-id="f6ec2-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6ec2-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="f6ec2-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="f6ec2-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f6ec2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6ec2-117">Remarks</span></span>

<span data-ttu-id="f6ec2-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-118">Optional.</span></span>

<span data-ttu-id="f6ec2-119">Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="f6ec2-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="f6ec2-120">**Command. LabelTitle** pode conter um valor do tipo *xs: String* restrito a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-120">**Command.LabelTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="f6ec2-121">Use a referência de caractere XML UCS (conjunto de caracteres universal) `&#xA;` para especificar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="f6ec2-122">O comprimento máximo é não associado.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="f6ec2-123">Se nenhum valor for fornecido para **Command. LabelTitle**, o elemento filho da [**cadeia de caracteres**](windowsribbon-element-string.md) será necessário.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-123">If no value is supplied for **Command.LabelTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="f6ec2-124">Se **Command. LabelTitle** contiver um valor e um elemento filho de [**cadeia**](windowsribbon-element-string.md) de caracteres, a **cadeia de caracteres** terá precedência.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-124">If **Command.LabelTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="f6ec2-125">O **comando. LabelTitle** só dá suporte ao alinhamento à esquerda.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-125">**Command.LabelTitle** only supports left alignment.</span></span>

<span data-ttu-id="f6ec2-126">Se um comando for exposto por meio de um item de menu e o valor do rótulo **Command. LabelTitle** ou [UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-label.md) contiver uma letra precedida por um e comercial, conforme mostrado no exemplo a seguir, essa letra será tratada como um KeyTip e um acelerador de teclado para esse comando pela estrutura da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-126">If a Command is exposed through a menu item and the value of **Command.LabelTitle** or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="f6ec2-127">Para exibir um e comercial em um rótulo, escape a designação de caractere especial com um e comercial duplo ( `&&` ), conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6ec2-127">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a><span data-ttu-id="f6ec2-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6ec2-128">Examples</span></span>

<span data-ttu-id="f6ec2-129">O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command. LabelTitle** .</span><span class="sxs-lookup"><span data-stu-id="f6ec2-129">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.LabelTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f6ec2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6ec2-130">Requirements</span></span>



| <span data-ttu-id="f6ec2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6ec2-131">Requirement</span></span> | <span data-ttu-id="f6ec2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f6ec2-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f6ec2-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6ec2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ec2-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f6ec2-134">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f6ec2-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6ec2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ec2-136">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f6ec2-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6ec2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6ec2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ec2-138">\_Rótulo de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="f6ec2-138">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





