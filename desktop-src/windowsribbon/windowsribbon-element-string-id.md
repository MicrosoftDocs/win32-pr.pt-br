---
title: Propriedade String.Id
description: Representa a ID exclusiva de um recurso de cadeia de caracteres.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Faixa de String.Id da Propriedade do Windows
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086203"
---
# <a name="stringid-property"></a><span data-ttu-id="04bbc-104">Propriedade String.Id</span><span class="sxs-lookup"><span data-stu-id="04bbc-104">String.Id property</span></span>

<span data-ttu-id="04bbc-105">Representa a ID exclusiva de um recurso de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="04bbc-105">Represents the unique ID of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="04bbc-106">Uso</span><span class="sxs-lookup"><span data-stu-id="04bbc-106">Usage</span></span>

``` syntax
<String.Id/>
```

## <a name="attributes"></a><span data-ttu-id="04bbc-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="04bbc-107">Attributes</span></span>

<span data-ttu-id="04bbc-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="04bbc-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="04bbc-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="04bbc-109">Child elements</span></span>

<span data-ttu-id="04bbc-110">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="04bbc-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="04bbc-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="04bbc-111">Parent elements</span></span>



| <span data-ttu-id="04bbc-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="04bbc-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="04bbc-113">**Strings**</span><span class="sxs-lookup"><span data-stu-id="04bbc-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="04bbc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="04bbc-114">Remarks</span></span>

<span data-ttu-id="04bbc-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="04bbc-115">Optional.</span></span>

<span data-ttu-id="04bbc-116">Pode ocorrer no máximo uma vez para cada elemento de [**cadeia de caracteres**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="04bbc-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="04bbc-117">O valor de **String.ID** deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="04bbc-117">The value for **String.Id** must be unique.</span></span>

<span data-ttu-id="04bbc-118">A ID é associada a uma definição de cadeia de caracteres no arquivo de cabeçalho da faixa de, por exemplo, `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="04bbc-118">The ID is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="04bbc-119">Esse elemento contém um valor da União de tipos *xs: positiveInteger* e *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="04bbc-119">This element contains a value from the union of types *xs:positiveInteger* and *xs:string*.</span></span> <span data-ttu-id="04bbc-120">O valor é restrito a um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="04bbc-120">The value is constrained to a integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="04bbc-121">O comprimento máximo é de 10 caracteres com zeros à esquerda opcionais.</span><span class="sxs-lookup"><span data-stu-id="04bbc-121">The maximum length is 10 characters with optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="04bbc-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="04bbc-122">Examples</span></span>

<span data-ttu-id="04bbc-123">O exemplo a seguir demonstra a marcação para um elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma declaração **String.ID** .</span><span class="sxs-lookup"><span data-stu-id="04bbc-123">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Id** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="04bbc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04bbc-124">Requirements</span></span>



| <span data-ttu-id="04bbc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="04bbc-125">Requirement</span></span> | <span data-ttu-id="04bbc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="04bbc-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="04bbc-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04bbc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="04bbc-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="04bbc-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="04bbc-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04bbc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="04bbc-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="04bbc-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





