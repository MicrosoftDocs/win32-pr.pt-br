---
title: midl_user_allocate atributo
description: A \_ função de alocação de usuário MIDL \_ é uma função que os aplicativos cliente e servidor fornecem para alocar memória.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate do atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294035"
---
# <a name="midl_user_allocate-attribute"></a><span data-ttu-id="31a90-104">atributo de alocação de \_ usuário MIDL \_</span><span class="sxs-lookup"><span data-stu-id="31a90-104">midl\_user\_allocate attribute</span></span>

<span data-ttu-id="31a90-105">A função de **\_ \_ alocação de usuário MIDL** é uma função que os aplicativos cliente e servidor fornecem para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="31a90-105">The **midl\_user\_allocate** function is a function that client and server applications provide to allocate memory.</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a><span data-ttu-id="31a90-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31a90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a90-107">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="31a90-107">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="31a90-108">Especifica a contagem de bytes a serem alocados.</span><span class="sxs-lookup"><span data-stu-id="31a90-108">Specifies the count of bytes to allocate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31a90-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="31a90-109">Remarks</span></span>

<span data-ttu-id="31a90-110">Os aplicativos cliente e os aplicativos de servidor devem implementar a função de **\_ \_ alocação de usuário MIDL** , a menos que você esteja compilando no modo uso-Compatibility ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="31a90-110">Both client applications and server applications must implement the **midl\_user\_allocate** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="31a90-111">Os aplicativos e os stubs gerados chamam a **\_ \_ alocação de usuário de MIDL** ao lidar com objetos referenciados por ponteiros:</span><span class="sxs-lookup"><span data-stu-id="31a90-111">Applications and generated stubs call **midl\_user\_allocate** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="31a90-112">O aplicativo de servidor deve chamar o **\_ usuário MIDL \_ ALLOCATE** para alocar memória para o aplicativos € ", por exemplo, ao criar um novo nó.</span><span class="sxs-lookup"><span data-stu-id="31a90-112">The server application should call **midl\_user\_allocate** to allocate memory for the applicationâ€”for example, when creating a new node.</span></span>
-   <span data-ttu-id="31a90-113">O stub do servidor chama o **usuário de MIDL \_ \_ alocar** ao desempacotar dados apontados para o espaço de endereço do servidor.</span><span class="sxs-lookup"><span data-stu-id="31a90-113">The server stub calls **midl\_user\_allocate** when unmarshaling pointed-at data into the server address space.</span></span>
-   <span data-ttu-id="31a90-114">O stub do cliente chama a **\_ \_ alocação do usuário de MIDL** ao desempacotar dados do servidor que é referenciado por um ponteiro [**out**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="31a90-114">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an [**out**](out-idl.md) pointer.</span></span> <span data-ttu-id="31a90-115">Observe que para **\[** [](in.md) **\]** ponteiros in, **\[ out \]** e **\[** [**Unique**](unique.md) **\]** , o stub do cliente chama o **usuário de MIDL \_ \_ ALLOCATE** somente se o valor do ponteiro **\[ exclusivo \]** era **nulo** na entrada e muda para um valor não **nulo** durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="31a90-115">Note that for **\[**[**in**](in.md)**\]**, **\[out\]**, and **\[**[**unique**](unique.md)**\]** pointers, the client stub calls **midl\_user\_allocate** only if the **\[unique\]** pointer value was **NULL** on input and changes to a non-**NULL** value during the call.</span></span> <span data-ttu-id="31a90-116">Se o ponteiro **\[ \] exclusivo** não for **nulo** na entrada, o stub do cliente gravará os dados associados em uma memória existente.</span><span class="sxs-lookup"><span data-stu-id="31a90-116">If the **\[unique\]** pointer was non-**NULL** on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="31a90-117">Se **a \_ \_ alocação de usuário MIDL** falhar ao alocar memória, ela deverá retornar um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="31a90-117">If **midl\_user\_allocate** fails to allocate memory, it must return a **NULL** pointer.</span></span>

<span data-ttu-id="31a90-118">É recomendável que **a \_ \_ alocação de usuário de MIDL** retorne um ponteiro que tenha 8 bytes alinhados.</span><span class="sxs-lookup"><span data-stu-id="31a90-118">It is recommended that **midl\_user\_allocate** return a pointer that is 8 bytes aligned.</span></span>

## <a name="examples"></a><span data-ttu-id="31a90-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31a90-119">Examples</span></span>


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a><span data-ttu-id="31a90-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="31a90-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a90-121">**aloca**</span><span class="sxs-lookup"><span data-stu-id="31a90-121">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="31a90-122">**Storage**</span><span class="sxs-lookup"><span data-stu-id="31a90-122">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="31a90-123">Matrizes e ponteiros</span><span class="sxs-lookup"><span data-stu-id="31a90-123">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="31a90-124">Atributos de matriz e de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="31a90-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="31a90-125">**no**</span><span class="sxs-lookup"><span data-stu-id="31a90-125">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="31a90-126">**usuário de MIDL \_ \_ gratuito**</span><span class="sxs-lookup"><span data-stu-id="31a90-126">**midl\_user\_free**</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="31a90-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="31a90-127">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="31a90-128">**fora**</span><span class="sxs-lookup"><span data-stu-id="31a90-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="31a90-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="31a90-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="31a90-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="31a90-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="31a90-131">**diferente**</span><span class="sxs-lookup"><span data-stu-id="31a90-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 