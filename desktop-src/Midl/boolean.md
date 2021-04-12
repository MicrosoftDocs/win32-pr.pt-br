---
title: atributo booliano
description: A palavra-chave booliana indica que a expressão de constante ou de expressões associada ao identificador usa apenas os valores TRUE e FALSE.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- atributo booliano MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364915"
---
# <a name="boolean-attribute"></a><span data-ttu-id="41128-104">atributo booliano</span><span class="sxs-lookup"><span data-stu-id="41128-104">boolean attribute</span></span>

<span data-ttu-id="41128-105">A palavra-chave **booliana** indica que a expressão de constante ou de expressões associada ao identificador usa apenas os valores **true** e **false**.</span><span class="sxs-lookup"><span data-stu-id="41128-105">The keyword **boolean** indicates that the expression or constant expression associated with the identifier takes only the values **TRUE** and **FALSE**.</span></span>

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="41128-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41128-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41128-107">*nome-do-identificador*</span><span class="sxs-lookup"><span data-stu-id="41128-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="41128-108">Especifica um identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="41128-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="41128-109">Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="41128-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41128-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="41128-110">Remarks</span></span>

<span data-ttu-id="41128-111">O tipo **booliano** é um dos tipos base da linguagem IDL.</span><span class="sxs-lookup"><span data-stu-id="41128-111">The **boolean** type is one of the base types of the IDL language.</span></span> <span data-ttu-id="41128-112">O tipo **booliano** pode aparecer como um especificador de tipo em declarações [**const**](const.md) , declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e como um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="41128-112">The **boolean** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="41128-113">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="41128-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="41128-114">O tipo base **booliano** não é compatível com o atributo [**oleautomation**](oleautomation.md) .</span><span class="sxs-lookup"><span data-stu-id="41128-114">The **boolean** base type is not compatible with the [**oleautomation**](oleautomation.md) attribute.</span></span> <span data-ttu-id="41128-115">Use VARIANT \_ bool em suas interfaces compatíveis com a automação.</span><span class="sxs-lookup"><span data-stu-id="41128-115">Use VARIANT\_BOOL in your Automation-compatible interfaces.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="41128-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="41128-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41128-117">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="41128-117">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="41128-118">**const**</span><span class="sxs-lookup"><span data-stu-id="41128-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="41128-119">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="41128-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="41128-120">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="41128-120">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="41128-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="41128-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




