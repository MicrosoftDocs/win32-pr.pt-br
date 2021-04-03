---
title: atributo Char
description: A palavra-chave Char especifica um item de dados de 8 bits.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- atributo Char MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823356"
---
# <a name="char-attribute"></a><span data-ttu-id="b2088-104">atributo Char</span><span class="sxs-lookup"><span data-stu-id="b2088-104">char attribute</span></span>

<span data-ttu-id="b2088-105">A palavra-chave **Char** especifica um item de dados de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="b2088-105">The **char** keyword specifies an 8-bit data item.</span></span>

``` syntax
char identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="b2088-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2088-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2088-107">*nome-do-identificador*</span><span class="sxs-lookup"><span data-stu-id="b2088-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b2088-108">Especifica um identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="b2088-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="b2088-109">Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="b2088-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2088-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2088-110">Remarks</span></span>

<span data-ttu-id="b2088-111">A palavra-chave **Char** identifica um item de dados que tem 8 bits.</span><span class="sxs-lookup"><span data-stu-id="b2088-111">The keyword **char** identifies a data item that has 8 bits.</span></span> <span data-ttu-id="b2088-112">Para o compilador MIDL, um **Char** não é assinado por padrão e é sinônimo de **Char** [**não assinado**](unsigned.md) .</span><span class="sxs-lookup"><span data-stu-id="b2088-112">To the MIDL compiler, a **char** is unsigned by default and is synonymous with [**unsigned**](unsigned.md) **char**.</span></span>

<span data-ttu-id="b2088-113">Nesta versão do Microsoft RPC, as tabelas de conversão de caracteres que convertem entre ASCII e EBCDIC são criadas nas bibliotecas de tempo de execução e não podem ser alteradas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b2088-113">In this version of Microsoft RPC, the character translation tables that convert between ASCII and EBCDIC are built into the run-time libraries and cannot be changed by the user.</span></span>

<span data-ttu-id="b2088-114">O tipo **Char** é um dos tipos base da IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="b2088-114">The **char** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="b2088-115">O tipo **Char** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="b2088-115">The **char** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="b2088-116">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="b2088-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="b2088-117">Os compiladores de IDL do DCE não aceitam a palavra-chave [**assinaled**](signed.md) aplicada a tipos de **caracteres** .</span><span class="sxs-lookup"><span data-stu-id="b2088-117">DCE IDL compilers do not accept the keyword [**signed**](signed.md) applied to **char** types.</span></span> <span data-ttu-id="b2088-118">Portanto, esse recurso não está disponível quando você usa a opção [**/OSF**](-osf.md) do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="b2088-118">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2088-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2088-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2088-120">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="b2088-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="b2088-121">**minuciosa**</span><span class="sxs-lookup"><span data-stu-id="b2088-121">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="b2088-122">**/Char**</span><span class="sxs-lookup"><span data-stu-id="b2088-122">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="b2088-123">**const**</span><span class="sxs-lookup"><span data-stu-id="b2088-123">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="b2088-124">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="b2088-124">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b2088-125">**/osf**</span><span class="sxs-lookup"><span data-stu-id="b2088-125">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="b2088-126">**inteiro**</span><span class="sxs-lookup"><span data-stu-id="b2088-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="b2088-127">**Strings**</span><span class="sxs-lookup"><span data-stu-id="b2088-127">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="b2088-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="b2088-128">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="b2088-129">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="b2088-129">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="b2088-130">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="b2088-130">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




