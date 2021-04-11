---
title: atributo de enumeração
description: A palavra-chave enum identifica um tipo enumerado.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- atributo de enumeração MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293086"
---
# <a name="enum-attribute"></a><span data-ttu-id="5c54c-104">atributo de enumeração</span><span class="sxs-lookup"><span data-stu-id="5c54c-104">enum attribute</span></span>

<span data-ttu-id="5c54c-105">A palavra-chave **enum** identifica um tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="5c54c-105">The keyword **enum** identifies an enumerated type.</span></span>

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a><span data-ttu-id="5c54c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c54c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c54c-107">*Tags*</span><span class="sxs-lookup"><span data-stu-id="5c54c-107">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="5c54c-108">Especifica uma marca opcional para o tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="5c54c-108">Specifies an optional tag for the enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="5c54c-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="5c54c-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="5c54c-110">Especifica a enumeração específica.</span><span class="sxs-lookup"><span data-stu-id="5c54c-110">Specifies the particular enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="5c54c-111">*valor inteiro*</span><span class="sxs-lookup"><span data-stu-id="5c54c-111">*integer-value*</span></span> 
</dt> <dd>

<span data-ttu-id="5c54c-112">Especifica um valor inteiro constante.</span><span class="sxs-lookup"><span data-stu-id="5c54c-112">Specifies a constant integer value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c54c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c54c-113">Remarks</span></span>

<span data-ttu-id="5c54c-114">os tipos de **Enumeração** podem aparecer como especificadores de tipo em declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como o tipo de retorno de função ou como um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="5c54c-114">**enum** types can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (either as the function-return-type or as a parameter-type specifier).</span></span> <span data-ttu-id="5c54c-115">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="5c54c-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="5c54c-116">No modo padrão do compilador de MIDL, você pode atribuir valores inteiros a enumeradores.</span><span class="sxs-lookup"><span data-stu-id="5c54c-116">In the MIDL compiler's default mode, you can assign integer values to enumerators.</span></span> <span data-ttu-id="5c54c-117">(Esse recurso não está disponível quando você compila com o comutador [**/OSF**](-osf.md) .) Assim como acontece com enumeradores de linguagem C, os nomes de enumeradores devem ser exclusivos, mas os valores do enumerador não precisam ser.</span><span class="sxs-lookup"><span data-stu-id="5c54c-117">(This feature is not available when you compile with the [**/osf**](-osf.md) switch.) As with C-language enumerators, enumerator names must be unique, but the enumerator values need not be.</span></span>

<span data-ttu-id="5c54c-118">Quando os operadores de atribuição não são fornecidos, os identificadores são mapeados para inteiros consecutivos da esquerda para a direita, começando com zero.</span><span class="sxs-lookup"><span data-stu-id="5c54c-118">When assignment operators are not provided, identifiers are mapped to consecutive integers from left to right, starting with zero.</span></span> <span data-ttu-id="5c54c-119">Quando operadores de atribuição são fornecidos, os valores atribuídos começam do valor atribuído mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="5c54c-119">When assignment operators are provided, assigned values start from the most recently assigned value.</span></span>

<span data-ttu-id="5c54c-120">O número máximo de identificadores é 65.535.</span><span class="sxs-lookup"><span data-stu-id="5c54c-120">The maximum number of identifiers is 65,535.</span></span>

<span data-ttu-id="5c54c-121">Objetos do tipo **enum** são tipos [**int**](int.md) , e seu tamanho depende do sistema.</span><span class="sxs-lookup"><span data-stu-id="5c54c-121">Objects of type **enum** are [**int**](int.md) types, and their size is system-dependent.</span></span> <span data-ttu-id="5c54c-122">Por padrão, os objetos de tipos **enum** são tratados como objetos de 16 bits do tipo [**sem sinal**](unsigned.md) [**curto**](short.md) quando transmitidos por uma rede.</span><span class="sxs-lookup"><span data-stu-id="5c54c-122">By default, objects of **enum** types are treated as 16-bit objects of type [**unsigned**](unsigned.md) [**short**](short.md) when transmitted over a network.</span></span> <span data-ttu-id="5c54c-123">Os valores fora do intervalo 0-32.767 causam o \_ valor de enumeração RPC X da exceção \_ de tempo de execução \_ \_ fora \_ do \_ intervalo.</span><span class="sxs-lookup"><span data-stu-id="5c54c-123">Values outside the range 0 - 32,767 cause the run-time exception RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="5c54c-124">Para transmitir objetos como entidades de 32 bits, aplique o **\[** atributo de [**\_ Enumeração v1**](v1-enum.md) **\]** ao typedef de **Enumeração** .</span><span class="sxs-lookup"><span data-stu-id="5c54c-124">To transmit objects as 32-bit entities, apply the **\[**[**v1\_enum**](v1-enum.md)**\]** attribute to the **enum** typedef.</span></span>

## <a name="examples"></a><span data-ttu-id="5c54c-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c54c-125">Examples</span></span>

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a><span data-ttu-id="5c54c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c54c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c54c-127">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="5c54c-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="5c54c-128">**int**</span><span class="sxs-lookup"><span data-stu-id="5c54c-128">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="5c54c-129">**short**</span><span class="sxs-lookup"><span data-stu-id="5c54c-129">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="5c54c-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="5c54c-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="5c54c-131">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="5c54c-131">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="5c54c-132">**\_Enumeração v1**</span><span class="sxs-lookup"><span data-stu-id="5c54c-132">**v1\_enum**</span></span>](v1-enum.md)
</dt> </dl>

 

 




