---
title: Propriedade Command. TooltipTitle
description: Representa um título de dica de ferramenta.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- Faixa de das propriedades do Windows de Propriedade Command. TooltipTitle
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60f4ddea77fbf88a15d5d27e90ca5660bc0edb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455780"
---
# <a name="commandtooltiptitle-property"></a><span data-ttu-id="17cf7-104">Propriedade Command. TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="17cf7-104">Command.TooltipTitle property</span></span>

<span data-ttu-id="17cf7-105">Representa um título de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="17cf7-105">Represents a tooltip title.</span></span>

## <a name="usage"></a><span data-ttu-id="17cf7-106">Uso</span><span class="sxs-lookup"><span data-stu-id="17cf7-106">Usage</span></span>

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a><span data-ttu-id="17cf7-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="17cf7-107">Attributes</span></span>

<span data-ttu-id="17cf7-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="17cf7-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="17cf7-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="17cf7-109">Child elements</span></span>



| <span data-ttu-id="17cf7-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="17cf7-110">Element</span></span>                                                   | <span data-ttu-id="17cf7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="17cf7-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="17cf7-112">**Strings**</span><span class="sxs-lookup"><span data-stu-id="17cf7-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="17cf7-113">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="17cf7-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="17cf7-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="17cf7-114">Parent elements</span></span>



| <span data-ttu-id="17cf7-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="17cf7-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="17cf7-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="17cf7-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="17cf7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="17cf7-117">Remarks</span></span>

<span data-ttu-id="17cf7-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="17cf7-118">Optional.</span></span>

<span data-ttu-id="17cf7-119">Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="17cf7-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="17cf7-120">**Command. TooltipTitle** pode conter um valor do tipo *xs: String* restrito a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="17cf7-120">**Command.TooltipTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="17cf7-121">Use a referência de caractere XML UCS (conjunto de caracteres universal) `&#xA;` para especificar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="17cf7-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="17cf7-122">O comprimento máximo é não associado.</span><span class="sxs-lookup"><span data-stu-id="17cf7-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="17cf7-123">Se nenhum valor for fornecido para **Command. TooltipTitle**, o elemento filho da [**cadeia de caracteres**](windowsribbon-element-string.md) será necessário.</span><span class="sxs-lookup"><span data-stu-id="17cf7-123">If no value is supplied for **Command.TooltipTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="17cf7-124">Se **Command. TooltipTitle** contiver um valor e um elemento filho de [**cadeia**](windowsribbon-element-string.md) de caracteres, a **cadeia de caracteres** terá precedência.</span><span class="sxs-lookup"><span data-stu-id="17cf7-124">If **Command.TooltipTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="17cf7-125">O **comando. TooltipTitle** só dá suporte ao alinhamento à esquerda.</span><span class="sxs-lookup"><span data-stu-id="17cf7-125">**Command.TooltipTitle** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="17cf7-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17cf7-126">Examples</span></span>

<span data-ttu-id="17cf7-127">O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command. TooltipTitle** .</span><span class="sxs-lookup"><span data-stu-id="17cf7-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="17cf7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17cf7-128">Requirements</span></span>



| <span data-ttu-id="17cf7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="17cf7-129">Requirement</span></span> | <span data-ttu-id="17cf7-130">Valor</span><span class="sxs-lookup"><span data-stu-id="17cf7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="17cf7-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17cf7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="17cf7-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="17cf7-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="17cf7-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17cf7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="17cf7-134">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="17cf7-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17cf7-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="17cf7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17cf7-136">\_TooltipTitle PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="17cf7-136">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





