---
description: Solicita que o estado de replicação da máquina virtual seja alterado para o valor especificado e atue na relação de replicação primária da máquina virtual.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Método RequestReplicationStateChange da classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505687"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="dad93-103">Método RequestReplicationStateChange da classe de \_ ComputerSystem Msvm</span><span class="sxs-lookup"><span data-stu-id="dad93-103">RequestReplicationStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="dad93-104">Solicita que o estado de replicação da máquina virtual seja alterado para o valor especificado e atue na relação de replicação primária da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dad93-104">Requests that the replication state of the virtual machine be changed to the specified value and acts on the primary replication relationship of the virtual machine.</span></span> <span data-ttu-id="dad93-105">Enquanto a alteração de estado estiver em andamento, a propriedade **replicationstate** será alterada para o valor do parâmetro *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="dad93-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="dad93-106">Esse método só tem suporte para instâncias da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representam uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dad93-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="dad93-107">A partir do Windows 8.1, recomendamos não usar o **RequestReplicationStateChange** para solicitar a alteração do estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="dad93-107">Starting with Windows 8.1, we recommend not to use **RequestReplicationStateChange** anymore to request changing of replication state.</span></span> <span data-ttu-id="dad93-108">Em vez disso, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="dad93-108">Instead, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="dad93-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dad93-109">Syntax</span></span>


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="dad93-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dad93-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad93-111">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dad93-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad93-112">O novo estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="dad93-112">The new replication state.</span></span> <span data-ttu-id="dad93-113">O deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dad93-113">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="dad93-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Pronto para iniciar a replicação inicial** (1)</span><span class="sxs-lookup"><span data-stu-id="dad93-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dad93-115">Pronto para iniciar a replicação inicial.</span><span class="sxs-lookup"><span data-stu-id="dad93-115">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="dad93-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Aguardando para concluir a replicação inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="dad93-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dad93-117">Aguardando para concluir a replicação inicial.</span><span class="sxs-lookup"><span data-stu-id="dad93-117">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="dad93-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="dad93-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dad93-119">Replicando.</span><span class="sxs-lookup"><span data-stu-id="dad93-119">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="dad93-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicação sincronizada concluída** (4)</span><span class="sxs-lookup"><span data-stu-id="dad93-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dad93-121">Replicação sincronizada concluída.</span><span class="sxs-lookup"><span data-stu-id="dad93-121">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="dad93-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (7)</span><span class="sxs-lookup"><span data-stu-id="dad93-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dad93-123">Suspender a replicação.</span><span class="sxs-lookup"><span data-stu-id="dad93-123">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="dad93-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancelar ressincronização** (9)</span><span class="sxs-lookup"><span data-stu-id="dad93-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="dad93-125">Cancele a ressincronização.</span><span class="sxs-lookup"><span data-stu-id="dad93-125">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dad93-126">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="dad93-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad93-127">Uma referência opcional a um objeto [**Msvm \_ ConcreteJob**](msvm-concretejob.md) que é retornado se a operação é executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="dad93-127">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="dad93-128">Se estiver presente, a referência retornada poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="dad93-128">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="dad93-129">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dad93-129">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad93-130">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="dad93-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad93-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dad93-131">Return value</span></span>

<span data-ttu-id="dad93-132">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dad93-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="dad93-133">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dad93-133">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="dad93-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="dad93-134">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dad93-135"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="dad93-136">Êxito</span><span class="sxs-lookup"><span data-stu-id="dad93-136">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="dad93-137"><dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-137"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="dad93-138">A transição é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="dad93-138">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="dad93-139"><dt>32768</dt> <dt>**com falha**</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-139"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="dad93-140"><dt>**Acesso negado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-140"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="dad93-141"><dt>**Sem suporte**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-141"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="dad93-142">O <dt>**status é desconhecido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-142"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="dad93-143"><dt>**Tempo limite**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-143"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="dad93-144"><dt>**Parâmetro inválido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-144"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="dad93-145">Não há suporte para o valor especificado em um dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dad93-145">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="dad93-146">O <dt>**sistema está em uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-146"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="dad93-147"><dt>**Estado inválido para esta operação**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-147"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="dad93-148">O valor especificado no parâmetro *requestedstate* não tem suporte no modo de replicação ou no estado atual.</span><span class="sxs-lookup"><span data-stu-id="dad93-148">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="dad93-149"><dt>**Tipo de dados incorreto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-149"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="dad93-150">O <dt>**sistema não está disponível**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-150"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="dad93-151"><dt>**Memória insuficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-151"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="dad93-152"><dt>**Arquivo não encontrado**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-152"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="dad93-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dad93-153">Requirements</span></span>



| <span data-ttu-id="dad93-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="dad93-154">Requirement</span></span> | <span data-ttu-id="dad93-155">Valor</span><span class="sxs-lookup"><span data-stu-id="dad93-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dad93-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad93-156">Minimum supported client</span></span><br/> | <span data-ttu-id="dad93-157">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dad93-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dad93-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad93-158">Minimum supported server</span></span><br/> | <span data-ttu-id="dad93-159">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dad93-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dad93-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="dad93-160">Namespace</span></span><br/>                | <span data-ttu-id="dad93-161">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dad93-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dad93-162">MOF</span><span class="sxs-lookup"><span data-stu-id="dad93-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dad93-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dad93-164">DLL</span><span class="sxs-lookup"><span data-stu-id="dad93-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dad93-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dad93-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dad93-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="dad93-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad93-167">**Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="dad93-167">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




