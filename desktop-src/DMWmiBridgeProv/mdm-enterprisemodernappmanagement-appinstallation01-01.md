---
title: Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: A \_ classe MDM EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 é usada para instalar aplicativos da Windows Store ou de um local hospedado.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cd3fc5478e73df5276fdc9d6a1d66c9649dd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918845"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="7b0a7-105">\_Classe MDM EnterpriseModernAppManagement \_ AppInstallation01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="7b0a7-105">MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="7b0a7-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7b0a7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7b0a7-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7b0a7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7b0a7-108">A classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** é usada para instalar aplicativos da Windows Store ou de um local hospedado.</span><span class="sxs-lookup"><span data-stu-id="7b0a7-108">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class is used to install apps from the Windows Store or a hosted location.</span></span>

<span data-ttu-id="7b0a7-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7b0a7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0a7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b0a7-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a><span data-ttu-id="7b0a7-111">Membros</span><span class="sxs-lookup"><span data-stu-id="7b0a7-111">Members</span></span>

<span data-ttu-id="7b0a7-112">A classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7b0a7-112">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="7b0a7-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="7b0a7-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="7b0a7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7b0a7-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7b0a7-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="7b0a7-115">Methods</span></span>

<span data-ttu-id="7b0a7-116">A classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7b0a7-116">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these methods.</span></span>



| <span data-ttu-id="7b0a7-117">Método</span><span class="sxs-lookup"><span data-stu-id="7b0a7-117">Method</span></span>                                                                                                    | <span data-ttu-id="7b0a7-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b0a7-118">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b0a7-119">**HostedInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-119">**HostedInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | <span data-ttu-id="7b0a7-120">Método para executar uma instalação de um pacote de aplicativo de um local hospedado (pode ser uma unidade local, uma UNC ou uma fonte de dados HTTPS).</span><span class="sxs-lookup"><span data-stu-id="7b0a7-120">Method to perform an install of an app package from a hosted location (this can be a local drive, a UNC, or https data source).</span></span><br/> |
| [<span data-ttu-id="7b0a7-121">**StoreInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-121">**StoreInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | <span data-ttu-id="7b0a7-122">Método para executar uma instalação de um aplicativo e uma licença da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="7b0a7-122">Method to perform an install of an app and a license from the Windows Store.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="7b0a7-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7b0a7-123">Properties</span></span>

<span data-ttu-id="7b0a7-124">A classe **MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7b0a7-124">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b0a7-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b0a7-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b0a7-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b0a7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b0a7-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b0a7-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b0a7-129">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="7b0a7-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="7b0a7-130">Para essa classe, a cadeia de caracteres é "AppInstallation".</span><span class="sxs-lookup"><span data-stu-id="7b0a7-130">For this class, the string is "AppInstallation".</span></span>

</dd> <dt>

[<span data-ttu-id="7b0a7-131">LastError</span><span class="sxs-lookup"><span data-stu-id="7b0a7-131">LastError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b0a7-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b0a7-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7b0a7-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7b0a7-134">LastErrorDesc</span><span class="sxs-lookup"><span data-stu-id="7b0a7-134">LastErrorDesc</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b0a7-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b0a7-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7b0a7-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b0a7-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b0a7-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b0a7-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b0a7-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b0a7-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b0a7-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b0a7-141">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="7b0a7-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="7b0a7-142">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span><span class="sxs-lookup"><span data-stu-id="7b0a7-142">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span></span>

</dd> <dt>

[<span data-ttu-id="7b0a7-143">ProgressStatus</span><span class="sxs-lookup"><span data-stu-id="7b0a7-143">ProgressStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b0a7-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b0a7-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7b0a7-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7b0a7-146">Status</span><span class="sxs-lookup"><span data-stu-id="7b0a7-146">Status</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b0a7-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7b0a7-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b0a7-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7b0a7-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b0a7-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b0a7-149">Requirements</span></span>



| <span data-ttu-id="7b0a7-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b0a7-150">Requirement</span></span> | <span data-ttu-id="7b0a7-151">Valor</span><span class="sxs-lookup"><span data-stu-id="7b0a7-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0a7-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b0a7-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7b0a7-153">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7b0a7-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b0a7-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b0a7-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7b0a7-155">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7b0a7-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7b0a7-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b0a7-156">Namespace</span></span><br/>                | <span data-ttu-id="7b0a7-157">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7b0a7-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7b0a7-158">MOF</span><span class="sxs-lookup"><span data-stu-id="7b0a7-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b0a7-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a7-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b0a7-160">DLL</span><span class="sxs-lookup"><span data-stu-id="7b0a7-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b0a7-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a7-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b0a7-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b0a7-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b0a7-163">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="7b0a7-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

