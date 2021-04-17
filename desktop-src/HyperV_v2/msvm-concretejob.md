---
description: Representa uma unidade de trabalho e é usado para acompanhar o progresso de operações assíncronas.
ms.assetid: 33c13880-92a4-4367-8f0b-ecdf38b2ff8e
title: Classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob
- Msvm_ConcreteJob.KillJob
- Msvm_ConcreteJob.InstanceID
- Msvm_ConcreteJob.Caption
- Msvm_ConcreteJob.Description
- Msvm_ConcreteJob.ElementName
- Msvm_ConcreteJob.InstallDate
- Msvm_ConcreteJob.Name
- Msvm_ConcreteJob.OperationalStatus
- Msvm_ConcreteJob.StatusDescriptions
- Msvm_ConcreteJob.Status
- Msvm_ConcreteJob.HealthState
- Msvm_ConcreteJob.CommunicationStatus
- Msvm_ConcreteJob.DetailedStatus
- Msvm_ConcreteJob.OperatingStatus
- Msvm_ConcreteJob.PrimaryStatus
- Msvm_ConcreteJob.JobStatus
- Msvm_ConcreteJob.TimeSubmitted
- Msvm_ConcreteJob.ScheduledStartTime
- Msvm_ConcreteJob.StartTime
- Msvm_ConcreteJob.ElapsedTime
- Msvm_ConcreteJob.JobRunTimes
- Msvm_ConcreteJob.RunMonth
- Msvm_ConcreteJob.RunDay
- Msvm_ConcreteJob.RunDayOfWeek
- Msvm_ConcreteJob.RunStartInterval
- Msvm_ConcreteJob.LocalOrUtcTime
- Msvm_ConcreteJob.UntilTime
- Msvm_ConcreteJob.Notify
- Msvm_ConcreteJob.Owner
- Msvm_ConcreteJob.Priority
- Msvm_ConcreteJob.PercentComplete
- Msvm_ConcreteJob.DeleteOnCompletion
- Msvm_ConcreteJob.ErrorCode
- Msvm_ConcreteJob.ErrorDescription
- Msvm_ConcreteJob.ErrorSummaryDescription
- Msvm_ConcreteJob.RecoveryAction
- Msvm_ConcreteJob.OtherRecoveryAction
- Msvm_ConcreteJob.JobState
- Msvm_ConcreteJob.TimeOfLastStateChange
- Msvm_ConcreteJob.TimeBeforeRemoval
- Msvm_ConcreteJob.Cancellable
- Msvm_ConcreteJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2cff9594bfd39cf365020a1da8ae2f1ec0aea562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770406"
---
# <a name="msvm_concretejob-class"></a><span data-ttu-id="cf0b8-103">\_Classe Msvm ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="cf0b8-103">Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="cf0b8-104">Uma versão concreta do trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-104">A concrete version of job.</span></span> <span data-ttu-id="cf0b8-105">Essa classe representa uma unidade de trabalho genérica e instanciável, como um trabalho de lote ou de impressão, e é usada especificamente no Hyper-V para acompanhar o progresso de operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-105">This class represents a generic and instantiatable unit of work, such as a batch or a print job, and is specifically used in Hyper-V to track the progress of asynchronous operations.</span></span>

<span data-ttu-id="cf0b8-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf0b8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf0b8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteJob : CIM_ConcreteJob
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
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 
                00000000000500.000000:000
              ;
  boolean  Cancellable;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="cf0b8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cf0b8-108">Members</span></span>

<span data-ttu-id="cf0b8-109">A classe **Msvm \_ ConcreteJob** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cf0b8-109">The **Msvm\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="cf0b8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf0b8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="cf0b8-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cf0b8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cf0b8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf0b8-112">Methods</span></span>

<span data-ttu-id="cf0b8-113">A classe **Msvm \_ ConcreteJob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-113">The **Msvm\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="cf0b8-114">Método</span><span class="sxs-lookup"><span data-stu-id="cf0b8-114">Method</span></span>                                                            | <span data-ttu-id="cf0b8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf0b8-115">Description</span></span>                                                                      |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="cf0b8-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-116">**GetError**</span></span>](geterror-msvm-concretejob.md)                     | <span data-ttu-id="cf0b8-117">Recupera o objeto de erro para o trabalho, se houver um.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-117">Retrieves the error object for the job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="cf0b8-118">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-118">**GetErrorEx**</span></span>](geterrorex-msvm-concretejob.md)                 | <span data-ttu-id="cf0b8-119">Recupera os objetos de erro para o trabalho, caso existam.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-119">Retrieves the error objects for the job, if any exist.</span></span><br/>                |
| <span data-ttu-id="cf0b8-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-120">**KillJob**</span></span>                                                       | <span data-ttu-id="cf0b8-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-121">This method is not supported.</span></span><br/>                                         |
| [<span data-ttu-id="cf0b8-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-122">**RequestStateChange**</span></span>](requeststatechange-msvm-concretejob.md) | <span data-ttu-id="cf0b8-123">Solicita que o estado do trabalho seja alterado para o estado especificado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-123">Requests that the state of the job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cf0b8-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cf0b8-124">Properties</span></span>

<span data-ttu-id="cf0b8-125">A classe **Msvm \_ ConcreteJob** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-125">The **Msvm\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf0b8-126">**Cancelável**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-127">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-129">Indica se o trabalho pode ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="cf0b8-130">O valor dessa propriedade não garante que uma solicitação para cancelar o trabalho seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-131">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-134">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-134">A short description of the object.</span></span> <span data-ttu-id="cf0b8-135">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-137">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-139">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="cf0b8-140">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cf0b8-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-142">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-142">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-145">Especifica se o trabalho deve ser excluído automaticamente após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-145">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="cf0b8-146">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-146">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-147">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-150">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="cf0b8-150">A description of the object.</span></span> <span data-ttu-id="cf0b8-151">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-152">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-152">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-153">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-155">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-155">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="cf0b8-156">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cf0b8-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-158">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-158">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-159">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-161">O intervalo de tempo em que o trabalho foi executado ou o tempo de execução total se o trabalho for concluído.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-161">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="cf0b8-162">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-162">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-166">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-166">A display name for the object.</span></span> <span data-ttu-id="cf0b8-167">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-168">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-168">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-169">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-171">Um código de erro específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-171">A vendor-specific error code.</span></span> <span data-ttu-id="cf0b8-172">O valor deve ser definido como zero se o trabalho for concluído sem erros.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-172">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="cf0b8-173">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-173">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-174">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-174">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-177">Uma cadeia de caracteres que contém a descrição do erro do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-177">A string that contains the vendor error description.</span></span> <span data-ttu-id="cf0b8-178">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-178">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-179">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-179">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-182">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabalho CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="cf0b8-182">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-183">Uma descrição resumida do erro, se presente.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-183">A summary description of the error, if present.</span></span> <span data-ttu-id="cf0b8-184">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-184">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-185">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-185">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-186">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-188">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-188">The current health of the element.</span></span> <span data-ttu-id="cf0b8-189">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-189">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="cf0b8-190">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-190">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="cf0b8-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-192">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-192">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-193">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-195">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-195">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="cf0b8-196">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-200">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-201">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="cf0b8-202">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-203">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-203">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-204">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-206">O número de vezes que o trabalho deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-206">The number of times that the job should be run.</span></span> <span data-ttu-id="cf0b8-207">Um valor de 1 indica que o trabalho não é recorrente, enquanto qualquer valor diferente de zero indica um limite para o número de vezes que o trabalho será recorrente.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-207">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="cf0b8-208">Zero indica que não há nenhum limite para o número de vezes que o trabalho pode ser processado, mas será encerrado após o tempo de espera ter sido atingido **ou o trabalho** será encerrado manualmente.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-208">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="cf0b8-209">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-209">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-210">**JobState**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-210">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-211">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-213">**JobState** é uma enumeração de inteiro que indica o estado operacional de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-213">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="cf0b8-214">Ele também pode indicar transições entre esses Estados, por exemplo, "desligando" e "Iniciando".</span><span class="sxs-lookup"><span data-stu-id="cf0b8-214">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="cf0b8-215">Essa propriedade é herdada do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-215">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="cf0b8-216">Valor</span><span class="sxs-lookup"><span data-stu-id="cf0b8-216">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="cf0b8-217">Significado</span><span class="sxs-lookup"><span data-stu-id="cf0b8-217">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="cf0b8-218"><dt>**Novo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-218"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="cf0b8-219">O trabalho nunca foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-219">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="cf0b8-220"><dt>**Iniciando**</dt> em <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-220"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="cf0b8-221">O trabalho está sendo movido dos Estados 2 (novo), 5 (suspensos) ou 11 (serviço) para o estado 4 (em execução).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-221">The job is moving from the 2 (New), 5 (Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                   |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="cf0b8-222"><dt>**Executando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-222"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="cf0b8-223">O trabalho está em execução.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-223">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="cf0b8-224"><dt>**Suspenso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-224"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="cf0b8-225">O trabalho é interrompido, mas pode ser reiniciado de maneira direta.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-225">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="cf0b8-226"><dt>**Desligando**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-226"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="cf0b8-227">O trabalho está mudando para um estado de 7 (concluído), 8 (encerrado) ou 9 (eliminado).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-227">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="cf0b8-228"><dt>**Concluído**</dt> em <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-228"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="cf0b8-229">O trabalho foi concluído normalmente.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-229">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="cf0b8-230"><dt>**Terminada**</dt> em <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-230"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="cf0b8-231">O trabalho foi interrompido por uma solicitação de alteração de estado "Terminate".</span><span class="sxs-lookup"><span data-stu-id="cf0b8-231">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="cf0b8-232">O trabalho e todos os seus processos subjacentes são encerrados e podem ser reiniciados apenas como um novo trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-232">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="cf0b8-233">O requisito de que o trabalho seja reiniciado somente como um novo trabalho é específico ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-233">The requirement that the job be restarted only as a new job is job-specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="cf0b8-234"><dt>**Encerrado**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-234"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="cf0b8-235">O trabalho foi interrompido por uma solicitação de alteração de estado "Kill".</span><span class="sxs-lookup"><span data-stu-id="cf0b8-235">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="cf0b8-236">Os processos subjacentes ainda podem estar em execução, e uma limpeza pode ser necessária para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-236">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="cf0b8-237"><dt>**Exceção**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-237"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="cf0b8-238">O trabalho está em um estado anormal que pode indicar uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-238">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="cf0b8-239">O status real do trabalho pode estar disponível por meio de objetos específicos do trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-239">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="cf0b8-240"><dt>**Serviço**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-240"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="cf0b8-241">O trabalho está em um estado específico do fornecedor que dá suporte à descoberta de problemas ou à resolução, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-241">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="cf0b8-242"><dt>**DMTF reservado**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-242"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="cf0b8-243">Reservado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-243">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="cf0b8-244"><dt>**Fornecedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-244"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="cf0b8-245">Reservado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-245">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="cf0b8-246">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-246">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-249">Uma cadeia de caracteres que representa o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-249">A string that represents the job status.</span></span> <span data-ttu-id="cf0b8-250">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-250">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-251">**JobType**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-251">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-252">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-254">Indica o tipo de trabalho que está sendo acompanhado por este objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-254">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cf0b8-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Definir máquina virtual** (1)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Define Virtual Machine** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modificar máquina virtual** (2)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modify Virtual Machine** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Destruir máquina virtual** (3)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Destroy Virtual Machine** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>

<span data-ttu-id="cf0b8-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modificar as configurações do serviço de gerenciamento** (4)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modify Management Service Settings** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Inicializar máquina virtual** (10)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Initialize Virtual Machine** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Aguardando para iniciar a máquina virtual** (11)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Waiting to Start Virtual Machine** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Iniciar máquina virtual** (12)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Start Virtual Machine** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>Desligar a **máquina virtual** (13)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Power Off Virtual Machine** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Salvar máquina virtual** (14)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Save Virtual Machine** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restaurar máquina virtual** (15)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restore Virtual Machine** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Desligar máquina virtual** (16)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Shut Down Virtual Machine** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Pausar máquina virtual** (26)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Pause Virtual Machine** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Retomar máquina virtual** (27)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Resume Virtual Machine** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Redefinir máquina virtual** (28)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Reset Virtual Machine** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Reinicializar máquina virtual** (29)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Reboot Virtual Machine** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="cf0b8-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Adicionar recursos de máquina virtual** (30)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Add Virtual Machine Resources** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="cf0b8-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modificar recursos de máquina virtual** (31)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modify Virtual Machine Resources** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="cf0b8-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Remover recursos de máquina virtual** (32)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Remove Virtual Machine Resources** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>

<span data-ttu-id="cf0b8-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Solicitar memória de máquina virtual inicial** (40)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Request Initial Virtual Machine Memory** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Adicionar memória à máquina virtual** (41)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Add Memory to Virtual Machine** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Remover memória da máquina virtual** (42)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Remove Memory from Virtual Machine** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>

<span data-ttu-id="cf0b8-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Mesclando discos VHD** (50)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Merging VHD Disks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Criar um instantâneo VSS dentro da máquina virtual** (51)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Create VSS Snapshot inside Virtual Machine** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>

<span data-ttu-id="cf0b8-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Obter dados de configuração de importação** (60)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Get Import Setting Data** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Importar máquina virtual** (61)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Import Virtual Machine** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Exportar máquina virtual** (62)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Export Virtual Machine** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>

<span data-ttu-id="cf0b8-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Registrar configuração** (63)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Register Configuration** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>

<span data-ttu-id="cf0b8-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Cancelar o registro da configuração** (64)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Unregister Configuration** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Máquina virtual de instantâneo** (70)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Snapshot Virtual Machine** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="cf0b8-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Aplicar instantâneo de máquina virtual** (71)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Apply Virtual Machine Snapshot** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="cf0b8-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Excluir instantâneo de máquina virtual** (72)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Delete Virtual Machine Snapshot** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>

<span data-ttu-id="cf0b8-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Limpar o estado do instantâneo da máquina virtual** (73)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Clear Virtual Machine Snapshot State** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>

<span data-ttu-id="cf0b8-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Adicionar recursos ao pool de recursos** (80)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Add Resources to Resource Pool** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>

<span data-ttu-id="cf0b8-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Remover recursos do pool de recursos** (81)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Remove Resources from Resource Pool** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>

<span data-ttu-id="cf0b8-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modificar as configurações do servidor de replicação** (90)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modify Replication Server Settings** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="cf0b8-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Criar relação de replicação** (91)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Create Replication Relationship** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>

<span data-ttu-id="cf0b8-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modificar as configurações de relação de replicação** (92)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modify Replication Relationship Settings** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="cf0b8-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Remover relação de replicação** (93)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Remove Replication Relationship** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>

<span data-ttu-id="cf0b8-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Iniciar a replicação inicial da faixa** (94)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Start Inband Initial Replication** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>

<span data-ttu-id="cf0b8-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Replicação de importação** (95)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Import Replication** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>

<span data-ttu-id="cf0b8-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Replicar alteração de estado** (96)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Replicate State Change** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>

<span data-ttu-id="cf0b8-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Iniciar failover** (97)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Initiate Failover** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>

<span data-ttu-id="cf0b8-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Reverter failover** (98)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Revert Failover** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>

<span data-ttu-id="cf0b8-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Failover de confirmação** (99)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Commit Failover** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>

<span data-ttu-id="cf0b8-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Replicação sincronizada do Inititate** (100)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Inititate Synced Replication** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>

<span data-ttu-id="cf0b8-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Cancelar replicação sincronizada** (101)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Cancel Synced Replication** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>

<span data-ttu-id="cf0b8-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Iniciar réplica de teste** (102)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Initiate Test Replica** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>

<span data-ttu-id="cf0b8-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Remover réplica de teste** (103)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Remove Test Replica** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>

<span data-ttu-id="cf0b8-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Replicação inversa** (104)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Reverse Replication** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>

<span data-ttu-id="cf0b8-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Delta de envio de replicação** (105)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Replication Sending Delta** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>

<span data-ttu-id="cf0b8-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Delta de recebimento de replicação** (106)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Replication Receiving Delta** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="cf0b8-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Ressincronização** (107)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>

<span data-ttu-id="cf0b8-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Aplicar log de alterações** (108)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Apply change log** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>

<span data-ttu-id="cf0b8-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Parar replicação inicial** (109)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Stop Initial Replication** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>

<span data-ttu-id="cf0b8-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Parar a ressincronização** (110)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Stop Resynchronizing** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>

<span data-ttu-id="cf0b8-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Obter estatísticas de réplica** (111)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Get Replica statistics** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="cf0b8-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Preparar o verificador de consistência** (112)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Prepare for Consistency Checker** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>

<span data-ttu-id="cf0b8-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Verificador de consistência** (113)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Consistency Checker** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="cf0b8-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Parar verificador de consistência** (114)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Stop Consistency Checker** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>

<span data-ttu-id="cf0b8-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Conexão de replicação de teste** (115)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Test Replication Connection** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>

<span data-ttu-id="cf0b8-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Enviando réplica inicial** (116)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Sending Initial Replica** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>

<span data-ttu-id="cf0b8-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Iniciar ressincronização de replicação inicial** (117)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Start Resync Initial Replication** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>

<span data-ttu-id="cf0b8-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Iniciar a exportação de replicação inicial** (118)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Start Export Initial Replication** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>

<span data-ttu-id="cf0b8-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Redefinir estatísticas de réplica** (119)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Reset Replica Statistics** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>

<span data-ttu-id="cf0b8-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Aplicar deltas registrados** (120)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Apply Registered Deltas** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>

<span data-ttu-id="cf0b8-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Ressincronizando a replicação estendida** (121)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Resynchronizing Extended Replication** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>

<span data-ttu-id="cf0b8-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Lendo a configuração da réplica de teste** (122)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Reading Test Replica Configuration** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>

<span data-ttu-id="cf0b8-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Alterar o modo de replicação para primário** (123)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Change the replication mode to primary** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>

<span data-ttu-id="cf0b8-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Iniciar o failback** (124)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Initiate Failback** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>

<span data-ttu-id="cf0b8-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Atualizar conjunto de discos** (125)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Update Disk Set** (125)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-326">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-326">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>

<span data-ttu-id="cf0b8-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Definir comutador Ethernet** (130)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Define Ethernet Switch** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>

<span data-ttu-id="cf0b8-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modificar as configurações do comutador Ethernet** (131)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modify Ethernet Switch Settings** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>

<span data-ttu-id="cf0b8-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Destruir comutador Ethernet** (132)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Destroy Ethernet Switch** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="cf0b8-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Adicionar recursos de comutador Ethernet** (133)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Add Ethernet Switch Resources** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="cf0b8-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modificar recursos do comutador Ethernet** (134)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modify Ethernet Switch Resources** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="cf0b8-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Remover recursos do comutador Ethernet** (135)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Remove Ethernet Switch Resources** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Validar máquina virtual planejada** (140)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Validate Planned Virtual Machine** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizando a máquina virtual** (141)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizing Virtual Machine** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>

<span data-ttu-id="cf0b8-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Criando um pool de recursos** (150)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Creating a Resource Pool** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="cf0b8-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Alterando os recursos pai de um pool de recursos** (151)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Changing the Parent Resources of a Resource Pool** (151)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="cf0b8-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Alterando as configurações não alloction de um pool de recursos** (152)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Changing the Non-alloction Settings of a Resource Pool** (152)</span></span>


</dt> <dd></dd> <dt>

<span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>

<span data-ttu-id="cf0b8-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Excluindo um pool de recursos** (153)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Deleting a Resource Pool** (153)</span></span>


</dt> <dd></dd> <dt>

<span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="cf0b8-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Habilitar GPU do RemoteFx** (160)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Enable RemoteFx GPU** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="cf0b8-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Desabilitar GPU do RemoteFx** (161)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Disable RemoteFx GPU** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>

<span data-ttu-id="cf0b8-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modificar as configurações do serviço 3D** (162)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modify 3D Service Settings** (162)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-342">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-342">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>

<span data-ttu-id="cf0b8-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Máquina virtual de backup** (170)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Backup Virtual Machine** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>

<span data-ttu-id="cf0b8-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Interface do serviço de convidado** (180)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Guest Service Interface** (180)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-345">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-345">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>

<span data-ttu-id="cf0b8-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Consultar informações do cluster de convidado** (181)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Query Guest Cluster Information** (181)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-347">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-347">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>

<span data-ttu-id="cf0b8-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Definir coleção** (190)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Define Collection** (190)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-349">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-349">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>

<span data-ttu-id="cf0b8-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destruir coleção** (191)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destroy Collection** (191)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-351">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-351">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>

<span data-ttu-id="cf0b8-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Renomear coleção** (192)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Rename Collection** (192)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-353">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-353">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>

<span data-ttu-id="cf0b8-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Adicionar membro à coleção** (193)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Add Member to Collection** (193)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-355">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-355">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>

<span data-ttu-id="cf0b8-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Remover membro da coleção** (194)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Remove Member from Collection** (194)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-357">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-357">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>

<span data-ttu-id="cf0b8-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Adicionar configuração à coleção** (195)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Add Setting to Collection** (195)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-359">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-359">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>

<span data-ttu-id="cf0b8-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Remover configuração da coleção** (196)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Remove Setting from Collection** (196)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-361">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-361">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>

<span data-ttu-id="cf0b8-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modificar configuração na coleção** (197)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modify Setting on Collection** (197)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-363">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-363">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>

<span data-ttu-id="cf0b8-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Coleção de instantâneos** (198)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Snapshot Collection** (198)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-365">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-365">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>

<span data-ttu-id="cf0b8-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Converter instantâneo para ponto de referência** (200)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convert Snapshot to Reference Point** (200)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-367">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-367">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>

<span data-ttu-id="cf0b8-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Criar ponto de referência** (201)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Create Reference Point** (201)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-369">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-369">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>

<span data-ttu-id="cf0b8-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Excluir ponto de referência** (202)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Delete Reference Point** (202)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-371">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-371">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>

<span data-ttu-id="cf0b8-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Ponto de referência de exportação** (203)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Export Reference Point** (203)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-373">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-373">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>

<span data-ttu-id="cf0b8-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Remover dados associados do ponto de referência** (204)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Remove Associated Data from Reference Point** (204)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-375">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-375">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="cf0b8-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Criar ponto de referência na coleção** (205)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Create Reference Point on Collection** (205)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-377">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-377">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="cf0b8-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Exportar ponto de referência na coleção** (206)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Export Reference Point on Collection** (206)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-379">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-379">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="cf0b8-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Remover dados associados do ponto de referência na coleção** (207)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Remove Associated Data from Reference Point on Collection** (207)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-381">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-381">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="cf0b8-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Excluir ponto de referência na coleção** (208)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Delete Reference Point on Collection** (208)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-383">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-383">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>

<span data-ttu-id="cf0b8-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Importar metadados do ponto de referência** (209)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Import Reference Point metadata** (209)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-385">Valor adicionado no Windows 10 como **ponto de referência de limpeza**.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-385">Value added in Windows 10 as **Cleanup Reference Point**.</span></span>

 

</dd> <dt>

<span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>

<span data-ttu-id="cf0b8-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Montar ou desmontar dispositivo atribuível** (260)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Mount or Dismount Assignable Device** (260)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="cf0b8-387">Valor adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-387">Value added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cf0b8-388">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-388">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-389">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-391">Indica se as horas representadas nas propriedades **RunStartInterval** e **UntilTime** representam horários locais ou horários UTC.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-391">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="cf0b8-392">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="cf0b8-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Hora local** (1)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Hora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cf0b8-395">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-395">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-396">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-398">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-398">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-399">O nome de exibição para esta instância de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-399">The display name for this instance of a job.</span></span> <span data-ttu-id="cf0b8-400">Além disso, o nome de exibição pode ser usado como uma propriedade para uma pesquisa ou consulta.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-400">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="cf0b8-401">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-402">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-402">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-405">O usuário que é notificado após a conclusão ou falha do trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-405">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="cf0b8-406">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-406">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-407">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-407">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-408">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-410">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="cf0b8-410">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="cf0b8-411">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cf0b8-412">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-414">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-416">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-416">The current statuses of the object.</span></span> <span data-ttu-id="cf0b8-417">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-418">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-418">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-419">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-421">Uma cadeia de caracteres que descreve a ação de recuperação quando a propriedade **recoveryaction** da instância é 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-421">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="cf0b8-422">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-422">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-423">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-423">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-426">O usuário que enviou o trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-426">The user who submitted the job.</span></span> <span data-ttu-id="cf0b8-427">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-427">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-428">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-428">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-429">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-431">Qualificadores: **MinValue** (0), **MaxValue** (100), **unidades** ("percent")</span><span class="sxs-lookup"><span data-stu-id="cf0b8-431">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-432">A porcentagem de conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-432">The completion percentage of the job.</span></span> <span data-ttu-id="cf0b8-433">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-433">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-434">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-434">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-435">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-436">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-437">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-437">Provides high level status information.</span></span> <span data-ttu-id="cf0b8-438">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-438">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="cf0b8-439">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-439">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cf0b8-440">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-440">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-441">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-441">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-442">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-442">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-444">A importância da execução de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-444">The importance of a job's execution.</span></span> <span data-ttu-id="cf0b8-445">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-445">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-446">**Recuperação de**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-446">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-447">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-448">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-449">Descreve a ação de recuperação a ser executada para um trabalho que não foi executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-449">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="cf0b8-450">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-450">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="cf0b8-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>Não **continuar** (2)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar com o próximo trabalho** (3)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Executar trabalho novamente** (4)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Executar trabalho de recuperação** (5)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cf0b8-457">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-457">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-458">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-458">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-459">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-460">Qualificadores: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-460">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-461">O dia do mês em que o trabalho deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-461">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="cf0b8-462">Há diferentes interpretações para essa propriedade, dependendo do valor de **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-462">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="cf0b8-463">Quando **RunDayOfWeek** é 0 e **RunDay** é positivo, **RunDay** define o dia do mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-463">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="cf0b8-464">Por exemplo, se **RunDayOfWeek** for 0 e **RunDay** for 12, o trabalho será processado nos <sup>12 dias do</sup> mês.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-464">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="cf0b8-465">Quando **RunDayOfWeek** é 0 e **RunDay** é negativo, **RunDay** define o número de dias antes do último dia do mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-465">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="cf0b8-466">1 indica o último dia do mês, 2 indica um dia antes do último dia do mês e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-466">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="cf0b8-467">Por exemplo, se **RunDayOfWeek** for 0 e **RunDay** for 1, o trabalho será processado no último dia do mês.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-467">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="cf0b8-468">Quando **RunDayOfWeek** não for 0, **RunDayOfWeek** será o dia da semana em que o trabalho será processado, em relação a **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-468">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="cf0b8-469">Por exemplo, se **RunDay** for 15 e **RunDayOfWeek** for 7 (+ sábado), o trabalho será processado no primeiro sábado, em ou <sup>após 15 dias</sup> do mês.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-469">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="cf0b8-470">Se **RunDay** for 20 e **RunDayOfWeek** for 7 (sábado), o trabalho será processado no primeiro sábado, em ou antes <sup>dos 20 dias</sup> do mês.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-470">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="cf0b8-471">Se **RunDay** for 1 e **RunDayOfWeek** for 1 (domingo), o trabalho será processado no último domingo do mês.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-471">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="cf0b8-472">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-472">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-473">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-473">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-474">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-474">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-476">Um inteiro positivo ou negativo usado em conjunto com **RunDay** para indicar o dia da semana ou mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-476">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="cf0b8-477">Consulte a descrição da propriedade **RunDay** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-477">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="cf0b8-478">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-478">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="cf0b8-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Sexta** (6)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Quinta** (5)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Quarta** (4)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Terça-feira** (3)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Segunda** (2)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Segunda** (2)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Terça-feira** (3)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Quarta-feira** (4)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Quinta-feira** (5)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Sexta-feira** (6)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cf0b8-494">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-494">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-495">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-495">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-496">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-497">O mês durante o qual o trabalho deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-497">The month during which the job should be processed.</span></span> <span data-ttu-id="cf0b8-498">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-498">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="cf0b8-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Janeiro** (0)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Fevereiro** (1)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Março** (2)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Abril** (3)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Maio** (4)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Junho** (5)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Julho** (6)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Setembro** (8)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Outubro** (9)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembro** (10)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dezembro** (11)</span><span class="sxs-lookup"><span data-stu-id="cf0b8-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cf0b8-511">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-511">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-512">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-512">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-513">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-514">O intervalo de tempo após a meia-noite quando o trabalho deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-514">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="cf0b8-515">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-515">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-516">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-516">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-517">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-517">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-518">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-519">A hora de início agendada para o trabalho, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-519">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="cf0b8-520">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-520">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-521">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-521">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-522">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-522">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-523">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-524">A hora em que o trabalho começou.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-524">The time that the job began.</span></span> <span data-ttu-id="cf0b8-525">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-525">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-526">**Status**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-526">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-527">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-528">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-528">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-529">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-530">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-531">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-532">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-533">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="cf0b8-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="cf0b8-534">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="cf0b8-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-535">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-535">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-536">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-536">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-537">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-538">A quantidade de tempo, em minutos, que o trabalho é retido após a conclusão da execução, com êxito ou falha na execução.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-538">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="cf0b8-539">O trabalho deve permanecer em existência por algum período de tempo, independentemente do valor da propriedade **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="cf0b8-539">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="cf0b8-540">O padrão é de cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-540">The default is five minutes.</span></span> <span data-ttu-id="cf0b8-541">Essa propriedade é herdada do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))e é sempre definida como 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-541">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-543">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-544">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-545">A data ou a hora em que o estado do trabalho foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-545">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="cf0b8-546">Se o estado do trabalho não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-546">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="cf0b8-547">Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-547">If a state change was requested but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="cf0b8-548">Essa propriedade é herdada do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-548">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-549">**Timeenvio**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-549">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-550">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-550">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-551">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-551">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-552">A hora em que o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-552">The time that the job was submitted.</span></span> <span data-ttu-id="cf0b8-553">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-553">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="cf0b8-554">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-554">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf0b8-555">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-555">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf0b8-556">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf0b8-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf0b8-557">A hora em que o trabalho não é válido ou deve ser parado.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-557">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="cf0b8-558">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-558">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf0b8-559">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf0b8-559">Remarks</span></span>

<span data-ttu-id="cf0b8-560">O acesso à classe **Msvm \_ ConcreteJob** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="cf0b8-560">Access to the **Msvm\_ConcreteJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cf0b8-561">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cf0b8-561">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf0b8-562">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf0b8-562">Requirements</span></span>



| <span data-ttu-id="cf0b8-563">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf0b8-563">Requirement</span></span> | <span data-ttu-id="cf0b8-564">Valor</span><span class="sxs-lookup"><span data-stu-id="cf0b8-564">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0b8-565">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf0b8-565">Minimum supported client</span></span><br/> | <span data-ttu-id="cf0b8-566">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cf0b8-566">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cf0b8-567">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf0b8-567">Minimum supported server</span></span><br/> | <span data-ttu-id="cf0b8-568">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cf0b8-568">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf0b8-569">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf0b8-569">Namespace</span></span><br/>                | <span data-ttu-id="cf0b8-570">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="cf0b8-570">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cf0b8-571">MOF</span><span class="sxs-lookup"><span data-stu-id="cf0b8-571">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf0b8-572"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-572"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf0b8-573">DLL</span><span class="sxs-lookup"><span data-stu-id="cf0b8-573">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf0b8-574"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf0b8-574"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf0b8-575">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf0b8-575">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf0b8-576">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="cf0b8-576">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="cf0b8-577">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf0b8-577">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cf0b8-578">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="cf0b8-578">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

