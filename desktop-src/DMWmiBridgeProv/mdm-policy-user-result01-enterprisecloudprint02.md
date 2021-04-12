---
title: Classe MDM_Policy_User_Result01_EnterpriseCloudPrint02
description: A \_ classe Result01 EnterpriseCloudPrint02 do usuário da política de MDM \_ \_ \_ representa as políticas de impressão em nuvem disponíveis.
ms.assetid: cf830cb5-2477-4b21-9d98-9fa9989daa7f
keywords:
- Classe MDM_Policy_User_Result01_EnterpriseCloudPrint02
- Classe MDM_Policy_User_Result01_EnterpriseCloudPrint02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_EnterpriseCloudPrint02
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dfa75d102da3a61ff0a9f2094d31e0ba5b4abca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455203"
---
# <a name="mdm_policy_user_result01_enterprisecloudprint02-class"></a><span data-ttu-id="d9a23-105">Result01 de usuário de política de MDM- \_ \_ \_ \_ classe EnterpriseCloudPrint02</span><span class="sxs-lookup"><span data-stu-id="d9a23-105">MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class</span></span>

<span data-ttu-id="d9a23-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d9a23-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d9a23-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="d9a23-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d9a23-108">A \_ classe Result01 EnterpriseCloudPrint02 do usuário da política de MDM \_ \_ \_ representa as políticas de impressão em nuvem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d9a23-108">The MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class represents the available cloud print policies.</span></span>

<span data-ttu-id="d9a23-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d9a23-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a23-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9a23-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_EnterpriseCloudPrint02
{
  string InstanceID;
  string ParentID;
  string CloudPrinterDiscoveryEndPoint;
  string CloudPrintOAuthAuthority;
  string CloudPrintOAuthClientId;
  string CloudPrintResourceId;
  sint32 DiscoveryMaxPrinterLimit;
  string MopriaDiscoveryResourceId;
};
```

## <a name="members"></a><span data-ttu-id="d9a23-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d9a23-111">Members</span></span>

<span data-ttu-id="d9a23-112">A **classe \_ \_ \_ Result01 \_ EnterpriseCloudPrint02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d9a23-112">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these types of members:</span></span>

-   [<span data-ttu-id="d9a23-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9a23-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9a23-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9a23-114">Properties</span></span>

<span data-ttu-id="d9a23-115">A **classe \_ \_ \_ Result01 \_ EnterpriseCloudPrint02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d9a23-115">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d9a23-116">CloudPrinterDiscoveryEndPoint</span><span class="sxs-lookup"><span data-stu-id="d9a23-116">CloudPrinterDiscoveryEndPoint</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a23-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9a23-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9a23-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a23-119">CloudPrintOAuthAuthority</span><span class="sxs-lookup"><span data-stu-id="d9a23-119">CloudPrintOAuthAuthority</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a23-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9a23-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9a23-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a23-122">CloudPrintOAuthClientId</span><span class="sxs-lookup"><span data-stu-id="d9a23-122">CloudPrintOAuthClientId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a23-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9a23-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9a23-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a23-125">CloudPrintResourceId</span><span class="sxs-lookup"><span data-stu-id="d9a23-125">CloudPrintResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a23-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9a23-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9a23-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a23-128">DiscoveryMaxPrinterLimit</span><span class="sxs-lookup"><span data-stu-id="d9a23-128">DiscoveryMaxPrinterLimit</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a23-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d9a23-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9a23-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9a23-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d9a23-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a23-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9a23-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9a23-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9a23-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a23-135">MopriaDiscoveryResourceId</span><span class="sxs-lookup"><span data-stu-id="d9a23-135">MopriaDiscoveryResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a23-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9a23-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d9a23-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9a23-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d9a23-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a23-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d9a23-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9a23-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9a23-141">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9a23-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9a23-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9a23-142">Requirements</span></span>



| <span data-ttu-id="d9a23-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9a23-143">Requirement</span></span> | <span data-ttu-id="d9a23-144">Valor</span><span class="sxs-lookup"><span data-stu-id="d9a23-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a23-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9a23-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a23-146">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d9a23-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9a23-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9a23-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a23-148">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d9a23-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d9a23-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9a23-149">Namespace</span></span><br/>                | <span data-ttu-id="d9a23-150">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d9a23-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d9a23-151">MOF</span><span class="sxs-lookup"><span data-stu-id="d9a23-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9a23-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9a23-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9a23-153">DLL</span><span class="sxs-lookup"><span data-stu-id="d9a23-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9a23-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9a23-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

