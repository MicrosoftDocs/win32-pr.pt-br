---
title: Constantes de Authentication-Level (rpcdce. h)
description: As constantes de nível de autenticação representam níveis de autenticação passados para várias funções de tempo de execução.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499691"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="7666e-103">Constantes em nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="7666e-103">Authentication-Level Constants</span></span>

<span data-ttu-id="7666e-104">As constantes de nível de autenticação representam níveis de autenticação passados para várias funções de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7666e-104">The authentication-level constants represent authentication levels passed to various run-time functions.</span></span> <span data-ttu-id="7666e-105">Esses níveis são listados em ordem crescente de autenticação.</span><span class="sxs-lookup"><span data-stu-id="7666e-105">These levels are listed in order of increasing authentication.</span></span> <span data-ttu-id="7666e-106">Cada novo nível adiciona à autenticação fornecida pelo nível anterior.</span><span class="sxs-lookup"><span data-stu-id="7666e-106">Each new level adds to the authentication provided by the previous level.</span></span> <span data-ttu-id="7666e-107">Se a biblioteca de tempo de execução RPC não oferecer suporte ao nível especificado, ela será automaticamente atualizada para o próximo nível de suporte mais alto.</span><span class="sxs-lookup"><span data-stu-id="7666e-107">If the RPC run-time library does not support the specified level, it automatically upgrades to the next higher supported level.</span></span>



| <span data-ttu-id="7666e-108">Constante</span><span class="sxs-lookup"><span data-stu-id="7666e-108">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="7666e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7666e-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="7666e-110"><dt>**\_padrão de \_ nível de autenticação RPC C \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7666e-110"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt></span></span> </dl>                    | <span data-ttu-id="7666e-111">Usa o nível de autenticação padrão para o serviço de autenticação especificado.</span><span class="sxs-lookup"><span data-stu-id="7666e-111">Uses the default authentication level for the specified authentication service.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="7666e-112"><dt>**RPC \_ C \_ Authn \_ nível \_ nenhum**</dt></span><span class="sxs-lookup"><span data-stu-id="7666e-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="7666e-113">Não executa nenhuma autenticação.</span><span class="sxs-lookup"><span data-stu-id="7666e-113">Performs no authentication.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="7666e-114"><dt>**\_conexão em \_ nível de autenticação RPC C \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7666e-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt></span></span> </dl>                    | <span data-ttu-id="7666e-115">Realiza a autenticação somente quando o cliente estabelece uma relação com um servidor.</span><span class="sxs-lookup"><span data-stu-id="7666e-115">Authenticates only when the client establishes a relationship with a server.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="7666e-116"><dt>**\_chamada de \_ nível de autenticação RPC C \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7666e-116"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt></span></span> </dl>                             | <span data-ttu-id="7666e-117">Autentica somente no início de cada chamada de procedimento remoto quando o servidor recebe a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7666e-117">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="7666e-118">Não se aplica a chamadas de procedimento remoto feitas usando as sequências de protocolo baseadas em conexão (aquelas que começam com o prefixo "ncacn").</span><span class="sxs-lookup"><span data-stu-id="7666e-118">Does not apply to remote procedure calls made using the connection-based protocol sequences (those that start with the prefix "ncacn").</span></span> <span data-ttu-id="7666e-119">Se a sequência de protocolo em um identificador de associação for uma sequência de protocolo baseada em conexão e você especificar esse nível, essa rotina usará a \_ constante do PCT do nível de autenticação RPC C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7666e-119">If the protocol sequence in a binding handle is a connection-based protocol sequence and you specify this level, this routine instead uses the RPC\_C\_AUTHN\_LEVEL\_PKT constant.</span></span><br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="7666e-120"><dt>**\_PCT do \_ nível de autenticação RPC C \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7666e-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt></span></span> </dl>                                | <span data-ttu-id="7666e-121">Autentica somente que todos os dados recebidos são do cliente esperado.</span><span class="sxs-lookup"><span data-stu-id="7666e-121">Authenticates only that all data received is from the expected client.</span></span> <span data-ttu-id="7666e-122">Não valida os dados em si.</span><span class="sxs-lookup"><span data-stu-id="7666e-122">Does not validate the data itself.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="7666e-123"><dt>**\_integridade de \_ pkt do \_ nível \_ de \_ autenticação RPC C**</dt></span><span class="sxs-lookup"><span data-stu-id="7666e-123"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt></span></span> </dl> | <span data-ttu-id="7666e-124">Autentica e verifica se nenhum dos dados transferidos entre o cliente e o servidor foi modificado.</span><span class="sxs-lookup"><span data-stu-id="7666e-124">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="7666e-125"><dt>**\_privacidade do \_ PCT do \_ nível \_ de \_ autenticação RPC C**</dt></span><span class="sxs-lookup"><span data-stu-id="7666e-125"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt></span></span> </dl>       | <span data-ttu-id="7666e-126">Inclui todos os níveis anteriores e garante que os dados de texto não criptografados só possam ser vistos pelo remetente e pelo destinatário.</span><span class="sxs-lookup"><span data-stu-id="7666e-126">Includes all previous levels, and ensures clear text data can only be seen by the sender and the receiver.</span></span> <span data-ttu-id="7666e-127">No caso local, isso envolve o uso de um canal seguro.</span><span class="sxs-lookup"><span data-stu-id="7666e-127">In the local case, this involves using a secure channel.</span></span> <span data-ttu-id="7666e-128">No caso remoto, isso envolve a criptografia do valor do argumento de cada chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="7666e-128">In the remote case, this involves encrypting the argument value of each remote procedure call.</span></span><br/>                                                                                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="7666e-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="7666e-129">Remarks</span></span>

<span data-ttu-id="7666e-130">Independentemente do valor especificado pela constante, **Ncalrpc** sempre usa a privacidade do \_ PCT de nível de autenticação RPC C \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7666e-130">Regardless of the value specified by the constant, **ncalrpc** always uses RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

## <a name="requirements"></a><span data-ttu-id="7666e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7666e-131">Requirements</span></span>



| <span data-ttu-id="7666e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7666e-132">Requirement</span></span> | <span data-ttu-id="7666e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7666e-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7666e-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7666e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7666e-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7666e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7666e-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7666e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7666e-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7666e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7666e-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7666e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7666e-139"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="7666e-139"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7666e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7666e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7666e-141">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="7666e-141">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="7666e-142">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="7666e-142">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="7666e-143">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="7666e-143">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[<span data-ttu-id="7666e-144">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="7666e-144">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="7666e-145">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="7666e-145">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="7666e-146">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="7666e-146">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="7666e-147">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="7666e-147">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





