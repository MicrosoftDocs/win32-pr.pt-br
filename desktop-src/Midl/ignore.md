---
title: ignorar atributo
description: O atributo \ ignore \ designa que um ponteiro contido em uma estrutura ou União e o objeto indicado pelo ponteiro não são transmitidos. O atributo \ ignore \ é restrito a membros de ponteiros de estruturas ou uniões.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- ignorar atributo MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823702"
---
# <a name="ignore-attribute"></a><span data-ttu-id="ab7c7-105">ignorar atributo</span><span class="sxs-lookup"><span data-stu-id="ab7c7-105">ignore attribute</span></span>

<span data-ttu-id="ab7c7-106">O atributo **\[ ignore \]** designa que um ponteiro contido em uma estrutura ou União e o objeto indicado pelo ponteiro não são transmitidos.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-106">The **\[ignore\]** attribute designates that a pointer contained in a structure or union and the object indicated by the pointer is not transmitted.</span></span> <span data-ttu-id="ab7c7-107">O atributo **\[ ignore \]** é restrito a membros de ponteiros de estruturas ou uniões.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-107">The **\[ignore\]** attribute is restricted to pointer members of structures or unions.</span></span>

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a><span data-ttu-id="ab7c7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab7c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab7c7-109">*ponteiro-tipo de membro*</span><span class="sxs-lookup"><span data-stu-id="ab7c7-109">*pointer-member-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ab7c7-110">Especifica o tipo do membro de ponteiro da estrutura ou União.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-110">Specifies the type of the pointer member of the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="ab7c7-111">*nome do ponteiro*</span><span class="sxs-lookup"><span data-stu-id="ab7c7-111">*pointer-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ab7c7-112">Especifica o nome do membro do ponteiro que deve ser ignorado durante o marshaling.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-112">Specifies the name of the pointer member that is to be ignored during marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab7c7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab7c7-113">Remarks</span></span>

<span data-ttu-id="ab7c7-114">O valor de um membro de estrutura com o atributo **\[ ignore \]** é indefinido no destino.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-114">The value of a structure member with the **\[ignore\]** attribute is undefined at the destination.</span></span> <span data-ttu-id="ab7c7-115">Um **\[** parâmetro [**in**](in.md) **\]** não está definido no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-115">An **\[**[**in**](in.md)**\]** parameter is not defined at the remote computer.</span></span> <span data-ttu-id="ab7c7-116">Um **\[** parâmetro de [**saída**](out-idl.md) **\]** não está definido no computador local.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-116">An **\[**[**out**](out-idl.md)**\]** parameter is not defined at the local computer.</span></span>

<span data-ttu-id="ab7c7-117">O atributo **\[ ignorar \]** permite que você impeça a transmissão de dados.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-117">The **\[ignore\]** attribute allows you to prevent transmission of data.</span></span> <span data-ttu-id="ab7c7-118">Isso é útil em situações como uma lista de links duplos.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-118">This is useful in situations such as a double-linked list.</span></span> <span data-ttu-id="ab7c7-119">O exemplo a seguir inclui uma lista vinculada dupla que apresenta o alias de dados:</span><span class="sxs-lookup"><span data-stu-id="ab7c7-119">The following example includes a double-linked list that introduces data aliasing:</span></span>

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

<span data-ttu-id="ab7c7-120">O alias ocorre no exemplo anterior porque a mesma área de memória está disponível de dois ponteiros diferentes na função **p** e **p->avançar >anterior**.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-120">Aliasing occurs in the preceding example because the same memory area is available from two different pointers in the function **p** and **p->next->previous**.</span></span>

<span data-ttu-id="ab7c7-121">Observe que **\[ ignorar \]** não pode ser usado como um atributo de tipo.</span><span class="sxs-lookup"><span data-stu-id="ab7c7-121">Note that **\[ignore\]** cannot be used as a type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="ab7c7-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab7c7-122">Examples</span></span>

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="ab7c7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab7c7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7c7-124">Atributos de matriz e de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="ab7c7-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ab7c7-125">**Storage**</span><span class="sxs-lookup"><span data-stu-id="ab7c7-125">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="ab7c7-126">Matrizes e ponteiros</span><span class="sxs-lookup"><span data-stu-id="ab7c7-126">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="ab7c7-127">**no**</span><span class="sxs-lookup"><span data-stu-id="ab7c7-127">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="ab7c7-128">**fora**</span><span class="sxs-lookup"><span data-stu-id="ab7c7-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="ab7c7-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="ab7c7-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="ab7c7-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="ab7c7-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="ab7c7-131">**diferente**</span><span class="sxs-lookup"><span data-stu-id="ab7c7-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 