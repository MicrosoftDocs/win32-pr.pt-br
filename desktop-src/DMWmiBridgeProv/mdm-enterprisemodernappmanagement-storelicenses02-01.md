---
title: Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: A \_ classe MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 é usada para gerenciar licenças para aplicativos da loja.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a4549ba473afaf76bea3f23ec65aacf301121a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009591"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="f339b-105">\_Classe MDM EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="f339b-105">MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="f339b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f339b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f339b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f339b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f339b-108">A classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** é usada para gerenciar licenças para aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="f339b-108">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class is used to manage licenses for store apps.</span></span>

<span data-ttu-id="f339b-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f339b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f339b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f339b-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a><span data-ttu-id="f339b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f339b-111">Members</span></span>

<span data-ttu-id="f339b-112">A classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f339b-112">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="f339b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f339b-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="f339b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f339b-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f339b-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="f339b-115">Methods</span></span>

<span data-ttu-id="f339b-116">A classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f339b-116">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these methods.</span></span>



| <span data-ttu-id="f339b-117">Método</span><span class="sxs-lookup"><span data-stu-id="f339b-117">Method</span></span>                                                                                                              | <span data-ttu-id="f339b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f339b-118">Description</span></span>                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="f339b-119">**AddLicenseMethod**</span><span class="sxs-lookup"><span data-stu-id="f339b-119">**AddLicenseMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | <span data-ttu-id="f339b-120">Método para adicionar uma licença.</span><span class="sxs-lookup"><span data-stu-id="f339b-120">Method for adding a license.</span></span><br/>                 |
| [<span data-ttu-id="f339b-121">**GetLicenseFromStoreMethod**</span><span class="sxs-lookup"><span data-stu-id="f339b-121">**GetLicenseFromStoreMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | <span data-ttu-id="f339b-122">Método para obter uma licença da loja.</span><span class="sxs-lookup"><span data-stu-id="f339b-122">Method for getting a license from the store.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f339b-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f339b-123">Properties</span></span>

<span data-ttu-id="f339b-124">A classe **MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f339b-124">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f339b-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f339b-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f339b-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f339b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f339b-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f339b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f339b-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f339b-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f339b-129">Nó opcional.</span><span class="sxs-lookup"><span data-stu-id="f339b-129">Optional node.</span></span> <span data-ttu-id="f339b-130">ID da licença para um aplicativo do repositório instalado.</span><span class="sxs-lookup"><span data-stu-id="f339b-130">License ID for a store installed app.</span></span> <span data-ttu-id="f339b-131">A ID da licença geralmente é a PFN do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f339b-131">The license ID is generally the PFN of the app.</span></span>

<span data-ttu-id="f339b-132">As operações com suporte são adicionar, obter e excluir.</span><span class="sxs-lookup"><span data-stu-id="f339b-132">Supported operations are Add, Get, and Delete.</span></span>

</dd> <dt>

[<span data-ttu-id="f339b-133">LicenseCategory</span><span class="sxs-lookup"><span data-stu-id="f339b-133">LicenseCategory</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f339b-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f339b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f339b-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f339b-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f339b-136">LicenseUsage</span><span class="sxs-lookup"><span data-stu-id="f339b-136">LicenseUsage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f339b-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f339b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f339b-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f339b-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f339b-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f339b-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f339b-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f339b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f339b-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f339b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f339b-142">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f339b-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f339b-143">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="f339b-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="f339b-144">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span><span class="sxs-lookup"><span data-stu-id="f339b-144">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span></span>

</dd> <dt>

[<span data-ttu-id="f339b-145">RequesterID</span><span class="sxs-lookup"><span data-stu-id="f339b-145">RequesterID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f339b-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f339b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f339b-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f339b-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f339b-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f339b-148">Requirements</span></span>



| <span data-ttu-id="f339b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f339b-149">Requirement</span></span> | <span data-ttu-id="f339b-150">Valor</span><span class="sxs-lookup"><span data-stu-id="f339b-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f339b-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f339b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f339b-152">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f339b-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f339b-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f339b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f339b-154">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f339b-154">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f339b-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="f339b-155">Namespace</span></span><br/>                | <span data-ttu-id="f339b-156">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f339b-156">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f339b-157">MOF</span><span class="sxs-lookup"><span data-stu-id="f339b-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f339b-158"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f339b-158"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f339b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="f339b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f339b-160"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f339b-160"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f339b-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="f339b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f339b-162">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="f339b-162">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

