---
title: RPC_AUTHZ_HANDLE (rpcdce. h)
description: O tipo de dados de identificador de RPC \_ AUTHZ \_ declara um identificador de autorização. Esse identificador aponta para as informações de privilégios do aplicativo cliente que fez a chamada de procedimento remoto.
ms.assetid: 35b6a3f4-1703-4244-98fd-fad7de48b262
keywords:
- RPC_AUTHZ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b095100e1e224590ef6a285785da632e198e1b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086457"
---
# <a name="rpc_authz_handle"></a><span data-ttu-id="5c333-105">identificador do RPC \_ AUTHZ \_</span><span class="sxs-lookup"><span data-stu-id="5c333-105">RPC\_AUTHZ\_HANDLE</span></span>

<span data-ttu-id="5c333-106">O tipo de dados de **\_ \_ identificador de RPC AUTHZ** declara um identificador de autorização.</span><span class="sxs-lookup"><span data-stu-id="5c333-106">The **RPC\_AUTHZ\_HANDLE** data type declares an authorization handle.</span></span> <span data-ttu-id="5c333-107">Esse identificador aponta para as informações de privilégios do aplicativo cliente que fez a chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="5c333-107">This handle points to the privileges information for the client application that made the remote procedure call.</span></span>


```C++
typedef void* RPC_AUTHZ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="5c333-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c333-108">Requirements</span></span>



| <span data-ttu-id="5c333-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c333-109">Requirement</span></span> | <span data-ttu-id="5c333-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5c333-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c333-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c333-111">Minimum supported client</span></span><br/> | <span data-ttu-id="5c333-112">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c333-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5c333-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c333-113">Minimum supported server</span></span><br/> | <span data-ttu-id="5c333-114">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c333-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c333-115">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5c333-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c333-116"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c333-116"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c333-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c333-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c333-118">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="5c333-118">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> </dl>

 

 





