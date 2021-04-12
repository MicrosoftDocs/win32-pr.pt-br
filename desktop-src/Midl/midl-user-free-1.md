---
title: midl_user_free atributo
description: A \_ função gratuita do usuário MIDL \_ é fornecida por aplicativos cliente e servidor para desalocar a memória alocada dinamicamente.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free do atributo MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293982"
---
# <a name="midl_user_free-attribute"></a><span data-ttu-id="48a1f-104">atributo de usuário de MIDL \_ \_ livre</span><span class="sxs-lookup"><span data-stu-id="48a1f-104">midl\_user\_free attribute</span></span>

<span data-ttu-id="48a1f-105">A **função \_ \_ gratuita do usuário MIDL** é fornecida por aplicativos cliente e servidor para desalocar a memória alocada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="48a1f-105">The **midl\_user\_free** function is provided by client and server applications to deallocate dynamically allocated memory.</span></span>

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a><span data-ttu-id="48a1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48a1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a1f-107">*DTI*</span><span class="sxs-lookup"><span data-stu-id="48a1f-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="48a1f-108">Um ponteiro para o bloco de memória a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="48a1f-108">A pointer to the memory block to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48a1f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="48a1f-109">Remarks</span></span>

<span data-ttu-id="48a1f-110">O aplicativo cliente e o aplicativo de servidor devem implementar a função de **\_ usuário \_ de MIDL** , a menos que você esteja compilando no modo uso-Compatibility ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="48a1f-110">Both client application and server application must implement the **midl\_user\_free** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="48a1f-111">A função de **\_ usuário \_ de MIDL** deve ser capaz de liberar todo o armazenamento alocado por [**\_ \_ alocação de usuário MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="48a1f-111">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span>

<span data-ttu-id="48a1f-112">Aplicativos e stubs chamam o **\_ usuário MIDL \_ gratuito** ao lidar com objetos referenciados por ponteiros:</span><span class="sxs-lookup"><span data-stu-id="48a1f-112">Applications and stubs call **midl\_user\_free** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="48a1f-113">O aplicativo de servidor deve chamar o **\_ usuário MIDL \_ gratuitamente** para memória livre alocada pelo aplicativos € ", por exemplo, ao excluir um nó especificado.</span><span class="sxs-lookup"><span data-stu-id="48a1f-113">The server application should call **midl\_user\_free** to free memory allocated by the applicationâ€”for example, when deleting a specified node.</span></span>
-   <span data-ttu-id="48a1f-114">O stub de servidor chama o **\_ usuário MIDL \_ gratuitamente** para liberar memória no servidor após o marshaling de todos os **\[** [](out-idl.md) **\]** argumentos, **\[** argumentos [**de**](in.md) **saída \]** e o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="48a1f-114">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all **\[**[**out**](out-idl.md)**\]** arguments, **\[**[**in**](in.md), **out\]** arguments, and the return value.</span></span>

## <a name="examples"></a><span data-ttu-id="48a1f-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48a1f-115">Examples</span></span>


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a><span data-ttu-id="48a1f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="48a1f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a1f-117">**Storage**</span><span class="sxs-lookup"><span data-stu-id="48a1f-117">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="48a1f-118">Matrizes e ponteiros</span><span class="sxs-lookup"><span data-stu-id="48a1f-118">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="48a1f-119">Atributos de matriz e de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="48a1f-119">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="48a1f-120">**no**</span><span class="sxs-lookup"><span data-stu-id="48a1f-120">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="48a1f-121">**\_alocar usuário de MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="48a1f-121">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="48a1f-122">**/osf**</span><span class="sxs-lookup"><span data-stu-id="48a1f-122">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="48a1f-123">**fora**</span><span class="sxs-lookup"><span data-stu-id="48a1f-123">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="48a1f-124">**diferente**</span><span class="sxs-lookup"><span data-stu-id="48a1f-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 