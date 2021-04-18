---
title: atributo de byte
description: A palavra-chave byte Especifica um item de dados de 8 bits.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- MIDL de atributo de byte
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105751865"
---
# <a name="byte-attribute"></a><span data-ttu-id="17960-104">atributo de byte</span><span class="sxs-lookup"><span data-stu-id="17960-104">byte attribute</span></span>

<span data-ttu-id="17960-105">A palavra-chave **byte** especifica um item de dados de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="17960-105">The **byte** keyword specifies an 8-bit data item.</span></span>

``` syntax
byte identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="17960-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17960-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17960-107">*nome-do-identificador*</span><span class="sxs-lookup"><span data-stu-id="17960-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="17960-108">Especifica um identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="17960-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="17960-109">Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="17960-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17960-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="17960-110">Remarks</span></span>

<span data-ttu-id="17960-111">Um item de dados de **byte** não passa por nenhuma conversão para transmissão na rede, uma vez que um tipo de [**caractere**](char-idl.md) pode.</span><span class="sxs-lookup"><span data-stu-id="17960-111">A **byte** data item does not undergo any conversion for transmission on the network as a [**char**](char-idl.md) type might.</span></span>

<span data-ttu-id="17960-112">O tipo de **byte** é um dos tipos base da IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="17960-112">The **byte** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="17960-113">O tipo de **byte** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="17960-113">The **byte** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="17960-114">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="17960-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="17960-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="17960-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17960-116">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="17960-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="17960-117">**char**</span><span class="sxs-lookup"><span data-stu-id="17960-117">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="17960-118">**const**</span><span class="sxs-lookup"><span data-stu-id="17960-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="17960-119">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="17960-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="17960-120">**typedef**</span><span class="sxs-lookup"><span data-stu-id="17960-120">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




