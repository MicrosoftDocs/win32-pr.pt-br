---
title: Classe MDM_Policy_Config01_Security02
description: A \_ classe MDM Policy \_ Config01 \_ Security02 representa as políticas de segurança disponíveis.
ms.assetid: 8db74f3f-a7a5-4e93-8aeb-111dcf2111fa
keywords:
- Classe MDM_Policy_Config01_Security02
- Classe MDM_Policy_Config01_Security02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Security02
- MDM_Policy_Config01_Security02.InstanceID
- MDM_Policy_Config01_Security02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268e1e01cddb72ddd85e3c18369bdb998bb315aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009421"
---
# <a name="mdm_policy_config01_security02-class"></a><span data-ttu-id="72b2e-105">\_Classe MDM \_ Config01 \_ Security02</span><span class="sxs-lookup"><span data-stu-id="72b2e-105">MDM\_Policy\_Config01\_Security02 class</span></span>

<span data-ttu-id="72b2e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="72b2e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="72b2e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="72b2e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="72b2e-108">A classe **MDM \_ Policy \_ Config01 \_ Security02** representa as políticas de segurança disponíveis.</span><span class="sxs-lookup"><span data-stu-id="72b2e-108">The **MDM\_Policy\_Config01\_Security02** class represents the security policies available.</span></span>

<span data-ttu-id="72b2e-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="72b2e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b2e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72b2e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Security02
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

## <a name="members"></a><span data-ttu-id="72b2e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="72b2e-111">Members</span></span>

<span data-ttu-id="72b2e-112">A **classe \_ \_ Config01 \_ Security02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="72b2e-112">The **MDM\_Policy\_Config01\_Security02** class has these types of members:</span></span>

-   [<span data-ttu-id="72b2e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72b2e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72b2e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72b2e-114">Properties</span></span>

<span data-ttu-id="72b2e-115">A **classe \_ \_ Config01 \_ Security02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="72b2e-115">The **MDM\_Policy\_Config01\_Security02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="72b2e-116">AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="72b2e-116">AllowAddProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b2e-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72b2e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72b2e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72b2e-119">AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="72b2e-119">AllowRemoveProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b2e-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72b2e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72b2e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72b2e-122">ClearTPMIfNotReady</span><span class="sxs-lookup"><span data-stu-id="72b2e-122">ClearTPMIfNotReady</span></span>](/windows/client-management/mdm/policy-csp-security#security-cleartpmifnotready)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b2e-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72b2e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72b2e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="72b2e-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="72b2e-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b2e-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72b2e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72b2e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72b2e-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="72b2e-129">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="72b2e-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="72b2e-130">Para essa classe, a cadeia de caracteres é "Security".</span><span class="sxs-lookup"><span data-stu-id="72b2e-130">For this class, the string is "Security".</span></span>

</dd> <dt>

<span data-ttu-id="72b2e-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="72b2e-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b2e-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="72b2e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72b2e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72b2e-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="72b2e-135">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="72b2e-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="72b2e-136">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="72b2e-136">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="72b2e-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span><span class="sxs-lookup"><span data-stu-id="72b2e-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span></span>](/windows/client-management/mdm/policy-csp-security#security-preventautomaticdeviceencryptionforazureadjoineddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b2e-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72b2e-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72b2e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72b2e-140">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="72b2e-140">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b2e-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72b2e-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72b2e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72b2e-143">RequireProvisioningPackageSignature</span><span class="sxs-lookup"><span data-stu-id="72b2e-143">RequireProvisioningPackageSignature</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireprovisioningpackagesignature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b2e-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72b2e-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72b2e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="72b2e-146">RequireRetrieveHealthCertificateOnBoot</span><span class="sxs-lookup"><span data-stu-id="72b2e-146">RequireRetrieveHealthCertificateOnBoot</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireretrievehealthcertificateonboot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b2e-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="72b2e-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b2e-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="72b2e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72b2e-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72b2e-149">Requirements</span></span>



| <span data-ttu-id="72b2e-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b2e-150">Requirement</span></span> | <span data-ttu-id="72b2e-151">Valor</span><span class="sxs-lookup"><span data-stu-id="72b2e-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b2e-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72b2e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="72b2e-153">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="72b2e-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72b2e-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72b2e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="72b2e-155">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="72b2e-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="72b2e-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="72b2e-156">Namespace</span></span><br/>                | <span data-ttu-id="72b2e-157">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="72b2e-157">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="72b2e-158">MOF</span><span class="sxs-lookup"><span data-stu-id="72b2e-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72b2e-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72b2e-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="72b2e-160">DLL</span><span class="sxs-lookup"><span data-stu-id="72b2e-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72b2e-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72b2e-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b2e-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="72b2e-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b2e-163">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="72b2e-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

