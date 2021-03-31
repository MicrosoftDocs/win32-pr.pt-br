---
title: atributo do Hyper
description: A palavra-chave Hyper indica um inteiro de 64 bits que pode ser declarado como assinado ou não assinado.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- MIDL do atributo do Hyper
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638425"
---
# <a name="hyper-attribute"></a><span data-ttu-id="89603-104">atributo do Hyper</span><span class="sxs-lookup"><span data-stu-id="89603-104">hyper attribute</span></span>

<span data-ttu-id="89603-105">A palavra-chave **Hyper** indica um inteiro de 64 bits que pode ser declarado como assinado ou não assinado.</span><span class="sxs-lookup"><span data-stu-id="89603-105">The keyword **hyper** indicates a 64-bit integer that can be declared as either signed or unsigned.</span></span>

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="89603-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89603-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89603-107">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="89603-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="89603-108">Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="89603-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="89603-109">(Os declaradores de função e as declarações de campo de bits não são permitidas em estruturas que são transmitidas em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="89603-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="89603-110">Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="89603-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89603-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="89603-111">Remarks</span></span>

<span data-ttu-id="89603-112">O tipo de **Hyper** é um dos tipos base da IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="89603-112">The **hyper** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="89603-113">O tipo de **Hyper** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="89603-113">The **hyper** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="89603-114">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="89603-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="89603-115">Para plataformas de 16 bits, o compilador MIDL substitui o Hyper inteiros não assinados por **MIDL \_ uhyper**.</span><span class="sxs-lookup"><span data-stu-id="89603-115">For 16-bit platforms, the MIDL compiler replaces unsigned hyper integers with **MIDL\_uhyper**.</span></span> <span data-ttu-id="89603-116">Isso permite que as interfaces com inteiros de Hyper não assinados sejam definidas em plataformas que não dão suporte diretamente a inteiros de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="89603-116">This allows interfaces with unsigned hyper integers to be defined on platforms that do not directly support 64-bit integers.</span></span> <span data-ttu-id="89603-117">O **MIDL \_ uhyper** é definido nos arquivos de cabeçalho RPC.</span><span class="sxs-lookup"><span data-stu-id="89603-117">**MIDL\_uhyper** is defined in the RPC header files.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="89603-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="89603-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89603-119">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="89603-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="89603-120">**const**</span><span class="sxs-lookup"><span data-stu-id="89603-120">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="89603-121">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="89603-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="89603-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="89603-122">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




