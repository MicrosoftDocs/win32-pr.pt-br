---
title: RPC_NS_HANDLE (Rpcnsi. h)
description: O identificador do tipo de dados RPC \_ ns \_ define um identificador de serviço de nome.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499688"
---
# <a name="rpc_ns_handle"></a><span data-ttu-id="147f9-104">identificador de RPC \_ ns \_</span><span class="sxs-lookup"><span data-stu-id="147f9-104">RPC\_NS\_HANDLE</span></span>

<span data-ttu-id="147f9-105">O **\_ \_ identificador** do tipo de dados RPC NS define um identificador de serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="147f9-105">The data type **RPC\_NS\_HANDLE** defines a name-service handle.</span></span>


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="147f9-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="147f9-106">Remarks</span></span>

<span data-ttu-id="147f9-107">Um identificador de serviço de nome é uma variável opaca que contém informações que a biblioteca de tempo de execução RPC usa para retornar os seguintes dados de RPC do nome-do-serviço:</span><span class="sxs-lookup"><span data-stu-id="147f9-107">A name-service handle is an opaque variable containing information the RPC run-time library uses to return the following RPC data from the name-service database:</span></span>

-   <span data-ttu-id="147f9-108">Identificadores de associação de servidor</span><span class="sxs-lookup"><span data-stu-id="147f9-108">Server-binding handles</span></span>
-   <span data-ttu-id="147f9-109">UUIDs de recursos oferecidos por membros do perfil do servidor</span><span class="sxs-lookup"><span data-stu-id="147f9-109">UUIDs of resources offered by server profile members</span></span>
-   <span data-ttu-id="147f9-110">Membros do grupo</span><span class="sxs-lookup"><span data-stu-id="147f9-110">Group members</span></span>

<span data-ttu-id="147f9-111">O escopo de um identificador de serviço de nome é de uma rotina de "início" por meio da rotina "concluída" correspondente.</span><span class="sxs-lookup"><span data-stu-id="147f9-111">The scope of a name-service handle is from a "Begin" routine through the corresponding "Done" routine.</span></span>

<span data-ttu-id="147f9-112">Os aplicativos são responsáveis pelo controle de simultaneidade de identificadores de serviço de nome entre threads.</span><span class="sxs-lookup"><span data-stu-id="147f9-112">Applications are responsible for concurrency control of name-service handles across threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="147f9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="147f9-113">Requirements</span></span>



| <span data-ttu-id="147f9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="147f9-114">Requirement</span></span> | <span data-ttu-id="147f9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="147f9-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="147f9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="147f9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="147f9-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="147f9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="147f9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="147f9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="147f9-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="147f9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="147f9-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="147f9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="147f9-121"><dt>Rpcnsi. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="147f9-121"><dt>Rpcnsi.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="147f9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="147f9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="147f9-123">**RpcNsBindingImportBegin**</span><span class="sxs-lookup"><span data-stu-id="147f9-123">**RpcNsBindingImportBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[<span data-ttu-id="147f9-124">**RpcNsBindingImportDone**</span><span class="sxs-lookup"><span data-stu-id="147f9-124">**RpcNsBindingImportDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[<span data-ttu-id="147f9-125">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="147f9-125">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[<span data-ttu-id="147f9-126">**RpcNsBindingLookupBegin**</span><span class="sxs-lookup"><span data-stu-id="147f9-126">**RpcNsBindingLookupBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[<span data-ttu-id="147f9-127">**RpcNsBindingLookupDone**</span><span class="sxs-lookup"><span data-stu-id="147f9-127">**RpcNsBindingLookupDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[<span data-ttu-id="147f9-128">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="147f9-128">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





