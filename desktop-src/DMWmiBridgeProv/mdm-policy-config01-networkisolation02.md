---
title: Classe MDM_Policy_Config01_NetworkIsolation02
description: A \_ classe Config01 NetworkIsolation02 de política de MDM \_ \_ representa as políticas de navegador disponíveis.
ms.assetid: f25ecbef-d232-4731-bac8-38a7d597db00
keywords:
- Classe MDM_Policy_Config01_NetworkIsolation02
- Classe MDM_Policy_Config01_NetworkIsolation02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_NetworkIsolation02
- MDM_Policy_Config01_NetworkIsolation02.InstanceID
- MDM_Policy_Config01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9062d150de07860fd9d5b2510269ddcc3d2f8a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009344"
---
# <a name="mdm_policy_config01_networkisolation02-class"></a><span data-ttu-id="47b37-105">\_Classe MDM \_ Config01 \_ NetworkIsolation02</span><span class="sxs-lookup"><span data-stu-id="47b37-105">MDM\_Policy\_Config01\_NetworkIsolation02 class</span></span>

<span data-ttu-id="47b37-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="47b37-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="47b37-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="47b37-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="47b37-108">A **classe \_ \_ Config01 \_ NetworkIsolation02 de política de MDM** representa as políticas de navegador disponíveis.</span><span class="sxs-lookup"><span data-stu-id="47b37-108">The **MDM\_Policy\_Config01\_NetworkIsolation02** class represents the browser policies available.</span></span>

<span data-ttu-id="47b37-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="47b37-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="47b37-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47b37-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string NeutralResources;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="47b37-111">Membros</span><span class="sxs-lookup"><span data-stu-id="47b37-111">Members</span></span>

<span data-ttu-id="47b37-112">A **classe \_ \_ Config01 \_ NetworkIsolation02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="47b37-112">The **MDM\_Policy\_Config01\_NetworkIsolation02** class has these types of members:</span></span>

-   [<span data-ttu-id="47b37-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="47b37-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47b37-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="47b37-114">Properties</span></span>

<span data-ttu-id="47b37-115">A **classe \_ \_ Config01 \_ NetworkIsolation02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="47b37-115">The **MDM\_Policy\_Config01\_NetworkIsolation02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="47b37-116">EnterpriseCloudResources</span><span class="sxs-lookup"><span data-stu-id="47b37-116">EnterpriseCloudResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47b37-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47b37-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47b37-119">EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="47b37-119">EnterpriseInternalProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47b37-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47b37-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47b37-122">EnterpriseIPRange</span><span class="sxs-lookup"><span data-stu-id="47b37-122">EnterpriseIPRange</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47b37-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47b37-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47b37-125">EnterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="47b37-125">EnterpriseIPRangesAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="47b37-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47b37-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47b37-128">EnterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="47b37-128">EnterpriseNetworkDomainNames</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47b37-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47b37-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47b37-131">EnterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="47b37-131">EnterpriseProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47b37-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47b37-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47b37-134">EnterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="47b37-134">EnterpriseProxyServersAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="47b37-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47b37-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="47b37-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="47b37-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47b37-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="47b37-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b37-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47b37-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47b37-141">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="47b37-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="47b37-142">Para essa classe, a cadeia de caracteres é "NetworkIsolation".</span><span class="sxs-lookup"><span data-stu-id="47b37-142">For this class, the string is "NetworkIsolation".</span></span>

</dd> <dt>

[<span data-ttu-id="47b37-143">NeutralResources</span><span class="sxs-lookup"><span data-stu-id="47b37-143">NeutralResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47b37-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="47b37-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="47b37-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="47b37-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b37-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47b37-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b37-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="47b37-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b37-149">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47b37-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47b37-150">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="47b37-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="47b37-151">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="47b37-151">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47b37-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47b37-152">Requirements</span></span>



| <span data-ttu-id="47b37-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="47b37-153">Requirement</span></span> | <span data-ttu-id="47b37-154">Valor</span><span class="sxs-lookup"><span data-stu-id="47b37-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47b37-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47b37-155">Minimum supported client</span></span><br/> | <span data-ttu-id="47b37-156">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="47b37-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47b37-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47b37-157">Minimum supported server</span></span><br/> | <span data-ttu-id="47b37-158">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="47b37-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="47b37-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="47b37-159">Namespace</span></span><br/>                | <span data-ttu-id="47b37-160">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="47b37-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="47b37-161">MOF</span><span class="sxs-lookup"><span data-stu-id="47b37-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47b37-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47b37-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="47b37-163">DLL</span><span class="sxs-lookup"><span data-stu-id="47b37-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47b37-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47b37-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

