---
description: Contém informações sobre o perfil de conexão 802.1 X usado no momento para autenticação 802.1 X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: Estrutura de ONEX_CONNECTION_PROFILE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761419"
---
# <a name="onex_connection_profile-structure"></a><span data-ttu-id="63d66-103">Estrutura de perfil de \_ conexão Onex \_</span><span class="sxs-lookup"><span data-stu-id="63d66-103">ONEX\_CONNECTION\_PROFILE structure</span></span>

<span data-ttu-id="63d66-104">A estrutura de **\_ \_ perfil de conexão Onex** contém informações sobre o perfil de conexão 802.1 x usado atualmente para autenticação 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-104">The **ONEX\_CONNECTION\_PROFILE** structure contains information on the 802.1X connection profile currently used for 802.1X authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63d66-105">Syntax</span></span>


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a><span data-ttu-id="63d66-106">Membros</span><span class="sxs-lookup"><span data-stu-id="63d66-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="63d66-107">**DW**</span><span class="sxs-lookup"><span data-stu-id="63d66-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-108">A versão desta estrutura **de \_ \_ perfil de conexão Onex** .</span><span class="sxs-lookup"><span data-stu-id="63d66-108">The version of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-109">**dwTotalLen**</span><span class="sxs-lookup"><span data-stu-id="63d66-109">**dwTotalLen**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-110">O comprimento, em bytes, dessa estrutura **de \_ \_ perfil de conexão Onex** .</span><span class="sxs-lookup"><span data-stu-id="63d66-110">The length, in bytes, of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-111">**fOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="63d66-111">**fOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-112">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwOneXSupplicantFlags** .</span><span class="sxs-lookup"><span data-stu-id="63d66-112">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwOneXSupplicantFlags** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-113">**fsupplicantMode**</span><span class="sxs-lookup"><span data-stu-id="63d66-113">**fsupplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-114">Indica se a estrutura de **\_ \_ perfil de conexão Onex** contém dados válidos no membro **suplicante** .</span><span class="sxs-lookup"><span data-stu-id="63d66-114">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **supplicantMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-115">**fauthMode**</span><span class="sxs-lookup"><span data-stu-id="63d66-115">**fauthMode**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-116">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **AuthMode** .</span><span class="sxs-lookup"><span data-stu-id="63d66-116">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **authMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-117">**fHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="63d66-117">**fHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-118">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwHeldPeriod** .</span><span class="sxs-lookup"><span data-stu-id="63d66-118">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwHeldPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-119">**fAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="63d66-119">**fAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-120">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwAuthPeriod** .</span><span class="sxs-lookup"><span data-stu-id="63d66-120">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwAuthPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-121">**fStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="63d66-121">**fStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-122">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwStartPeriod** .</span><span class="sxs-lookup"><span data-stu-id="63d66-122">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwStartPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-123">**fMaxStart**</span><span class="sxs-lookup"><span data-stu-id="63d66-123">**fMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-124">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwMaxStart** .</span><span class="sxs-lookup"><span data-stu-id="63d66-124">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxStart** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-125">**fMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="63d66-125">**fMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-126">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwMaxAuthFailures** .</span><span class="sxs-lookup"><span data-stu-id="63d66-126">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxAuthFailures** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-127">**fNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="63d66-127">**fNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-128">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwNetworkAuthTimeout** .</span><span class="sxs-lookup"><span data-stu-id="63d66-128">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthTimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-129">**fAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="63d66-129">**fAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-130">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **bAllowLogonDialogs** .</span><span class="sxs-lookup"><span data-stu-id="63d66-130">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bAllowLogonDialogs** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-131">**fNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="63d66-131">**fNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-132">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **dwNetworkAuthWithUITimeout** .</span><span class="sxs-lookup"><span data-stu-id="63d66-132">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthWithUITimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-133">**fUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="63d66-133">**fUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-134">Indica se a estrutura do **\_ \_ perfil de conexão Onex** contém dados válidos no membro **bUserBasedVLan** .</span><span class="sxs-lookup"><span data-stu-id="63d66-134">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bUserBasedVLan** member.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-135">**dwOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="63d66-135">**dwOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-136">Um conjunto de sinalizadores 802.1 X que podem estar presentes no perfil.</span><span class="sxs-lookup"><span data-stu-id="63d66-136">A set of 802.1X flags that can be present in the profile.</span></span> <span data-ttu-id="63d66-137">Esses sinalizadores são reservados para uso interno pelo módulo de autenticação 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="63d66-137">These flags are reserved for internal use by the 802.1X authentication module.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-138">**suplicable**</span><span class="sxs-lookup"><span data-stu-id="63d66-138">**supplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-139">O elemento suplicamode no esquema 802.1 X que especifica o método de transmissão usado para EAPOL-Start mensagens.</span><span class="sxs-lookup"><span data-stu-id="63d66-139">The supplicantMode element in the 802.1X schema that specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="63d66-140">Para obter mais informações, consulte o [**elemento suplicante (Onex)**](onexschema-supplicantmode-onex-element.md) no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-140">For more information, see the [**supplicantMode (OneX) Element**](onexschema-supplicantmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="63d66-141">Valor</span><span class="sxs-lookup"><span data-stu-id="63d66-141">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="63d66-142">Significado</span><span class="sxs-lookup"><span data-stu-id="63d66-142">Meaning</span></span>                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <span data-ttu-id="63d66-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63d66-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="63d66-144">EAPOL-Start mensagens não são transmitidas.</span><span class="sxs-lookup"><span data-stu-id="63d66-144">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="63d66-145">Válido somente para perfis de LAN com fio.</span><span class="sxs-lookup"><span data-stu-id="63d66-145">Valid for wired LAN profiles only.</span></span><br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <span data-ttu-id="63d66-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="63d66-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="63d66-147">O cliente determina quando enviar EAPOL-Start pacotes com base na capacidade de rede.</span><span class="sxs-lookup"><span data-stu-id="63d66-147">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="63d66-148">EAPOL-Start mensagens são enviadas somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="63d66-148">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="63d66-149">Válido somente para perfis de LAN com fio.</span><span class="sxs-lookup"><span data-stu-id="63d66-149">Valid for wired LAN profiles only.</span></span><br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <span data-ttu-id="63d66-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="63d66-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="63d66-151">EAPOL-Start mensagens são transmitidas conforme especificado pelo 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="63d66-151">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="63d66-152">Válido para perfis de LAN com e sem fio.</span><span class="sxs-lookup"><span data-stu-id="63d66-152">Valid for both wired and wireless LAN profiles.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="63d66-153">**AuthMode**</span><span class="sxs-lookup"><span data-stu-id="63d66-153">**authMode**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-154">O elemento AuthMode no esquema 802.1 X que especifica o tipo de credenciais usado para autenticação 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="63d66-154">The authMode element in the 802.1X schema that specifies the type of credentials used for 802.1X authentication.</span></span> <span data-ttu-id="63d66-155">Para obter mais informações, consulte o [**elemento AuthMode (Onex)**](onexschema-authmode-onex-element.md) no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-155">For more information, see the [**authMode (OneX) Element**](onexschema-authmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="63d66-156">Valor</span><span class="sxs-lookup"><span data-stu-id="63d66-156">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="63d66-157">Significado</span><span class="sxs-lookup"><span data-stu-id="63d66-157">Meaning</span></span>                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <span data-ttu-id="63d66-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63d66-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="63d66-159">Use as credenciais do computador ou do usuário.</span><span class="sxs-lookup"><span data-stu-id="63d66-159">Use machine or user credentials.</span></span> <span data-ttu-id="63d66-160">Quando um usuário faz logon, as credenciais do usuário são usadas para autenticação.</span><span class="sxs-lookup"><span data-stu-id="63d66-160">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="63d66-161">Quando nenhum usuário está conectado, as credenciais do computador são usadas.</span><span class="sxs-lookup"><span data-stu-id="63d66-161">When no user is logged on, machine credentials are used.</span></span><br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <span data-ttu-id="63d66-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="63d66-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="63d66-163">Use somente as credenciais do computador.</span><span class="sxs-lookup"><span data-stu-id="63d66-163">Use machine credentials only.</span></span><br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <span data-ttu-id="63d66-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="63d66-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="63d66-165">Usar somente as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="63d66-165">Use user credentials only.</span></span><br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <span data-ttu-id="63d66-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="63d66-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span></span> </dl>                                 | <span data-ttu-id="63d66-167">Use somente credenciais de convidado (vazias).</span><span class="sxs-lookup"><span data-stu-id="63d66-167">Use guest (empty) credentials only.</span></span><br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <span data-ttu-id="63d66-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="63d66-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="63d66-169">As credenciais a serem usadas não estão especificadas.</span><span class="sxs-lookup"><span data-stu-id="63d66-169">Credentials to use are not specified.</span></span><br/>                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="63d66-170">**dwHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="63d66-170">**dwHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-171">O elemento heldPeriod no esquema 802.1 X que especifica o período de tempo, em segundos, no qual um cliente não tentará realizar a autenticação novamente após uma tentativa de autenticação com falha.</span><span class="sxs-lookup"><span data-stu-id="63d66-171">The heldPeriod element in the 802.1X schema that specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span> <span data-ttu-id="63d66-172">Para obter mais informações, consulte o [**elemento heldPeriod (Onex)**](onexschema-heldperiod-onex-element.md) no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-172">For more information, see the [**heldPeriod (OneX) Element**](onexschema-heldperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-173">**dwAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="63d66-173">**dwAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-174">O elemento authPeriod no esquema 802.1 X que especifica o período máximo de tempo, em segundos, no qual um cliente aguarda uma resposta do autenticador.</span><span class="sxs-lookup"><span data-stu-id="63d66-174">The authPeriod element in the 802.1X schema that specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="63d66-175">Se uma resposta não for recebida dentro do período especificado, o cliente assumirá que não há um autenticador presente na rede.</span><span class="sxs-lookup"><span data-stu-id="63d66-175">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="63d66-176">Para obter mais informações, consulte o [**elemento authPeriod (Onex)**](onexschema-authperiod-onex-element.md) no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-176">For more information, see the [**authPeriod (OneX) Element**](onexschema-authperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-177">**dwStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="63d66-177">**dwStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-178">O elemento startPeriod no esquema 802.1 X que especifica o período de tempo, em segundos, a aguardar antes de um EAPOL-Start ser enviado.</span><span class="sxs-lookup"><span data-stu-id="63d66-178">The startPeriod element in the 802.1X schema that specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="63d66-179">Uma mensagem de EAPOL-Start é enviada para iniciar o processo de autenticação 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="63d66-179">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span> <span data-ttu-id="63d66-180">Para obter mais informações, consulte o [**elemento startPeriod (Onex)**](onexschema-startperiod-onex-element.md) no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-180">For more information, see the [**startPeriod (OneX) Element**](onexschema-startperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-181">**dwMaxStart**</span><span class="sxs-lookup"><span data-stu-id="63d66-181">**dwMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-182">O elemento maxStart no esquema 802.1 X que especifica o número máximo de EAPOL-Start mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="63d66-182">The maxStart element in the 802.1X schema that specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="63d66-183">Depois que o número máximo de mensagens de EAPOL-Start tiver sido enviado, o cliente assumirá que não há um autenticador presente na rede.</span><span class="sxs-lookup"><span data-stu-id="63d66-183">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="63d66-184">Para obter mais informações, consulte o [**elemento maxStart (Onex)**](onexschema-maxstart-onex-element.md) no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-184">For more information, see the [**maxStart (OneX) Element**](onexschema-maxstart-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-185">**dwMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="63d66-185">**dwMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-186">O elemento maxAuthFailures no esquema 802.1 X que especifica o número máximo de falhas de autenticação permitidas para um conjunto de credenciais.</span><span class="sxs-lookup"><span data-stu-id="63d66-186">The maxAuthFailures element in the 802.1X schema that specifies the maximum number of authentication failures allowed for a set of credentials.</span></span> <span data-ttu-id="63d66-187">Para obter mais informações, consulte o elemento [**maxAuthFailures (Onex)**](onexschema-maxauthfailures-onex-element.md) no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-187">For more information, see the [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-188">**dwNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="63d66-188">**dwNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-189">O tempo, em segundos, para aguardar a conclusão da autenticação 802.1 X antes de o logon normal continuar.</span><span class="sxs-lookup"><span data-stu-id="63d66-189">The time, in seconds, to wait for 802.1X authentication completion before normal logon proceeds.</span></span> <span data-ttu-id="63d66-190">Esse valor é usado em cenários de logon único (SSO).</span><span class="sxs-lookup"><span data-stu-id="63d66-190">This value is used in single signon (SSO) scenarios.</span></span> <span data-ttu-id="63d66-191">Esse valor usa como padrão 10 segundos em um perfil 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="63d66-191">This value defaults to 10 seconds in an 802.1X profile.</span></span> <span data-ttu-id="63d66-192">Para obter mais informações, consulte o [**elemento maxDelay (logon único)**](onexschema-maxdelay-singlesignon-element.md) no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-192">For more information, see the [**maxDelay (singleSignOn) Element**](onexschema-maxdelay-singlesignon-element.md) in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-193">**dwNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="63d66-193">**dwNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-194">O tempo de duração máximo, em segundos, para aguardar uma conexão caso uma caixa de diálogo de interface do usuário que requer entrada do usuário seja exibida durante o SSO por logon.</span><span class="sxs-lookup"><span data-stu-id="63d66-194">The maximum duration time, in seconds, to wait for a connection in case a user interface dialog box that requires user input is displayed during the per-logon SSO.</span></span>

<span data-ttu-id="63d66-195">No Windows Vista com SP1 e posterior, esse valor é codificado para 10 minutos e não é configurável.</span><span class="sxs-lookup"><span data-stu-id="63d66-195">On Windows Vista with SP1 and later, this value is hardcoded to 10 minutes and is not configurable.</span></span> <span data-ttu-id="63d66-196">No Windows Vista versão para fabricação, esse valor usa como padrão 60 segundos em um perfil 802.1 X e foi controlado pelo elemento **maxDelayWithAdditionalDialogs** no esquema.</span><span class="sxs-lookup"><span data-stu-id="63d66-196">On Windows Vista Release to Manufacturing, this value defaults to 60 seconds in an 802.1X profile and was controlled by the **maxDelayWithAdditionalDialogs** element in the schema.</span></span>

<span data-ttu-id="63d66-197">No Windows Vista com SP1 e posterior, o elemento **maxDelayWithAdditionalDialogs** no esquema 802.1 x é ignorado e preterido.</span><span class="sxs-lookup"><span data-stu-id="63d66-197">On Windows Vista with SP1 and later, the **maxDelayWithAdditionalDialogs** element in the 802.1X schema is ignored and deprecated.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-198">**bAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="63d66-198">**bAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-199">Um valor que especifica se as caixas de diálogo EAP devem ser exibidas ao usar o SSO pré-logon.</span><span class="sxs-lookup"><span data-stu-id="63d66-199">A value that specifies whether to allow EAP dialogs to be displayed when using pre-logon SSO.</span></span> <span data-ttu-id="63d66-200">Para obter mais informações, consulte o elemento **allowAdditionalDialogs** no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-200">For more information, see the **allowAdditionalDialogs** element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="63d66-201">**bUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="63d66-201">**bUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="63d66-202">O elemento userBasedVirtualLan no esquema 802.1 X que especifica se a VLAN (LAN virtual) usada pelo dispositivo muda com base nas credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="63d66-202">The userBasedVirtualLan element in the 802.1X schema that specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="63d66-203">Alguns dispositivos de NAS (servidor de acesso à rede) alteram a VLAN após a autenticação de um usuário.</span><span class="sxs-lookup"><span data-stu-id="63d66-203">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="63d66-204">Quando userBasedVirtualLan for TRUE, o NAS poderá alterar a VLAN de um dispositivo após a autenticação de um usuário.</span><span class="sxs-lookup"><span data-stu-id="63d66-204">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span> <span data-ttu-id="63d66-205">Para obter mais informações, consulte o [**elemento userBasedVirtualLan (logon único)**](onexschema-userbasedvirtuallan-singlesignon-element.md) no esquema 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-205">For more information, see the [**userBasedVirtualLan (singleSignOn) Element**](onexschema-userbasedvirtuallan-singlesignon-element.md) in the 802.1X scheme.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63d66-206">Comentários</span><span class="sxs-lookup"><span data-stu-id="63d66-206">Remarks</span></span>

<span data-ttu-id="63d66-207">A estrutura do **\_ \_ perfil de conexão Onex** é usada pelo módulo 802.1 x, um novo componente de configuração sem fio com suporte no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="63d66-207">The **ONEX\_CONNECTION\_PROFILE** structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and later.</span></span>

<span data-ttu-id="63d66-208">Os [**\_ dados de \_ atualização \_ do resultado Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contêm informações sobre uma alteração de status para a autenticação 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-208">The [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contains information on a status change to 802.1X authentication.</span></span> <span data-ttu-id="63d66-209">A estrutura de dados de atualização de resultado de Onex é retornada quando o membro de **notificação** da estrutura de [**\_ \_ dados de notificação**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) de WLAN é  **802.1x de origem de notificação de WLAN \_ \_ \_** e o membro NotificationCode da estrutura de **dados de \_ notificação \_ de WLAN** para notificação recebida é OneXNotificationTypeResultUpdate. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63d66-209">The **ONEX\_RESULT\_UPDATE\_DATA** structure is returned when the **NotificationSource** member of the [**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) structure is **WLAN\_NOTIFICATION\_SOURCE\_ONEX** and the **NotificationCode** member of the **WLAN\_NOTIFICATION\_DATA** structure for received notification is **OneXNotificationTypeResultUpdate**.</span></span> <span data-ttu-id="63d66-210">Para essa notificação, o membro **pData** da estrutura **de \_ \_ dados de notificação de WLAN** aponta para uma estrutura de **\_ \_ \_ dados de atualização de resultado de Onex** que contém informações sobre a alteração do status de autenticação 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="63d66-210">For this notification, the **pData** member of the **WLAN\_NOTIFICATION\_DATA** structure points to an **ONEX\_RESULT\_UPDATE\_DATA** structure that contains information on the 802.1X authentication status change.</span></span>

<span data-ttu-id="63d66-211">Se o membro **fOneXAuthParams** na estrutura [**de \_ \_ \_ dados de atualização de resultado de Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) for definido, o membro **authParams** da estrutura de **\_ \_ \_ dados de atualização do resultado de Onex** conterá uma estrutura de [**\_ \_ Blob variável de Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) com uma estrutura de [**\_ \_ parâmetros de autenticação Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) inserida a partir do membro **dwOffset** do **\_ \_ BLOB da variável Onex**.</span><span class="sxs-lookup"><span data-stu-id="63d66-211">If the **fOneXAuthParams** member in the [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) structure is set, then the **authParams** member of the **ONEX\_RESULT\_UPDATE\_DATA** structure contains an [**ONEX\_VARIABLE\_BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) structure with an [**ONEX\_AUTH\_PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span> <span data-ttu-id="63d66-212">O membro **oneXConnProfile** da estrutura **de \_ \_ parâmetros de autenticação Onex** contém uma estrutura de **\_ \_ Blob variável de Onex** com uma estrutura de **\_ \_ perfil de conexão Onex** inserida a partir do membro **dwOffset** do **\_ \_ BLOB da variável Onex**.</span><span class="sxs-lookup"><span data-stu-id="63d66-212">The **oneXConnProfile** member of the **ONEX\_AUTH\_PARAMS** structure contains an **ONEX\_VARIABLE\_BLOB** structure with an **ONEX\_CONNECTION\_PROFILE** structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span>

<span data-ttu-id="63d66-213">A estrutura do **\_ \_ perfil de conexão Onex** não está definida em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="63d66-213">The **ONEX\_CONNECTION\_PROFILE** structure is not defined in a public header file.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d66-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63d66-214">Requirements</span></span>



| <span data-ttu-id="63d66-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="63d66-215">Requirement</span></span> | <span data-ttu-id="63d66-216">Valor</span><span class="sxs-lookup"><span data-stu-id="63d66-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63d66-217">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63d66-217">Minimum supported client</span></span><br/> | <span data-ttu-id="63d66-218">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63d66-218">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63d66-219">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63d66-219">Minimum supported server</span></span><br/> | <span data-ttu-id="63d66-220">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63d66-220">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63d66-221">Confira também</span><span class="sxs-lookup"><span data-stu-id="63d66-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d66-222">Sobre a arquitetura do ACM</span><span class="sxs-lookup"><span data-stu-id="63d66-222">About the ACM Architecture</span></span>](about-the-acm-architecture.md)
</dt> <dt>

[<span data-ttu-id="63d66-223">Esquema OneX</span><span class="sxs-lookup"><span data-stu-id="63d66-223">OneX Schema</span></span>](onexschema-schema.md)
</dt> <dt>

[<span data-ttu-id="63d66-224">**Elemento AuthMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="63d66-224">**authMode (OneX) Element**</span></span>](onexschema-authmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="63d66-225">**Elemento authPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="63d66-225">**authPeriod (OneX) Element**</span></span>](onexschema-authperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="63d66-226">**Elemento heldPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="63d66-226">**heldPeriod (OneX) Element**</span></span>](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="63d66-227">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="63d66-227">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[<span data-ttu-id="63d66-228">**Elemento maxStart (OneX)**</span><span class="sxs-lookup"><span data-stu-id="63d66-228">**maxStart (OneX) Element**</span></span>](onexschema-maxstart-onex-element.md)
</dt> <dt>

[<span data-ttu-id="63d66-229">**Elemento startPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="63d66-229">**startPeriod (OneX) Element**</span></span>](onexschema-startperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="63d66-230">**Elemento suplicable (OneX)**</span><span class="sxs-lookup"><span data-stu-id="63d66-230">**supplicantMode (OneX) Element**</span></span>](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="63d66-231">**Elemento userBasedVirtualLan (logon único)**</span><span class="sxs-lookup"><span data-stu-id="63d66-231">**userBasedVirtualLan (singleSignOn) Element**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[<span data-ttu-id="63d66-232">**\_parâmetros de autenticação Onex \_**</span><span class="sxs-lookup"><span data-stu-id="63d66-232">**ONEX\_AUTH\_PARAMS**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[<span data-ttu-id="63d66-233">**\_tipo de notificação Onex \_**</span><span class="sxs-lookup"><span data-stu-id="63d66-233">**ONEX\_NOTIFICATION\_TYPE**</span></span>](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[<span data-ttu-id="63d66-234">**\_dados de \_ atualização de resultados de Onex \_**</span><span class="sxs-lookup"><span data-stu-id="63d66-234">**ONEX\_RESULT\_UPDATE\_DATA**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[<span data-ttu-id="63d66-235">**Elemento de esquema OneX**</span><span class="sxs-lookup"><span data-stu-id="63d66-235">**OneX Schema Element**</span></span>](onexschema-onex-element.md)
</dt> <dt>

[<span data-ttu-id="63d66-236">**\_BLOB da variável de Onex \_**</span><span class="sxs-lookup"><span data-stu-id="63d66-236">**ONEX\_VARIABLE\_BLOB**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

<span data-ttu-id="63d66-237">[**\_dados de notificação da WLAN \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63d66-237">[**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="63d66-238">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="63d66-238">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
