---
title: Classe MDM_EnterpriseDataProtection_Settings01
description: A \_ classe MDM EnterpriseDataProtection \_ Settings01 é usada para configurar as configurações específicas de WIP (proteção de informações do Windows) (anteriormente conhecida como proteção de dados empresariais).
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- Classe MDM_EnterpriseDataProtection_Settings01
- Classe MDM_EnterpriseDataProtection_Settings01, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ef063a1a8d72666dc44a2276bcecfb7d420c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455596"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a><span data-ttu-id="6a06b-105">\_ \_ Classe SETTINGS01 do MDM EnterpriseDataProtection</span><span class="sxs-lookup"><span data-stu-id="6a06b-105">MDM\_EnterpriseDataProtection\_Settings01 class</span></span>

<span data-ttu-id="6a06b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="6a06b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6a06b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="6a06b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6a06b-108">A classe **MDM \_ EnterpriseDataProtection \_ Settings01** é usada para configurar as configurações específicas de WIP (proteção de informações do Windows) (anteriormente conhecida como proteção de dados empresariais).</span><span class="sxs-lookup"><span data-stu-id="6a06b-108">The **MDM\_EnterpriseDataProtection\_Settings01** class is used to configure Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span> <span data-ttu-id="6a06b-109">Para obter mais informações sobre WIP, consulte [proteger seus dados corporativos usando a EDP (proteção de dados empresariais)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="6a06b-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="6a06b-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6a06b-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a06b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a06b-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a><span data-ttu-id="6a06b-112">Membros</span><span class="sxs-lookup"><span data-stu-id="6a06b-112">Members</span></span>

<span data-ttu-id="6a06b-113">A **classe \_ \_ Settings01 de MDM EnterpriseDataProtection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6a06b-113">The **MDM\_EnterpriseDataProtection\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="6a06b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6a06b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a06b-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6a06b-115">Properties</span></span>

<span data-ttu-id="6a06b-116">A **classe \_ \_ Settings01 do MDM EnterpriseDataProtection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6a06b-116">The **MDM\_EnterpriseDataProtection\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6a06b-117">AllowAzureRMSForEDP</span><span class="sxs-lookup"><span data-stu-id="6a06b-117">AllowAzureRMSForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-118">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6a06b-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a06b-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6a06b-120">AllowUserDecryption</span><span class="sxs-lookup"><span data-stu-id="6a06b-120">AllowUserDecryption</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-121">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6a06b-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a06b-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6a06b-123">DataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="6a06b-123">DataRecoveryCertificate</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6a06b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a06b-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-126">Qualificadores: **octetstring**</span><span class="sxs-lookup"><span data-stu-id="6a06b-126">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6a06b-127">EDPEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="6a06b-127">EDPEnforcementLevel</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-128">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6a06b-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a06b-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6a06b-130">EDPShowIcons</span><span class="sxs-lookup"><span data-stu-id="6a06b-130">EDPShowIcons</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6a06b-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a06b-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6a06b-133">EnterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="6a06b-133">EnterpriseProtectedDomainNames</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6a06b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a06b-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6a06b-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6a06b-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6a06b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6a06b-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-139">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6a06b-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6a06b-140">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="6a06b-140">Identifies the name of the parent node.</span></span> <span data-ttu-id="6a06b-141">Para essa classe, a cadeia de caracteres é "Settings".</span><span class="sxs-lookup"><span data-stu-id="6a06b-141">For this class, the string is "Settings".</span></span>

</dd> <dt>

<span data-ttu-id="6a06b-142">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6a06b-142">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6a06b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6a06b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-145">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6a06b-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6a06b-146">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="6a06b-146">Describes the full path to the parent node.</span></span> <span data-ttu-id="6a06b-147">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseDataProtection"</span><span class="sxs-lookup"><span data-stu-id="6a06b-147">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="6a06b-148">RevokeOnUnenroll</span><span class="sxs-lookup"><span data-stu-id="6a06b-148">RevokeOnUnenroll</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-149">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6a06b-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a06b-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6a06b-151">RMSTemplateIDForEDP</span><span class="sxs-lookup"><span data-stu-id="6a06b-151">RMSTemplateIDForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6a06b-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a06b-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6a06b-154">SMBAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="6a06b-154">SMBAutoEncryptedFileExtensions</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a06b-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6a06b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a06b-156">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6a06b-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a06b-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a06b-157">Requirements</span></span>



| <span data-ttu-id="6a06b-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a06b-158">Requirement</span></span> | <span data-ttu-id="6a06b-159">Valor</span><span class="sxs-lookup"><span data-stu-id="6a06b-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a06b-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a06b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6a06b-161">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6a06b-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6a06b-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a06b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6a06b-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6a06b-163">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="6a06b-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a06b-164">Namespace</span></span><br/>                | <span data-ttu-id="6a06b-165">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="6a06b-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="6a06b-166">MOF</span><span class="sxs-lookup"><span data-stu-id="6a06b-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a06b-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a06b-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="6a06b-168">DLL</span><span class="sxs-lookup"><span data-stu-id="6a06b-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a06b-169"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="6a06b-169"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

