---
description: A estrutura de FORM_INFO_1 contém informações sobre um formulário de impressão. As informações incluem a origem dos formulários de impressão, seu nome, suas dimensões e as dimensões de sua área imprimível.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: Estrutura de FORM_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772726"
---
# <a name="form_info_1-structure"></a><span data-ttu-id="3a53e-104">Estrutura de FORM_INFO_1</span><span class="sxs-lookup"><span data-stu-id="3a53e-104">FORM_INFO_1 structure</span></span>

<span data-ttu-id="3a53e-105">A estrutura de **FORM_INFO_1** contém informações sobre um formulário de impressão.</span><span class="sxs-lookup"><span data-stu-id="3a53e-105">The **FORM_INFO_1** structure contains information about a print form.</span></span> <span data-ttu-id="3a53e-106">As informações incluem a origem do formulário de impressão, seu nome, suas dimensões e as dimensões de sua área imprimível.</span><span class="sxs-lookup"><span data-stu-id="3a53e-106">The information includes the print form's origin, its name, its dimensions, and the dimensions of its printable area.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a53e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a53e-107">Syntax</span></span>


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a><span data-ttu-id="3a53e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3a53e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3a53e-109">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="3a53e-109">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="3a53e-110">As propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="3a53e-110">The form properties.</span></span> <span data-ttu-id="3a53e-111">Os valores a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="3a53e-111">The following values are defined.</span></span>



| <span data-ttu-id="3a53e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="3a53e-112">Value</span></span>         | <span data-ttu-id="3a53e-113">Significado</span><span class="sxs-lookup"><span data-stu-id="3a53e-113">Meaning</span></span>                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a53e-114">FORM_USER</span><span class="sxs-lookup"><span data-stu-id="3a53e-114">FORM_USER</span></span>    | <span data-ttu-id="3a53e-115">Se esse sinalizador de bit for definido, o formulário terá sido definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3a53e-115">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="3a53e-116">Formulários com esse sinalizador definido são definidos no registro.</span><span class="sxs-lookup"><span data-stu-id="3a53e-116">Forms with this flag set are defined in the registry.</span></span>        |
| <span data-ttu-id="3a53e-117">FORM_BUILTIN</span><span class="sxs-lookup"><span data-stu-id="3a53e-117">FORM_BUILTIN</span></span> | <span data-ttu-id="3a53e-118">Se esse sinalizador de bit estiver definido, o formulário será parte do spooler.</span><span class="sxs-lookup"><span data-stu-id="3a53e-118">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="3a53e-119">As definições de formulário com este sinalizador definido não aparecem no registro.</span><span class="sxs-lookup"><span data-stu-id="3a53e-119">Form definitions with this flag set do not appear in the registry.</span></span> |
| <span data-ttu-id="3a53e-120">FORM_PRINTER</span><span class="sxs-lookup"><span data-stu-id="3a53e-120">FORM_PRINTER</span></span> | <span data-ttu-id="3a53e-121">Se esse sinalizador de bit for definido, o formulário será associado a uma determinada impressora e sua definição aparecerá no registro.</span><span class="sxs-lookup"><span data-stu-id="3a53e-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>          |



 

</dd> <dt>

<span data-ttu-id="3a53e-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="3a53e-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="3a53e-123">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do formulário.</span><span class="sxs-lookup"><span data-stu-id="3a53e-123">Pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="3a53e-124">O nome do formulário não pode exceder 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3a53e-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="3a53e-125">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="3a53e-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="3a53e-126">A largura e a altura, em milésimos de milímetros, do formulário.</span><span class="sxs-lookup"><span data-stu-id="3a53e-126">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> <dt>

<span data-ttu-id="3a53e-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="3a53e-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="3a53e-128">A largura e a altura, em milésimos de milímetros, do formulário.</span><span class="sxs-lookup"><span data-stu-id="3a53e-128">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a53e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a53e-129">Requirements</span></span>



| <span data-ttu-id="3a53e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a53e-130">Requirement</span></span> | <span data-ttu-id="3a53e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3a53e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a53e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a53e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3a53e-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a53e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3a53e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a53e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3a53e-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a53e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3a53e-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3a53e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a53e-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a53e-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3a53e-138">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3a53e-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3a53e-139">**_FORM_INFO_1W** (Unicode) e **_FORM_INFO_1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3a53e-139">**_FORM_INFO_1W** (Unicode) and **_FORM_INFO_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="3a53e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a53e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a53e-141">Impressão</span><span class="sxs-lookup"><span data-stu-id="3a53e-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3a53e-142">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="3a53e-142">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="3a53e-143">**AddFormat**</span><span class="sxs-lookup"><span data-stu-id="3a53e-143">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="3a53e-144">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="3a53e-144">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="3a53e-145">**Formulário**</span><span class="sxs-lookup"><span data-stu-id="3a53e-145">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




