---
title: Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
description: A \_ classe EnterpriseDataProtection01 RetrieveByTimeRange02 de relatórios do MDM \_ \_ é usada para recuperar os logs que existem dentro de StartTime e StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02, descrita
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec266e68bbaaafb1f1e3a78fba7ea6b91805096a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008899"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a><span data-ttu-id="fab48-105">\_Classe RetrieveByTimeRange02 de relatórios MDM \_ EnterpriseDataProtection01 \_</span><span class="sxs-lookup"><span data-stu-id="fab48-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="fab48-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="fab48-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fab48-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="fab48-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fab48-108">A **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 de relatórios do MDM** é usada para recuperar os logs que existem dentro de StartTime e StopTime.</span><span class="sxs-lookup"><span data-stu-id="fab48-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.</span></span> <span data-ttu-id="fab48-109">StartTime e StopTime são expressos no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="fab48-109">The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="fab48-110">Se StartTime e StopTime não forem especificados, os valores serão interpretados como a primeira hora existente ou a última.</span><span class="sxs-lookup"><span data-stu-id="fab48-110">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="fab48-111">Estes são os outros cenários possíveis:</span><span class="sxs-lookup"><span data-stu-id="fab48-111">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="fab48-112">Se StartTime e StopTime não forem especificados, ele retornará todos os logs existentes.</span><span class="sxs-lookup"><span data-stu-id="fab48-112">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="fab48-113">Se o StopTime for especificado, mas o StartTime não for especificado, todos os logs existentes antes de StopTime serão retornados.</span><span class="sxs-lookup"><span data-stu-id="fab48-113">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="fab48-114">Se StartTime for especificado, mas o StopTime não for especificado, todos os logs que existirem de StartTime serão retornados.</span><span class="sxs-lookup"><span data-stu-id="fab48-114">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="fab48-115">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fab48-115">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab48-116">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fab48-116">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="fab48-117">Membros</span><span class="sxs-lookup"><span data-stu-id="fab48-117">Members</span></span>

<span data-ttu-id="fab48-118">A **classe \_ RetrieveByTimeRange02 de relatórios do MDM \_ EnterpriseDataProtection01 \_** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fab48-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="fab48-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fab48-119">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fab48-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fab48-120">Properties</span></span>

<span data-ttu-id="fab48-121">A **classe \_ RetrieveByTimeRange02 de relatório do MDM \_ EnterpriseDataProtection01 \_** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fab48-121">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fab48-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fab48-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab48-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fab48-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab48-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fab48-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fab48-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fab48-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fab48-126">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="fab48-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="fab48-127">Para essa classe, a cadeia de caracteres é "RetrieveByTimeRange".</span><span class="sxs-lookup"><span data-stu-id="fab48-127">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="fab48-128">Logs</span><span class="sxs-lookup"><span data-stu-id="fab48-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab48-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fab48-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab48-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fab48-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fab48-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fab48-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab48-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fab48-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab48-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fab48-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fab48-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fab48-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fab48-135">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="fab48-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="fab48-136">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseDataProtection"</span><span class="sxs-lookup"><span data-stu-id="fab48-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="fab48-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="fab48-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab48-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fab48-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab48-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fab48-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fab48-140">StopTime</span><span class="sxs-lookup"><span data-stu-id="fab48-140">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab48-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fab48-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab48-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fab48-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fab48-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="fab48-143">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab48-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fab48-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fab48-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fab48-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fab48-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fab48-146">Requirements</span></span>



| <span data-ttu-id="fab48-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab48-147">Requirement</span></span> | <span data-ttu-id="fab48-148">Valor</span><span class="sxs-lookup"><span data-stu-id="fab48-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fab48-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fab48-149">Minimum supported client</span></span><br/> | <span data-ttu-id="fab48-150">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fab48-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fab48-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fab48-151">Minimum supported server</span></span><br/> | <span data-ttu-id="fab48-152">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fab48-152">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="fab48-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="fab48-153">Namespace</span></span><br/>                | <span data-ttu-id="fab48-154">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="fab48-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="fab48-155">MOF</span><span class="sxs-lookup"><span data-stu-id="fab48-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fab48-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fab48-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="fab48-157">DLL</span><span class="sxs-lookup"><span data-stu-id="fab48-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fab48-158"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="fab48-158"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

