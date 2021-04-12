---
title: atributo pequeno
description: A palavra-chave Small designa um número inteiro de 8 bits.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- MIDL de atributo pequeno
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364693"
---
# <a name="small-attribute"></a><span data-ttu-id="97b01-104">atributo pequeno</span><span class="sxs-lookup"><span data-stu-id="97b01-104">small attribute</span></span>

<span data-ttu-id="97b01-105">A palavra-chave **Small** designa um número inteiro de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="97b01-105">The **small** keyword designates an 8-bit integer number.</span></span>

``` syntax
small identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="97b01-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97b01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97b01-107">*nome-do-identificador*</span><span class="sxs-lookup"><span data-stu-id="97b01-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="97b01-108">Especifica um identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="97b01-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="97b01-109">Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="97b01-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97b01-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="97b01-110">Remarks</span></span>

<span data-ttu-id="97b01-111">A palavra-chave **Small** pode ser precedida por uma palavra-chave [**assinada**](signed.md) ou pela palavra-chave [**não**](unsigned.md)assinada.</span><span class="sxs-lookup"><span data-stu-id="97b01-111">The **small** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="97b01-112">A palavra-chave [**int**](int.md) é opcional e pode ser omitida.</span><span class="sxs-lookup"><span data-stu-id="97b01-112">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="97b01-113">Para o compilador MIDL, um pequeno inteiro é **assinado** por padrão e é sinônimo de **int pequeno assinado**.</span><span class="sxs-lookup"><span data-stu-id="97b01-113">To the MIDL compiler, a small integer is **signed** by default and is synonymous with **signed small int**.</span></span>

<span data-ttu-id="97b01-114">O tipo inteiro **pequeno** é um dos tipos base da linguagem IDL.</span><span class="sxs-lookup"><span data-stu-id="97b01-114">The **small** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="97b01-115">O tipo inteiro **pequeno** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="97b01-115">The **small** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="97b01-116">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="97b01-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="97b01-117">O sinal do tipo **pequeno** pode ser modificado pela opção de compilador MIDL [**/Char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="97b01-117">The sign of the **small** type can be modified by the MIDL compiler switch [**/char**](-char.md).</span></span> <span data-ttu-id="97b01-118">Para evitar confusão, especifique o sinal do tipo de inteiro com as palavras-chave [**assinadas**](signed.md) e [**não assinadas**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="97b01-118">To avoid confusion, specify the sign of the integer type with the keywords [**signed**](signed.md) and [**unsigned**](unsigned.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="97b01-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="97b01-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b01-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="97b01-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="97b01-121">**const**</span><span class="sxs-lookup"><span data-stu-id="97b01-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="97b01-122">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="97b01-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="97b01-123">**int**</span><span class="sxs-lookup"><span data-stu-id="97b01-123">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="97b01-124">**Longas**</span><span class="sxs-lookup"><span data-stu-id="97b01-124">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="97b01-125">**short**</span><span class="sxs-lookup"><span data-stu-id="97b01-125">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="97b01-126">**inteiro**</span><span class="sxs-lookup"><span data-stu-id="97b01-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="97b01-127">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="97b01-127">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="97b01-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="97b01-128">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




