---
title: Classe MDM_DeviceStatus_Battery01
description: A \_ classe MDM DeviceStatus \_ Battery01 é usada pela empresa para consultar o estado de conformidade da bateria de dispositivos com suas políticas corporativas.
ms.assetid: f4e92e2a-e267-467a-9905-2539dcaf8d8c
keywords:
- Classe MDM_DeviceStatus_Battery01
- Classe MDM_DeviceStatus_Battery01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Battery01
- MDM_DeviceStatus_Battery01.InstanceID
- MDM_DeviceStatus_Battery01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b89cd709c4d0d3d5ad3490114bc82d36aa4ef0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749066"
---
# <a name="mdm_devicestatus_battery01-class"></a><span data-ttu-id="9608d-105">\_ \_ Classe BATTERY01 do MDM DeviceStatus</span><span class="sxs-lookup"><span data-stu-id="9608d-105">MDM\_DeviceStatus\_Battery01 class</span></span>

<span data-ttu-id="9608d-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="9608d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9608d-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="9608d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9608d-108">A classe **MDM \_ DeviceStatus \_ Battery01** é usada pela empresa para consultar o estado de conformidade da bateria de dispositivos com suas políticas corporativas.</span><span class="sxs-lookup"><span data-stu-id="9608d-108">The **MDM\_DeviceStatus\_Battery01** class is used by the enterprise to query the state of battery compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="9608d-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9608d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9608d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9608d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Battery01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  sint32 EstimatedChargeRemaining;
  sint32 EstimatedRuntime;
};
```

## <a name="members"></a><span data-ttu-id="9608d-111">Membros</span><span class="sxs-lookup"><span data-stu-id="9608d-111">Members</span></span>

<span data-ttu-id="9608d-112">A **classe \_ \_ Battery01 de MDM DeviceStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9608d-112">The **MDM\_DeviceStatus\_Battery01** class has these types of members:</span></span>

-   [<span data-ttu-id="9608d-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9608d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9608d-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9608d-114">Properties</span></span>

<span data-ttu-id="9608d-115">A **classe \_ \_ Battery01 do MDM DeviceStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9608d-115">The **MDM\_DeviceStatus\_Battery01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9608d-116">EstimatedChargeRemaining</span><span class="sxs-lookup"><span data-stu-id="9608d-116">EstimatedChargeRemaining</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedchargeremaining)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9608d-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9608d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9608d-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9608d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9608d-119">EstimatedRuntime</span><span class="sxs-lookup"><span data-stu-id="9608d-119">EstimatedRuntime</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedruntime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9608d-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9608d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9608d-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9608d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9608d-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9608d-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9608d-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9608d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9608d-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9608d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9608d-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9608d-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9608d-126">Nó para a consulta de bateria.</span><span class="sxs-lookup"><span data-stu-id="9608d-126">Node for the battery query.</span></span>

</dd> <dt>

<span data-ttu-id="9608d-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9608d-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9608d-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9608d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9608d-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9608d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9608d-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9608d-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9608d-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="9608d-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="9608d-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="9608d-132">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="9608d-133">Status</span><span class="sxs-lookup"><span data-stu-id="9608d-133">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9608d-134">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9608d-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9608d-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9608d-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9608d-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9608d-136">Requirements</span></span>



| <span data-ttu-id="9608d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9608d-137">Requirement</span></span> | <span data-ttu-id="9608d-138">Valor</span><span class="sxs-lookup"><span data-stu-id="9608d-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9608d-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9608d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9608d-140">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9608d-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9608d-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9608d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9608d-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9608d-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9608d-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="9608d-143">Namespace</span></span><br/>                | <span data-ttu-id="9608d-144">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9608d-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9608d-145">MOF</span><span class="sxs-lookup"><span data-stu-id="9608d-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9608d-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9608d-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9608d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9608d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9608d-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9608d-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

