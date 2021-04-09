---
title: Classe MDM_Policy_Result01_NetworkIsolation02
description: A \_ classe Result01 NetworkIsolation02 de política de MDM \_ \_ representa as políticas de navegador disponíveis.
ms.assetid: f44f43fb-813b-4d40-a56c-0c497e004a8a
keywords:
- Classe MDM_Policy_Result01_NetworkIsolation02
- Classe MDM_Policy_Result01_NetworkIsolation02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_NetworkIsolation02
- MDM_Policy_Result01_NetworkIsolation02.InstanceID
- MDM_Policy_Result01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5611d7e00ab0fa5210a657b55a3f2990fdf40880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085450"
---
# <a name="mdm_policy_result01_networkisolation02-class"></a><span data-ttu-id="19b65-105">\_Classe MDM \_ Result01 \_ NetworkIsolation02</span><span class="sxs-lookup"><span data-stu-id="19b65-105">MDM\_Policy\_Result01\_NetworkIsolation02 class</span></span>

<span data-ttu-id="19b65-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="19b65-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="19b65-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="19b65-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="19b65-108">A **classe \_ \_ Result01 \_ NetworkIsolation02 de política de MDM** representa as políticas de navegador disponíveis.</span><span class="sxs-lookup"><span data-stu-id="19b65-108">The **MDM\_Policy\_Result01\_NetworkIsolation02** class represents the browser policies available.</span></span>

<span data-ttu-id="19b65-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="19b65-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b65-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19b65-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
  string NeutralResources;
};
```

## <a name="members"></a><span data-ttu-id="19b65-111">Membros</span><span class="sxs-lookup"><span data-stu-id="19b65-111">Members</span></span>

<span data-ttu-id="19b65-112">A **classe \_ \_ Result01 \_ NetworkIsolation02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="19b65-112">The **MDM\_Policy\_Result01\_NetworkIsolation02** class has these types of members:</span></span>

-   [<span data-ttu-id="19b65-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="19b65-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19b65-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="19b65-114">Properties</span></span>

<span data-ttu-id="19b65-115">A **classe \_ \_ Result01 \_ NetworkIsolation02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="19b65-115">The **MDM\_Policy\_Result01\_NetworkIsolation02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="19b65-116">EnterpriseCloudResources</span><span class="sxs-lookup"><span data-stu-id="19b65-116">EnterpriseCloudResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19b65-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19b65-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19b65-119">EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="19b65-119">EnterpriseInternalProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19b65-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19b65-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19b65-122">EnterpriseIPRange</span><span class="sxs-lookup"><span data-stu-id="19b65-122">EnterpriseIPRange</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19b65-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19b65-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19b65-125">EnterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="19b65-125">EnterpriseIPRangesAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="19b65-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19b65-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19b65-128">EnterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="19b65-128">EnterpriseNetworkDomainNames</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19b65-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19b65-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19b65-131">EnterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="19b65-131">EnterpriseProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19b65-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19b65-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="19b65-134">EnterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="19b65-134">EnterpriseProxyServersAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="19b65-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19b65-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19b65-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="19b65-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19b65-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19b65-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b65-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19b65-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19b65-141">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="19b65-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="19b65-142">Para essa classe, a cadeia de caracteres é "NetworkIsolation".</span><span class="sxs-lookup"><span data-stu-id="19b65-142">For this class, the string is "NetworkIsolation".</span></span>

</dd> <dt>

[<span data-ttu-id="19b65-143">NeutralResources</span><span class="sxs-lookup"><span data-stu-id="19b65-143">NeutralResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19b65-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="19b65-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19b65-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="19b65-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b65-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="19b65-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b65-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="19b65-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b65-149">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19b65-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19b65-150">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="19b65-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="19b65-151">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="19b65-151">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19b65-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19b65-152">Requirements</span></span>



| <span data-ttu-id="19b65-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="19b65-153">Requirement</span></span> | <span data-ttu-id="19b65-154">Valor</span><span class="sxs-lookup"><span data-stu-id="19b65-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b65-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19b65-155">Minimum supported client</span></span><br/> | <span data-ttu-id="19b65-156">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="19b65-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19b65-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19b65-157">Minimum supported server</span></span><br/> | <span data-ttu-id="19b65-158">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="19b65-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="19b65-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="19b65-159">Namespace</span></span><br/>                | <span data-ttu-id="19b65-160">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="19b65-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="19b65-161">MOF</span><span class="sxs-lookup"><span data-stu-id="19b65-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19b65-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19b65-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="19b65-163">DLL</span><span class="sxs-lookup"><span data-stu-id="19b65-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19b65-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19b65-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

