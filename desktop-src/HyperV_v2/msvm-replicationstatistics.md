---
description: Fornece estatísticas de replicação para uma máquina virtual.
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Classe Msvm_ReplicationStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792516"
---
# <a name="msvm_replicationstatistics-class"></a><span data-ttu-id="d14dd-103">\_Classe Msvm ReplicationStatistics</span><span class="sxs-lookup"><span data-stu-id="d14dd-103">Msvm\_ReplicationStatistics class</span></span>

<span data-ttu-id="d14dd-104">Fornece estatísticas de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d14dd-104">Provides replication statistics for a virtual machine.</span></span> <span data-ttu-id="d14dd-105">Essas estatísticas abrangem a duração especificada pelas propriedades **MonitoringStartTime** e **MonitoringInterval** da classe [**Msvm \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="d14dd-105">These statistics cover the duration specified by the **MonitoringStartTime** and **MonitoringInterval** properties of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class.</span></span>

<span data-ttu-id="d14dd-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d14dd-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d14dd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d14dd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a><span data-ttu-id="d14dd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d14dd-108">Members</span></span>

<span data-ttu-id="d14dd-109">A classe **Msvm \_ ReplicationStatistics** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d14dd-109">The **Msvm\_ReplicationStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="d14dd-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d14dd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d14dd-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d14dd-111">Properties</span></span>

<span data-ttu-id="d14dd-112">A classe **Msvm \_ ReplicationStatistics** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d14dd-112">The **Msvm\_ReplicationStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d14dd-113">**ApplicationConsistentSnapshotFailureCount**</span><span class="sxs-lookup"><span data-stu-id="d14dd-113">**ApplicationConsistentSnapshotFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14dd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-116">O número total de falhas de instantâneo do VSS.</span><span class="sxs-lookup"><span data-stu-id="d14dd-116">The total number of VSS snapshot failures.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d14dd-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d14dd-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-120">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d14dd-120">A short description of the object.</span></span> <span data-ttu-id="d14dd-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d14dd-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d14dd-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d14dd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-125">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d14dd-125">A description of the object.</span></span> <span data-ttu-id="d14dd-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d14dd-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d14dd-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d14dd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-130">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d14dd-130">A display name for the object.</span></span> <span data-ttu-id="d14dd-131">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d14dd-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-132">**Endstatistictime**</span><span class="sxs-lookup"><span data-stu-id="d14dd-132">**EndStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-133">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d14dd-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-135">A hora, em UTC, quando o serviço de réplica do Hyper-V parou de coletar dados de estatísticas de replicação.</span><span class="sxs-lookup"><span data-stu-id="d14dd-135">The time, in UTC, when the Hyper-V Replica service stopped gathering replication statistics data.</span></span> <span data-ttu-id="d14dd-136">Neste momento, um novo ciclo de estatísticas de replicação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="d14dd-136">At this time, a new replication statistics cycle starts.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d14dd-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d14dd-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-140">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d14dd-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-141">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d14dd-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d14dd-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d14dd-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-143">**LastTestFailoverTime**</span><span class="sxs-lookup"><span data-stu-id="d14dd-143">**LastTestFailoverTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-144">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d14dd-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-146">Indica a última vez em que um sistema de réplica de teste foi criado para uma máquina virtual habilitada para replicação no servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d14dd-146">Indicates the last time a test replica system was created for a replication enabled virtual machine on the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-147">**MaxReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="d14dd-147">**MaxReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-148">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14dd-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-150">A quantidade máxima de tempo necessário para concluir um único ciclo de replicação, em segundos.</span><span class="sxs-lookup"><span data-stu-id="d14dd-150">The maximum amount of time taken to complete a single replication cycle, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-151">**MaxReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="d14dd-151">**MaxReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-152">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d14dd-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-154">Máximo de dados de replicação transferidos para o sistema de host de recuperação, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d14dd-154">Maximum replication data transferred to the recovery host system, in bytes.</span></span> <span data-ttu-id="d14dd-155">Isso representa o tamanho máximo dos dados de replicação enviados por um único ciclo para esse intervalo.</span><span class="sxs-lookup"><span data-stu-id="d14dd-155">This represents the maximum size of replication data sent over a single cycle for this interval.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-156">**NetworkFailureCount**</span><span class="sxs-lookup"><span data-stu-id="d14dd-156">**NetworkFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14dd-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-159">O número total de erros de rede encontrados para o canal de replicação com o sistema host de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d14dd-159">The total number of network errors encountered for the replication channel with recovery host system.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-160">**PendingReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="d14dd-160">**PendingReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-161">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d14dd-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-163">O tamanho dos dados para uma replicação pendente, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d14dd-163">The size of the data for a pending replication, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-164">**ReplicationFailureCount**</span><span class="sxs-lookup"><span data-stu-id="d14dd-164">**ReplicationFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14dd-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-167">O número total de falhas de replicação.</span><span class="sxs-lookup"><span data-stu-id="d14dd-167">The total number of replication failures.</span></span> <span data-ttu-id="d14dd-168">Isso inclui erros de operação de replicação.</span><span class="sxs-lookup"><span data-stu-id="d14dd-168">This includes errors for replication operation.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-169">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="d14dd-169">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14dd-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-172">A integridade da replicação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d14dd-172">The replication health for the virtual machine.</span></span> <span data-ttu-id="d14dd-173">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d14dd-173">This will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d14dd-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (0)</span><span class="sxs-lookup"><span data-stu-id="d14dd-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not applicable** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d14dd-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (2)</span><span class="sxs-lookup"><span data-stu-id="d14dd-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="d14dd-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critical** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d14dd-178">**ReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="d14dd-178">**ReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-179">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14dd-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-181">Latência de replicação total ao transferir os dados para o sistema de host de recuperação, em segundos.</span><span class="sxs-lookup"><span data-stu-id="d14dd-181">Total replication latency while transferring the data to the recovery host system, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-182">**ReplicationMissCount**</span><span class="sxs-lookup"><span data-stu-id="d14dd-182">**ReplicationMissCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-183">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14dd-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-185">O número de ciclos de replicação perdidos.</span><span class="sxs-lookup"><span data-stu-id="d14dd-185">The number of missed replication cycles.</span></span> <span data-ttu-id="d14dd-186">Isso pode ser devido a cargas de trabalho pesadas, problemas de rede ou erros de replicação.</span><span class="sxs-lookup"><span data-stu-id="d14dd-186">This can be because of heavy workload, network issues, or replication errors.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-187">**ReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="d14dd-187">**ReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-188">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d14dd-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-190">A quantidade total de dados de replicação transferidos para o sistema de host de recuperação, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d14dd-190">The total amount of replication data transferred to the recovery host system, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-191">**ReplicationSuccessCount**</span><span class="sxs-lookup"><span data-stu-id="d14dd-191">**ReplicationSuccessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-192">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14dd-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-194">O número total de replicações bem-sucedidas para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d14dd-194">The total number of successful replications for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d14dd-195">**StartStatisticTime**</span><span class="sxs-lookup"><span data-stu-id="d14dd-195">**StartStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14dd-196">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d14dd-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d14dd-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d14dd-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14dd-198">A hora, em UTC, quando o serviço de réplica do Hyper-V começou a coletar dados de estatísticas de replicação.</span><span class="sxs-lookup"><span data-stu-id="d14dd-198">The time, in UTC, when the Hyper-V Replica service started gathering replication statistics data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d14dd-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d14dd-199">Requirements</span></span>



| <span data-ttu-id="d14dd-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="d14dd-200">Requirement</span></span> | <span data-ttu-id="d14dd-201">Valor</span><span class="sxs-lookup"><span data-stu-id="d14dd-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d14dd-202">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d14dd-202">Minimum supported client</span></span><br/> | <span data-ttu-id="d14dd-203">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d14dd-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d14dd-204">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d14dd-204">Minimum supported server</span></span><br/> | <span data-ttu-id="d14dd-205">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d14dd-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d14dd-206">Namespace</span><span class="sxs-lookup"><span data-stu-id="d14dd-206">Namespace</span></span><br/>                | <span data-ttu-id="d14dd-207">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d14dd-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d14dd-208">MOF</span><span class="sxs-lookup"><span data-stu-id="d14dd-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d14dd-209"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d14dd-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d14dd-210">DLL</span><span class="sxs-lookup"><span data-stu-id="d14dd-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d14dd-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d14dd-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

