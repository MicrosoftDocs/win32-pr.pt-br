---
description: Defina o conjunto de ações para o \_ código de \_ controle gerenciar atributos de conjunto de dados de armazenamento de IOCTL \_ \_ \_ .
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826382"
---
# <a name="device_data_management_set_action"></a><span data-ttu-id="772bd-103">\_ação do \_ conjunto de gerenciamento de dados do dispositivo \_ \_</span><span class="sxs-lookup"><span data-stu-id="772bd-103">DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION</span></span>

<span data-ttu-id="772bd-104">Os valores constantes a seguir são o conjunto de valores possíveis para o tipo de ação do conjunto de gerenciamento de dados do dispositivo, que é definido como o tipo **DWORD**. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="772bd-104">The following constant values are the set of possible values for the **DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION** type, which is defined as type **DWORD**.</span></span>

<dl> <dt>

<span data-ttu-id="772bd-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="772bd-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction\_None**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772bd-106">0</span><span class="sxs-lookup"><span data-stu-id="772bd-106">0</span></span>
</dt> <dt>



<span data-ttu-id="772bd-107">Nenhuma ação é executada.</span><span class="sxs-lookup"><span data-stu-id="772bd-107">No action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="772bd-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**</span><span class="sxs-lookup"><span data-stu-id="772bd-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction\_Trim**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772bd-109">1</span><span class="sxs-lookup"><span data-stu-id="772bd-109">1</span></span>
</dt> <dt>



<span data-ttu-id="772bd-110">Uma ação de corte é executada.</span><span class="sxs-lookup"><span data-stu-id="772bd-110">A trim action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="772bd-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**Notificação de DeviceDsmAction \_**</span><span class="sxs-lookup"><span data-stu-id="772bd-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**DeviceDsmAction\_Notification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772bd-112">2 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="772bd-112">2 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000002)</span></span>
</dt> <dt>



<span data-ttu-id="772bd-113">Uma ação de notificação é executada.</span><span class="sxs-lookup"><span data-stu-id="772bd-113">A notification action is performed.</span></span> <span data-ttu-id="772bd-114">Os parâmetros estão em uma estrutura de [**parâmetros de notificação do DSM do dispositivo \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) .</span><span class="sxs-lookup"><span data-stu-id="772bd-114">The parameters are in a [**DEVICE\_DSM\_NOTIFICATION\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) structure.</span></span> <span data-ttu-id="772bd-115">O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.</span><span class="sxs-lookup"><span data-stu-id="772bd-115">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="772bd-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**</span><span class="sxs-lookup"><span data-stu-id="772bd-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction\_OffloadRead**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772bd-117">3 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="772bd-117">3 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000003)</span></span>
</dt> <dt>



<span data-ttu-id="772bd-118">Uma ação de leitura de descarregamento é executada.</span><span class="sxs-lookup"><span data-stu-id="772bd-118">An offload read action is performed.</span></span> <span data-ttu-id="772bd-119">Os parâmetros estão em uma estrutura de [**\_ parâmetros de \_ \_ leitura \_ de descarregamento de DSM de dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) .</span><span class="sxs-lookup"><span data-stu-id="772bd-119">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_READ\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) structure.</span></span> <span data-ttu-id="772bd-120">A saída está em uma estrutura de [**\_ saída de \_ leitura \_ de descarregamento de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) .</span><span class="sxs-lookup"><span data-stu-id="772bd-120">The output is in a [**STORAGE\_OFFLOAD\_READ\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) structure.</span></span> <span data-ttu-id="772bd-121">O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.</span><span class="sxs-lookup"><span data-stu-id="772bd-121">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="772bd-122">**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="772bd-122">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="772bd-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**</span><span class="sxs-lookup"><span data-stu-id="772bd-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction\_OffloadWrite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772bd-124">4</span><span class="sxs-lookup"><span data-stu-id="772bd-124">4</span></span>
</dt> <dt>



<span data-ttu-id="772bd-125">Uma ação de gravação de descarregamento é executada.</span><span class="sxs-lookup"><span data-stu-id="772bd-125">An offload write action is performed.</span></span> <span data-ttu-id="772bd-126">Os parâmetros estão em uma estrutura de [**\_ parâmetros de \_ \_ gravação \_ de descarregamento de DSM de dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) .</span><span class="sxs-lookup"><span data-stu-id="772bd-126">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_WRITE\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) structure.</span></span> <span data-ttu-id="772bd-127">A saída está em uma estrutura de [**\_ saída de \_ gravação \_ de descarregamento de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .</span><span class="sxs-lookup"><span data-stu-id="772bd-127">The output is in a [**STORAGE\_OFFLOAD\_WRITE\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) structure.</span></span>

<span data-ttu-id="772bd-128">**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="772bd-128">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="772bd-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Alocação de DeviceDsmAction \_**</span><span class="sxs-lookup"><span data-stu-id="772bd-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**DeviceDsmAction\_Allocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772bd-130">5 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000005)</span><span class="sxs-lookup"><span data-stu-id="772bd-130">5 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000005)</span></span>
</dt> <dt>



<span data-ttu-id="772bd-131">Um bitmap de alocação é retornado para o primeiro intervalo de conjuntos de dados passado.</span><span class="sxs-lookup"><span data-stu-id="772bd-131">An allocation bitmap is returned for the first data set range passed in.</span></span> <span data-ttu-id="772bd-132">A saída está em uma estrutura de [**estado de provisionamento do conjunto de dados de dispositivo \_ \_ \_ lb \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) .</span><span class="sxs-lookup"><span data-stu-id="772bd-132">The output is in a [**DEVICE\_DATA\_SET\_LB\_PROVISIONING\_STATE**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) structure.</span></span> <span data-ttu-id="772bd-133">O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.</span><span class="sxs-lookup"><span data-stu-id="772bd-133">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="772bd-134">**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="772bd-134">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="772bd-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**\_Reparo DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="772bd-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction\_Repair**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772bd-136">6 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000006)</span><span class="sxs-lookup"><span data-stu-id="772bd-136">6 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000006)</span></span>
</dt> <dt>



<span data-ttu-id="772bd-137">Uma ação de reparo é executada.</span><span class="sxs-lookup"><span data-stu-id="772bd-137">A repair action is performed.</span></span> <span data-ttu-id="772bd-138">O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.</span><span class="sxs-lookup"><span data-stu-id="772bd-138">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="772bd-139">**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="772bd-139">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="772bd-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**Limpeza de DeviceDsmAction \_**</span><span class="sxs-lookup"><span data-stu-id="772bd-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction\_Scrub**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772bd-141">7 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000007)</span><span class="sxs-lookup"><span data-stu-id="772bd-141">7 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000007)</span></span>
</dt> <dt>



<span data-ttu-id="772bd-142">Uma ação de limpeza é executada.</span><span class="sxs-lookup"><span data-stu-id="772bd-142">A scrub action is performed.</span></span> <span data-ttu-id="772bd-143">O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.</span><span class="sxs-lookup"><span data-stu-id="772bd-143">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="772bd-144">**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="772bd-144">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="772bd-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**\_Resiliência DeviceDsmAction**</span><span class="sxs-lookup"><span data-stu-id="772bd-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**DeviceDsmAction\_Resiliency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="772bd-146">8 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000008)</span><span class="sxs-lookup"><span data-stu-id="772bd-146">8 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000008)</span></span>
</dt> <dt>



<span data-ttu-id="772bd-147">Uma ação de resiliência é executada.</span><span class="sxs-lookup"><span data-stu-id="772bd-147">A resiliency action is performed.</span></span> <span data-ttu-id="772bd-148">O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.</span><span class="sxs-lookup"><span data-stu-id="772bd-148">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="772bd-149">**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="772bd-149">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="772bd-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="772bd-150">Requirements</span></span>



| <span data-ttu-id="772bd-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="772bd-151">Requirement</span></span> | <span data-ttu-id="772bd-152">Valor</span><span class="sxs-lookup"><span data-stu-id="772bd-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772bd-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="772bd-153">Minimum supported client</span></span><br/> | <span data-ttu-id="772bd-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="772bd-154">Windows 7</span></span><br/>                                                                                      |
| <span data-ttu-id="772bd-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="772bd-155">Minimum supported server</span></span><br/> | <span data-ttu-id="772bd-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="772bd-156">Windows Server 2008 R2</span></span><br/>                                                                         |
| <span data-ttu-id="772bd-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="772bd-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="772bd-158"><dt>WinIoCtl. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="772bd-158"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



 

 




