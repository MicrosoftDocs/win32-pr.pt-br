---
title: atributo longo
description: A palavra-chave Long designa um inteiro de 32 bits.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- MIDL de atributo longo
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916721"
---
# <a name="long-attribute"></a><span data-ttu-id="1a9ad-104">atributo longo</span><span class="sxs-lookup"><span data-stu-id="1a9ad-104">long attribute</span></span>

<span data-ttu-id="1a9ad-105">A palavra-chave **Long** designa um inteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-105">The **long** keyword designates a 32-bit integer.</span></span>

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="1a9ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a9ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a9ad-107">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="1a9ad-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1a9ad-108">Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="1a9ad-109">(Os declaradores de função e as declarações de campo de bits não são permitidas em estruturas que são transmitidas em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="1a9ad-110">Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a9ad-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a9ad-111">Remarks</span></span>

<span data-ttu-id="1a9ad-112">A palavra-chave **Long** pode ser precedida por uma palavra-chave [**assinada**](signed.md) ou pela palavra-chave [**não**](unsigned.md)assinada.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-112">The **long** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="1a9ad-113">A palavra-chave [**int**](int.md) é opcional e pode ser omitida.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="1a9ad-114">Para o compilador MIDL, um inteiro longo é assinado por padrão e é sinônimo de **int Long assinado**. Em plataformas de 32 bits, **Long** é sinônimo de **int**.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-114">To the MIDL compiler, a long integer is signed by default and is synonymous with **signed long int**. On 32-bit platforms, **long** is synonymous with **int**.</span></span>

<span data-ttu-id="1a9ad-115">O tipo inteiro **longo** é um dos tipos base da linguagem IDL.</span><span class="sxs-lookup"><span data-stu-id="1a9ad-115">The **long** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="1a9ad-116">O tipo inteiro **longo** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="1a9ad-116">The **long** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="1a9ad-117">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="1a9ad-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a9ad-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a9ad-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a9ad-119">**const**</span><span class="sxs-lookup"><span data-stu-id="1a9ad-119">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="1a9ad-120">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="1a9ad-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="1a9ad-121">**Hyper**</span><span class="sxs-lookup"><span data-stu-id="1a9ad-121">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="1a9ad-122">**INT**</span><span class="sxs-lookup"><span data-stu-id="1a9ad-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="1a9ad-123">**short**</span><span class="sxs-lookup"><span data-stu-id="1a9ad-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="1a9ad-124">**inteiro**</span><span class="sxs-lookup"><span data-stu-id="1a9ad-124">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="1a9ad-125">**menores**</span><span class="sxs-lookup"><span data-stu-id="1a9ad-125">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="1a9ad-126">**typedef**</span><span class="sxs-lookup"><span data-stu-id="1a9ad-126">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="1a9ad-127">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="1a9ad-127">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




