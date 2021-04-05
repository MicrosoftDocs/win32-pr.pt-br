---
title: Propriedade Command.Name
description: Representa o nome de um comando.
ms.assetid: 36fb0b93-143f-4706-8c32-e6c818cce16f
keywords:
- Faixa de Command.Name da Propriedade do Windows
topic_type:
- apiref
api_name:
- Command.Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d93b830e29ca271052a4693b00ba64eee94309f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009662"
---
# <a name="commandname-property"></a><span data-ttu-id="5785e-104">Propriedade Command.Name</span><span class="sxs-lookup"><span data-stu-id="5785e-104">Command.Name property</span></span>

<span data-ttu-id="5785e-105">Representa o nome de um comando.</span><span class="sxs-lookup"><span data-stu-id="5785e-105">Represents the name of a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="5785e-106">Uso</span><span class="sxs-lookup"><span data-stu-id="5785e-106">Usage</span></span>

``` syntax
<Command.Name/>
```

## <a name="attributes"></a><span data-ttu-id="5785e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="5785e-107">Attributes</span></span>

<span data-ttu-id="5785e-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="5785e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5785e-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5785e-109">Child elements</span></span>

<span data-ttu-id="5785e-110">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="5785e-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5785e-111">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5785e-111">Parent elements</span></span>



| <span data-ttu-id="5785e-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="5785e-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="5785e-113">**Comando**</span><span class="sxs-lookup"><span data-stu-id="5785e-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5785e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5785e-114">Remarks</span></span>

<span data-ttu-id="5785e-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5785e-115">Optional.</span></span>

<span data-ttu-id="5785e-116">Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="5785e-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="5785e-117">**Command.Name** é referenciado na marcação para associar um comando a um controle por meio do atributo *CommandName* do controle.</span><span class="sxs-lookup"><span data-stu-id="5785e-117">**Command.Name** is referenced in markup to associate a Command with a control through the *CommandName* attribute of the control.</span></span>

<span data-ttu-id="5785e-118">Esse elemento contém um valor do tipo *xs: String*.</span><span class="sxs-lookup"><span data-stu-id="5785e-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="5785e-119">O valor é restrito a uma cadeia de caracteres que consiste em uma letra ou sublinhado seguido por qualquer sequência de letras, dígitos e sublinhados.</span><span class="sxs-lookup"><span data-stu-id="5785e-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="5785e-120">O comprimento máximo é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5785e-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="5785e-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5785e-121">Examples</span></span>

<span data-ttu-id="5785e-122">O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command.Name** .</span><span class="sxs-lookup"><span data-stu-id="5785e-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Name** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5785e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5785e-123">Requirements</span></span>



| <span data-ttu-id="5785e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5785e-124">Requirement</span></span> | <span data-ttu-id="5785e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5785e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5785e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5785e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5785e-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5785e-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5785e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5785e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5785e-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5785e-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





