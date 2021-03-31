---
description: Testa a conectividade de rede de uma VM em um ambiente de virtualização de rede do Windows.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Método TestNetworkConnection da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e8f15faacb1b8ad683b1ea9abfa9b91f5c376dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089996"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="0de1c-103">Método TestNetworkConnection da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="0de1c-103">TestNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="0de1c-104">Testa a conectividade de rede de uma VM em um ambiente de virtualização de rede do Windows.</span><span class="sxs-lookup"><span data-stu-id="0de1c-104">Tests the network connectivity of a VM in a Windows network virtualization environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0de1c-105">Syntax</span></span>


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0de1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0de1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de1c-107">*TargetNetworkAdapter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0de1c-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de1c-108">Referência a um [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) descrevendo o adaptador de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="0de1c-108">Reference to a [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) describing the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0de1c-109">*Isenviador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0de1c-109">*IsSender* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de1c-110">Indica se este método está sendo invocado no remetente ou no destinatário.</span><span class="sxs-lookup"><span data-stu-id="0de1c-110">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="0de1c-111">*SenderIP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0de1c-111">*SenderIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de1c-112">O endereço IP do remetente.</span><span class="sxs-lookup"><span data-stu-id="0de1c-112">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0de1c-113">*ReceiverIP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0de1c-113">*ReceiverIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de1c-114">O endereço MAC do remetente.</span><span class="sxs-lookup"><span data-stu-id="0de1c-114">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="0de1c-115">*ReceiverMac* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0de1c-115">*ReceiverMac* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de1c-116">O endereço MAC do remetente.</span><span class="sxs-lookup"><span data-stu-id="0de1c-116">The sender Mac address.</span></span>

</dd> <dt>

<span data-ttu-id="0de1c-117">*Isolamentoid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0de1c-117">*IsolationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de1c-118">A ID de isolamento.</span><span class="sxs-lookup"><span data-stu-id="0de1c-118">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="0de1c-119">*SequenceNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0de1c-119">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de1c-120">A ID de isolamento.</span><span class="sxs-lookup"><span data-stu-id="0de1c-120">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="0de1c-121">*RoundtripTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0de1c-121">*RoundTripTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0de1c-122">O tempo de ida e volta.</span><span class="sxs-lookup"><span data-stu-id="0de1c-122">The round trip time.</span></span>

</dd> <dt>

<span data-ttu-id="0de1c-123">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0de1c-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0de1c-124">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0de1c-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0de1c-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0de1c-125">Return value</span></span>

<span data-ttu-id="0de1c-126">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0de1c-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0de1c-127">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="0de1c-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0de1c-128">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="0de1c-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0de1c-129">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="0de1c-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0de1c-130">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="0de1c-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0de1c-131">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="0de1c-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0de1c-132">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0de1c-132">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0de1c-133">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0de1c-133">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0de1c-134">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0de1c-134">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0de1c-135">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0de1c-135">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0de1c-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0de1c-136">Requirements</span></span>



| <span data-ttu-id="0de1c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0de1c-137">Requirement</span></span> | <span data-ttu-id="0de1c-138">Valor</span><span class="sxs-lookup"><span data-stu-id="0de1c-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0de1c-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0de1c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0de1c-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0de1c-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0de1c-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0de1c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0de1c-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0de1c-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0de1c-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="0de1c-143">Namespace</span></span><br/>                | <span data-ttu-id="0de1c-144">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0de1c-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0de1c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="0de1c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0de1c-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0de1c-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0de1c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0de1c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0de1c-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0de1c-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0de1c-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="0de1c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de1c-150">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="0de1c-150">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

