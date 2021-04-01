---
title: Constantes de autorização (RpcDce. h)
description: Define o que o servidor autoriza.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645202"
---
# <a name="authorization-constants"></a><span data-ttu-id="52a8c-103">Constantes de autorização</span><span class="sxs-lookup"><span data-stu-id="52a8c-103">Authorization Constants</span></span>

<span data-ttu-id="52a8c-104">Define o que o servidor autoriza.</span><span class="sxs-lookup"><span data-stu-id="52a8c-104">Defines what the server authorizes.</span></span>



| <span data-ttu-id="52a8c-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="52a8c-105">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="52a8c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="52a8c-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="52a8c-107"><dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52a8c-107"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="52a8c-108">O servidor não executa nenhuma autorização.</span><span class="sxs-lookup"><span data-stu-id="52a8c-108">The server performs no authorization.</span></span> <span data-ttu-id="52a8c-109">Atualmente, o RPC \_ c \_ Authn \_ WinNT, o RPC \_ c \_ Authn \_ GSS \_ Schannel e o RPC \_ c \_ Authn \_ GSS \_ Kerberos todos usam somente RPC \_ c \_ AUTHZ \_ None.</span><span class="sxs-lookup"><span data-stu-id="52a8c-109">Currently, RPC\_C\_AUTHN\_WINNT, RPC\_C\_AUTHN\_GSS\_SCHANNEL, and RPC\_C\_AUTHN\_GSS\_KERBEROS all use only RPC\_C\_AUTHZ\_NONE.</span></span><br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="52a8c-110"><dt>**RPC \_ C \_ AUTHZ \_ nome**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="52a8c-110"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="52a8c-111">O servidor executa a autorização com base no nome principal do cliente.</span><span class="sxs-lookup"><span data-stu-id="52a8c-111">The server performs authorization based on the client's principal name.</span></span> <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="52a8c-112"><dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="52a8c-112"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="52a8c-113">O servidor executa a verificação de autorização usando as informações de PAC (certificado de atributo de privilégio) do cliente DCE, que são enviadas para o servidor com cada chamada de procedimento remoto feita usando o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="52a8c-113">The server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="52a8c-114">Geralmente, o acesso é verificado em relação às ACLs (listas de controle de acesso) do DCE.</span><span class="sxs-lookup"><span data-stu-id="52a8c-114">Generally, access is checked against DCE access control lists (ACLs).</span></span> <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="52a8c-115"><dt>**RPC \_ C \_ AUTHZ \_ padrão**</dt> , <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="52a8c-115"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="52a8c-116">O DCOM pode escolher o nível de autorização usando seu algoritmo normal de negociação ampla de segurança.</span><span class="sxs-lookup"><span data-stu-id="52a8c-116">DCOM can choose the authorization level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="52a8c-117">Para obter mais informações, consulte [negociação de cobertura de segurança](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="52a8c-117">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span><br/>                                                                                           |



## <a name="remarks"></a><span data-ttu-id="52a8c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="52a8c-118">Remarks</span></span>

<span data-ttu-id="52a8c-119">Essas constantes são usadas por métodos da interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) .</span><span class="sxs-lookup"><span data-stu-id="52a8c-119">These constants are used by methods of the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="52a8c-120">Eles são usados na estrutura [**de \_ \_ serviço de autenticação exclusiva**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , que é recuperada pela função [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) .</span><span class="sxs-lookup"><span data-stu-id="52a8c-120">They are used in the [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) structure, which is retrieved by the [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) function.</span></span> <span data-ttu-id="52a8c-121">Eles também são usados na estrutura [**de \_ \_ informações de autenticação exclusiva**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , que, por sua vez, é membro da estrutura [**exclusiva da \_ \_ lista de autenticação**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) .</span><span class="sxs-lookup"><span data-stu-id="52a8c-121">They are also used in the [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) structure, which in turn is a member of the [**SOLE\_AUTHENTICATION\_LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) structure.</span></span> <span data-ttu-id="52a8c-122">Essa estrutura, que é uma lista de serviços de autenticação, os serviços de autorização que eles executam e as informações de autenticação para cada serviço, são passadas para a função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e o método [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .</span><span class="sxs-lookup"><span data-stu-id="52a8c-122">This structure, which is a list of authentication services, the authorization services they perform, and the authentication information for each service, is passed to the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function and the [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="52a8c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52a8c-123">Requirements</span></span>



| <span data-ttu-id="52a8c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a8c-124">Requirement</span></span> | <span data-ttu-id="52a8c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="52a8c-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52a8c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52a8c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52a8c-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52a8c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="52a8c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52a8c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52a8c-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52a8c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52a8c-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52a8c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="52a8c-131"><dt>RpcDce. h</dt></span><span class="sxs-lookup"><span data-stu-id="52a8c-131"><dt>RpcDce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a8c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="52a8c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a8c-133">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="52a8c-133">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="52a8c-134">**CoQueryAuthenticationServices**</span><span class="sxs-lookup"><span data-stu-id="52a8c-134">**CoQueryAuthenticationServices**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[<span data-ttu-id="52a8c-135">**IClientSecurity**</span><span class="sxs-lookup"><span data-stu-id="52a8c-135">**IClientSecurity**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[<span data-ttu-id="52a8c-136">**\_informações de autenticação exclusiva \_**</span><span class="sxs-lookup"><span data-stu-id="52a8c-136">**SOLE\_AUTHENTICATION\_INFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[<span data-ttu-id="52a8c-137">**\_serviço de autenticação exclusivo \_**</span><span class="sxs-lookup"><span data-stu-id="52a8c-137">**SOLE\_AUTHENTICATION\_SERVICE**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

