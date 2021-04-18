---
title: Classe MDM_Policy_Result01_RemoteManagement02
description: A \_ classe MDM Policy \_ Result01 \_ RemoteManagement02 representa as políticas de gerenciamento remoto.
ms.assetid: f6eb96ff-a40e-4602-a812-786d1a89bf12
keywords:
- Classe MDM_Policy_Result01_RemoteManagement02
- Classe MDM_Policy_Result01_RemoteManagement02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteManagement02
- MDM_Policy_Result01_RemoteManagement02.InstanceID
- MDM_Policy_Result01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a60228e39c8e1d6604534c8bd052ec7d40105e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454680"
---
# <a name="mdm_policy_result01_remotemanagement02-class"></a><span data-ttu-id="0fae4-105">\_Classe MDM \_ Result01 \_ RemoteManagement02</span><span class="sxs-lookup"><span data-stu-id="0fae4-105">MDM\_Policy\_Result01\_RemoteManagement02 class</span></span>

<span data-ttu-id="0fae4-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0fae4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0fae4-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0fae4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0fae4-108">A \_ classe MDM Policy \_ Result01 \_ RemoteManagement02 representa as políticas de gerenciamento remoto.</span><span class="sxs-lookup"><span data-stu-id="0fae4-108">The MDM\_Policy\_Result01\_RemoteManagement02 class represents the remote management policies.</span></span>

<span data-ttu-id="0fae4-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0fae4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fae4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fae4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteManagement02
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

## <a name="members"></a><span data-ttu-id="0fae4-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0fae4-111">Members</span></span>

<span data-ttu-id="0fae4-112">A **classe \_ \_ Result01 \_ RemoteManagement02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0fae4-112">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="0fae4-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0fae4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fae4-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0fae4-114">Properties</span></span>

<span data-ttu-id="0fae4-115">A **classe \_ \_ Result01 \_ RemoteManagement02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0fae4-115">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0fae4-116">\_Cliente AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="0fae4-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-119">\_Serviço AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="0fae4-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-122">AllowCredSSPAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="0fae4-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-125">AllowCredSSPAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="0fae4-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-128">AllowRemoteServerManagement</span><span class="sxs-lookup"><span data-stu-id="0fae4-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-131">\_Cliente AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="0fae4-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-134">\_Serviço AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="0fae4-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-137">DisallowDigestAuthentication</span><span class="sxs-lookup"><span data-stu-id="0fae4-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-140">DisallowNegotiateAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="0fae4-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-143">DisallowNegotiateAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="0fae4-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-146">DisallowStoringOfRunAsCredentials</span><span class="sxs-lookup"><span data-stu-id="0fae4-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0fae4-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0fae4-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0fae4-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0fae4-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0fae4-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0fae4-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0fae4-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-156">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0fae4-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-157">SpecifyChannelBindingTokenHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="0fae4-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="0fae4-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-162">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-163">TurnOnCompatibilityHTTPListener</span><span class="sxs-lookup"><span data-stu-id="0fae4-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0fae4-166">TurnOnCompatibilityHTTPSListener</span><span class="sxs-lookup"><span data-stu-id="0fae4-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fae4-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0fae4-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fae4-168">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0fae4-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fae4-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fae4-169">Requirements</span></span>



| <span data-ttu-id="0fae4-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fae4-170">Requirement</span></span> | <span data-ttu-id="0fae4-171">Valor</span><span class="sxs-lookup"><span data-stu-id="0fae4-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fae4-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fae4-172">Minimum supported client</span></span><br/> | <span data-ttu-id="0fae4-173">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0fae4-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0fae4-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fae4-174">Minimum supported server</span></span><br/> | <span data-ttu-id="0fae4-175">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0fae4-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0fae4-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fae4-176">Namespace</span></span><br/>                | <span data-ttu-id="0fae4-177">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0fae4-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0fae4-178">MOF</span><span class="sxs-lookup"><span data-stu-id="0fae4-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fae4-179"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fae4-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fae4-180">DLL</span><span class="sxs-lookup"><span data-stu-id="0fae4-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fae4-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fae4-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

