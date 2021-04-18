---
title: atributo não assinado
description: A palavra-chave não assinada indica que o bit mais significativo de uma variável de inteiro representa um bit de dados em vez de um bit assinado.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- atributo não assinado MIDL
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105757134"
---
# <a name="unsigned-attribute"></a><span data-ttu-id="73ab5-104">atributo não assinado</span><span class="sxs-lookup"><span data-stu-id="73ab5-104">unsigned attribute</span></span>

<span data-ttu-id="73ab5-105">A palavra-chave **não assinada** indica que o bit mais significativo de uma variável de inteiro representa um bit de dados em vez de um bit assinado.</span><span class="sxs-lookup"><span data-stu-id="73ab5-105">The **unsigned** keyword indicates that the most significant bit of an integer variable represents a data bit rather than a signed bit.</span></span>

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="73ab5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73ab5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ab5-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="73ab5-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="73ab5-108">Pode ser qualquer [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**int**](int.md), [**Short**](short.md)e [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="73ab5-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="73ab5-109">*nome-do-identificador*</span><span class="sxs-lookup"><span data-stu-id="73ab5-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="73ab5-110">Especifica um identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="73ab5-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="73ab5-111">Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="73ab5-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73ab5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="73ab5-112">Remarks</span></span>

<span data-ttu-id="73ab5-113">Essa palavra-chave é opcional e pode ser usada com qualquer um dos tipos de caractere e inteiro [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)e [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="73ab5-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="73ab5-114">Opcionalmente, você pode incluir a palavra-chave [**int**](int.md) após os qualificadores de tipo **longo**, **curto** e **pequeno**.</span><span class="sxs-lookup"><span data-stu-id="73ab5-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="73ab5-115">Quando você usa o [**/Char**](-char.md)do compilador de MIDL, os tipos de caractere e inteiro que aparecem no arquivo IDL sem palavras-chave de sinal explícitos podem aparecer com a palavra-chave [**assinada**](signed.md) ou **não** assinado no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="73ab5-115">When you use the MIDL compiler switch [**/char**](-char.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the [**signed**](signed.md) or **unsigned** keyword in the generated header file.</span></span> <span data-ttu-id="73ab5-116">Para evitar confusão, especifique o sinal dos tipos inteiro e de caractere.</span><span class="sxs-lookup"><span data-stu-id="73ab5-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="73ab5-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="73ab5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ab5-118">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="73ab5-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="73ab5-119">**char**</span><span class="sxs-lookup"><span data-stu-id="73ab5-119">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="73ab5-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="73ab5-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="73ab5-121">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="73ab5-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="73ab5-122">**int**</span><span class="sxs-lookup"><span data-stu-id="73ab5-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="73ab5-123">**Longas**</span><span class="sxs-lookup"><span data-stu-id="73ab5-123">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="73ab5-124">**short**</span><span class="sxs-lookup"><span data-stu-id="73ab5-124">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="73ab5-125">**inteiro**</span><span class="sxs-lookup"><span data-stu-id="73ab5-125">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="73ab5-126">**menores**</span><span class="sxs-lookup"><span data-stu-id="73ab5-126">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="73ab5-127">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="73ab5-127">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




