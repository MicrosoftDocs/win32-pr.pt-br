---
description: Gerencia a replicação de uma máquina virtual.
ms.assetid: 0335fb94-5f2b-43be-bfb4-bc6811c5b507
title: Classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService
- Msvm_ReplicationService.InstanceID
- Msvm_ReplicationService.Caption
- Msvm_ReplicationService.Description
- Msvm_ReplicationService.ElementName
- Msvm_ReplicationService.InstallDate
- Msvm_ReplicationService.Name
- Msvm_ReplicationService.OperationalStatus
- Msvm_ReplicationService.StatusDescriptions
- Msvm_ReplicationService.Status
- Msvm_ReplicationService.HealthState
- Msvm_ReplicationService.CommunicationStatus
- Msvm_ReplicationService.DetailedStatus
- Msvm_ReplicationService.OperatingStatus
- Msvm_ReplicationService.PrimaryStatus
- Msvm_ReplicationService.EnabledState
- Msvm_ReplicationService.OtherEnabledState
- Msvm_ReplicationService.RequestedState
- Msvm_ReplicationService.EnabledDefault
- Msvm_ReplicationService.TimeOfLastStateChange
- Msvm_ReplicationService.AvailableRequestedStates
- Msvm_ReplicationService.TransitioningToState
- Msvm_ReplicationService.SystemCreationClassName
- Msvm_ReplicationService.SystemName
- Msvm_ReplicationService.CreationClassName
- Msvm_ReplicationService.PrimaryOwnerName
- Msvm_ReplicationService.PrimaryOwnerContact
- Msvm_ReplicationService.StartMode
- Msvm_ReplicationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86e9140e2fe9b047c57c762be2e0fba048511993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170065"
---
# <a name="msvm_replicationservice-class"></a><span data-ttu-id="2aeed-103">\_Classe Msvm ReplicationService</span><span class="sxs-lookup"><span data-stu-id="2aeed-103">Msvm\_ReplicationService class</span></span>

<span data-ttu-id="2aeed-104">Gerencia a replicação de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-104">Manages the replication for a virtual machine.</span></span>

<span data-ttu-id="2aeed-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2aeed-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aeed-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2aeed-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Replica Service";
  string   Description = "Replication Service";
  string   ElementName;
  datetime InstallDate;
  string   Name = "replicasvc";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ReplicationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="2aeed-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2aeed-107">Members</span></span>

<span data-ttu-id="2aeed-108">A classe **Msvm \_ ReplicationService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2aeed-108">The **Msvm\_ReplicationService** class has these types of members:</span></span>

-   [<span data-ttu-id="2aeed-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2aeed-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2aeed-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2aeed-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2aeed-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2aeed-111">Methods</span></span>

<span data-ttu-id="2aeed-112">A classe **Msvm \_ ReplicationService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2aeed-112">The **Msvm\_ReplicationService** class has these methods.</span></span>



| <span data-ttu-id="2aeed-113">Método</span><span class="sxs-lookup"><span data-stu-id="2aeed-113">Method</span></span>                                                                                                 | <span data-ttu-id="2aeed-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2aeed-114">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aeed-115">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="2aeed-115">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="2aeed-116">Adiciona uma entrada de autorização a um servidor.</span><span class="sxs-lookup"><span data-stu-id="2aeed-116">Adds an authorization entry to a server.</span></span><br/>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2aeed-117">**ChangeReplicationModeToPrimary**</span><span class="sxs-lookup"><span data-stu-id="2aeed-117">**ChangeReplicationModeToPrimary**</span></span>](changereplicationmodetoprimary-msvm-replicationservice.md)       | <span data-ttu-id="2aeed-118">Altera a relação de replicação estendida para a relação primária de uma máquina virtual de réplica.</span><span class="sxs-lookup"><span data-stu-id="2aeed-118">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="2aeed-119">A máquina virtual de réplica deve estar em um estado de failover confirmado.</span><span class="sxs-lookup"><span data-stu-id="2aeed-119">The replica virtual machine must be in a failover committed state.</span></span><br/> <span data-ttu-id="2aeed-120">**Windows 8.1:** Não há suporte para este método até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2aeed-120">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="2aeed-121">**CommitFailover**</span><span class="sxs-lookup"><span data-stu-id="2aeed-121">**CommitFailover**</span></span>](commitfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="2aeed-122">Confirma o instantâneo de recuperação que o método [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) usou para um failover.</span><span class="sxs-lookup"><span data-stu-id="2aeed-122">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="2aeed-123">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="2aeed-123">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="2aeed-124">Cria um novo relacionamento de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-124">Creates a new replication relationship for a virtual machine.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="2aeed-125">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="2aeed-125">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)                   | <span data-ttu-id="2aeed-126">Recupera estatísticas de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-126">Retrieves replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="2aeed-127">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="2aeed-127">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)               | <span data-ttu-id="2aeed-128">Recupera as estatísticas de replicação associadas ao relacionamento de replicação especificado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-128">Retrieves the replication statistics that are associated with specified replication relationship of the virtual machine.</span></span><br/> <span data-ttu-id="2aeed-129">**Windows 8.1:** Não há suporte para este método até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2aeed-129">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                    |
| [<span data-ttu-id="2aeed-130">**GetSystemCertificates**</span><span class="sxs-lookup"><span data-stu-id="2aeed-130">**GetSystemCertificates**</span></span>](getsystemcertificates-msvm-replicationservice.md)                         | <span data-ttu-id="2aeed-131">Recupera os certificados do sistema em um sistema host.</span><span class="sxs-lookup"><span data-stu-id="2aeed-131">Retrieves the system certificates on a host system.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="2aeed-132">**ImportInitialReplica**</span><span class="sxs-lookup"><span data-stu-id="2aeed-132">**ImportInitialReplica**</span></span>](importinitialreplica-msvm-replicationservice.md)                           | <span data-ttu-id="2aeed-133">Importa a replicação inicial para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-133">Imports the initial replication for a virtual machine.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="2aeed-134">**InitiateFailback**</span><span class="sxs-lookup"><span data-stu-id="2aeed-134">**InitiateFailback**</span></span>](initiatefailback-msvm-replicationservice.md)                                   | <span data-ttu-id="2aeed-135">Inicia o failback para uma máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2aeed-135">Initiates the failback for a recovery virtual machine.</span></span> <span data-ttu-id="2aeed-136">Ou seja, define o failover para a máquina virtual para um aplicativo ou uma imagem consistente de falha.</span><span class="sxs-lookup"><span data-stu-id="2aeed-136">That is, sets the failover for the virtual machine to an app or crash consistent image.</span></span><br/> <span data-ttu-id="2aeed-137">**Windows 8.1:** Não há suporte para este método até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2aeed-137">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                              |
| [<span data-ttu-id="2aeed-138">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="2aeed-138">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)                                   | <span data-ttu-id="2aeed-139">Inicia um failover para uma máquina virtual para um aplicativo ou uma imagem de ponto de replicação padrão.</span><span class="sxs-lookup"><span data-stu-id="2aeed-139">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="2aeed-140">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="2aeed-140">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="2aeed-141">Modifica uma entrada de autorização em um servidor.</span><span class="sxs-lookup"><span data-stu-id="2aeed-141">Modifies an authorization entry on a server.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="2aeed-142">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="2aeed-142">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)                 | <span data-ttu-id="2aeed-143">Modifica as configurações de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-143">Modifies the replication settings for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="2aeed-144">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="2aeed-144">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)                         | <span data-ttu-id="2aeed-145">Modifica as configurações para o serviço de réplica do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="2aeed-145">Modifies the settings for the Hyper-V Replica service.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="2aeed-146">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="2aeed-146">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="2aeed-147">Remove a entrada de autorização de um servidor.</span><span class="sxs-lookup"><span data-stu-id="2aeed-147">Removes the authorization entry from a server.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="2aeed-148">**RemoveReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="2aeed-148">**RemoveReplicationRelationship**</span></span>](removereplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="2aeed-149">Remove um relacionamento de replicação de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-149">Removes a virtual machine replication relationship.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="2aeed-150">**RemoveReplicationRelationshipEx**</span><span class="sxs-lookup"><span data-stu-id="2aeed-150">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)     | <span data-ttu-id="2aeed-151">Remove a relação de replicação da máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="2aeed-151">Removes the specified virtual machine replication relationship.</span></span> <span data-ttu-id="2aeed-152">Para uma máquina virtual de réplica, a replicação primária não poderá ser removida se a replicação estendida estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="2aeed-152">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span><br/> <span data-ttu-id="2aeed-153">**Windows 8.1:** Não há suporte para este método até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2aeed-153">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>     |
| [<span data-ttu-id="2aeed-154">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2aeed-154">**RequestStateChange**</span></span>](msvm-replicationservice-requeststatechange.md)                               | <span data-ttu-id="2aeed-155">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="2aeed-155">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2aeed-156">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="2aeed-156">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)               | <span data-ttu-id="2aeed-157">Redefine as estatísticas de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-157">Resets the replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="2aeed-158">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="2aeed-158">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)           | <span data-ttu-id="2aeed-159">Redefine as estatísticas de replicação que estão associadas à relação de replicação especificada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-159">Resets replication statistics that are associated with the specified replication relationship of a virtual machine.</span></span><br/> <span data-ttu-id="2aeed-160">**Windows 8.1:** Não há suporte para este método até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2aeed-160">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                         |
| [<span data-ttu-id="2aeed-161">**Sincronizar novamente**</span><span class="sxs-lookup"><span data-stu-id="2aeed-161">**Resynchronize**</span></span>](resynchronize-msvm-replicationservice.md)                                         | <span data-ttu-id="2aeed-162">Executa uma operação de ressincronização na máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="2aeed-162">Performs a resynchronization operation on the specified virtual machine.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="2aeed-163">**ReverseReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="2aeed-163">**ReverseReplicationRelationship**</span></span>](reversereplicationrelationship-msvm-replicationservice.md)       | <span data-ttu-id="2aeed-164">Replica uma máquina virtual com failover de volta para o servidor primário.</span><span class="sxs-lookup"><span data-stu-id="2aeed-164">Replicates a failed-over virtual machine back to the primary server.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="2aeed-165">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="2aeed-165">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="2aeed-166">Reverte o failover atual de uma máquina virtual descartando o disco de failover atual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-166">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="2aeed-167">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="2aeed-167">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="2aeed-168">Define a entrada de autorização de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-168">Sets the replication authorization entry for a virtual machine.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="2aeed-169">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="2aeed-169">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md) | <span data-ttu-id="2aeed-170">Define as configurações de IP do adaptador de rede a serem aplicadas a uma máquina virtual após um failover.</span><span class="sxs-lookup"><span data-stu-id="2aeed-170">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="2aeed-171">**StartReplication**</span><span class="sxs-lookup"><span data-stu-id="2aeed-171">**StartReplication**</span></span>](startreplication-msvm-replicationservice.md)                                   | <span data-ttu-id="2aeed-172">Inicia a replicação de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aeed-172">Starts the replication of a virtual machine.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="2aeed-173">**StartService**</span><span class="sxs-lookup"><span data-stu-id="2aeed-173">**StartService**</span></span>](msvm-replicationservice-startservice.md)                                           | <span data-ttu-id="2aeed-174">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="2aeed-174">Starts the service.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="2aeed-175">**StopService**</span><span class="sxs-lookup"><span data-stu-id="2aeed-175">**StopService**</span></span>](msvm-replicationservice-stopservice.md)                                             | <span data-ttu-id="2aeed-176">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="2aeed-176">Stops the service.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="2aeed-177">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="2aeed-177">**TestReplicaSystem**</span></span>](testreplicasystem-msvm-replicationservice.md)                                 | <span data-ttu-id="2aeed-178">Cria uma nova réplica de uma máquina virtual com o instantâneo especificado para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="2aeed-178">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="2aeed-179">**TestReplicationConnection**</span><span class="sxs-lookup"><span data-stu-id="2aeed-179">**TestReplicationConnection**</span></span>](testreplicationconnection-msvm-replicationservice.md)                 | <span data-ttu-id="2aeed-180">Verifica se a replicação pode ser habilitada do sistema de host atual para o sistema de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="2aeed-180">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span><br/>                                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="2aeed-181">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2aeed-181">Properties</span></span>

<span data-ttu-id="2aeed-182">A classe **Msvm \_ ReplicationService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2aeed-182">The **Msvm\_ReplicationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2aeed-183">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2aeed-183">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-184">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-186">Indica os valores possíveis para o parâmetro *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="2aeed-186">Indicates the possible values for the *RequestedState* parameter.</span></span> <span data-ttu-id="2aeed-187">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2aeed-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-188">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="2aeed-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-191">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="2aeed-191">A short description of the object.</span></span> <span data-ttu-id="2aeed-192">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de réplica do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="2aeed-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Replica Service".</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2aeed-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-194">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-196">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="2aeed-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2aeed-197">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2aeed-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2aeed-198">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2aeed-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2aeed-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2aeed-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="2aeed-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="2aeed-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="2aeed-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="2aeed-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2aeed-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2aeed-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2aeed-206">)</span><span class="sxs-lookup"><span data-stu-id="2aeed-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2aeed-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2aeed-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-210">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2aeed-210">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-211">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="2aeed-211">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2aeed-212">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ ReplicationService".</span><span class="sxs-lookup"><span data-stu-id="2aeed-212">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ReplicationService".</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-213">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2aeed-213">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-216">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="2aeed-216">A description of the object.</span></span> <span data-ttu-id="2aeed-217">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de replicação".</span><span class="sxs-lookup"><span data-stu-id="2aeed-217">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service".</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-218">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2aeed-218">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-219">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-221">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="2aeed-221">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2aeed-222">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2aeed-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2aeed-223">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2aeed-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2aeed-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="2aeed-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="2aeed-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="2aeed-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="2aeed-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="2aeed-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="2aeed-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2aeed-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2aeed-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2aeed-232">)</span><span class="sxs-lookup"><span data-stu-id="2aeed-232">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2aeed-233">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2aeed-233">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-236">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="2aeed-236">A display name for the object.</span></span> <span data-ttu-id="2aeed-237">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2aeed-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2aeed-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-239">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-241">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="2aeed-241">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="2aeed-242">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="2aeed-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="2aeed-243">Valor</span><span class="sxs-lookup"><span data-stu-id="2aeed-243">Value</span></span>                                                                        | <span data-ttu-id="2aeed-244">Significado</span><span class="sxs-lookup"><span data-stu-id="2aeed-244">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="2aeed-245"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2aeed-245"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2aeed-246">habilitado</span><span class="sxs-lookup"><span data-stu-id="2aeed-246">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2aeed-247">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2aeed-247">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-248">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-250">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="2aeed-250">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2aeed-251">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="2aeed-251">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="2aeed-252">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="2aeed-252">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="2aeed-253">Valor</span><span class="sxs-lookup"><span data-stu-id="2aeed-253">Value</span></span>                                                                        | <span data-ttu-id="2aeed-254">Significado</span><span class="sxs-lookup"><span data-stu-id="2aeed-254">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="2aeed-255"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2aeed-255"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2aeed-256">habilitado</span><span class="sxs-lookup"><span data-stu-id="2aeed-256">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2aeed-257">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2aeed-257">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-258">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-260">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="2aeed-260">The current health of the element.</span></span> <span data-ttu-id="2aeed-261">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="2aeed-261">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="2aeed-262">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="2aeed-262">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="2aeed-263">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="2aeed-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="2aeed-264">Valor</span><span class="sxs-lookup"><span data-stu-id="2aeed-264">Value</span></span>                                                                        | <span data-ttu-id="2aeed-265">Significado</span><span class="sxs-lookup"><span data-stu-id="2aeed-265">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="2aeed-266"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2aeed-266"><dt>5</dt></span></span> </dl> | <span data-ttu-id="2aeed-267">O status de integridade é normal.</span><span class="sxs-lookup"><span data-stu-id="2aeed-267">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2aeed-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2aeed-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-269">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2aeed-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-271">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="2aeed-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="2aeed-272">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2aeed-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2aeed-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-276">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="2aeed-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-277">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="2aeed-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2aeed-278">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2aeed-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-279">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2aeed-279">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-282">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2aeed-282">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-283">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="2aeed-283">The label by which the object is known.</span></span> <span data-ttu-id="2aeed-284">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "replicasvc".</span><span class="sxs-lookup"><span data-stu-id="2aeed-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "replicasvc".</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-285">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2aeed-285">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-286">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-288">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="2aeed-288">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2aeed-289">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2aeed-289">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2aeed-290">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2aeed-290">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2aeed-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2aeed-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="2aeed-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="2aeed-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="2aeed-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="2aeed-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="2aeed-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="2aeed-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="2aeed-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="2aeed-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="2aeed-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="2aeed-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="2aeed-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="2aeed-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="2aeed-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="2aeed-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="2aeed-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="2aeed-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2aeed-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2aeed-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2aeed-310">)</span><span class="sxs-lookup"><span data-stu-id="2aeed-310">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2aeed-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2aeed-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-312">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-314">Uma matriz que contém os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="2aeed-314">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="2aeed-315">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2aeed-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="2aeed-316">O valor no índice zero será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2aeed-316">The value at index zero will be one of the following values.</span></span>



| <span data-ttu-id="2aeed-317">Valor</span><span class="sxs-lookup"><span data-stu-id="2aeed-317">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="2aeed-318">Significado</span><span class="sxs-lookup"><span data-stu-id="2aeed-318">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="2aeed-319"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2aeed-319"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                  | <span data-ttu-id="2aeed-320">O serviço de replicação está funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="2aeed-320">The replication service is operating normally.</span></span><br/>                                                                     |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span><dl> <span data-ttu-id="2aeed-321"><dt>**Erro**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2aeed-321"><dt>**Error**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="2aeed-322">Um ou mais ouvintes de rede de replicação não estão em execução.</span><span class="sxs-lookup"><span data-stu-id="2aeed-322">One or more replication network listeners are not running.</span></span> <span data-ttu-id="2aeed-323">Verifique se as configurações do serviço de replicação são válidas.</span><span class="sxs-lookup"><span data-stu-id="2aeed-323">Verify that the replication service settings are valid.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2aeed-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2aeed-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-327">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="2aeed-327">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="2aeed-328">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="2aeed-328">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2aeed-329">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2aeed-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-330">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="2aeed-330">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-333">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2aeed-333">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-334">Todas as informações sobre como o proprietário principal do serviço podem ser atingidas (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="2aeed-334">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="2aeed-335">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="2aeed-335">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-336">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="2aeed-336">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-339">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="2aeed-339">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-340">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="2aeed-340">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="2aeed-341">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="2aeed-341">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="2aeed-342">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="2aeed-342">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2aeed-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-344">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-346">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="2aeed-346">Provides high level status information.</span></span> <span data-ttu-id="2aeed-347">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="2aeed-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="2aeed-348">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2aeed-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2aeed-349">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2aeed-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2aeed-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2aeed-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="2aeed-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="2aeed-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="2aeed-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2aeed-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2aeed-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2aeed-356">)</span><span class="sxs-lookup"><span data-stu-id="2aeed-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2aeed-357">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2aeed-357">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-358">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-360">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="2aeed-360">The last requested or desired state for the element.</span></span> <span data-ttu-id="2aeed-361">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="2aeed-361">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="2aeed-362">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais para um elemento.</span><span class="sxs-lookup"><span data-stu-id="2aeed-362">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="2aeed-363">Uma instância específica da classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não oferecer suporte à propriedade **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="2aeed-363">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="2aeed-364">Se isso ocorrer, o valor 12 ("não aplicável") será usado.</span><span class="sxs-lookup"><span data-stu-id="2aeed-364">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="2aeed-365">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="2aeed-365">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="2aeed-366">Valor</span><span class="sxs-lookup"><span data-stu-id="2aeed-366">Value</span></span>                                                                         | <span data-ttu-id="2aeed-367">Significado</span><span class="sxs-lookup"><span data-stu-id="2aeed-367">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="2aeed-368"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2aeed-368"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2aeed-369">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="2aeed-369">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2aeed-370">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="2aeed-370">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-371">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2aeed-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-373">Indica se o serviço está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="2aeed-373">Indicates whether the service is currently running.</span></span> <span data-ttu-id="2aeed-374">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="2aeed-374">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-375">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="2aeed-375">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-378">Qualificadores: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="2aeed-378">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-379">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="2aeed-379">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="2aeed-380">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="2aeed-380">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-381">**Status**</span><span class="sxs-lookup"><span data-stu-id="2aeed-381">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-384">Indica o status do elemento.</span><span class="sxs-lookup"><span data-stu-id="2aeed-384">Indicates the status of the element.</span></span> <span data-ttu-id="2aeed-385">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "OK".</span><span class="sxs-lookup"><span data-stu-id="2aeed-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-386">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2aeed-386">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-387">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-389">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="2aeed-389">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2aeed-390">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2aeed-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2aeed-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-392">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-394">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2aeed-394">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-395">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="2aeed-395">The scoping system's creation class name.</span></span> <span data-ttu-id="2aeed-396">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="2aeed-396">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-397">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2aeed-397">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-398">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2aeed-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-400">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2aeed-400">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-401">O nome NetBIOS do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="2aeed-401">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="2aeed-402">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="2aeed-402">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2aeed-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-404">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2aeed-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-406">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="2aeed-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2aeed-407">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2aeed-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2aeed-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2aeed-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2aeed-409">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2aeed-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2aeed-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2aeed-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2aeed-411">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="2aeed-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2aeed-412">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2aeed-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2aeed-413">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2aeed-413">Requirements</span></span>



| <span data-ttu-id="2aeed-414">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aeed-414">Requirement</span></span> | <span data-ttu-id="2aeed-415">Valor</span><span class="sxs-lookup"><span data-stu-id="2aeed-415">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aeed-416">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2aeed-416">Minimum supported client</span></span><br/> | <span data-ttu-id="2aeed-417">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2aeed-417">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2aeed-418">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2aeed-418">Minimum supported server</span></span><br/> | <span data-ttu-id="2aeed-419">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2aeed-419">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2aeed-420">Namespace</span><span class="sxs-lookup"><span data-stu-id="2aeed-420">Namespace</span></span><br/>                | <span data-ttu-id="2aeed-421">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2aeed-421">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2aeed-422">MOF</span><span class="sxs-lookup"><span data-stu-id="2aeed-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2aeed-423"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2aeed-423"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2aeed-424">DLL</span><span class="sxs-lookup"><span data-stu-id="2aeed-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aeed-425"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2aeed-425"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

