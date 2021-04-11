---
title: Classe MDM_Policy_Result01_Security02
description: A \_ classe MDM Policy \_ Result01 \_ Security02 representa as políticas de segurança disponíveis.
ms.assetid: e4f9bbeb-b542-454d-930b-0b4ac88fe189
keywords:
- Classe MDM_Policy_Result01_Security02
- Classe MDM_Policy_Result01_Security02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Security02
- MDM_Policy_Result01_Security02.InstanceID
- MDM_Policy_Result01_Security02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 959d5cbc9382b4bef0899f5b44d8ee2d171bd704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009168"
---
# <a name="mdm_policy_result01_security02-class"></a><span data-ttu-id="d70f0-105">\_Classe MDM \_ Result01 \_ Security02</span><span class="sxs-lookup"><span data-stu-id="d70f0-105">MDM\_Policy\_Result01\_Security02 class</span></span>

<span data-ttu-id="d70f0-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d70f0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d70f0-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="d70f0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d70f0-108">A classe **MDM \_ Policy \_ Result01 \_ Security02** representa as políticas de segurança disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d70f0-108">The **MDM\_Policy\_Result01\_Security02** class represents the security policies available.</span></span>

<span data-ttu-id="d70f0-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d70f0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d70f0-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d70f0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Security02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddProvisioningPackage;
  sint32 AllowRemoveProvisioningPackage;
  sint32 ClearTPMIfNotReady;
  sint32 PreventAutomaticDeviceEncryptionForAzureADJoinedDevices;
  sint32 RequireDeviceEncryption;
  sint32 RequireProvisioningPackageSignature;
  sint32 RequireRetrieveHealthCertificateOnBoot;
};
```

## <a name="members"></a><span data-ttu-id="d70f0-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d70f0-111">Members</span></span>

<span data-ttu-id="d70f0-112">A **classe \_ \_ Result01 \_ Security02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d70f0-112">The **MDM\_Policy\_Result01\_Security02** class has these types of members:</span></span>

-   [<span data-ttu-id="d70f0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d70f0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d70f0-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d70f0-114">Properties</span></span>

<span data-ttu-id="d70f0-115">A **classe \_ \_ Result01 \_ Security02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d70f0-115">The **MDM\_Policy\_Result01\_Security02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d70f0-116">AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="d70f0-116">AllowAddProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70f0-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d70f0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70f0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d70f0-119">AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="d70f0-119">AllowRemoveProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70f0-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d70f0-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70f0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d70f0-122">ClearTPMIfNotReady</span><span class="sxs-lookup"><span data-stu-id="d70f0-122">ClearTPMIfNotReady</span></span>](/windows/client-management/mdm/policy-csp-security#security-cleartpmifnotready)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70f0-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d70f0-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70f0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d70f0-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d70f0-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70f0-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70f0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d70f0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d70f0-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d70f0-129">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="d70f0-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="d70f0-130">Para essa classe, a cadeia de caracteres é "Security".</span><span class="sxs-lookup"><span data-stu-id="d70f0-130">For this class, the string is "Security".</span></span>

</dd> <dt>

<span data-ttu-id="d70f0-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d70f0-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70f0-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d70f0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d70f0-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d70f0-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d70f0-135">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="d70f0-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="d70f0-136">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="d70f0-136">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="d70f0-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span><span class="sxs-lookup"><span data-stu-id="d70f0-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span></span>](/windows/client-management/mdm/policy-csp-security#security-preventautomaticdeviceencryptionforazureadjoineddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70f0-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d70f0-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70f0-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d70f0-140">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="d70f0-140">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70f0-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d70f0-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70f0-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d70f0-143">RequireProvisioningPackageSignature</span><span class="sxs-lookup"><span data-stu-id="d70f0-143">RequireProvisioningPackageSignature</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireprovisioningpackagesignature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70f0-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d70f0-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70f0-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d70f0-146">RequireRetrieveHealthCertificateOnBoot</span><span class="sxs-lookup"><span data-stu-id="d70f0-146">RequireRetrieveHealthCertificateOnBoot</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireretrievehealthcertificateonboot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d70f0-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d70f0-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d70f0-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d70f0-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d70f0-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d70f0-149">Requirements</span></span>



| <span data-ttu-id="d70f0-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="d70f0-150">Requirement</span></span> | <span data-ttu-id="d70f0-151">Valor</span><span class="sxs-lookup"><span data-stu-id="d70f0-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d70f0-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d70f0-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d70f0-153">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d70f0-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d70f0-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d70f0-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d70f0-155">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d70f0-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d70f0-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="d70f0-156">Namespace</span></span><br/>                | <span data-ttu-id="d70f0-157">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d70f0-157">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="d70f0-158">MOF</span><span class="sxs-lookup"><span data-stu-id="d70f0-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d70f0-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d70f0-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d70f0-160">DLL</span><span class="sxs-lookup"><span data-stu-id="d70f0-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d70f0-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d70f0-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d70f0-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="d70f0-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d70f0-163">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="d70f0-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

