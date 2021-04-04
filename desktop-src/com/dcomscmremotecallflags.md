---
title: DCOMSCMRemoteCallFlags
description: Controla o comportamento de chamadas do Gerenciador de controle de serviço (DCOMSCM) local DCOM para um DCOMSCM remoto.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- COM valor do registro DCOMSCMRemoteCallFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008420"
---
# <a name="dcomscmremotecallflags"></a><span data-ttu-id="d15c8-104">DCOMSCMRemoteCallFlags</span><span class="sxs-lookup"><span data-stu-id="d15c8-104">DCOMSCMRemoteCallFlags</span></span>

<span data-ttu-id="d15c8-105">Controla o comportamento de chamadas do Gerenciador de controle de serviço (DCOMSCM) local DCOM para um DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="d15c8-105">Controls the behavior of calls from the local DCOM Service Control Manager (DCOMSCM) to a remote DCOMSCM.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d15c8-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="d15c8-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a><span data-ttu-id="d15c8-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d15c8-107">Remarks</span></span>

<span data-ttu-id="d15c8-108">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d15c8-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="d15c8-109">Valor</span><span class="sxs-lookup"><span data-stu-id="d15c8-109">Value</span></span> | <span data-ttu-id="d15c8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d15c8-110">Description</span></span>                                       |
|-------|---------------------------------------------------|
| <span data-ttu-id="d15c8-111">0x1</span><span class="sxs-lookup"><span data-stu-id="d15c8-111">0x1</span></span>   | <span data-ttu-id="d15c8-112">**a \_ ativação do DCOMSCM \_ usa \_ todos os \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="d15c8-112">**DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES**</span></span>  |
| <span data-ttu-id="d15c8-113">0x2</span><span class="sxs-lookup"><span data-stu-id="d15c8-113">0x2</span></span>   | <span data-ttu-id="d15c8-114">**\_ativação DCOMSCM \_ \_ não permitir chamada não segura \_**</span><span class="sxs-lookup"><span data-stu-id="d15c8-114">**DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL**</span></span> |
| <span data-ttu-id="d15c8-115">0x4</span><span class="sxs-lookup"><span data-stu-id="d15c8-115">0x4</span></span>   | <span data-ttu-id="d15c8-116">**DCOMSCM \_ resolver \_ usar \_ todos os \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="d15c8-116">**DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES**</span></span>     |
| <span data-ttu-id="d15c8-117">0x8</span><span class="sxs-lookup"><span data-stu-id="d15c8-117">0x8</span></span>   | <span data-ttu-id="d15c8-118">**DCOMSCM \_ resolver \_ \_ não permitir chamada não segura \_**</span><span class="sxs-lookup"><span data-stu-id="d15c8-118">**DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL**</span></span>    |
| <span data-ttu-id="d15c8-119">0x10</span><span class="sxs-lookup"><span data-stu-id="d15c8-119">0x10</span></span>  | <span data-ttu-id="d15c8-120">**DCOMSCM \_ ping \_ use \_ mid \_ AUTHNSERVICE**</span><span class="sxs-lookup"><span data-stu-id="d15c8-120">**DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE**</span></span>         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a><span data-ttu-id="d15c8-121">DCOMSCM \_ ativação \_ use \_ todas as \_ AUTHNSERVICES descrição</span><span class="sxs-lookup"><span data-stu-id="d15c8-121">DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="d15c8-122">Quando o cliente emite uma solicitação de ativação que usa as configurações de segurança padrão, o DCOMSCM local usa o serviço de autenticação Negotiate ao fazer a chamada RPC de ativação para o DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="d15c8-122">When the client issues an activation request that uses the default security settings, the local DCOMSCM uses the Negotiate authentication service when making the activation RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="d15c8-123">Se a chamada falhar, o DCOMSCM local fará a chamada RPC de ativação usando sem segurança.</span><span class="sxs-lookup"><span data-stu-id="d15c8-123">If the call fails, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="d15c8-124">**Windows Server 2003 e Windows XP/2000:** Se a chamada RPC de ativação que usa o serviço de autenticação Negotiate falhar, o DCOMSCM local fará a chamada RPC de ativação usando Kerberos, NTLM ou outros provedores de segurança configurados.</span><span class="sxs-lookup"><span data-stu-id="d15c8-124">**Windows Server 2003 and Windows XP/2000:** If the activation RPC call that uses the Negotiate authentication service fails, the local DCOMSCM makes the activation RPC call using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="d15c8-125">Se nenhum provedor de segurança funcionar, o DCOMSCM local fará a chamada RPC de ativação usando sem segurança.</span><span class="sxs-lookup"><span data-stu-id="d15c8-125">If no security providers work, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="d15c8-126">Ao definir esse sinalizador, o DCOMSCM local no Windows Vista ou superior pode ser feito para se comportar como sistemas anteriores ao vista.</span><span class="sxs-lookup"><span data-stu-id="d15c8-126">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="d15c8-127">Não é recomendável definir esse sinalizador, a menos que necessário por motivos de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="d15c8-127">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a><span data-ttu-id="d15c8-128">\_Descrição da \_ \_ chamada não segura de DCOMSCM Activation inallow \_</span><span class="sxs-lookup"><span data-stu-id="d15c8-128">DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="d15c8-129">Se o sinalizador de **\_ \_ \_ \_ chamada não segura de ativação DCOMSCM** for definido, o DCOMSCM local não fará uma chamada RPC de ativação não segura.</span><span class="sxs-lookup"><span data-stu-id="d15c8-129">If the **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure activation RPC call.</span></span> <span data-ttu-id="d15c8-130">Para permitir que os clientes façam solicitações de ativação com configurações de segurança não padrão, especifique a estrutura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) ao fazer a solicitação de ativação.</span><span class="sxs-lookup"><span data-stu-id="d15c8-130">To enable clients to make activation requests with non-default security settings, specify the [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure when making the activation request.</span></span> <span data-ttu-id="d15c8-131">Nesse caso, a **ativação do \_ DCOMSCM \_ usa \_ todas as \_ AUTHNSERVICES** e a **ativação do DCOMSCM não permitir sinalizadores de \_ \_ \_ \_ chamada não seguros** são ignorados.</span><span class="sxs-lookup"><span data-stu-id="d15c8-131">In this case, the **DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES** and **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flags are ignored.</span></span>

<span data-ttu-id="d15c8-132">Não é recomendável definir esse sinalizador, a menos que todos os clientes e servidores na rede estejam totalmente autenticados.</span><span class="sxs-lookup"><span data-stu-id="d15c8-132">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_resolve_use_all_authnservices-description"></a><span data-ttu-id="d15c8-133">DCOMSCM \_ resolver \_ usar \_ todas as \_ AUTHNSERVICES descrição</span><span class="sxs-lookup"><span data-stu-id="d15c8-133">DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="d15c8-134">Quando o cliente desempacotar uma referência de objeto, o DCOMSCM local usará o serviço de autenticação Negotiate ao fazer a chamada RPC de resolução OXID para o DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="d15c8-134">When the client unmarshals an object reference, the local DCOMSCM uses the Negotiate authentication service when making the OXID Resolution RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="d15c8-135">Se a chamada falhar, o DCOMSCM local fará a chamada RPC de resolução OXID usando sem segurança.</span><span class="sxs-lookup"><span data-stu-id="d15c8-135">If the call fails, the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="d15c8-136">**Windows Server 2003 e Windows XP/2000:** Se a chamada RPC de resolução OXID usando o serviço de autenticação Negotiate falhar, o DCOMSCM local fará a chamada RPC de resolução OXID usando Kerberos, NTLM ou outros provedores de segurança configurados.</span><span class="sxs-lookup"><span data-stu-id="d15c8-136">**Windows Server 2003 and Windows XP/2000:** If the OXID Resolution RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the OXID Resolution RPC call by using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="d15c8-137">Se nenhum provedor de segurança funcionar, o DCOMSCM local fará a chamada RPC de resolução OXID usando sem segurança.</span><span class="sxs-lookup"><span data-stu-id="d15c8-137">If no security providers work, then the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="d15c8-138">Ao definir esse sinalizador, o DCOMSCM local no Windows Vista ou superior pode ser feito para se comportar como sistemas anteriores ao vista.</span><span class="sxs-lookup"><span data-stu-id="d15c8-138">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="d15c8-139">Não é recomendável definir esse sinalizador, a menos que necessário por motivos de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="d15c8-139">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a><span data-ttu-id="d15c8-140">DCOMSCM \_ resolver \_ \_ não permitir descrição da chamada não segura \_</span><span class="sxs-lookup"><span data-stu-id="d15c8-140">DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="d15c8-141">Se o sinalizador de **chamada não segura de DCOMSCM \_ resolver não \_ \_ seguro \_** estiver definido, o DCOMSCM local não fará uma chamada RPC de resolução oxid não segura.</span><span class="sxs-lookup"><span data-stu-id="d15c8-141">If the **DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure OXID Resolution RPC call.</span></span> <span data-ttu-id="d15c8-142">Além disso, o DCOMSCM local não faz uma chamada RPC de ping de coleta de lixo sem segurança.</span><span class="sxs-lookup"><span data-stu-id="d15c8-142">In addition, the local DCOMSCM does not make an unsecure garbage collection Ping RPC call.</span></span> <span data-ttu-id="d15c8-143">Não é recomendável definir esse sinalizador, a menos que todos os clientes e servidores na rede estejam totalmente autenticados.</span><span class="sxs-lookup"><span data-stu-id="d15c8-143">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_ping_use_mid_authnservice-description"></a><span data-ttu-id="d15c8-144">DCOMSCM \_ ping \_ use \_ média \_ AUTHNSERVICE descrição</span><span class="sxs-lookup"><span data-stu-id="d15c8-144">DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE Description</span></span>

<span data-ttu-id="d15c8-145">O DCOMSCM local usa o serviço de autenticação Negotiate ao fazer a chamada RPC de ping de coleta de lixo para o DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="d15c8-145">The local DCOMSCM uses the Negotiate authentication service when making the garbage-collection Ping RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="d15c8-146">Se a chamada falhar, o local DCOMSCM fará a chamada RPC de ping de coleta de lixo usando sem segurança.</span><span class="sxs-lookup"><span data-stu-id="d15c8-146">If the call fails, the local DCOMSCM makes the garbage-collection Ping RPC call using no security.</span></span>

<span data-ttu-id="d15c8-147">**Windows Server 2003 e Windows XP/2000:** Se a chamada RPC de ping de coleta de lixo usando o serviço de autenticação Negotiate falhar, o DCOMSCM local fará a chamada RPC de ping de coleta de lixo usando Kerberos, NTLM e outros provedores de segurança configurados.</span><span class="sxs-lookup"><span data-stu-id="d15c8-147">**Windows Server 2003 and Windows XP/2000:** If the garbage-collection Ping RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the garbage collection Ping RPC call by using Kerberos, NTLM, and other configured security providers.</span></span> <span data-ttu-id="d15c8-148">Se nenhum provedor de segurança funcionar, o DCOMSCM local fará a chamada RPC de ping de coleta de lixo usando sem segurança.</span><span class="sxs-lookup"><span data-stu-id="d15c8-148">If no security providers work, then the local DCOMSCM makes the garbage collection Ping RPC call using no security.</span></span>

<span data-ttu-id="d15c8-149">Ao definir esse sinalizador, o DCOMSCM local no Windows Vista ou superior pode ser feito para se comportar como sistemas anteriores ao vista.</span><span class="sxs-lookup"><span data-stu-id="d15c8-149">By setting this flag, the local DCOMSCM on Windows Vista or above can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="d15c8-150">Não é recomendável definir o sinalizador **DCOMSCM \_ de \_ uso \_ de \_ AUTHNSERVICE médio** , a menos que necessário por motivos de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="d15c8-150">It is not recommended to set the **DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE** flag unless required for compatibility reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d15c8-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d15c8-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d15c8-152">Autenticação para conexões remotas</span><span class="sxs-lookup"><span data-stu-id="d15c8-152">Authentication for Remote Connections</span></span>](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[<span data-ttu-id="d15c8-153">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="d15c8-153">EnableDCOM</span></span>](enabledcom.md)
</dt> <dt>

[<span data-ttu-id="d15c8-154">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="d15c8-154">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="d15c8-155">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="d15c8-155">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 