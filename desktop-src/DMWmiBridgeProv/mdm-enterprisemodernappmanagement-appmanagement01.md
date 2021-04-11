---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01
description: A \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 inicia o Windows Update examina e relata o último erro de verificação.
ms.assetid: f579a7c9-2e98-4e34-b45b-db8a4d553c57
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01
- Classe MDM_EnterpriseModernAppManagement_AppManagement01, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1f2a3739fe16d4a13e409d7d152645d4653336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163600"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="94ff5-105">\_ \_ Classe APPMANAGEMENT01 do MDM EnterpriseModernAppManagement</span><span class="sxs-lookup"><span data-stu-id="94ff5-105">MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="94ff5-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="94ff5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="94ff5-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="94ff5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="94ff5-108">A classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01** inicia o Windows Update examina e relata o último erro de verificação.</span><span class="sxs-lookup"><span data-stu-id="94ff5-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class starts the Windows Update scan and reports the last scan error.</span></span>

<span data-ttu-id="94ff5-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="94ff5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ff5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94ff5-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01
{
  string InstanceID;
  string ParentID;
  sint32 LastScanError;
  string AppInventoryQuery;
  string AppInventoryResults;
  string RemovePackage;
};
```

## <a name="members"></a><span data-ttu-id="94ff5-111">Membros</span><span class="sxs-lookup"><span data-stu-id="94ff5-111">Members</span></span>

<span data-ttu-id="94ff5-112">A **classe \_ \_ AppManagement01 de MDM EnterpriseModernAppManagement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="94ff5-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these types of members:</span></span>

-   [<span data-ttu-id="94ff5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="94ff5-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="94ff5-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94ff5-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="94ff5-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="94ff5-115">Methods</span></span>

<span data-ttu-id="94ff5-116">A **classe \_ \_ AppManagement01 do MDM EnterpriseModernAppManagement** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="94ff5-116">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these methods.</span></span>



| <span data-ttu-id="94ff5-117">Método</span><span class="sxs-lookup"><span data-stu-id="94ff5-117">Method</span></span>                                                                                               | <span data-ttu-id="94ff5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="94ff5-118">Description</span></span>                                             |
|:-----------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="94ff5-119">**RemovePackageMethod**</span><span class="sxs-lookup"><span data-stu-id="94ff5-119">**RemovePackageMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-removepackagemethod.md) | <span data-ttu-id="94ff5-120">Método para remover pacotes.</span><span class="sxs-lookup"><span data-stu-id="94ff5-120">Method for removing packages.</span></span><br/>                |
| [<span data-ttu-id="94ff5-121">**UpdateScanMethod**</span><span class="sxs-lookup"><span data-stu-id="94ff5-121">**UpdateScanMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-updatescanmethod.md)       | <span data-ttu-id="94ff5-122">Método para iniciar a verificação de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="94ff5-122">Method for starting the Windows Update scan.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="94ff5-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94ff5-123">Properties</span></span>

<span data-ttu-id="94ff5-124">A **classe \_ \_ AppManagement01 do MDM EnterpriseModernAppManagement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="94ff5-124">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="94ff5-125">AppInventoryQuery</span><span class="sxs-lookup"><span data-stu-id="94ff5-125">AppInventoryQuery</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryquery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ff5-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94ff5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94ff5-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94ff5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="94ff5-128">AppInventoryResults</span><span class="sxs-lookup"><span data-stu-id="94ff5-128">AppInventoryResults</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryresults)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ff5-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94ff5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94ff5-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94ff5-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="94ff5-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="94ff5-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ff5-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94ff5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94ff5-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94ff5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94ff5-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="94ff5-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="94ff5-135">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="94ff5-135">Identifies the name of the parent node.</span></span> <span data-ttu-id="94ff5-136">Para essa classe, a cadeia de caracteres é "AppManagement".</span><span class="sxs-lookup"><span data-stu-id="94ff5-136">For this class, the string is "AppManagement".</span></span>

</dd> <dt>

[<span data-ttu-id="94ff5-137">LastScanError</span><span class="sxs-lookup"><span data-stu-id="94ff5-137">LastScanError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-lastscanerror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ff5-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="94ff5-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="94ff5-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94ff5-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="94ff5-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="94ff5-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ff5-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94ff5-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94ff5-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94ff5-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94ff5-143">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="94ff5-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="94ff5-144">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="94ff5-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="94ff5-145">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseModernAppManagement/"</span><span class="sxs-lookup"><span data-stu-id="94ff5-145">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/"</span></span>

</dd> <dt>

[<span data-ttu-id="94ff5-146">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="94ff5-146">RemovePackage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-removepackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="94ff5-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94ff5-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94ff5-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="94ff5-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94ff5-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94ff5-149">Requirements</span></span>



| <span data-ttu-id="94ff5-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ff5-150">Requirement</span></span> | <span data-ttu-id="94ff5-151">Valor</span><span class="sxs-lookup"><span data-stu-id="94ff5-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ff5-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94ff5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="94ff5-153">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="94ff5-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94ff5-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94ff5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="94ff5-155">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="94ff5-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="94ff5-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="94ff5-156">Namespace</span></span><br/>                | <span data-ttu-id="94ff5-157">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="94ff5-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="94ff5-158">MOF</span><span class="sxs-lookup"><span data-stu-id="94ff5-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94ff5-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94ff5-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="94ff5-160">DLL</span><span class="sxs-lookup"><span data-stu-id="94ff5-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94ff5-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94ff5-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ff5-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="94ff5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ff5-163">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="94ff5-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

