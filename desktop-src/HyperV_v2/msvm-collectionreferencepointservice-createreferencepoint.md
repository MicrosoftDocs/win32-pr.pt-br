---
description: Cria um ponto de referência de uma coleção de sistemas virtuais.
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Método CreateReferencePoint da classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7681795ee18965e3e04b75c800e3e574d6627ea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297712"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="720a2-103">Método CreateReferencePoint da \_ classe CollectionReferencePointService Msvm</span><span class="sxs-lookup"><span data-stu-id="720a2-103">CreateReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="720a2-104">Cria um ponto de referência de uma coleção de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="720a2-104">Creates a reference point of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="720a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="720a2-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="720a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="720a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="720a2-107">*Coleção* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="720a2-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="720a2-108">Referência à coleção de sistema virtual afetada.</span><span class="sxs-lookup"><span data-stu-id="720a2-108">Reference to the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="720a2-109">*ReferencePointSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="720a2-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="720a2-110">Configurações de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="720a2-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="720a2-111">*ReferencePointType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="720a2-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="720a2-112">Indica o tipo do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="720a2-112">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="720a2-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="720a2-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="720a2-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Baseado em log** (1)</span><span class="sxs-lookup"><span data-stu-id="720a2-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="720a2-115">Rastreamento de log de réplica do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="720a2-115">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="720a2-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Baseado em RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="720a2-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="720a2-117">Com base em Controle de Alterações resilientes de discos virtuais.</span><span class="sxs-lookup"><span data-stu-id="720a2-117">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="720a2-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="720a2-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="720a2-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="720a2-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="720a2-120">*ResultingReferencePointCollection* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="720a2-120">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="720a2-121">Ponto de referência resultante de uma coleção de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="720a2-121">Resulting reference point of a virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="720a2-122">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="720a2-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="720a2-123">Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="720a2-123">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="720a2-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="720a2-124">Return value</span></span>

<span data-ttu-id="720a2-125">Se for bem-sucedido, retornará 0 (sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="720a2-125">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="720a2-126">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="720a2-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-127">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="720a2-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-128">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="720a2-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-129">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="720a2-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-130">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="720a2-130">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-131">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="720a2-131">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-132">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="720a2-132">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-133">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="720a2-133">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-134">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="720a2-134">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-135">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="720a2-135">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="720a2-136">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="720a2-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="720a2-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="720a2-137">Requirements</span></span>



| <span data-ttu-id="720a2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="720a2-138">Requirement</span></span> | <span data-ttu-id="720a2-139">Valor</span><span class="sxs-lookup"><span data-stu-id="720a2-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="720a2-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="720a2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="720a2-141">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="720a2-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="720a2-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="720a2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="720a2-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="720a2-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="720a2-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="720a2-144">Namespace</span></span><br/>                | <span data-ttu-id="720a2-145">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="720a2-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="720a2-146">MOF</span><span class="sxs-lookup"><span data-stu-id="720a2-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="720a2-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="720a2-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="720a2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="720a2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="720a2-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="720a2-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="720a2-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="720a2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="720a2-151">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="720a2-151">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




