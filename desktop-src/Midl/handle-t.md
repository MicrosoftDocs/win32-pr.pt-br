---
title: handle_t atributo
description: A \_ palavra-chave t do manipulador declara um objeto para ser do identificador de tipo de identificador primitivo \_ t. Um identificador de associação primitiva é um objeto de dados que pode ser usado pelo aplicativo para representar a associação.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t do atributo MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293955"
---
# <a name="handle_t-attribute"></a><span data-ttu-id="2e676-105">\_atributo t do manipulador</span><span class="sxs-lookup"><span data-stu-id="2e676-105">handle\_t attribute</span></span>

<span data-ttu-id="2e676-106">A palavra-chave **\_ t do manipulador** declara um objeto para ser do identificador de tipo de identificador primitivo **\_ t**.</span><span class="sxs-lookup"><span data-stu-id="2e676-106">The **handle\_t** keyword declares an object to be of the primitive handle type **handle\_t**.</span></span> <span data-ttu-id="2e676-107">Um identificador de associação primitiva é um objeto de dados que pode ser usado pelo aplicativo para representar a associação.</span><span class="sxs-lookup"><span data-stu-id="2e676-107">A primitive binding handle is a data object that can be used by the application to represent the binding.</span></span>

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a><span data-ttu-id="2e676-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e676-108">Parameters</span></span>

<span data-ttu-id="2e676-109">Este atributo não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2e676-109">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e676-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e676-110">Remarks</span></span>

<span data-ttu-id="2e676-111">O **tipo \_ t de identificador** é um dos tipos predefinidos da IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="2e676-111">The **handle\_t** type is one of the predefined types of the interface definition language (IDL).</span></span> <span data-ttu-id="2e676-112">Ele pode aparecer como um especificador de tipo em declarações de [**typedef**](typedef.md) , declarações gerais e declaradores de função (como um especificador de tipo de retorno de função e um especificador de tipo de parâmetro).</span><span class="sxs-lookup"><span data-stu-id="2e676-112">It can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="2e676-113">Para o contexto no qual os especificadores de tipo aparecem, consulte [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="2e676-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="2e676-114">No Microsoft RPC, os parâmetros do tipo **identificador \_ t** só podem ocorrer como **\[** [**em**](in.md) **\]** parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2e676-114">In Microsoft RPC, parameters of type **handle\_t** can occur only as **\[**[**in**](in.md)**\]** parameters.</span></span> <span data-ttu-id="2e676-115">Os identificadores primitivos não podem ter o **\[** atributo [**exclusivo**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2e676-115">Primitive handles cannot have the **\[**[**unique**](unique.md)**\]** or **\[**[**ptr**](ptr.md)**\]** attribute.</span></span>

<span data-ttu-id="2e676-116">Parâmetros do tipo **Handle \_ t** (parâmetros de identificador primitivo) não são transmitidos na rede.</span><span class="sxs-lookup"><span data-stu-id="2e676-116">Parameters of type **handle\_t** (primitive handle parameters) are not transmitted on the network.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e676-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e676-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e676-118">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="2e676-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="2e676-119">Associação e identificadores</span><span class="sxs-lookup"><span data-stu-id="2e676-119">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="2e676-120">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="2e676-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2e676-121">**no**</span><span class="sxs-lookup"><span data-stu-id="2e676-121">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="2e676-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="2e676-122">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="2e676-123">**ptr**</span><span class="sxs-lookup"><span data-stu-id="2e676-123">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="2e676-124">**diferente**</span><span class="sxs-lookup"><span data-stu-id="2e676-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 