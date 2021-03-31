---
title: Propriedade String. Symbol
description: Representa o nome de um recurso de cadeia de caracteres.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- Faixa de de propriedades do Windows da propriedade String. Symbol
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824208"
---
# <a name="stringsymbol-property"></a><span data-ttu-id="6336f-104">Propriedade String. Symbol</span><span class="sxs-lookup"><span data-stu-id="6336f-104">String.Symbol property</span></span>

<span data-ttu-id="6336f-105">Representa o nome de um recurso de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6336f-105">Represents the name of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="6336f-106">Uso</span><span class="sxs-lookup"><span data-stu-id="6336f-106">Usage</span></span>

``` syntax
<String.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="6336f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="6336f-107">Attributes</span></span>

<span data-ttu-id="6336f-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="6336f-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6336f-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6336f-109">Child elements</span></span>

<span data-ttu-id="6336f-110">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="6336f-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6336f-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6336f-111">Parent elements</span></span>



| <span data-ttu-id="6336f-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="6336f-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="6336f-113">**String**</span><span class="sxs-lookup"><span data-stu-id="6336f-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6336f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6336f-114">Remarks</span></span>

<span data-ttu-id="6336f-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6336f-115">Optional.</span></span>

<span data-ttu-id="6336f-116">Pode ocorrer no máximo uma vez para cada elemento de [**cadeia de caracteres**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="6336f-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="6336f-117">O símbolo é associado a uma definição de cadeia de caracteres no arquivo de cabeçalho da faixa de, por exemplo, `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="6336f-117">The symbol is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="6336f-118">Esse elemento contém um valor do tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="6336f-118">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="6336f-119">O valor é restrito a uma cadeia de caracteres composta de uma letra ou sublinhado seguido por qualquer sequência de letras, dígitos ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="6336f-119">The value is constrained to a string composed of a letter or underscore followed by any sequence of letters, digits, or underscores.</span></span>

<span data-ttu-id="6336f-120">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6336f-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="6336f-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6336f-121">Examples</span></span>

<span data-ttu-id="6336f-122">O exemplo a seguir demonstra a marcação para um elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma declaração **String. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="6336f-122">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Symbol** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="6336f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6336f-123">Requirements</span></span>



| <span data-ttu-id="6336f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6336f-124">Requirement</span></span> | <span data-ttu-id="6336f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6336f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6336f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6336f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6336f-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6336f-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6336f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6336f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6336f-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="6336f-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





