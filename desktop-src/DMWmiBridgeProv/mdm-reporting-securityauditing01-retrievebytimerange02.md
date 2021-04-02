---
title: Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
description: A \_ classe SecurityAuditing01 RetrieveByTimeRange02 de relatórios do MDM \_ \_ é usada para recuperar os logs que existem dentro de StartTime e StopTime.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02, descrita
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbbe47dfb3ff23c1d1bd891053375e19d6e503e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644290"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a><span data-ttu-id="91d00-105">\_Classe RetrieveByTimeRange02 de relatórios MDM \_ SecurityAuditing01 \_</span><span class="sxs-lookup"><span data-stu-id="91d00-105">MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="91d00-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="91d00-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="91d00-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="91d00-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="91d00-108">A **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 de relatórios do MDM** é usada para recuperar os logs que existem dentro de StartTime e StopTime. os StartTime e StopTime são expressos no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="91d00-108">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="91d00-109">Se StartTime e StopTime não forem especificados, os valores serão interpretados como a primeira hora existente ou a última.</span><span class="sxs-lookup"><span data-stu-id="91d00-109">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="91d00-110">Estes são os outros cenários possíveis:</span><span class="sxs-lookup"><span data-stu-id="91d00-110">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="91d00-111">Se StartTime e StopTime não forem especificados, ele retornará todos os logs existentes.</span><span class="sxs-lookup"><span data-stu-id="91d00-111">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="91d00-112">Se o StopTime for especificado, mas o StartTime não for especificado, todos os logs existentes antes de StopTime serão retornados.</span><span class="sxs-lookup"><span data-stu-id="91d00-112">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="91d00-113">Se StartTime for especificado, mas o StopTime não for especificado, todos os logs que existirem de StartTime serão retornados.</span><span class="sxs-lookup"><span data-stu-id="91d00-113">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="91d00-114">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="91d00-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d00-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91d00-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a><span data-ttu-id="91d00-116">Membros</span><span class="sxs-lookup"><span data-stu-id="91d00-116">Members</span></span>

<span data-ttu-id="91d00-117">A **classe \_ RetrieveByTimeRange02 de relatórios do MDM \_ SecurityAuditing01 \_** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="91d00-117">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="91d00-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="91d00-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91d00-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="91d00-119">Properties</span></span>

<span data-ttu-id="91d00-120">A **classe \_ RetrieveByTimeRange02 de relatório do MDM \_ SecurityAuditing01 \_** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="91d00-120">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91d00-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="91d00-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d00-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91d00-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d00-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="91d00-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d00-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91d00-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91d00-125">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="91d00-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="91d00-126">Para essa classe, a cadeia de caracteres é "RetrieveByTimeRange".</span><span class="sxs-lookup"><span data-stu-id="91d00-126">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="91d00-127">Logs</span><span class="sxs-lookup"><span data-stu-id="91d00-127">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d00-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91d00-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d00-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91d00-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="91d00-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="91d00-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d00-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91d00-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d00-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="91d00-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91d00-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="91d00-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="91d00-134">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="91d00-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="91d00-135">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/SecurityAuditing"</span><span class="sxs-lookup"><span data-stu-id="91d00-135">For this class, the string is "./Vendor/MSFT/SecurityAuditing"</span></span>

</dd> <dt>

[<span data-ttu-id="91d00-136">StartTime</span><span class="sxs-lookup"><span data-stu-id="91d00-136">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d00-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91d00-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d00-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91d00-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="91d00-139">StopTime</span><span class="sxs-lookup"><span data-stu-id="91d00-139">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="91d00-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="91d00-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91d00-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="91d00-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91d00-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91d00-142">Requirements</span></span>



| <span data-ttu-id="91d00-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d00-143">Requirement</span></span> | <span data-ttu-id="91d00-144">Valor</span><span class="sxs-lookup"><span data-stu-id="91d00-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d00-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91d00-145">Minimum supported client</span></span><br/> | <span data-ttu-id="91d00-146">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="91d00-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="91d00-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91d00-147">Minimum supported server</span></span><br/> | <span data-ttu-id="91d00-148">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="91d00-148">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="91d00-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="91d00-149">Namespace</span></span><br/>                | <span data-ttu-id="91d00-150">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="91d00-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="91d00-151">MOF</span><span class="sxs-lookup"><span data-stu-id="91d00-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91d00-152"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91d00-152"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="91d00-153">DLL</span><span class="sxs-lookup"><span data-stu-id="91d00-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91d00-154"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="91d00-154"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

