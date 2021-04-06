---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01_03
description: A \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 03 fornece informações específicas sobre o aplicativo, como nome, versão e Publicador.
ms.assetid: 424e68de-1411-490f-b33b-5243ffa5a31e
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_03
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_03, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_03
- MDM_EnterpriseModernAppManagement_AppManagement01_03.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24c028c6a1f0d551fc54cb078376dcdef968abc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085991"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_03-class"></a><span data-ttu-id="eaaca-105">\_Classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 03</span><span class="sxs-lookup"><span data-stu-id="eaaca-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_03 class</span></span>

<span data-ttu-id="eaaca-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="eaaca-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eaaca-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="eaaca-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eaaca-108">A classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** fornece informações específicas sobre o aplicativo, como nome, versão e Publicador.</span><span class="sxs-lookup"><span data-stu-id="eaaca-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class provides specific information about the app, such as name, version, and publisher.</span></span>

<span data-ttu-id="eaaca-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="eaaca-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaaca-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaaca-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_03
{
  string InstanceID;
  string ParentID;
  string Name;
  string Version;
  string Publisher;
  string Architecture;
  string InstallLocation;
  sint32 IsFramework;
  sint32 IsBundle;
  string InstallDate;
  string ResourceID;
  sint32 PackageStatus;
  sint32 RequiresReinstall;
  string Users;
  sint32 IsProvisioned;
};
```

## <a name="members"></a><span data-ttu-id="eaaca-111">Membros</span><span class="sxs-lookup"><span data-stu-id="eaaca-111">Members</span></span>

<span data-ttu-id="eaaca-112">A classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="eaaca-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these types of members:</span></span>

-   [<span data-ttu-id="eaaca-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eaaca-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eaaca-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eaaca-114">Properties</span></span>

<span data-ttu-id="eaaca-115">A classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="eaaca-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="eaaca-116">Arquitetura</span><span class="sxs-lookup"><span data-stu-id="eaaca-116">Architecture</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-architecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-119">InstallDate</span><span class="sxs-lookup"><span data-stu-id="eaaca-119">InstallDate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-122">InstallLocation</span><span class="sxs-lookup"><span data-stu-id="eaaca-122">InstallLocation</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eaaca-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eaaca-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eaaca-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eaaca-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eaaca-129">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="eaaca-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="eaaca-130">Para essa classe, a cadeia de caracteres é a instância do nome completo do pacote.</span><span class="sxs-lookup"><span data-stu-id="eaaca-130">For this class, the string is the instance of the package full name.</span></span>

</dd> <dt>

[<span data-ttu-id="eaaca-131">Isbundle</span><span class="sxs-lookup"><span data-stu-id="eaaca-131">IsBundle</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isbundle)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eaaca-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-134">Isframework</span><span class="sxs-lookup"><span data-stu-id="eaaca-134">IsFramework</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isframework)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eaaca-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-137">Isprovisionado</span><span class="sxs-lookup"><span data-stu-id="eaaca-137">IsProvisioned</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isprovisioned)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eaaca-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-140">Nome</span><span class="sxs-lookup"><span data-stu-id="eaaca-140">Name</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-143">PackageStatus</span><span class="sxs-lookup"><span data-stu-id="eaaca-143">PackageStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-packagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eaaca-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eaaca-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="eaaca-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eaaca-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-149">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eaaca-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eaaca-150">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="eaaca-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="eaaca-151">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*enterpriseid* / *PackageFamilyName*"</span><span class="sxs-lookup"><span data-stu-id="eaaca-151">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="eaaca-152">Publicador</span><span class="sxs-lookup"><span data-stu-id="eaaca-152">Publisher</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-publisher)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-155">RequiresReinstall</span><span class="sxs-lookup"><span data-stu-id="eaaca-155">RequiresReinstall</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-requiresreinstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-156">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="eaaca-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-158">ResourceID</span><span class="sxs-lookup"><span data-stu-id="eaaca-158">ResourceID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-resourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-161">Usuários</span><span class="sxs-lookup"><span data-stu-id="eaaca-161">Users</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-users)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eaaca-164">Versão</span><span class="sxs-lookup"><span data-stu-id="eaaca-164">Version</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-version)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaaca-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eaaca-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaaca-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eaaca-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eaaca-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaaca-167">Requirements</span></span>



| <span data-ttu-id="eaaca-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaaca-168">Requirement</span></span> | <span data-ttu-id="eaaca-169">Valor</span><span class="sxs-lookup"><span data-stu-id="eaaca-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaaca-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaaca-170">Minimum supported client</span></span><br/> | <span data-ttu-id="eaaca-171">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="eaaca-171">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eaaca-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaaca-172">Minimum supported server</span></span><br/> | <span data-ttu-id="eaaca-173">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eaaca-173">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="eaaca-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="eaaca-174">Namespace</span></span><br/>                | <span data-ttu-id="eaaca-175">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="eaaca-175">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="eaaca-176">MOF</span><span class="sxs-lookup"><span data-stu-id="eaaca-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaaca-177"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaaca-177"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaaca-178">DLL</span><span class="sxs-lookup"><span data-stu-id="eaaca-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaaca-179"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaaca-179"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaaca-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaaca-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaaca-181">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="eaaca-181">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

