---
title: Propriedade String. Content
description: Representa o conteúdo de um recurso de cadeia de caracteres.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Faixa de das propriedades de String. Content do Windows
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763034"
---
# <a name="stringcontent-property"></a><span data-ttu-id="5bbb6-104">Propriedade String. Content</span><span class="sxs-lookup"><span data-stu-id="5bbb6-104">String.Content property</span></span>

<span data-ttu-id="5bbb6-105">Representa o conteúdo de um recurso de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5bbb6-105">Represents the content of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="5bbb6-106">Uso</span><span class="sxs-lookup"><span data-stu-id="5bbb6-106">Usage</span></span>

``` syntax
<String.Content/>
```

## <a name="attributes"></a><span data-ttu-id="5bbb6-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="5bbb6-107">Attributes</span></span>

<span data-ttu-id="5bbb6-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="5bbb6-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5bbb6-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5bbb6-109">Child elements</span></span>

<span data-ttu-id="5bbb6-110">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="5bbb6-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5bbb6-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5bbb6-111">Parent elements</span></span>



| <span data-ttu-id="5bbb6-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="5bbb6-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="5bbb6-113">**Strings**</span><span class="sxs-lookup"><span data-stu-id="5bbb6-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5bbb6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bbb6-114">Remarks</span></span>

<span data-ttu-id="5bbb6-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5bbb6-115">Optional.</span></span>

<span data-ttu-id="5bbb6-116">Pode ocorrer no máximo uma vez para cada elemento de [**cadeia de caracteres**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="5bbb6-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="5bbb6-117">Esse elemento contém um valor do tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="5bbb6-117">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="5bbb6-118">O valor é restrito a uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="5bbb6-118">The value is constrained to a string composed of any sequence of characters, including white space and line-break characters.</span></span>

<span data-ttu-id="5bbb6-119">O comprimento máximo é não associado.</span><span class="sxs-lookup"><span data-stu-id="5bbb6-119">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="5bbb6-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5bbb6-120">Examples</span></span>

<span data-ttu-id="5bbb6-121">O exemplo a seguir demonstra a marcação para um elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma declaração **String. Content** .</span><span class="sxs-lookup"><span data-stu-id="5bbb6-121">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Content** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="5bbb6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bbb6-122">Requirements</span></span>



| <span data-ttu-id="5bbb6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bbb6-123">Requirement</span></span> | <span data-ttu-id="5bbb6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5bbb6-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5bbb6-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bbb6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5bbb6-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5bbb6-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5bbb6-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bbb6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5bbb6-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5bbb6-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





