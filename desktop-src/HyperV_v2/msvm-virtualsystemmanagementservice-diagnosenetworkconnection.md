---
description: Diagnostica a conectividade de rede de uma VM em um ambiente de virtualização de rede do Windows.
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Método DiagnoseNetworkConnection da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 70760f771e3908265a4ac70ebc1cbdf957d652c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770211"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="15492-103">Método DiagnoseNetworkConnection da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="15492-103">DiagnoseNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="15492-104">Diagnostica a conectividade de rede de uma VM em um ambiente de virtualização de rede do Windows.</span><span class="sxs-lookup"><span data-stu-id="15492-104">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="15492-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15492-105">Syntax</span></span>


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="15492-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15492-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15492-107">*TargetNetworkAdapter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15492-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15492-108">Referência a um [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que descreve o adaptador de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="15492-108">Reference to an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) that describes the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="15492-109">*DiagnosticSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15492-109">*DiagnosticSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15492-110">As configurações de diagnóstico a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="15492-110">The diagnostic settings to use.</span></span>

</dd> <dt>

<span data-ttu-id="15492-111">*DiagnosticInformation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="15492-111">*DiagnosticInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15492-112">Em caso de sucesso, retorna as informações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="15492-112">On success, returns the diagnostic information.</span></span>

</dd> <dt>

<span data-ttu-id="15492-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="15492-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15492-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="15492-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15492-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15492-115">Return value</span></span>

<span data-ttu-id="15492-116">Retorna 0 ou 4096 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="15492-116">Returns a 0 or 4096 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="15492-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="15492-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="15492-118">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="15492-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="15492-119">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="15492-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="15492-120">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="15492-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="15492-121">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="15492-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="15492-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="15492-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="15492-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="15492-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="15492-124">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="15492-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="15492-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="15492-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="15492-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15492-126">Requirements</span></span>



| <span data-ttu-id="15492-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="15492-127">Requirement</span></span> | <span data-ttu-id="15492-128">Valor</span><span class="sxs-lookup"><span data-stu-id="15492-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15492-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15492-129">Minimum supported client</span></span><br/> | <span data-ttu-id="15492-130">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="15492-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="15492-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15492-131">Minimum supported server</span></span><br/> | <span data-ttu-id="15492-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="15492-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="15492-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="15492-133">Namespace</span></span><br/>                | <span data-ttu-id="15492-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="15492-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15492-135">MOF</span><span class="sxs-lookup"><span data-stu-id="15492-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15492-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15492-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15492-137">DLL</span><span class="sxs-lookup"><span data-stu-id="15492-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15492-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15492-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15492-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="15492-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15492-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="15492-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

