---
description: Essa classe representa um trabalho de operação de migração criado para armazenamento ou migração de sistema virtual pelo serviço de migração de sistema virtual.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770215"
---
# <a name="msvm_migrationjob-class"></a><span data-ttu-id="3a8b5-103">\_Classe Msvm MigrationJob</span><span class="sxs-lookup"><span data-stu-id="3a8b5-103">Msvm\_MigrationJob class</span></span>

<span data-ttu-id="3a8b5-104">Essa classe representa um trabalho de operação de migração criado para armazenamento ou migração de sistema virtual pelo serviço de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-104">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span>

<span data-ttu-id="3a8b5-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a8b5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a8b5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="3a8b5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3a8b5-107">Members</span></span>

<span data-ttu-id="3a8b5-108">A classe **Msvm \_ MigrationJob** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3a8b5-108">The **Msvm\_MigrationJob** class has these types of members:</span></span>

-   [<span data-ttu-id="3a8b5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a8b5-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a8b5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a8b5-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a8b5-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a8b5-111">Methods</span></span>

<span data-ttu-id="3a8b5-112">A classe **Msvm \_ MigrationJob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-112">The **Msvm\_MigrationJob** class has these methods.</span></span>



| <span data-ttu-id="3a8b5-113">Método</span><span class="sxs-lookup"><span data-stu-id="3a8b5-113">Method</span></span>                                                             | <span data-ttu-id="3a8b5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a8b5-114">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a8b5-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-115">**GetError**</span></span>](geterror-msvm-migrationjob.md)                     | <span data-ttu-id="3a8b5-116">Recupera o objeto de erro para o trabalho de migração, se houver um.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-116">Retrieves the error object for the migration job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="3a8b5-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-117">**GetErrorEx**</span></span>](geterrorex-msvm-migrationjob.md)                 | <span data-ttu-id="3a8b5-118">Recupera os objetos de erro para o trabalho de migração, se existir algum.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-118">Retrieves the error objects for the migration job, if any exist.</span></span><br/>                |
| <span data-ttu-id="3a8b5-119">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-119">**KillJob**</span></span>                                                        | <span data-ttu-id="3a8b5-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-120">This method is not supported.</span></span><br/>                                                   |
| [<span data-ttu-id="3a8b5-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-121">**RequestStateChange**</span></span>](requeststatechange-msvm-migrationjob.md) | <span data-ttu-id="3a8b5-122">Solicita que o estado do trabalho de migração seja alterado para o estado especificado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-122">Requests that the state of the migration job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3a8b5-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a8b5-123">Properties</span></span>

<span data-ttu-id="3a8b5-124">A classe **Msvm \_ MigrationJob** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-124">The **Msvm\_MigrationJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a8b5-125">**Cancelável**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-125">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-126">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-128">Indica se o trabalho pode ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-128">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="3a8b5-129">O valor dessa propriedade não garante que uma solicitação para cancelar o trabalho seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-129">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-130">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-133">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-133">A short description of the object.</span></span> <span data-ttu-id="3a8b5-134">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-135">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-135">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-136">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-138">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-138">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3a8b5-139">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-139">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3a8b5-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-141">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-141">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-144">Especifica se o trabalho deve ser excluído automaticamente após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-144">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="3a8b5-145">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-145">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-149">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="3a8b5-149">A description of the object.</span></span> <span data-ttu-id="3a8b5-150">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-151">**DestinationHost**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-151">**DestinationHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-154">O nome do host da plataforma de virtualização de destino para a qual o sistema virtual está migrando.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-154">The hostname of the destination virtualization platform that the virtual system is migrating to.</span></span> <span data-ttu-id="3a8b5-155">Isso será **nulo** para migração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-155">This will be **Null** for storage migration.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-157">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-159">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3a8b5-160">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3a8b5-161">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-162">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-163">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-165">O intervalo de tempo em que o trabalho foi executado ou o tempo de execução total se o trabalho for concluído.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-165">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="3a8b5-166">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-170">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-170">A display name for the object.</span></span> <span data-ttu-id="3a8b5-171">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-173">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-175">Um código de erro específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-175">A vendor-specific error code.</span></span> <span data-ttu-id="3a8b5-176">O valor deve ser definido como zero se o trabalho for concluído sem erros.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="3a8b5-177">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-181">Uma cadeia de caracteres que contém a descrição do erro do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="3a8b5-182">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-186">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabalho CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="3a8b5-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-187">Uma descrição resumida do erro, se presente.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-187">A summary description of the error, if present.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-188">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-188">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-189">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-191">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-191">The current health of the element.</span></span> <span data-ttu-id="3a8b5-192">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-192">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="3a8b5-193">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-193">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="3a8b5-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-196">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-198">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-198">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="3a8b5-199">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-200">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-200">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-203">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-203">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-204">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3a8b5-205">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-206">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-206">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-207">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-209">O número de vezes que o trabalho deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-209">The number of times that the job should be run.</span></span> <span data-ttu-id="3a8b5-210">Um valor de 1 indica que o trabalho não é recorrente, enquanto qualquer valor diferente de zero indica um limite para o número de vezes que o trabalho será recorrente.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-210">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="3a8b5-211">Zero indica que não há nenhum limite para o número de vezes que o trabalho pode ser processado, mas será encerrado após o tempo de espera ter sido atingido **ou o trabalho** será encerrado manualmente.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-211">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="3a8b5-212">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-212">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-213">**JobState**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-213">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-214">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-216">**JobState** é uma enumeração de inteiro que indica o estado operacional de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-216">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="3a8b5-217">Ele também pode indicar transições entre esses Estados, por exemplo, "desligando" e "Iniciando".</span><span class="sxs-lookup"><span data-stu-id="3a8b5-217">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="3a8b5-218">Essa propriedade é herdada do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-218">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="3a8b5-219">Valor</span><span class="sxs-lookup"><span data-stu-id="3a8b5-219">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="3a8b5-220">Significado</span><span class="sxs-lookup"><span data-stu-id="3a8b5-220">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="3a8b5-221"><dt>**Novo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-221"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="3a8b5-222">O trabalho nunca foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-222">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="3a8b5-223"><dt>**Iniciando**</dt> em <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-223"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="3a8b5-224">O trabalho está sendo movido dos Estados 2 (novo), 5 (suspensos) ou 11 (serviço) para o estado 4 (em execução).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-224">The job is moving from the 2 (New), 5(Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="3a8b5-225"><dt>**Executando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-225"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="3a8b5-226">O trabalho está em execução.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-226">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="3a8b5-227"><dt>**Suspenso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-227"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="3a8b5-228">O trabalho é interrompido, mas pode ser reiniciado de maneira direta.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-228">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="3a8b5-229"><dt>**Desligando**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-229"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="3a8b5-230">O trabalho está mudando para um estado de 7 (concluído), 8 (encerrado) ou 9 (eliminado).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-230">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="3a8b5-231"><dt>**Concluído**</dt> em <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-231"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="3a8b5-232">O trabalho foi concluído normalmente.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-232">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="3a8b5-233"><dt>**Terminada**</dt> em <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-233"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="3a8b5-234">O trabalho foi interrompido por uma solicitação de alteração de estado "Terminate".</span><span class="sxs-lookup"><span data-stu-id="3a8b5-234">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="3a8b5-235">O trabalho e todos os seus processos subjacentes são encerrados e podem ser reiniciados apenas como um novo trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-235">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="3a8b5-236">O requisito de que o trabalho seja reiniciado somente como um novo trabalho é específico do trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-236">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="3a8b5-237"><dt>**Encerrado**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-237"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="3a8b5-238">O trabalho foi interrompido por uma solicitação de alteração de estado "Kill".</span><span class="sxs-lookup"><span data-stu-id="3a8b5-238">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="3a8b5-239">Os processos subjacentes ainda podem estar em execução, e uma limpeza pode ser necessária para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-239">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="3a8b5-240"><dt>**Exceção**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-240"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="3a8b5-241">O trabalho está em um estado anormal que pode indicar uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-241">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="3a8b5-242">O status real do trabalho pode estar disponível por meio de objetos específicos do trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-242">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="3a8b5-243"><dt>**Serviço**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-243"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="3a8b5-244">O trabalho está em um estado específico do fornecedor que dá suporte à descoberta de problemas ou à resolução, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-244">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="3a8b5-245"><dt>**DMTF reservado**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-245"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="3a8b5-246">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-246">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="3a8b5-247"><dt>**Fornecedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-247"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="3a8b5-248">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-248">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="3a8b5-249">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-250">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-252">Uma cadeia de caracteres que representa o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-252">A string that represents the job status.</span></span> <span data-ttu-id="3a8b5-253">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-253">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-254">**JobType**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-254">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-255">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-257">Indica o tipo de trabalho que está sendo acompanhado por este objeto.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-257">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a8b5-258">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-258">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="3a8b5-259">**Criando máquina virtual remota** (300)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-259">**Creating Remote Virtual Machine** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

<span data-ttu-id="3a8b5-260">**Verificando a compatibilidade da máquina virtual** (301)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-260">**Checking Virtual Machine Compatibility** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="3a8b5-261">**Verificando a compatibilidade de máquina virtual e armazenamento** (302)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-261">**Checking Virtual Machine and Storage Compatibility** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="3a8b5-262">**Verificando a compatibilidade de armazenamento** (303)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-262">**Checking Storage Compatibility** (303)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

<span data-ttu-id="3a8b5-263">**Verificando a migração de armazenamento** (304)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-263">**Checking Storage Migration** (304)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="3a8b5-264">**Movendo máquina virtual** (305)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-264">**Moving Virtual Machine** (305)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

<span data-ttu-id="3a8b5-265">**Movendo a máquina virtual e o armazenamento** (306)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-265">**Moving Virtual Machine and Storage** (306)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

<span data-ttu-id="3a8b5-266">**Movendo o armazenamento** (307)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-266">**Moving Storage** (307)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a8b5-267">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-267">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-268">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-270">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-270">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<span data-ttu-id="3a8b5-271">Indica se as horas representadas nas propriedades **RunStartInterval** e **UntilTime** representam horários locais ou horários UTC.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-271">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dl> <dt>

<span data-ttu-id="3a8b5-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Hora local** (1)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Hora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a8b5-274">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-274">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-275">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-277">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span><span class="sxs-lookup"><span data-stu-id="3a8b5-277">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-278">O tipo de migração representado por esse objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-278">The migration type represented by this job object.</span></span> <span data-ttu-id="3a8b5-279">Esse será um dos valores definidos para a propriedade **migratype** da classe [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="3a8b5-279">This will be one of the values defined for the **MigrationType** property of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-280">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-281">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-283">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-283">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-284">O nome de exibição para esta instância de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-284">The display name for this instance of a job.</span></span> <span data-ttu-id="3a8b5-285">Além disso, o nome de exibição pode ser usado como uma propriedade para uma pesquisa ou consulta.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-285">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="3a8b5-286">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-287">**NewResourceSettingData**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-287">**NewResourceSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-288">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-290">Para uma migração dinâmica, isso sempre será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-290">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="3a8b5-291">Para uma migração de armazenamento, se isso for **NULL**, nenhum dos VHDs (discos rígidos virtuais) da máquina virtual será movido.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-291">For a storage migration, if this is **Null**, none of the virtual machine's virtual hard disks (VHDs) will be moved.</span></span> <span data-ttu-id="3a8b5-292">Caso contrário, isso conterá uma matriz de instâncias inseridas da classe [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) que representam os VHDs a serem movidos.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-292">Otherwise, this will contain an array of embedded instances of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class that represent the VHDs to be moved.</span></span> <span data-ttu-id="3a8b5-293">A propriedade **Connection** dessas instâncias especificará o local de destino do VHD.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-293">The **Connection** property of these instances will specify the destination location of the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-294">**NewSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-294">**NewSystemSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-297">Para uma migração dinâmica, isso sempre será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-297">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="3a8b5-298">Para uma migração de armazenamento, se isso for **NULL**, as raízes de dados da máquina virtual não serão movidas.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-298">For a storage migration, if this is **Null**, the virtual machine's data roots are not moving.</span></span> <span data-ttu-id="3a8b5-299">Caso contrário, isso conterá uma instância incorporada da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) , em que as propriedades **ExternalDataRoot**, **SnapshotDataRoot** e **SwapFileDataRoot** especificarão as novas raízes de dados.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-299">Otherwise, this will contain an embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class, where the **ExternalDataRoot**, **SnapshotDataRoot**, and **SwapFileDataRoot** properties will specify the new data roots.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-300">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-300">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-303">O usuário que é notificado após a conclusão ou falha do trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-303">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="3a8b5-304">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-304">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-305">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-305">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-306">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-308">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="3a8b5-308">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3a8b5-309">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3a8b5-310">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-312">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-314">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-314">The current statuses of the object.</span></span> <span data-ttu-id="3a8b5-315">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-316">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-316">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-319">Uma cadeia de caracteres que descreve a ação de recuperação quando a propriedade **recoveryaction** da instância é 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-319">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="3a8b5-320">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-320">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-321">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-321">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-324">O usuário que enviou o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-324">The user who submitted the job.</span></span> <span data-ttu-id="3a8b5-325">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-325">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-326">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-326">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-327">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-329">Qualificadores: **MinValue** (0), **MaxValue** (100), **unidades** ("percent")</span><span class="sxs-lookup"><span data-stu-id="3a8b5-329">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-330">A porcentagem de conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-330">The completion percentage of the job.</span></span> <span data-ttu-id="3a8b5-331">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-331">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-332">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-332">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-333">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-333">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-335">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-335">Provides high level status information.</span></span> <span data-ttu-id="3a8b5-336">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-336">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3a8b5-337">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-337">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3a8b5-338">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-339">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-339">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-340">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-342">A importância da execução de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-342">The importance of a job's execution.</span></span> <span data-ttu-id="3a8b5-343">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-343">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-344">**Recuperação de**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-344">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-345">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-347">Descreve a ação de recuperação a ser executada para um trabalho de execução sem êxito.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-347">Describes the recovery action to be taken for an unsuccessfully run job.</span></span> <span data-ttu-id="3a8b5-348">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-348">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="3a8b5-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>Não **continuar** (2)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar com o próximo trabalho** (3)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Executar trabalho novamente** (4)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Executar trabalho de recuperação** (5)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a8b5-355">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-355">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-356">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-356">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-358">Qualificadores: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-358">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-359">O dia do mês em que o trabalho deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-359">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="3a8b5-360">Há diferentes interpretações para essa propriedade, dependendo do valor de **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-360">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="3a8b5-361">Quando **RunDayOfWeek** é 0 e **RunDay** é positivo, **RunDay** define o dia do mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-361">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="3a8b5-362">Por exemplo, se **RunDayOfWeek** for 0 e **RunDay** for 12, o trabalho será processado nos <sup>12 dias do</sup> mês.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-362">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="3a8b5-363">Quando **RunDayOfWeek** é 0 e **RunDay** é negativo, **RunDay** define o número de dias antes do último dia do mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-363">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="3a8b5-364">1 indica o último dia do mês, 2 indica um dia antes do último dia do mês e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-364">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="3a8b5-365">Por exemplo, se **RunDayOfWeek** for 0 e **RunDay** for 1, o trabalho será processado no último dia do mês.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-365">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="3a8b5-366">Quando **RunDayOfWeek** não for 0, **RunDayOfWeek** será o dia da semana em que o trabalho será processado, em relação a **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-366">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="3a8b5-367">Por exemplo, se **RunDay** for 15 e **RunDayOfWeek** for 7 (+ sábado), o trabalho será processado no primeiro sábado, em ou <sup>após 15 dias</sup> do mês.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-367">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="3a8b5-368">Se **RunDay** for 20 e **RunDayOfWeek** for 7 (sábado), o trabalho será processado no primeiro sábado, em ou antes <sup>dos 20 dias</sup> do mês.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-368">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="3a8b5-369">Se **RunDay** for 1 e **RunDayOfWeek** for 1 (domingo), o trabalho será processado no último domingo do mês.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-369">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="3a8b5-370">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-370">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-371">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-371">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-372">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-372">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-374">Um inteiro positivo ou negativo usado em conjunto com **RunDay** para indicar o dia da semana ou mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-374">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="3a8b5-375">Consulte a descrição da propriedade **RunDay** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-375">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="3a8b5-376">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-376">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="3a8b5-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Sexta** (6)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Quinta** (5)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Quarta** (4)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Terça-feira** (3)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Segunda** (2)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Segunda** (2)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Terça-feira** (3)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Quarta-feira** (4)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Quinta-feira** (5)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Sexta-feira** (6)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a8b5-392">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-392">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-393">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-393">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-395">O mês durante o qual o trabalho deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-395">The month during which the job should be processed.</span></span> <span data-ttu-id="3a8b5-396">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-396">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="3a8b5-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Janeiro** (0)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Fevereiro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Março** (2)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Abril** (3)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Maio** (4)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Junho** (5)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Julho** (6)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Setembro** (8)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Outubro** (9)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembro** (10)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dezembro** (11)</span><span class="sxs-lookup"><span data-stu-id="3a8b5-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a8b5-409">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-409">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-410">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-412">O intervalo de tempo após a meia-noite quando o trabalho deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-412">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="3a8b5-413">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-414">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-414">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-415">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-417">A hora de início agendada para o trabalho, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-417">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="3a8b5-418">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-419">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-419">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-420">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-420">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-422">A hora em que o trabalho começou.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-422">The time that the job began.</span></span> <span data-ttu-id="3a8b5-423">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-423">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-424">**Status**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-424">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-425">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-427">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-428">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-428">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-429">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-429">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-431">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="3a8b5-431">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3a8b5-432">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="3a8b5-432">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-433">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-433">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-434">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-436">A quantidade de tempo, em minutos, que o trabalho é retido após a conclusão da execução, com êxito ou falha na execução.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-436">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="3a8b5-437">O trabalho deve permanecer em existência por algum período de tempo, independentemente do valor da propriedade **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="3a8b5-437">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="3a8b5-438">O padrão é de cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-438">The default is five minutes.</span></span> <span data-ttu-id="3a8b5-439">Essa propriedade é herdada do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))e é sempre definida como 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-439">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-440">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-440">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-441">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-443">A data ou a hora em que o estado do trabalho foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-443">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="3a8b5-444">Se o estado do trabalho não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-444">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="3a8b5-445">Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-445">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="3a8b5-446">Essa propriedade é herdada do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-446">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-447">**Timeenvio**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-447">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-448">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-448">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-450">A hora em que o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-450">The time that the job was submitted.</span></span> <span data-ttu-id="3a8b5-451">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-451">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-452">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-452">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-453">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-454">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-455">A hora em que o trabalho não é válido ou deve ser parado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-455">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="3a8b5-456">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="3a8b5-456">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3a8b5-457">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-457">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a8b5-458">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a8b5-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a8b5-459">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a8b5-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a8b5-460">O nome exclusivo do sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="3a8b5-460">The unique name of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a8b5-461">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a8b5-461">Requirements</span></span>



| <span data-ttu-id="3a8b5-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a8b5-462">Requirement</span></span> | <span data-ttu-id="3a8b5-463">Valor</span><span class="sxs-lookup"><span data-stu-id="3a8b5-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8b5-464">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a8b5-464">Minimum supported client</span></span><br/> | <span data-ttu-id="3a8b5-465">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3a8b5-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a8b5-466">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a8b5-466">Minimum supported server</span></span><br/> | <span data-ttu-id="3a8b5-467">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3a8b5-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a8b5-468">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a8b5-468">Namespace</span></span><br/>                | <span data-ttu-id="3a8b5-469">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3a8b5-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a8b5-470">MOF</span><span class="sxs-lookup"><span data-stu-id="3a8b5-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a8b5-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a8b5-472">DLL</span><span class="sxs-lookup"><span data-stu-id="3a8b5-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a8b5-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a8b5-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

