---
title: Propriedade Command. Symbol
description: Representa o nome de um comando que pode ser referenciado externamente.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Faixa de das propriedades do Windows do comando. Symbol
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764514"
---
# <a name="commandsymbol-property"></a><span data-ttu-id="3fef7-104">Propriedade Command. Symbol</span><span class="sxs-lookup"><span data-stu-id="3fef7-104">Command.Symbol property</span></span>

<span data-ttu-id="3fef7-105">Representa o nome de um [**comando**](windowsribbon-element-command.md) que pode ser referenciado externamente.</span><span class="sxs-lookup"><span data-stu-id="3fef7-105">Represents the name of a [**Command**](windowsribbon-element-command.md) that can be referenced externally.</span></span>

## <a name="usage"></a><span data-ttu-id="3fef7-106">Uso</span><span class="sxs-lookup"><span data-stu-id="3fef7-106">Usage</span></span>

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="3fef7-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="3fef7-107">Attributes</span></span>

<span data-ttu-id="3fef7-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="3fef7-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3fef7-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3fef7-109">Child elements</span></span>

<span data-ttu-id="3fef7-110">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="3fef7-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="3fef7-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3fef7-111">Parent elements</span></span>



| <span data-ttu-id="3fef7-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fef7-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="3fef7-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="3fef7-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3fef7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fef7-114">Remarks</span></span>

<span data-ttu-id="3fef7-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3fef7-115">Optional.</span></span>

<span data-ttu-id="3fef7-116">Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="3fef7-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="3fef7-117">O símbolo é associado a uma definição de comando no arquivo de cabeçalho da faixa de, por exemplo, `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="3fef7-117">The symbol is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="3fef7-118">Esse elemento contém um valor do tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="3fef7-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="3fef7-119">O valor é restrito a uma cadeia de caracteres que consiste em uma letra ou sublinhado seguido por qualquer sequência de letras, dígitos e sublinhados.</span><span class="sxs-lookup"><span data-stu-id="3fef7-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="3fef7-120">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3fef7-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="3fef7-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3fef7-121">Examples</span></span>

<span data-ttu-id="3fef7-122">O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="3fef7-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Symbol** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3fef7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fef7-123">Requirements</span></span>



| <span data-ttu-id="3fef7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fef7-124">Requirement</span></span> | <span data-ttu-id="3fef7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3fef7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3fef7-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fef7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3fef7-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3fef7-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3fef7-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fef7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3fef7-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="3fef7-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





