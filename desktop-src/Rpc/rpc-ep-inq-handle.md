---
title: RPC_EP_INQ_HANDLE (Rpcasync. h)
description: O \_ tipo de dados do identificador de INQ do EP RPC \_ \_ declara um identificador para um contexto de consulta. Os aplicativos RPC o usam para exibir informações de endereço do servidor armazenadas no mapa do ponto de extremidade.
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c34c64b5601b31485808924fc57dbe3412b6009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369854"
---
# <a name="rpc_ep_inq_handle"></a><span data-ttu-id="45626-105">\_identificador de \_ INQ do EP RPC \_</span><span class="sxs-lookup"><span data-stu-id="45626-105">RPC\_EP\_INQ\_HANDLE</span></span>

<span data-ttu-id="45626-106">O tipo de dados do **\_ identificador de \_ INQ \_ do EP RPC** declara um identificador para um contexto de consulta.</span><span class="sxs-lookup"><span data-stu-id="45626-106">The **RPC\_EP\_INQ\_HANDLE** data type declares a handle for an inquiry context.</span></span> <span data-ttu-id="45626-107">Os aplicativos RPC o usam para exibir informações de endereço do servidor armazenadas no mapa do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="45626-107">RPC applications use it to view server address information stored in the endpoint map.</span></span>


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="45626-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45626-108">Requirements</span></span>



| <span data-ttu-id="45626-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="45626-109">Requirement</span></span> | <span data-ttu-id="45626-110">Valor</span><span class="sxs-lookup"><span data-stu-id="45626-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45626-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45626-111">Minimum supported client</span></span><br/> | <span data-ttu-id="45626-112">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45626-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="45626-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45626-113">Minimum supported server</span></span><br/> | <span data-ttu-id="45626-114">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45626-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="45626-115">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45626-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="45626-116"><dt>Rpcasync. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45626-116"><dt>Rpcasync.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45626-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="45626-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45626-118">**RpcMgmtEpEltInqBegin**</span><span class="sxs-lookup"><span data-stu-id="45626-118">**RpcMgmtEpEltInqBegin**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[<span data-ttu-id="45626-119">**RpcMgmtEpEltInqNext**</span><span class="sxs-lookup"><span data-stu-id="45626-119">**RpcMgmtEpEltInqNext**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[<span data-ttu-id="45626-120">**RpcMgmtEpEltInqDone**</span><span class="sxs-lookup"><span data-stu-id="45626-120">**RpcMgmtEpEltInqDone**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





