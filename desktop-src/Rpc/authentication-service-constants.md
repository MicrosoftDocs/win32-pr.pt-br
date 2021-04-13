---
title: Constantes de Authentication-Service (rpcdce. h)
description: As constantes do serviço de autenticação representam os serviços de autenticação passados para várias funções de tempo de execução.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499690"
---
# <a name="authentication-service-constants"></a><span data-ttu-id="e2cd3-103">Authentication-Service constantes</span><span class="sxs-lookup"><span data-stu-id="e2cd3-103">Authentication-Service Constants</span></span>

<span data-ttu-id="e2cd3-104">As constantes do serviço de autenticação representam os serviços de autenticação passados para várias funções de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-104">The authentication service constants represent the authentication services passed to various run-time functions.</span></span>

<span data-ttu-id="e2cd3-105">As constantes a seguir são valores válidos para o parâmetro *AuthnSvc* .</span><span class="sxs-lookup"><span data-stu-id="e2cd3-105">The following constants are valid values for the *AuthnSvc* parameter.</span></span>



| <span data-ttu-id="e2cd3-106">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e2cd3-106">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="e2cd3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2cd3-107">Description</span></span>                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <span data-ttu-id="e2cd3-108"><dt>**RPC \_ C \_ Authn \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-108"><dt>**RPC\_C\_AUTHN\_NONE**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="e2cd3-109">Sem autenticação.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-109">No authentication.</span></span><br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <span data-ttu-id="e2cd3-110"><dt>**RPC \_ C \_ Authn \_ DCE \_ privado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-110"><dt>**RPC\_C\_AUTHN\_DCE\_PRIVATE**</dt> <dt>1</dt></span></span> </dl>        | <span data-ttu-id="e2cd3-111">Use a autenticação de chave privada de DCE (ambiente de computação distribuída).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-111">Use Distributed Computing Environment (DCE) private key authentication.</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <span data-ttu-id="e2cd3-112"><dt>**RPC \_ C \_ Authn \_ DCE \_**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-112"><dt>**RPC\_C\_AUTHN\_DCE\_PUBLIC**</dt> <dt>2</dt></span></span> </dl>           | <span data-ttu-id="e2cd3-113">Autenticação de chave pública do DCE (reservada para uso futuro).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-113">DCE public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <span data-ttu-id="e2cd3-114"><dt>**RPC \_ C \_ Authn \_ Dec \_ público**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-114"><dt>**RPC\_C\_AUTHN\_DEC\_PUBLIC**</dt> <dt>4</dt></span></span> </dl>           | <span data-ttu-id="e2cd3-115">Autenticação de chave pública DEC (reservada para uso futuro).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-115">DEC public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <span data-ttu-id="e2cd3-116"><dt>**RPC \_ C \_ Authn \_ GSS \_ Negotiate**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-116"><dt>**RPC\_C\_AUTHN\_GSS\_NEGOTIATE**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="e2cd3-117">Use o [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-117">Use the [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span></span> <span data-ttu-id="e2cd3-118">Esse SSP negocia entre o uso dos provedores de suporte de segurança de protocolo NTLM e Kerberos (SSP).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-118">This SSP negotiates between the use of the NTLM and Kerberos protocol Security Support Providers (SSP).</span></span><br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <span data-ttu-id="e2cd3-119"><dt>**RPC \_ C \_ Authn \_ WinNT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-119"><dt>**RPC\_C\_AUTHN\_WINNT**</dt> <dt>10</dt></span></span> </dl>                          | <span data-ttu-id="e2cd3-120">Use o [SSP do Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-120">Use the [Microsoft NT LAN Manager (NTLM) SSP](/windows/desktop/SecAuthN/microsoft-ntlm).</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <span data-ttu-id="e2cd3-121"><dt>**RPC \_ C \_ Authn \_ GSS \_ Schannel**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-121"><dt>**RPC\_C\_AUTHN\_GSS\_SCHANNEL**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="e2cd3-122">Use o [SSP do Schannel](/windows/desktop/SecAuthN/secure-channel).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-122">Use the [Schannel SSP](/windows/desktop/SecAuthN/secure-channel).</span></span> <span data-ttu-id="e2cd3-123">Esse SSP dá suporte ao protocolo SSL, à tecnologia de comunicação privada (PCT) e ao protocolo TLS.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-123">This SSP supports Secure Socket Layer (SSL), private communication technology (PCT), and transport level security (TLS).</span></span><br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <span data-ttu-id="e2cd3-124"><dt>**RPC \_ C \_ Authn \_ GSS \_ Kerberos**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-124"><dt>**RPC\_C\_AUTHN\_GSS\_KERBEROS**</dt> <dt>16</dt></span></span> </dl>    | <span data-ttu-id="e2cd3-125">Use o [SSP do Microsoft Kerberos](/windows/desktop/SecAuthN/microsoft-kerberos).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-125">Use the [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span></span><br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <span data-ttu-id="e2cd3-126"><dt>**RPC \_ C \_ Authn \_ DPA**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-126"><dt>**RPC\_C\_AUTHN\_DPA**</dt> <dt>17</dt></span></span> </dl>                                | <span data-ttu-id="e2cd3-127">Usar a autenticação de senha distribuída (DPA).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-127">Use Distributed Password Authentication (DPA).</span></span><br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <span data-ttu-id="e2cd3-128"><dt>**RPC \_ C \_ Authn \_ MSN**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-128"><dt>**RPC\_C\_AUTHN\_MSN**</dt> <dt>18</dt></span></span> </dl>                                | <span data-ttu-id="e2cd3-129">Protocolo de autenticação SSP usado para a rede da Microsoft (MSN).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-129">Authentication protocol SSP used for the Microsoft Network (MSN).</span></span><br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <span data-ttu-id="e2cd3-130"><dt>**RPC \_ C \_ Authn \_ Digest**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-130"><dt>**RPC\_C\_AUTHN\_DIGEST**</dt> <dt>21</dt></span></span> </dl>                       | <span data-ttu-id="e2cd3-131">Windows XP ou posterior: usar o [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span><span class="sxs-lookup"><span data-stu-id="e2cd3-131">Windows XP or later: Use the [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span></span><br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <span data-ttu-id="e2cd3-132"><dt>**RPC \_ \_ \_ Nego de \_ extensão C Authn**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-132"><dt>**RPC\_C\_AUTHN\_NEGO\_EXTENDER**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="e2cd3-133">Windows 7 ou posterior: reservado.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-133">Windows 7 or later: Reserved.</span></span> <span data-ttu-id="e2cd3-134">Não usar</span><span class="sxs-lookup"><span data-stu-id="e2cd3-134">Do not use</span></span><br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <span data-ttu-id="e2cd3-135"><dt>**RPC \_ C \_ Authn \_ MQ**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-135"><dt>**RPC\_C\_AUTHN\_MQ**</dt> <dt>100</dt></span></span> </dl>                                  | <span data-ttu-id="e2cd3-136">Esse SSP fornece um wrapper compatível com SSPI para o protocolo de nível de transporte do MSMQ (fila de mensagens da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-136">This SSP provides an SSPI-compatible wrapper for the Microsoft Message Queue (MSMQ) transport-level protocol.</span></span><br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <span data-ttu-id="e2cd3-137"><dt>**RPC \_ C \_ Authn \_ padrão**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-137"><dt>**RPC\_C\_AUTHN\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl>            | <span data-ttu-id="e2cd3-138">Use o serviço de autenticação padrão.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-138">Use the default authentication service.</span></span><br/>                                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="e2cd3-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2cd3-139">Remarks</span></span>

<span data-ttu-id="e2cd3-140">Especifique \_ o RPC C \_ Authn \_ None para desativar a autenticação para chamadas de procedimento remoto feitas em um identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-140">Specify RPC\_C\_AUTHN\_NONE to turn off authentication for remote procedure calls made over a binding handle.</span></span> <span data-ttu-id="e2cd3-141">Quando você especifica \_ \_ o padrão RPC c Authn \_ , a biblioteca de tempo de execução RPC usa o \_ serviço de autenticação RPC c \_ Authn \_ WinNT para chamadas de procedimento remoto feitas usando o identificador de associação.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-141">When you specify RPC\_C\_AUTHN\_DEFAULT, the RPC run-time library uses the RPC\_C\_AUTHN\_WINNT authentication service for remote procedure calls made using the binding handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2cd3-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2cd3-142">Requirements</span></span>



| <span data-ttu-id="e2cd3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2cd3-143">Requirement</span></span> | <span data-ttu-id="e2cd3-144">Valor</span><span class="sxs-lookup"><span data-stu-id="e2cd3-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2cd3-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2cd3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e2cd3-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e2cd3-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e2cd3-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2cd3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e2cd3-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e2cd3-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e2cd3-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e2cd3-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2cd3-150"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2cd3-150"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2cd3-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2cd3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2cd3-152">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-152">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="e2cd3-153">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-153">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="e2cd3-154">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-154">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="e2cd3-155">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-155">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="e2cd3-156">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-156">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="e2cd3-157">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-157">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

