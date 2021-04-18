---
description: Solicita que o estado de replicação da relação de replicação da máquina virtual seja alterado para o valor especificado.
ms.assetid: 8EC78CCC-2997-4239-A20C-BA56F848ECB6
title: 'Método Msvm_ComputerSystem:: RequestReplicationStateChangeEx'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChangeEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d77db9dff90f985991c8e9013ea4f239cb6479f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750271"
---
# <a name="msvm_computersystemrequestreplicationstatechangeex-method"></a><span data-ttu-id="69815-103">\_Método Msvm ComputerSystem:: RequestReplicationStateChangeEx</span><span class="sxs-lookup"><span data-stu-id="69815-103">Msvm\_ComputerSystem::RequestReplicationStateChangeEx method</span></span>

<span data-ttu-id="69815-104">Solicita que o estado de replicação da relação de replicação da máquina virtual seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="69815-104">Requests that the replication state of the replication relationship of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="69815-105">Enquanto a alteração de estado estiver em andamento, a propriedade **replicationstate** será alterada para o valor do parâmetro *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="69815-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="69815-106">Esse método só tem suporte para instâncias da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representam uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="69815-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="69815-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69815-107">Syntax</span></span>


```C++
uint32 RequestReplicationStateChangeEx(
  [in]  string              ReplicationRelationship,
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="69815-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69815-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69815-109">*ReplicationRelationship* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69815-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69815-110">Uma representação de cadeia de caracteres de uma instância inserida da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define a relação de replicação para a solicitação de alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="69815-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for state change request.</span></span> <span data-ttu-id="69815-111">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="69815-111">This parameter is optional.</span></span> <span data-ttu-id="69815-112">Quando não for especificado, a solicitação será executada na relação de replicação primária.</span><span class="sxs-lookup"><span data-stu-id="69815-112">When it's unspecified, the request runs on the primary replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="69815-113">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69815-113">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69815-114">O novo estado de replicação.</span><span class="sxs-lookup"><span data-stu-id="69815-114">The new replication state.</span></span> <span data-ttu-id="69815-115">O deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="69815-115">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="69815-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Pronto para iniciar a replicação inicial** (1)</span><span class="sxs-lookup"><span data-stu-id="69815-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="69815-117">Pronto para iniciar a replicação inicial.</span><span class="sxs-lookup"><span data-stu-id="69815-117">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="69815-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Aguardando para concluir a replicação inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="69815-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="69815-119">Aguardando para concluir a replicação inicial.</span><span class="sxs-lookup"><span data-stu-id="69815-119">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="69815-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="69815-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="69815-121">Replicando.</span><span class="sxs-lookup"><span data-stu-id="69815-121">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="69815-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicação sincronizada concluída** (4)</span><span class="sxs-lookup"><span data-stu-id="69815-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="69815-123">Replicação sincronizada concluída.</span><span class="sxs-lookup"><span data-stu-id="69815-123">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="69815-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (7)</span><span class="sxs-lookup"><span data-stu-id="69815-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="69815-125">Suspender a replicação.</span><span class="sxs-lookup"><span data-stu-id="69815-125">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="69815-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancelar ressincronização** (9)</span><span class="sxs-lookup"><span data-stu-id="69815-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="69815-127">Cancele a ressincronização.</span><span class="sxs-lookup"><span data-stu-id="69815-127">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="69815-128">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="69815-128">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69815-129">Uma referência opcional a um objeto [**Msvm \_ ConcreteJob**](msvm-concretejob.md) que é retornado se a operação é executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="69815-129">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="69815-130">Se estiver presente, a referência retornada poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="69815-130">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="69815-131">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69815-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69815-132">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="69815-132">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69815-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69815-133">Return value</span></span>

<span data-ttu-id="69815-134">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="69815-134">This method returns one of the following values.</span></span>



| <span data-ttu-id="69815-135">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="69815-135">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="69815-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="69815-136">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69815-137"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="69815-137"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="69815-138">Êxito</span><span class="sxs-lookup"><span data-stu-id="69815-138">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="69815-139"><dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="69815-139"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="69815-140">A transição é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="69815-140">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="69815-141"><dt>32768</dt> <dt>**com falha**</dt></span><span class="sxs-lookup"><span data-stu-id="69815-141"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="69815-142"><dt>**Acesso negado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="69815-142"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="69815-143"><dt>**Sem suporte**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="69815-143"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="69815-144">O <dt>**status é desconhecido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="69815-144"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="69815-145"><dt>**Tempo limite**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="69815-145"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="69815-146"><dt>**Parâmetro inválido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="69815-146"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="69815-147">Não há suporte para o valor especificado em um dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="69815-147">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="69815-148">O <dt>**sistema está em uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="69815-148"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="69815-149"><dt>**Estado inválido para esta operação**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="69815-149"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="69815-150">O valor especificado no parâmetro *requestedstate* não tem suporte no modo de replicação ou no estado atual.</span><span class="sxs-lookup"><span data-stu-id="69815-150">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="69815-151"><dt>**Tipo de dados incorreto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="69815-151"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="69815-152">O <dt>**sistema não está disponível**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="69815-152"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="69815-153"><dt>**Memória insuficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="69815-153"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="69815-154"><dt>**Arquivo não encontrado**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="69815-154"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="69815-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69815-155">Requirements</span></span>



| <span data-ttu-id="69815-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="69815-156">Requirement</span></span> | <span data-ttu-id="69815-157">Valor</span><span class="sxs-lookup"><span data-stu-id="69815-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69815-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69815-158">Minimum supported client</span></span><br/> | <span data-ttu-id="69815-159">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69815-159">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="69815-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69815-160">Minimum supported server</span></span><br/> | <span data-ttu-id="69815-161">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="69815-161">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69815-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="69815-162">Namespace</span></span><br/>                | <span data-ttu-id="69815-163">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="69815-163">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="69815-164">MOF</span><span class="sxs-lookup"><span data-stu-id="69815-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69815-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69815-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69815-166">DLL</span><span class="sxs-lookup"><span data-stu-id="69815-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69815-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69815-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69815-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="69815-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69815-169">**Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="69815-169">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




