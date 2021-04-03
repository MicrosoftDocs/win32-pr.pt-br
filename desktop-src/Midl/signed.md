---
title: atributo assinado
description: A palavra-chave signed indica que o bit mais significativo de uma variável de inteiro representa um bit de sinal em vez de um bit de dados.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- MIDL de atributo assinado
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823102"
---
# <a name="signed-attribute"></a><span data-ttu-id="ac530-104">atributo assinado</span><span class="sxs-lookup"><span data-stu-id="ac530-104">signed attribute</span></span>

<span data-ttu-id="ac530-105">A palavra-chave **signed** indica que o bit mais significativo de uma variável de inteiro representa um bit de sinal em vez de um bit de dados.</span><span class="sxs-lookup"><span data-stu-id="ac530-105">The **signed** keyword indicates the most significant bit of an integer variable represents a sign bit rather than a data bit.</span></span>

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="ac530-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac530-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac530-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="ac530-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="ac530-108">Pode ser qualquer [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)e [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="ac530-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac530-109">*nome-do-identificador*</span><span class="sxs-lookup"><span data-stu-id="ac530-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ac530-110">Especifica um identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="ac530-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="ac530-111">Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="ac530-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac530-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac530-112">Remarks</span></span>

<span data-ttu-id="ac530-113">Essa palavra-chave é opcional e pode ser usada com qualquer um dos tipos de caractere e inteiro [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)e [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="ac530-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="ac530-114">Opcionalmente, você pode incluir a palavra-chave [**int**](int.md) após os qualificadores de tipo **longo**, **curto** e **pequeno**.</span><span class="sxs-lookup"><span data-stu-id="ac530-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="ac530-115">Quando você usa os tipos [**Char**](char-idl.md), Character e Integer do compilador MIDL que aparecem no arquivo IDL sem palavras-chave de sinal explícitos podem aparecer com as palavras-chave assinadas ou [**não**](unsigned.md) **assinados** no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="ac530-115">When you use the MIDL compiler switch [**char**](char-idl.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the **signed** or [**unsigned**](unsigned.md) keywords in the generated header file.</span></span> <span data-ttu-id="ac530-116">Para evitar confusão, especifique o sinal dos tipos inteiro e de caractere.</span><span class="sxs-lookup"><span data-stu-id="ac530-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac530-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac530-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac530-118">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="ac530-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="ac530-119">**/Char**</span><span class="sxs-lookup"><span data-stu-id="ac530-119">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="ac530-120">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="ac530-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ac530-121">**INT**</span><span class="sxs-lookup"><span data-stu-id="ac530-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="ac530-122">**Longas**</span><span class="sxs-lookup"><span data-stu-id="ac530-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="ac530-123">**short**</span><span class="sxs-lookup"><span data-stu-id="ac530-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="ac530-124">**menores**</span><span class="sxs-lookup"><span data-stu-id="ac530-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="ac530-125">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="ac530-125">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="ac530-126">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="ac530-126">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




