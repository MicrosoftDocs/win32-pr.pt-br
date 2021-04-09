---
title: Atributo switch_type
description: O atributo \ switch \_ Type \ identifica o tipo da variável usada como discriminante de União. O tipo de opção pode ser um número inteiro, caractere, booliano ou tipo de enumeração.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type do atributo MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823287"
---
# <a name="switch_type-attribute"></a><span data-ttu-id="2f4bf-105">alterar \_ atributo de tipo</span><span class="sxs-lookup"><span data-stu-id="2f4bf-105">switch\_type attribute</span></span>

<span data-ttu-id="2f4bf-106">O atributo **\[ \_ tipo \] de comutador** identifica o tipo da variável usada como discriminante de União.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-106">The **\[switch\_type\]** attribute identifies the type of the variable used as the union discriminant.</span></span> <span data-ttu-id="2f4bf-107">O tipo de opção pode ser um número inteiro, caractere, booliano ou tipo de enumeração.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-107">The switch type can be an integer, character, Boolean, or enumeration type.</span></span>

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a><span data-ttu-id="2f4bf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f4bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f4bf-109">*especificador de tipo de switch*</span><span class="sxs-lookup"><span data-stu-id="2f4bf-109">*switch-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="2f4bf-110">Especifica um tipo [**int**](int.md), [**Char**](char-idl.md), [**Boolean**](boolean.md)ou [**enum**](enum.md) ou um identificador desse tipo.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-110">Specifies an [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md), or [**enum**](enum.md) type, or an identifier of such a type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f4bf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f4bf-111">Remarks</span></span>

<span data-ttu-id="2f4bf-112">Enquanto o atributo de **\[ \_ tipo \] de opção** identifica o tipo de variável, o **\[** atributo [**switch \_ é**](switch-is.md) **\]** especifica o nome do parâmetro que é o discriminante de União.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-112">While the **\[switch\_type\]** attribute identifies the variable type, the **\[**[**switch\_is**](switch-is.md)**\]** attribute specifies the name of the parameter that is the union discriminant.</span></span> <span data-ttu-id="2f4bf-113">O atributo de **\[ \_ tipo \] de comutador** se aplica a parâmetros ou membros de estruturas ou uniões.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-113">The **\[switch\_type\]** attribute applies to parameters or members of structures or unions.</span></span>

<span data-ttu-id="2f4bf-114">A União e seu discriminante devem ser especificados no mesmo nível lógico.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-114">The union and its discriminant must be specified at the same logical level.</span></span> <span data-ttu-id="2f4bf-115">Quando Union é um parâmetro, o discriminante de União deve ser outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-115">When the union is a parameter, the union discriminant must be another parameter.</span></span> <span data-ttu-id="2f4bf-116">Quando Union é um campo de uma estrutura, discriminante deve ser outro campo da estrutura no mesmo nível que o campo Union.</span><span class="sxs-lookup"><span data-stu-id="2f4bf-116">When the union is a field of a structure, the discriminant must be another field of the structure at the same level as the union field.</span></span>

## <a name="examples"></a><span data-ttu-id="2f4bf-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2f4bf-117">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="2f4bf-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f4bf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4bf-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2f4bf-119">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="2f4bf-120">**º**</span><span class="sxs-lookup"><span data-stu-id="2f4bf-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="2f4bf-121">Uniões encapsuladas</span><span class="sxs-lookup"><span data-stu-id="2f4bf-121">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="2f4bf-122">**enumera**</span><span class="sxs-lookup"><span data-stu-id="2f4bf-122">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="2f4bf-123">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="2f4bf-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2f4bf-124">**INT**</span><span class="sxs-lookup"><span data-stu-id="2f4bf-124">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="2f4bf-125">Uniões não encapsuladas</span><span class="sxs-lookup"><span data-stu-id="2f4bf-125">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="2f4bf-126">**switch \_ é**</span><span class="sxs-lookup"><span data-stu-id="2f4bf-126">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="2f4bf-127">**unida**</span><span class="sxs-lookup"><span data-stu-id="2f4bf-127">**union**</span></span>](union.md)
</dt> </dl>

 

 




