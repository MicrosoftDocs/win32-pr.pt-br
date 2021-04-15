---
title: Sinalizadores de método EAP (Eaptypes. h)
description: Os sinalizadores de método EAP são usados nas funções suplicante, autenticador e par para especificar comportamentos de uma sessão de autenticação EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454581"
---
# <a name="eap-method-flags"></a><span data-ttu-id="2c256-103">Sinalizadores de método EAP</span><span class="sxs-lookup"><span data-stu-id="2c256-103">EAP Method Flags</span></span>

<span data-ttu-id="2c256-104">Os sinalizadores de método EAP são usados nas funções suplicante, autenticador e par para especificar comportamentos de uma sessão de autenticação EAP.</span><span class="sxs-lookup"><span data-stu-id="2c256-104">The EAP method flags are used within the supplicant, authenticator, and peer functions to specify behaviors of an EAP authentication session.</span></span>

<dl> <dt>

<span data-ttu-id="2c256-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Sinalizador EAP \_ Reserved1**</span><span class="sxs-lookup"><span data-stu-id="2c256-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP\_FLAG\_Reserved1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2c256-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="2c256-107">Não use.</span><span class="sxs-lookup"><span data-stu-id="2c256-107">Do not use.</span></span> <span data-ttu-id="2c256-108">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2c256-108">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**\_sinalizador EAP \_ não \_ interativo**</span><span class="sxs-lookup"><span data-stu-id="2c256-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP\_FLAG\_NON\_INTERACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2c256-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="2c256-111">Não exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2c256-111">Do not display a user interface (UI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**\_logon do sinalizador EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2c256-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP\_FLAG\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-113">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2c256-113">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="2c256-114">Os dados do usuário foram obtidos do logon do Windows.</span><span class="sxs-lookup"><span data-stu-id="2c256-114">User data was obtained from Windows logon.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**\_visualização do sinalizador EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2c256-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP\_FLAG\_PREVIEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-116">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2c256-116">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="2c256-117">Mostrar a interface do usuário de credenciais antes de autenticar, mesmo que as credenciais armazenadas em cache estejam presentes.</span><span class="sxs-lookup"><span data-stu-id="2c256-117">Show credentials UI before authenticating, even if cached credentials are present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ SINALIZADOR \_ Reserved2**</span><span class="sxs-lookup"><span data-stu-id="2c256-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span> **EAP\_FLAG\_Reserved2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c256-119">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="2c256-120">Não use.</span><span class="sxs-lookup"><span data-stu-id="2c256-120">Do not use.</span></span> <span data-ttu-id="2c256-121">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2c256-121">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**\_autenticação do \_ computador do sinalizador EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2c256-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP\_FLAG\_MACHINE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-123">0x00000020</span><span class="sxs-lookup"><span data-stu-id="2c256-123">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="2c256-124">Usar autenticação no nível do computador; não definir esse sinalizador indica que a autenticação de nível de usuário está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="2c256-124">Use machine level authentication; not setting this flag indicates user level authentication is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**\_acesso de \_ convidado do sinalizador EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2c256-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP\_FLAG\_GUEST\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="2c256-126">0x00000040</span><span class="sxs-lookup"><span data-stu-id="2c256-126">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="2c256-127">Indica uma solicitação para fornecer acesso de convidado.</span><span class="sxs-lookup"><span data-stu-id="2c256-127">Indicates a request to provide guest access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Sinalizador EAP \_ Reserved3**</span><span class="sxs-lookup"><span data-stu-id="2c256-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP\_FLAG\_Reserved3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-129">0x00000080</span><span class="sxs-lookup"><span data-stu-id="2c256-129">0x00000080</span></span> 
</dt> <dt>



<span data-ttu-id="2c256-130">Não use.</span><span class="sxs-lookup"><span data-stu-id="2c256-130">Do not use.</span></span> <span data-ttu-id="2c256-131">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2c256-131">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ SINALIZADOR \_ Reserved4**</span><span class="sxs-lookup"><span data-stu-id="2c256-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span> **EAP\_FLAG\_Reserved4**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-133">0x00000100</span><span class="sxs-lookup"><span data-stu-id="2c256-133">0x00000100</span></span> 
</dt> <dt>



<span data-ttu-id="2c256-134">Não use.</span><span class="sxs-lookup"><span data-stu-id="2c256-134">Do not use.</span></span> <span data-ttu-id="2c256-135">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2c256-135">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**\_ \_ retomada \_ do sinalizador EAP da \_ hibernação**</span><span class="sxs-lookup"><span data-stu-id="2c256-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP\_FLAG\_RESUME\_FROM\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-137">0x00000200</span><span class="sxs-lookup"><span data-stu-id="2c256-137">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="2c256-138">Indica que esta é a primeira chamada após a atividade do computador ter sido retomada de um período de hibernação.</span><span class="sxs-lookup"><span data-stu-id="2c256-138">Indicates this is the first call after machine activity has resumed from a period of hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ SINALIZADOR \_ Reserved5**</span><span class="sxs-lookup"><span data-stu-id="2c256-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span> **EAP\_FLAG\_Reserved5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-140">0x00000400</span><span class="sxs-lookup"><span data-stu-id="2c256-140">0x00000400</span></span> 
</dt> <dt>



<span data-ttu-id="2c256-141">Não use.</span><span class="sxs-lookup"><span data-stu-id="2c256-141">Do not use.</span></span> <span data-ttu-id="2c256-142">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2c256-142">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Sinalizador EAP \_ Reserved6**</span><span class="sxs-lookup"><span data-stu-id="2c256-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP\_FLAG\_Reserved6**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-144">0x00000800</span><span class="sxs-lookup"><span data-stu-id="2c256-144">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="2c256-145">Não use.</span><span class="sxs-lookup"><span data-stu-id="2c256-145">Do not use.</span></span> <span data-ttu-id="2c256-146">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2c256-146">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_ \_ autenticação completa do sinalizador EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2c256-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP\_FLAG\_FULL\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-148">0x00001000</span><span class="sxs-lookup"><span data-stu-id="2c256-148">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="2c256-149">Indica que os métodos de túnel devem executar uma autenticação completa em vez de uma versão abreviada, como [EAP protegido (PEAP) reconexão rápida](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="2c256-149">Indicates that tunnel methods should perform a full authentication instead of an abbreviated version, such as [Protected EAP (PEAP) Fast Reconnect](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**o \_ sinalizador \_ EAP \_ prefere \_ credenciais Alt**</span><span class="sxs-lookup"><span data-stu-id="2c256-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP\_FLAG\_PREFER\_ALT\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="2c256-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="2c256-152">Indica que as credenciais passadas para [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) são preferenciais para todas as outras formas de recuperação de credencial, mesmo que os dados de configuração passados para a função atual solicitem um modo diferente de recuperação de credencial.</span><span class="sxs-lookup"><span data-stu-id="2c256-152">Indicates credentials passed into [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) are preferred to all other forms of credential retrieval, even if configuration data passed into the current function requests a different mode of credential retrieval.</span></span>

> [!Note]  
> <span data-ttu-id="2c256-153">Esse sinalizador só é usado pelo [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="2c256-153">This flag is only used by [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Sinalizador EAP \_ Reserved7**</span><span class="sxs-lookup"><span data-stu-id="2c256-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP\_FLAG\_Reserved7**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-155">0x00004000</span><span class="sxs-lookup"><span data-stu-id="2c256-155">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="2c256-156">Não use.</span><span class="sxs-lookup"><span data-stu-id="2c256-156">Do not use.</span></span> <span data-ttu-id="2c256-157">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2c256-157">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**\_alteração do \_ estado de integridade do sinalizador EAP peer \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c256-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**EAP\_PEER\_FLAG\_HEALTH\_STATE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-159">0x00008000</span><span class="sxs-lookup"><span data-stu-id="2c256-159">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="2c256-160">Indica que a causa da nova autenticação é um retorno de chamada NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) ); A NAP iniciou a sessão de autenticação porque o estado de integridade foi alterado.</span><span class="sxs-lookup"><span data-stu-id="2c256-160">Indicates the cause of re-authentication is a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) callback; NAP initiated the authentication session because the health state changed.</span></span> <span data-ttu-id="2c256-161">Esse sinalizador deve ser enviado somente quando essa função é chamada por um retorno de chamada [*NotificationHandler*](/previous-versions/windows/desktop/api) específico de NAP fornecido por uma chamada anterior para essa função.</span><span class="sxs-lookup"><span data-stu-id="2c256-161">This flag must be sent only when this function is called by a NAP-specific [*NotificationHandler*](/previous-versions/windows/desktop/api) callback provided by a previous call to this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_ \_ interface do usuário suprimir sinalizador EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2c256-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP\_FLAG\_SUPRESS\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-163">0x00010000</span><span class="sxs-lookup"><span data-stu-id="2c256-163">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="2c256-164">Continue a autenticação com as informações disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2c256-164">Continue authentication with available information.</span></span> <span data-ttu-id="2c256-165">Se a autenticação não puder continuar, falhará.</span><span class="sxs-lookup"><span data-stu-id="2c256-165">If the authentication cannot proceed then fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_pré- \_ \_ logon do sinalizador EAP**</span><span class="sxs-lookup"><span data-stu-id="2c256-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP\_FLAG\_PRE\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-167">0x00020000</span><span class="sxs-lookup"><span data-stu-id="2c256-167">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="2c256-168">Indica que o EAPHost deve fornecer SSO (logon único).</span><span class="sxs-lookup"><span data-stu-id="2c256-168">Indicates that EAPHost should provide Single-Sign-On (SSO).</span></span> <span data-ttu-id="2c256-169">Para obter mais informações, consulte [SSO e PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="2c256-169">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**\_autenticação de \_ usuário do sinalizador EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2c256-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP\_FLAG\_USER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-171">0x00040000</span><span class="sxs-lookup"><span data-stu-id="2c256-171">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="2c256-172">Indica a autenticação de nível de usuário para métodos herdados que não podem definir o **\_ sinalizador EAP \_ \_ auth**.</span><span class="sxs-lookup"><span data-stu-id="2c256-172">Indicates user level authentication for legacy methods that cannot set **EAP\_FLAG\_MACHINE\_AUTH**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_sinalizador EAP \_ confg \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="2c256-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP\_FLAG\_CONFG\_READONLY**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="2c256-174">0x00080000</span><span class="sxs-lookup"><span data-stu-id="2c256-174">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="2c256-175">Indica que a configuração pode ser exibida, mas não atualizada.</span><span class="sxs-lookup"><span data-stu-id="2c256-175">Indicates the configuration can be viewed but not updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c256-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Sinalizador EAP \_ Reserved8**</span><span class="sxs-lookup"><span data-stu-id="2c256-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP\_FLAG\_Reserved8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c256-177">0x00100000</span><span class="sxs-lookup"><span data-stu-id="2c256-177">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="2c256-178">Não use.</span><span class="sxs-lookup"><span data-stu-id="2c256-178">Do not use.</span></span> <span data-ttu-id="2c256-179">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2c256-179">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c256-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c256-180">Requirements</span></span>



| <span data-ttu-id="2c256-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c256-181">Requirement</span></span> | <span data-ttu-id="2c256-182">Valor</span><span class="sxs-lookup"><span data-stu-id="2c256-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c256-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c256-183">Minimum supported client</span></span><br/> | <span data-ttu-id="2c256-184">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c256-184">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c256-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c256-185">Minimum supported server</span></span><br/> | <span data-ttu-id="2c256-186">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c256-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c256-187">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c256-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c256-188"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c256-188"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c256-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c256-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c256-190">Constantes do EAPHost comuns</span><span class="sxs-lookup"><span data-stu-id="2c256-190">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

