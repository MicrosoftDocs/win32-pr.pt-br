---
title: atributo int
description: A palavra-chave int especifica um número inteiro com sinal de 32 bits em plataformas de 32 bits. Em plataformas de 16 bits, a palavra-chave int é uma palavra-chave opcional que pode acompanhar as palavras-chaves pequenas, curtas e longas.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- atributo int MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638423"
---
# <a name="int-attribute"></a><span data-ttu-id="2c468-105">atributo int</span><span class="sxs-lookup"><span data-stu-id="2c468-105">int attribute</span></span>

<span data-ttu-id="2c468-106">A palavra-chave **int** especifica um número inteiro com sinal de 32 bits em plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2c468-106">The keyword **int** specifies a 32-bit signed integer on 32-bit platforms.</span></span> <span data-ttu-id="2c468-107">Em plataformas de 16 bits, a palavra-chave **int** é uma palavra-chave opcional que pode acompanhar as palavras-chaves [**pequenas**](small.md), [**curtas**](short.md)e [**longas**](long.md).</span><span class="sxs-lookup"><span data-stu-id="2c468-107">On 16-bit platforms, the keyword **int** is an optional keyword that can accompany the keywords [**small**](small.md), [**short**](short.md), and [**long**](long.md).</span></span>

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="2c468-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c468-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c468-109">*modificador de número inteiro*</span><span class="sxs-lookup"><span data-stu-id="2c468-109">*integer-modifier*</span></span> 
</dt> <dd>

<span data-ttu-id="2c468-110">Especifica a palavra-chave [**Small**](small.md), [**Short**](short.md), [**Long**](long.md), [**Hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)ou [**\_ \_ Int64**](--int64.md), que seleciona o tamanho dos dados inteiros.</span><span class="sxs-lookup"><span data-stu-id="2c468-110">Specifies the keyword [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_\_int3264**](--int3264.md), or [**\_\_int64**](--int64.md),which selects the size of the integer data.</span></span> <span data-ttu-id="2c468-111">Em plataformas de 16 bits, o qualificador de tamanho deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="2c468-111">On 16-bit platforms, the size qualifier must be present.</span></span>

</dd> <dt>

<span data-ttu-id="2c468-112">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="2c468-112">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2c468-113">Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="2c468-113">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="2c468-114">(Os declaradores de função e as declarações de campo de bits não são permitidas em estruturas que são transmitidas em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="2c468-114">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="2c468-115">Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="2c468-115">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c468-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c468-116">Remarks</span></span>

<span data-ttu-id="2c468-117">Os tipos de inteiros estão entre os tipos base da IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="2c468-117">Integer types are among the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="2c468-118">Eles podem aparecer como especificadores de tipo em declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="2c468-118">They can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="2c468-119">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="2c468-119">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="2c468-120">Se nenhuma especificação de sinal de inteiro for fornecida, o tipo de inteiro padrão será [**assinado**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="2c468-120">If no integer sign specification is provided, the integer type defaults to [**signed**](signed.md).</span></span>

<span data-ttu-id="2c468-121">Os compiladores de IDL do DCE não permitem que a palavra-chave seja [**assinada**](signed.md) para especificar o sinal dos tipos inteiros.</span><span class="sxs-lookup"><span data-stu-id="2c468-121">DCE IDL compilers do not allow the keyword [**signed**](signed.md) to specify the sign of integer types.</span></span> <span data-ttu-id="2c468-122">Portanto, esse recurso não está disponível quando você usa a opção [**/OSF**](-osf.md) do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="2c468-122">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="2c468-123">A Microsoft não recomenda o uso do \_ \_ int3264 para comunicação remota se puder ser evitada.</span><span class="sxs-lookup"><span data-stu-id="2c468-123">Microsoft does not recommend the use of \_\_int3264 for remoting if it can be avoided.</span></span> <span data-ttu-id="2c468-124">Consulte o tópico em [**\_ \_ int3264**](--int3264.md) para obter mais informações sobre o uso e as limitações dele.</span><span class="sxs-lookup"><span data-stu-id="2c468-124">Please see the topic on [**\_\_int3264**](--int3264.md) for more information regarding it's use and limitations.</span></span>

## <a name="examples"></a><span data-ttu-id="2c468-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c468-125">Examples</span></span>

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a><span data-ttu-id="2c468-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c468-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c468-127">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="2c468-127">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="2c468-128">**enumera**</span><span class="sxs-lookup"><span data-stu-id="2c468-128">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="2c468-129">**Hyper**</span><span class="sxs-lookup"><span data-stu-id="2c468-129">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="2c468-130">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="2c468-130">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2c468-131">**Longas**</span><span class="sxs-lookup"><span data-stu-id="2c468-131">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="2c468-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="2c468-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="2c468-133">**short**</span><span class="sxs-lookup"><span data-stu-id="2c468-133">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="2c468-134">**inteiro**</span><span class="sxs-lookup"><span data-stu-id="2c468-134">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="2c468-135">**menores**</span><span class="sxs-lookup"><span data-stu-id="2c468-135">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="2c468-136">**struct**</span><span class="sxs-lookup"><span data-stu-id="2c468-136">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="2c468-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="2c468-137">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="2c468-138">**unida**</span><span class="sxs-lookup"><span data-stu-id="2c468-138">**union**</span></span>](union.md)
</dt> </dl>

 

 




