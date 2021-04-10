---
title: atributo curto
description: A palavra-chave Short designa um inteiro de 16 bits.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- MIDL de atributo curto
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293260"
---
# <a name="short-attribute"></a><span data-ttu-id="e3fb2-104">atributo curto</span><span class="sxs-lookup"><span data-stu-id="e3fb2-104">short attribute</span></span>

<span data-ttu-id="e3fb2-105">A palavra-chave **Short** designa um inteiro de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-105">The **short** keyword designates a 16-bit integer.</span></span>

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="e3fb2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3fb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3fb2-107">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="e3fb2-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e3fb2-108">Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e3fb2-109">(Os declaradores de função e as declarações de campo de bits não são permitidas em estruturas que são transmitidas em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="e3fb2-110">Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3fb2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3fb2-111">Remarks</span></span>

<span data-ttu-id="e3fb2-112">A palavra-chave **Short** pode ser precedida por uma palavra-chave [**assinada**](signed.md) ou pela palavra-chave [**não**](unsigned.md)assinada.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-112">The **short** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="e3fb2-113">A palavra-chave [**int**](int.md) é opcional e pode ser omitida.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="e3fb2-114">Para o compilador MIDL, um inteiro curto é assinado por padrão e é sinônimo de **int-Short assinado**.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-114">To the MIDL compiler, a short integer is signed by default and is synonymous with **signed short int**.</span></span>

<span data-ttu-id="e3fb2-115">O tipo inteiro **curto** é um dos tipos base da linguagem IDL.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-115">The **short** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="e3fb2-116">O tipo inteiro **curto** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="e3fb2-116">The **short** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="e3fb2-117">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="e3fb2-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e3fb2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3fb2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3fb2-119">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="e3fb2-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e3fb2-120">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="e3fb2-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e3fb2-121">**int**</span><span class="sxs-lookup"><span data-stu-id="e3fb2-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="e3fb2-122">**Longas**</span><span class="sxs-lookup"><span data-stu-id="e3fb2-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="e3fb2-123">**inteiro**</span><span class="sxs-lookup"><span data-stu-id="e3fb2-123">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="e3fb2-124">**menores**</span><span class="sxs-lookup"><span data-stu-id="e3fb2-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="e3fb2-125">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="e3fb2-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




