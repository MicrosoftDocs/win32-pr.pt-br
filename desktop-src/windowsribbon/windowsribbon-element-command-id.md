---
title: Propriedade Command.Id
description: Representa uma ID exclusiva para um comando.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Faixa de Command.Id da Propriedade do Windows
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e259e5fd74e3037afde3d4c001000b5a17a9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455787"
---
# <a name="commandid-property"></a><span data-ttu-id="bc523-104">Propriedade Command.Id</span><span class="sxs-lookup"><span data-stu-id="bc523-104">Command.Id property</span></span>

<span data-ttu-id="bc523-105">Representa uma ID exclusiva para um comando.</span><span class="sxs-lookup"><span data-stu-id="bc523-105">Represents a unique ID for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="bc523-106">Uso</span><span class="sxs-lookup"><span data-stu-id="bc523-106">Usage</span></span>

``` syntax
<Command.Id/>
```

## <a name="attributes"></a><span data-ttu-id="bc523-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="bc523-107">Attributes</span></span>

<span data-ttu-id="bc523-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="bc523-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bc523-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bc523-109">Child elements</span></span>

<span data-ttu-id="bc523-110">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="bc523-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="bc523-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="bc523-111">Parent elements</span></span>



| <span data-ttu-id="bc523-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="bc523-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="bc523-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="bc523-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bc523-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc523-114">Remarks</span></span>

<span data-ttu-id="bc523-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bc523-115">Optional.</span></span>

<span data-ttu-id="bc523-116">Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="bc523-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="bc523-117">A ID é associada a uma definição de comando no arquivo de cabeçalho da faixa de, por exemplo, `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="bc523-117">The ID is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="bc523-118">Esse elemento contém um valor da União de tipos *xs: positiveInteger* e *xs: String* restrito a um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive.</span><span class="sxs-lookup"><span data-stu-id="bc523-118">This element contains a value from the union of types *xs:positiveInteger* and *xs:string* constrained to an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="bc523-119">O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais.</span><span class="sxs-lookup"><span data-stu-id="bc523-119">The maximum length is 10 characters, including optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="bc523-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc523-120">Examples</span></span>

<span data-ttu-id="bc523-121">O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command.ID** .</span><span class="sxs-lookup"><span data-stu-id="bc523-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Id** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bc523-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc523-122">Requirements</span></span>



| <span data-ttu-id="bc523-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc523-123">Requirement</span></span> | <span data-ttu-id="bc523-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bc523-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bc523-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc523-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bc523-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bc523-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bc523-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc523-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bc523-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="bc523-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





