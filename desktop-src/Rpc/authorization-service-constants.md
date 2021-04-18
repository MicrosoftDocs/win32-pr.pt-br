---
title: Constantes de Authorization-Service (rpcdce. h)
description: As constantes do serviço de autorização representam os serviços de autorização passados para várias funções de tempo de execução.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499852"
---
# <a name="authorization-service-constants"></a><span data-ttu-id="e3241-103">Authorization-Service constantes</span><span class="sxs-lookup"><span data-stu-id="e3241-103">Authorization-Service Constants</span></span>

<span data-ttu-id="e3241-104">As constantes do serviço de autorização representam os serviços de autorização passados para várias funções de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="e3241-104">The authorization service constants represent the authorization services passed to various run-time functions.</span></span>

<span data-ttu-id="e3241-105">As constantes a seguir são valores válidos para o parâmetro *AuthzSvc* .</span><span class="sxs-lookup"><span data-stu-id="e3241-105">The following constants are valid values for the *AuthzSvc* parameter.</span></span> <span data-ttu-id="e3241-106">A maioria dos aplicativos encontra RPC \_ C \_ AUTHZ \_ não suficiente.</span><span class="sxs-lookup"><span data-stu-id="e3241-106">Most applications find RPC\_C\_AUTHZ\_NON sufficient.</span></span>



| <span data-ttu-id="e3241-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e3241-107">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="e3241-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3241-108">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="e3241-109"><dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e3241-109"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="e3241-110">O servidor não executa nenhuma autorização.</span><span class="sxs-lookup"><span data-stu-id="e3241-110">Server performs no authorization.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="e3241-111"><dt>**RPC \_ C \_ AUTHZ \_ nome**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e3241-111"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="e3241-112">O servidor executa a autorização com base no nome principal do cliente.</span><span class="sxs-lookup"><span data-stu-id="e3241-112">Server performs authorization based on the client's principal name.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="e3241-113"><dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e3241-113"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="e3241-114">O servidor executa a verificação de autorização usando as informações de PAC (certificado de atributo de privilégio) do cliente DCE, que são enviadas para o servidor com cada chamada de procedimento remoto feita usando o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="e3241-114">Server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="e3241-115">Geralmente, o acesso é verificado em relação às[ACLs](/windows/desktop/api/winnt/ns-winnt-acl)(listas de controle de acesso) do DCE.</span><span class="sxs-lookup"><span data-stu-id="e3241-115">Generally, access is checked against DCE access control lists ([ACLs](/windows/desktop/api/winnt/ns-winnt-acl)).</span></span><br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="e3241-116"><dt>**RPC \_ C \_ AUTHZ \_ padrão**</dt> , <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="e3241-116"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="e3241-117">O servidor usa o serviço de autorização padrão para o SSP atual.</span><span class="sxs-lookup"><span data-stu-id="e3241-117">Server uses the default authorization service for the current SSP.</span></span><br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="e3241-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3241-118">Requirements</span></span>



| <span data-ttu-id="e3241-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3241-119">Requirement</span></span> | <span data-ttu-id="e3241-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e3241-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e3241-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3241-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3241-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3241-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e3241-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3241-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3241-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3241-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e3241-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e3241-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3241-126"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3241-126"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3241-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3241-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3241-128">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="e3241-128">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="e3241-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="e3241-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="e3241-130">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="e3241-130">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="e3241-131">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="e3241-131">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="e3241-132">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e3241-132">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="e3241-133">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e3241-133">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[<span data-ttu-id="e3241-134">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="e3241-134">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

