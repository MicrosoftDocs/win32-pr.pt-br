---
title: wchar_t atributo
description: A \_ palavra-chave WCHAR t designa um tipo de caractere largo.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t do atributo MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2020
ms.locfileid: "104007204"
---
# <a name="wchar_t-attribute"></a><span data-ttu-id="5dae6-104">atributo do WCHAR \_ t</span><span class="sxs-lookup"><span data-stu-id="5dae6-104">wchar\_t attribute</span></span>

<span data-ttu-id="5dae6-105">A palavra-chave **WCHAR \_ t** designa um tipo de caractere largo.</span><span class="sxs-lookup"><span data-stu-id="5dae6-105">The **wchar\_t** keyword designates a wide-character type.</span></span>

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="5dae6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5dae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dae6-107">*nome-do-identificador*</span><span class="sxs-lookup"><span data-stu-id="5dae6-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5dae6-108">Especifica um identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="5dae6-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="5dae6-109">Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="5dae6-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dae6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dae6-110">Remarks</span></span>

<span data-ttu-id="5dae6-111">O tipo **WCHAR \_ t** é definido pelo MIDL como um objeto de dados [**curto**](short.md) [**não assinado**](unsigned.md) (16 bits).</span><span class="sxs-lookup"><span data-stu-id="5dae6-111">The **wchar\_t** type is defined by MIDL as an [**unsigned**](unsigned.md) [**short**](short.md) (16-bit) data object.</span></span>

<span data-ttu-id="5dae6-112">O compilador MIDL permite redefinição de **WCHAR \_ t**, mas somente se for consistente com a definição anterior.</span><span class="sxs-lookup"><span data-stu-id="5dae6-112">The MIDL compiler allows redefinition of **wchar\_t**, but only if it is consistent with the preceding definition.</span></span>

<span data-ttu-id="5dae6-113">O tipo de caractere largo é um dos tipos predefinidos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="5dae6-113">The wide-character type is one of the predefined types of MIDL.</span></span> <span data-ttu-id="5dae6-114">O tipo de caractere largo pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="5dae6-114">The wide-character type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="5dae6-115">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="5dae6-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="5dae6-116">O atributo de **\[ cadeia de caracteres \]** pode ser aplicado a um ponteiro ou matriz do tipo **WCHAR \_ t**.</span><span class="sxs-lookup"><span data-stu-id="5dae6-116">The **\[string\]** attribute can be applied to a pointer or array of type **wchar\_t**.</span></span>

<span data-ttu-id="5dae6-117">Use o caractere **L** antes de um caractere ou uma constante de cadeia de caracteres para designar a constante de tipo de caractere largo.</span><span class="sxs-lookup"><span data-stu-id="5dae6-117">Use the **L** character before a character or a string constant to designate the wide character type constant.</span></span>

## <a name="see-also"></a><span data-ttu-id="5dae6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dae6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dae6-119">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="5dae6-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="5dae6-120">**char**</span><span class="sxs-lookup"><span data-stu-id="5dae6-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="5dae6-121">**const**</span><span class="sxs-lookup"><span data-stu-id="5dae6-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="5dae6-122">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="5dae6-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5dae6-123">**short**</span><span class="sxs-lookup"><span data-stu-id="5dae6-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="5dae6-124">**typedef**</span><span class="sxs-lookup"><span data-stu-id="5dae6-124">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="5dae6-125">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="5dae6-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




