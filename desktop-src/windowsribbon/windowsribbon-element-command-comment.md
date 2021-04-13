---
title: Propriedade Command. Comment
description: Representa um comentário ou uma anotação para um comando.
ms.assetid: 4ac5c7d4-9627-4703-bd3c-594d9497ba24
keywords:
- Faixa de das propriedades do Windows do comando. Comment
topic_type:
- apiref
api_name:
- Command.Comment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7df2131234623dd30fc90339634a932eca5bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369846"
---
# <a name="commandcomment-property"></a><span data-ttu-id="615cb-104">Propriedade Command. Comment</span><span class="sxs-lookup"><span data-stu-id="615cb-104">Command.Comment property</span></span>

<span data-ttu-id="615cb-105">Representa um comentário ou uma anotação para um comando.</span><span class="sxs-lookup"><span data-stu-id="615cb-105">Represents a comment, or annotation, for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="615cb-106">Uso</span><span class="sxs-lookup"><span data-stu-id="615cb-106">Usage</span></span>

``` syntax
<Command.Comment/>
```

## <a name="attributes"></a><span data-ttu-id="615cb-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="615cb-107">Attributes</span></span>

<span data-ttu-id="615cb-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="615cb-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="615cb-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="615cb-109">Child elements</span></span>

<span data-ttu-id="615cb-110">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="615cb-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="615cb-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="615cb-111">Parent elements</span></span>



| <span data-ttu-id="615cb-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="615cb-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="615cb-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="615cb-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="615cb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="615cb-114">Remarks</span></span>

<span data-ttu-id="615cb-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="615cb-115">Optional.</span></span>

<span data-ttu-id="615cb-116">Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="615cb-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="615cb-117">O comentário é associado a uma definição de comando no arquivo de cabeçalho da faixa de, por exemplo, `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="615cb-117">The comment is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="615cb-118">Esse elemento contém um valor do tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="615cb-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="615cb-119">O comprimento máximo é de 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="615cb-119">The maximum length is 250 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="615cb-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="615cb-120">Examples</span></span>

<span data-ttu-id="615cb-121">O exemplo a seguir demonstra a marcação para um elemento de [**comando**](windowsribbon-element-command.md) com uma declaração de **comando. Comment** .</span><span class="sxs-lookup"><span data-stu-id="615cb-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Comment** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="615cb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="615cb-122">Requirements</span></span>



| <span data-ttu-id="615cb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="615cb-123">Requirement</span></span> | <span data-ttu-id="615cb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="615cb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="615cb-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="615cb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="615cb-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="615cb-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="615cb-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="615cb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="615cb-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="615cb-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





