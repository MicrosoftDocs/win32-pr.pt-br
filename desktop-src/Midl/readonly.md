---
title: atributo readonly
description: O atributo \ ReadOnly \ proíbe a atribuição a uma variável.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- MIDL de atributo ReadOnly
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917255"
---
# <a name="readonly-attribute"></a><span data-ttu-id="d07d5-104">atributo readonly</span><span class="sxs-lookup"><span data-stu-id="d07d5-104">readonly attribute</span></span>

<span data-ttu-id="d07d5-105">O atributo **\[ ReadOnly \]** proíbe a atribuição a uma variável.</span><span class="sxs-lookup"><span data-stu-id="d07d5-105">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span>

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a><span data-ttu-id="d07d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d07d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d07d5-107">*opcional-atributos*</span><span class="sxs-lookup"><span data-stu-id="d07d5-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="d07d5-108">Zero ou mais atributos MIDL.</span><span class="sxs-lookup"><span data-stu-id="d07d5-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="d07d5-109">*tipo de dados*</span><span class="sxs-lookup"><span data-stu-id="d07d5-109">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d07d5-110">O tipo dos dados contidos no *identificador*.</span><span class="sxs-lookup"><span data-stu-id="d07d5-110">The type of the data contained by *identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="d07d5-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="d07d5-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="d07d5-112">Um nome pelo qual o software pode se referir ao local de armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="d07d5-112">A name by which the software can refer to the data storage location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d07d5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d07d5-113">Remarks</span></span>

<span data-ttu-id="d07d5-114">O atributo **\[ ReadOnly \]** proíbe a atribuição a uma variável.</span><span class="sxs-lookup"><span data-stu-id="d07d5-114">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span> <span data-ttu-id="d07d5-115">somente há suporte para **\[ ReadOnly \]** no nível do parâmetro, não no nível do método.</span><span class="sxs-lookup"><span data-stu-id="d07d5-115">**\[readonly\]** is only supported at the parameter level, not at the method level.</span></span>

### <a name="flags"></a><span data-ttu-id="d07d5-116">Flags</span><span class="sxs-lookup"><span data-stu-id="d07d5-116">Flags</span></span>

<span data-ttu-id="d07d5-117">VARFLAG \_ FREADONLY</span><span class="sxs-lookup"><span data-stu-id="d07d5-117">VARFLAG\_FREADONLY</span></span>

## <a name="examples"></a><span data-ttu-id="d07d5-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d07d5-118">Examples</span></span>

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a><span data-ttu-id="d07d5-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d07d5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d07d5-120">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="d07d5-120">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="d07d5-121">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="d07d5-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d07d5-122">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="d07d5-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d07d5-123">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="d07d5-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 