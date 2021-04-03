---
title: RPC_BINDING_HANDLE (rpcdce. h)
description: O \_ tipo de dados identificador de associação RPC declara um identificador de associação que contém informações que a biblioteca de tempo de execução RPC usa para acessar informações de associação.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645222"
---
# <a name="rpc_binding_handle"></a><span data-ttu-id="465fa-104">\_identificador de associação RPC \_</span><span class="sxs-lookup"><span data-stu-id="465fa-104">RPC\_BINDING\_HANDLE</span></span>

<span data-ttu-id="465fa-105">O tipo de dados **\_ identificador de associação RPC** declara um identificador de associação que contém informações que a biblioteca de tempo de execução RPC usa para acessar informações de associação.</span><span class="sxs-lookup"><span data-stu-id="465fa-105">The **RPC\_BINDING HANDLE** data type declares a binding handle containing information that the RPC run-time library uses to access binding information.</span></span>


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="465fa-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="465fa-106">Remarks</span></span>

<span data-ttu-id="465fa-107">A biblioteca de tempo de execução usa informações de associação para estabelecer uma relação de cliente-servidor que permite a execução de chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="465fa-107">The run-time library uses binding information to establish a client-server relationship that allows the execution of remote procedure calls.</span></span> <span data-ttu-id="465fa-108">Com base no contexto no qual um identificador de associação é criado, ele é considerado um identificador de associação de servidor ou um identificador de associação de cliente.</span><span class="sxs-lookup"><span data-stu-id="465fa-108">Based on the context in which a binding handle is created, it is considered a server-binding handle or a client-binding handle.</span></span>

<span data-ttu-id="465fa-109">Um identificador de associação de servidor contém as informações necessárias para um cliente estabelecer uma relação com um servidor específico.</span><span class="sxs-lookup"><span data-stu-id="465fa-109">A server-binding handle contains the information necessary for a client to establish a relationship with a specific server.</span></span> <span data-ttu-id="465fa-110">Qualquer número de rotinas de tempo de execução da API RPC retorna um identificador de associação de servidor que pode ser usado para fazer uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="465fa-110">Any number of RPC API run-time routines return a server-binding handle that can be used for making a remote procedure call.</span></span>

<span data-ttu-id="465fa-111">Um identificador de associação de cliente não pode ser usado para fazer uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="465fa-111">A client-binding handle cannot be used to make a remote procedure call.</span></span> <span data-ttu-id="465fa-112">A biblioteca de tempo de execução RPC cria e fornece um identificador de ligação de cliente para um procedimento chamado-Server (também chamado de rotina Server-Manager) como \_ o \_ parâmetro identificador de associação RPC.</span><span class="sxs-lookup"><span data-stu-id="465fa-112">The RPC run-time library creates and provides a client-binding handle to a called-server procedure (also called a server-manager routine) as the RPC\_BINDING\_HANDLE parameter.</span></span> <span data-ttu-id="465fa-113">O identificador de associação de cliente contém informações sobre o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="465fa-113">The client-binding handle contains information about the calling client.</span></span>

<span data-ttu-id="465fa-114">As funções \*\* \* RpcBinding\* _ _*e \* RpcNsBinding*_ retornam o código de status RPC \_ S \_ \_ tipo \_ de associação incorreto \_ quando um aplicativo fornece o tipo de identificador de associação incorreto.</span><span class="sxs-lookup"><span data-stu-id="465fa-114">The **RpcBinding\** _ and _*RpcNsBinding\*\*_ functions return the status code RPC\_S\_WRONG\_KIND\_OF\_BINDING when an application provides the incorrect binding-handle type.</span></span>

<span data-ttu-id="465fa-115">Um aplicativo pode compartilhar um único identificador de associação entre vários threads de execução.</span><span class="sxs-lookup"><span data-stu-id="465fa-115">An application can share a single binding handle across multiple threads of execution.</span></span> <span data-ttu-id="465fa-116">A biblioteca de tempo de execução RPC gerencia chamadas de procedimento remoto simultâneas que usam um único identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="465fa-116">The RPC run-time library manages concurrent remote procedure calls that use a single binding handle.</span></span> <span data-ttu-id="465fa-117">No entanto, o aplicativo é responsável pelo controle de simultaneidade de identificador de associação para operações que modificam um identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="465fa-117">However, the application is responsible for binding handle concurrency control for operations that modify a binding handle.</span></span> <span data-ttu-id="465fa-118">Essas operações incluem as seguintes rotinas:</span><span class="sxs-lookup"><span data-stu-id="465fa-118">These operations include the following routines:</span></span>

-   [<span data-ttu-id="465fa-119">_ *RpcBindingFree*\*</span><span class="sxs-lookup"><span data-stu-id="465fa-119">_ *RpcBindingFree*\*</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [<span data-ttu-id="465fa-120">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="465fa-120">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [<span data-ttu-id="465fa-121">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="465fa-121">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [<span data-ttu-id="465fa-122">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="465fa-122">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

<span data-ttu-id="465fa-123">Por exemplo, se um aplicativo compartilha um identificador de associação entre dois threads de execução e redefine o ponto de extremidade de identificador de associação em um dos threads chamando [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="465fa-123">For example, if an application shares a binding handle across two threads of execution and resets the binding-handle endpoint in one of the threads by calling [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), the results are undefined.</span></span> <span data-ttu-id="465fa-124">O identificador de associação no outro thread também pode ser redefinido, ou a operação pode falhar ou o processo pode falhar.</span><span class="sxs-lookup"><span data-stu-id="465fa-124">The binding handle on the other thread may also be reset, or the operation may fail, or the process may crash.</span></span> <span data-ttu-id="465fa-125">Um erro comum é liberar um identificador de associação enquanto uma chamada está em andamento; Isso geralmente falha no processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="465fa-125">A common error is freeing a binding handle while a call on it is in progress; this usually crashes the calling process.</span></span>

<span data-ttu-id="465fa-126">Se você não quiser a simultaneidade, você pode criar um aplicativo que crie uma cópia de um identificador de ligação chamando [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span><span class="sxs-lookup"><span data-stu-id="465fa-126">If you do not want concurrency, you can design an application to create a copy of a binding handle by calling [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span></span> <span data-ttu-id="465fa-127">Nesse caso, uma operação para o primeiro identificador de ligação não tem nenhum efeito no segundo identificador de ligação.</span><span class="sxs-lookup"><span data-stu-id="465fa-127">In this case, an operation to the first binding handle has no effect on the second binding handle.</span></span>

<span data-ttu-id="465fa-128">As rotinas que exigem um identificador de associação como um parâmetro mostram um tipo de dados de **\_ \_ identificador de associação RPC**.</span><span class="sxs-lookup"><span data-stu-id="465fa-128">Routines requiring a binding handle as a parameter show a data type of **RPC\_BINDING\_HANDLE**.</span></span> <span data-ttu-id="465fa-129">Os parâmetros de identificador de associação são passados por valor.</span><span class="sxs-lookup"><span data-stu-id="465fa-129">Binding-handle parameters are passed by value.</span></span>

## <a name="requirements"></a><span data-ttu-id="465fa-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="465fa-130">Requirements</span></span>



| <span data-ttu-id="465fa-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="465fa-131">Requirement</span></span> | <span data-ttu-id="465fa-132">Valor</span><span class="sxs-lookup"><span data-stu-id="465fa-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="465fa-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="465fa-133">Minimum supported client</span></span><br/> | <span data-ttu-id="465fa-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="465fa-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="465fa-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="465fa-135">Minimum supported server</span></span><br/> | <span data-ttu-id="465fa-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="465fa-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="465fa-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="465fa-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="465fa-138"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="465fa-138"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





