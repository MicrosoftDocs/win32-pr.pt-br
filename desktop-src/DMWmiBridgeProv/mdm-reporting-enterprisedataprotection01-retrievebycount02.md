---
title: Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
description: A \_ classe RetrieveByCount02 de relatório do MDM \_ EnterpriseDataProtection01 \_ é usada para recuperar um número especificado de logs do StartTime.
ms.assetid: 0a581d5a-129b-48c3-a7a1-3947cc1e2ee9
keywords:
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02, descrita
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fcc6e7ed3ccb630b500179d7273bdd09a21477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454666"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebycount02-class"></a><span data-ttu-id="c9d5b-105">\_Classe RetrieveByCount02 de relatórios MDM \_ EnterpriseDataProtection01 \_</span><span class="sxs-lookup"><span data-stu-id="c9d5b-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02 class</span></span>

<span data-ttu-id="c9d5b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c9d5b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c9d5b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c9d5b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c9d5b-108">A **classe \_ RetrieveByCount02 de relatório do MDM \_ EnterpriseDataProtection01 \_** é usada para recuperar um número especificado de logs do StartTime.</span><span class="sxs-lookup"><span data-stu-id="c9d5b-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class is used to retrieve a specified number of logs from the StartTime.</span></span> <span data-ttu-id="c9d5b-109">O StartTime é expresso no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="c9d5b-109">The StartTime is expressed in ISO 8601 format.</span></span> <span data-ttu-id="c9d5b-110">Você pode definir o número de logs exigidos definindo LogCount e StartTime.</span><span class="sxs-lookup"><span data-stu-id="c9d5b-110">You can set the number of logs required by setting LogCount and StartTime.</span></span> <span data-ttu-id="c9d5b-111">Ele retorna o número especificado de log ou menos, se o número total de logs for menor que LogCount.</span><span class="sxs-lookup"><span data-stu-id="c9d5b-111">It returns the specified number of log or less, if the total number logs is less than LogCount.</span></span>

<span data-ttu-id="c9d5b-112">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c9d5b-112">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d5b-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9d5b-113">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="c9d5b-114">Membros</span><span class="sxs-lookup"><span data-stu-id="c9d5b-114">Members</span></span>

<span data-ttu-id="c9d5b-115">A **classe \_ RetrieveByCount02 de relatórios do MDM \_ EnterpriseDataProtection01 \_** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c9d5b-115">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these types of members:</span></span>

-   [<span data-ttu-id="c9d5b-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9d5b-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9d5b-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9d5b-117">Properties</span></span>

<span data-ttu-id="c9d5b-118">A **classe \_ RetrieveByCount02 de relatório do MDM \_ EnterpriseDataProtection01 \_** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c9d5b-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9d5b-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c9d5b-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d5b-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9d5b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9d5b-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9d5b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9d5b-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c9d5b-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c9d5b-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="c9d5b-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="c9d5b-124">Para essa classe, a cadeia de caracteres é "RetrieveByCount".</span><span class="sxs-lookup"><span data-stu-id="c9d5b-124">For this class, the string is "RetrieveByCount".</span></span>

</dd> <dt>

[<span data-ttu-id="c9d5b-125">LogCount</span><span class="sxs-lookup"><span data-stu-id="c9d5b-125">LogCount</span></span>](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d5b-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c9d5b-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9d5b-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c9d5b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c9d5b-128">Logs</span><span class="sxs-lookup"><span data-stu-id="c9d5b-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d5b-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9d5b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9d5b-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c9d5b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c9d5b-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c9d5b-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d5b-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9d5b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9d5b-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9d5b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9d5b-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c9d5b-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c9d5b-135">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="c9d5b-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="c9d5b-136">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseDataProtection"</span><span class="sxs-lookup"><span data-stu-id="c9d5b-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="c9d5b-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="c9d5b-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d5b-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9d5b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9d5b-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c9d5b-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c9d5b-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9d5b-140">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9d5b-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c9d5b-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9d5b-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c9d5b-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9d5b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9d5b-143">Requirements</span></span>



| <span data-ttu-id="c9d5b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9d5b-144">Requirement</span></span> | <span data-ttu-id="c9d5b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="c9d5b-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d5b-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9d5b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c9d5b-147">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c9d5b-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c9d5b-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9d5b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c9d5b-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c9d5b-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="c9d5b-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9d5b-150">Namespace</span></span><br/>                | <span data-ttu-id="c9d5b-151">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c9d5b-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="c9d5b-152">MOF</span><span class="sxs-lookup"><span data-stu-id="c9d5b-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9d5b-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9d5b-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="c9d5b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="c9d5b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9d5b-155"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="c9d5b-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

