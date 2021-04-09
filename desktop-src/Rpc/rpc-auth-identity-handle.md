---
title: RPC_AUTH_IDENTITY_HANDLE (rpcdce. h)
description: O \_ tipo de \_ dados identificador de identidade de autenticação RPC \_ declara um identificador que aponta para uma estrutura que contém as credenciais de autenticação e autorização do cliente especificadas para chamadas de procedimento remoto.
ms.assetid: 06e45348-a392-45be-9f8a-e77ef887f26c
keywords:
- RPC_AUTH_IDENTITY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86559e7852172d34898d48f13bb2975ed792d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086458"
---
# <a name="rpc_auth_identity_handle"></a><span data-ttu-id="18e42-104">\_identificador de \_ identidade de autenticação RPC \_</span><span class="sxs-lookup"><span data-stu-id="18e42-104">RPC\_AUTH\_IDENTITY\_HANDLE</span></span>

<span data-ttu-id="18e42-105">O tipo de dados **\_ identificador de \_ identidade \_ de autenticação RPC** declara um identificador que aponta para uma estrutura que contém as credenciais de autenticação e autorização do cliente especificadas para chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="18e42-105">The **RPC\_AUTH\_IDENTITY\_HANDLE** data type declares a handle that points to a structure containing the client's authentication and authorization credentials specified for remote procedure calls.</span></span>


```C++
typedef void* RPC_AUTH_IDENTITY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="18e42-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18e42-106">Requirements</span></span>



| <span data-ttu-id="18e42-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="18e42-107">Requirement</span></span> | <span data-ttu-id="18e42-108">Valor</span><span class="sxs-lookup"><span data-stu-id="18e42-108">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e42-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18e42-109">Minimum supported client</span></span><br/> | <span data-ttu-id="18e42-110">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18e42-110">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="18e42-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18e42-111">Minimum supported server</span></span><br/> | <span data-ttu-id="18e42-112">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18e42-112">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="18e42-113">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="18e42-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="18e42-114"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18e42-114"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18e42-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="18e42-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e42-116">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="18e42-116">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="18e42-117">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="18e42-117">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> </dl>

 

 





