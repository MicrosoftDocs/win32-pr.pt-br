---
title: alterar atributo
description: A palavra-chave switch seleciona o discriminante para uma \_ União encapsulada.
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- alterar atributo MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916777"
---
# <a name="switch-attribute"></a><span data-ttu-id="9bc7c-104">alterar atributo</span><span class="sxs-lookup"><span data-stu-id="9bc7c-104">switch attribute</span></span>

<span data-ttu-id="9bc7c-105">A palavra-chave **switch** seleciona o discriminante para uma [**\_ União encapsulada**](encapsulated-unions.md).</span><span class="sxs-lookup"><span data-stu-id="9bc7c-105">The **switch** keyword selects the discriminant for an [**encapsulated\_union**](encapsulated-unions.md).</span></span>

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a><span data-ttu-id="9bc7c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bc7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bc7c-107">*tipo de opção*</span><span class="sxs-lookup"><span data-stu-id="9bc7c-107">*switch-type*</span></span> 
</dt> <dd>

<span data-ttu-id="9bc7c-108">Especifica um tipo [**int**](int.md), [**Char**](-char.md), [**enum**](enum.md) ou um identificador que resolve para um desses tipos.</span><span class="sxs-lookup"><span data-stu-id="9bc7c-108">Specifies an [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) type, or an identifier that resolves to one of these types.</span></span>

</dd> <dt>

<span data-ttu-id="9bc7c-109">*nome do comutador*</span><span class="sxs-lookup"><span data-stu-id="9bc7c-109">*switch-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9bc7c-110">Especifica o nome da variável do tipo *switch-type* que atua como o discriminante de União.</span><span class="sxs-lookup"><span data-stu-id="9bc7c-110">Specifies the name of the variable of type *switch-type* that acts as the union discriminant.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9bc7c-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9bc7c-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="9bc7c-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bc7c-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc7c-113">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="9bc7c-113">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9bc7c-114">Uniões não encapsuladas</span><span class="sxs-lookup"><span data-stu-id="9bc7c-114">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="9bc7c-115">**switch \_ é**</span><span class="sxs-lookup"><span data-stu-id="9bc7c-115">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="9bc7c-116">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="9bc7c-116">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="9bc7c-117">**unida**</span><span class="sxs-lookup"><span data-stu-id="9bc7c-117">**union**</span></span>](union.md)
</dt> </dl>

 

 




