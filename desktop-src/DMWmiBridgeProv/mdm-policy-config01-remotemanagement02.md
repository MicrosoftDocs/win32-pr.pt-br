---
title: Classe MDM_Policy_Config01_RemoteManagement02
description: A política de MDM \_ \_ Config01 \_ RemoteManagement02 políticas de gerenciamento remoto.
ms.assetid: 2eabbf72-00a4-4c61-9ae1-ff49067cb502
keywords:
- Classe MDM_Policy_Config01_RemoteManagement02
- Classe MDM_Policy_Config01_RemoteManagement02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteManagement02
- MDM_Policy_Config01_RemoteManagement02.InstanceID
- MDM_Policy_Config01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76aa1a04735897d0b1c8f0e16572dd124b601c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824391"
---
# <a name="mdm_policy_config01_remotemanagement02-class"></a><span data-ttu-id="d575b-105">\_Classe MDM \_ Config01 \_ RemoteManagement02</span><span class="sxs-lookup"><span data-stu-id="d575b-105">MDM\_Policy\_Config01\_RemoteManagement02 class</span></span>

<span data-ttu-id="d575b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d575b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d575b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="d575b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d575b-108">A política de MDM \_ \_ Config01 \_ RemoteManagement02 políticas de gerenciamento remoto.</span><span class="sxs-lookup"><span data-stu-id="d575b-108">The MDM\_Policy\_Config01\_RemoteManagement02 remote management policies.</span></span>

<span data-ttu-id="d575b-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d575b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d575b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d575b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteManagement02
{
  string InstanceID;
  string ParentID;
  string AllowBasicAuthentication_Client;
  string AllowBasicAuthentication_Service;
  string AllowCredSSPAuthenticationClient;
  string AllowCredSSPAuthenticationService;
  string AllowRemoteServerManagement;
  string AllowUnencryptedTraffic_Client;
  string AllowUnencryptedTraffic_Service;
  string DisallowDigestAuthentication;
  string DisallowNegotiateAuthenticationClient;
  string DisallowNegotiateAuthenticationService;
  string DisallowStoringOfRunAsCredentials;
  string SpecifyChannelBindingTokenHardeningLevel;
  string TrustedHosts;
  string TurnOnCompatibilityHTTPListener;
  string TurnOnCompatibilityHTTPSListener;
};
```

## <a name="members"></a><span data-ttu-id="d575b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d575b-111">Members</span></span>

<span data-ttu-id="d575b-112">A **classe \_ \_ Config01 \_ RemoteManagement02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d575b-112">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="d575b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d575b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d575b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d575b-114">Properties</span></span>

<span data-ttu-id="d575b-115">A **classe \_ \_ Config01 \_ RemoteManagement02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d575b-115">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d575b-116">\_Cliente AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="d575b-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-119">\_Serviço AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="d575b-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-122">AllowCredSSPAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="d575b-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-125">AllowCredSSPAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="d575b-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-128">AllowRemoteServerManagement</span><span class="sxs-lookup"><span data-stu-id="d575b-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-131">\_Cliente AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="d575b-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-134">\_Serviço AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="d575b-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-137">DisallowDigestAuthentication</span><span class="sxs-lookup"><span data-stu-id="d575b-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-140">DisallowNegotiateAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="d575b-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-143">DisallowNegotiateAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="d575b-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-146">DisallowStoringOfRunAsCredentials</span><span class="sxs-lookup"><span data-stu-id="d575b-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d575b-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d575b-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d575b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d575b-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d575b-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d575b-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d575b-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d575b-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d575b-156">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d575b-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-157">SpecifyChannelBindingTokenHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="d575b-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="d575b-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-162">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-163">TurnOnCompatibilityHTTPListener</span><span class="sxs-lookup"><span data-stu-id="d575b-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d575b-166">TurnOnCompatibilityHTTPSListener</span><span class="sxs-lookup"><span data-stu-id="d575b-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d575b-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d575b-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d575b-168">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d575b-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d575b-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d575b-169">Requirements</span></span>



| <span data-ttu-id="d575b-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="d575b-170">Requirement</span></span> | <span data-ttu-id="d575b-171">Valor</span><span class="sxs-lookup"><span data-stu-id="d575b-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d575b-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d575b-172">Minimum supported client</span></span><br/> | <span data-ttu-id="d575b-173">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d575b-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d575b-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d575b-174">Minimum supported server</span></span><br/> | <span data-ttu-id="d575b-175">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d575b-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d575b-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="d575b-176">Namespace</span></span><br/>                | <span data-ttu-id="d575b-177">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d575b-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d575b-178">MOF</span><span class="sxs-lookup"><span data-stu-id="d575b-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d575b-179"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d575b-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d575b-180">DLL</span><span class="sxs-lookup"><span data-stu-id="d575b-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d575b-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d575b-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

