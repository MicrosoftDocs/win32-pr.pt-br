---
title: force_allocate atributo
description: O atributo ACF \ Force \_ ALLOCATE \ força um parâmetro de ponteiro a ser alocado usando a alocação de \_ usuário MIDL \_ em vez de otimizar a alocação.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate do atributo MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453996"
---
# <a name="force_allocate-attribute"></a><span data-ttu-id="6bd1b-104">forçar \_ alocação de atributo</span><span class="sxs-lookup"><span data-stu-id="6bd1b-104">force\_allocate attribute</span></span>

<span data-ttu-id="6bd1b-105">O atributo ACF de \[ **\_ realocação Force** \] força um parâmetro de ponteiro a ser alocado usando a [**\_ \_ alocação de usuário MIDL**](midl-user-allocate-1.md) em vez de otimizar a alocação.</span><span class="sxs-lookup"><span data-stu-id="6bd1b-105">The ACF attribute \[**force\_allocate**\] forces a pointer parameter to be allocated using [**midl\_user\_allocate**](midl-user-allocate-1.md) instead of optimizing away the allocation.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a><span data-ttu-id="6bd1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bd1b-106">Parameters</span></span>

<span data-ttu-id="6bd1b-107">Este atributo não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6bd1b-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bd1b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bd1b-108">Remarks</span></span>

<span data-ttu-id="6bd1b-109">O RPC tenta minimizar as alocações de memória no servidor fornecendo ponteiros para buffers de memória internos.</span><span class="sxs-lookup"><span data-stu-id="6bd1b-109">RPC attempts to minimize memory allocations on the server by supplying pointers to internal memory buffers.</span></span> <span data-ttu-id="6bd1b-110">Essa abordagem pode causar problemas para aplicativos que tentam chamar diretamente [**o \_ usuário MIDL \_ gratuitamente**](midl-user-free-1.md) em ponteiros fornecidos por RPC, porque um ponteiro otimizado não pode ser liberado.</span><span class="sxs-lookup"><span data-stu-id="6bd1b-110">This approach can cause problems for applications that attempt to directly call [**midl\_user\_free**](midl-user-free-1.md) on RPC-supplied pointers, because a pointer that has been optimized cannot be freed.</span></span> <span data-ttu-id="6bd1b-111">A marcação de um parâmetro com **\[ forçar \_ alocação \]** impedirá essa otimização para todos os ponteiros que a derivam.</span><span class="sxs-lookup"><span data-stu-id="6bd1b-111">Marking a parameter with **\[force\_allocate\]** will prevent this optimization for all pointers deriving it.</span></span>

<span data-ttu-id="6bd1b-112">Outro uso comum para a **\[ \_ distribuição \] forçada** é garantir o alinhamento da memória que está sendo apontada se um aplicativo exigir um alinhamento maior do que a da memória apontada.</span><span class="sxs-lookup"><span data-stu-id="6bd1b-112">Another common use for **\[force\_allocate\]** is to guarantee the alignment of the memory being pointed to if an application requires an alignment greater than that of the memory pointed to.</span></span> <span data-ttu-id="6bd1b-113">Por exemplo, os aplicativos geralmente passam dados em uma matriz genérica de bytes em vez de usar o tipo real, mas um byte só é garantido para ser alinhado em 1, o que pode causar problemas para aplicativos que assumem um alinhamento maior.</span><span class="sxs-lookup"><span data-stu-id="6bd1b-113">For example, applications often pass data in a generic array of bytes rather than using the actual type, but a byte is only guaranteed to be aligned at 1, which may cause problems for applications that assume a larger alignment.</span></span> <span data-ttu-id="6bd1b-114">Ao marcar o parâmetro com **\[ forçar \_ alocação \]**, o aplicativo pode garantir que toda a memória apontada terá um alinhamento igual ao que é garantido pelo [**usuário de MIDL \_ \_ alocar**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="6bd1b-114">By marking the parameter with **\[force\_allocate\]**, the application can guarantee all memory pointed to will have an alignment equal to that guaranteed by [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6bd1b-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6bd1b-115">Examples</span></span>

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a><span data-ttu-id="6bd1b-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bd1b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bd1b-117">Evitando a ocultação de informações</span><span class="sxs-lookup"><span data-stu-id="6bd1b-117">Avoiding Information Hiding</span></span>](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[<span data-ttu-id="6bd1b-118">Criando interfaces compatíveis com 64 bits</span><span class="sxs-lookup"><span data-stu-id="6bd1b-118">Designing 64-bit-Compatible Interfaces</span></span>](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[<span data-ttu-id="6bd1b-119">**\_alocar usuário de MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="6bd1b-119">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="6bd1b-120">**usuário de MIDL \_ \_ gratuito**</span><span class="sxs-lookup"><span data-stu-id="6bd1b-120">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="6bd1b-121">**aloca**</span><span class="sxs-lookup"><span data-stu-id="6bd1b-121">**allocate**</span></span>](allocate.md)
</dt> </dl>

 

 