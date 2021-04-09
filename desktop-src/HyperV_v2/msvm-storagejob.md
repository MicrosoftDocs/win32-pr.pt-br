---
description: Representa um trabalho de operação de armazenamento criado pelo serviço de gerenciamento de imagens Microsoft Hyper-V.
ms.assetid: a1517c1f-7fb6-4203-a5ec-2ecdfcbc4e8c
title: Classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob
- Msvm_StorageJob.KillJob
- Msvm_StorageJob.InstanceID
- Msvm_StorageJob.Caption
- Msvm_StorageJob.Description
- Msvm_StorageJob.ElementName
- Msvm_StorageJob.InstallDate
- Msvm_StorageJob.Name
- Msvm_StorageJob.OperationalStatus
- Msvm_StorageJob.StatusDescriptions
- Msvm_StorageJob.Status
- Msvm_StorageJob.HealthState
- Msvm_StorageJob.CommunicationStatus
- Msvm_StorageJob.DetailedStatus
- Msvm_StorageJob.OperatingStatus
- Msvm_StorageJob.PrimaryStatus
- Msvm_StorageJob.JobStatus
- Msvm_StorageJob.TimeSubmitted
- Msvm_StorageJob.ScheduledStartTime
- Msvm_StorageJob.StartTime
- Msvm_StorageJob.ElapsedTime
- Msvm_StorageJob.JobRunTimes
- Msvm_StorageJob.RunMonth
- Msvm_StorageJob.RunDay
- Msvm_StorageJob.RunDayOfWeek
- Msvm_StorageJob.RunStartInterval
- Msvm_StorageJob.LocalOrUtcTime
- Msvm_StorageJob.UntilTime
- Msvm_StorageJob.Notify
- Msvm_StorageJob.Owner
- Msvm_StorageJob.Priority
- Msvm_StorageJob.PercentComplete
- Msvm_StorageJob.DeleteOnCompletion
- Msvm_StorageJob.ErrorCode
- Msvm_StorageJob.ErrorDescription
- Msvm_StorageJob.ErrorSummaryDescription
- Msvm_StorageJob.RecoveryAction
- Msvm_StorageJob.OtherRecoveryAction
- Msvm_StorageJob.JobState
- Msvm_StorageJob.TimeOfLastStateChange
- Msvm_StorageJob.TimeBeforeRemoval
- Msvm_StorageJob.Cancellable
- Msvm_StorageJob.Child
- Msvm_StorageJob.JobCompletionStatusCode
- Msvm_StorageJob.Parent
- Msvm_StorageJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3014cb9a8201d7baceaf39bb760b17c33844abeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837421"
---
# <a name="msvm_storagejob-class"></a><span data-ttu-id="612c3-103">\_Classe Msvm StorageJob</span><span class="sxs-lookup"><span data-stu-id="612c3-103">Msvm\_StorageJob class</span></span>

<span data-ttu-id="612c3-104">Representa um trabalho de operação de armazenamento criado pelo serviço de gerenciamento de imagens Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="612c3-104">Represents a storage operation job created by the Microsoft Hyper-V Image Management Service.</span></span>

<span data-ttu-id="612c3-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="612c3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="612c3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="612c3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
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
  datetime TimeBeforeRemoval = 00000000000500.000000:000";
  boolean  Cancellable;
  string   Child;
  UINT32   JobCompletionStatusCode;
  string   Parent;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="612c3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="612c3-107">Members</span></span>

<span data-ttu-id="612c3-108">A classe **Msvm \_ StorageJob** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="612c3-108">The **Msvm\_StorageJob** class has these types of members:</span></span>

-   [<span data-ttu-id="612c3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="612c3-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="612c3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="612c3-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="612c3-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="612c3-111">Methods</span></span>

<span data-ttu-id="612c3-112">A classe **Msvm \_ StorageJob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="612c3-112">The **Msvm\_StorageJob** class has these methods.</span></span>



| <span data-ttu-id="612c3-113">Método</span><span class="sxs-lookup"><span data-stu-id="612c3-113">Method</span></span>                                                           | <span data-ttu-id="612c3-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="612c3-114">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="612c3-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="612c3-115">**GetError**</span></span>](msvm-storagejob-geterror.md)                     | <span data-ttu-id="612c3-116">Recupera o erro que descreve o motivo pelo qual o trabalho falhou.</span><span class="sxs-lookup"><span data-stu-id="612c3-116">Retrieves the error that describes the reason why the job failed.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="612c3-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="612c3-117">**GetErrorEx**</span></span>](geterrorex-msvm-storagejob.md)                 | <span data-ttu-id="612c3-118">Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma instância de [**\_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="612c3-118">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="612c3-119">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma ou mais instâncias de **\_ erro Msvm** são retornadas.</span><span class="sxs-lookup"><span data-stu-id="612c3-119">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span><br/> |
| <span data-ttu-id="612c3-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="612c3-120">**KillJob**</span></span>                                                      | <span data-ttu-id="612c3-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="612c3-121">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="612c3-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="612c3-122">**RequestStateChange**</span></span>](msvm-storagejob-requeststatechange.md) | <span data-ttu-id="612c3-123">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="612c3-123">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="612c3-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="612c3-124">Properties</span></span>

<span data-ttu-id="612c3-125">A classe **Msvm \_ StorageJob** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="612c3-125">The **Msvm\_StorageJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="612c3-126">**Cancelável**</span><span class="sxs-lookup"><span data-stu-id="612c3-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-127">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="612c3-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-129">Indica se o trabalho pode ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="612c3-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="612c3-130">O valor dessa propriedade não garante que uma solicitação para cancelar o trabalho seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="612c3-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="612c3-131">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="612c3-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-134">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="612c3-134">A short description of the object.</span></span> <span data-ttu-id="612c3-135">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-136">**Filho**</span><span class="sxs-lookup"><span data-stu-id="612c3-136">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-139">Em caso de falha da operação assíncrona, essa propriedade contém o caminho completo do filho do VHD que está sendo afetado por essa operação.</span><span class="sxs-lookup"><span data-stu-id="612c3-139">On failure of the asynchronous operation, this property contains the full path of the child of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="612c3-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="612c3-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-141">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-143">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="612c3-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="612c3-144">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="612c3-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="612c3-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-146">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="612c3-146">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-147">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="612c3-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-149">Especifica se o trabalho deve ser excluído automaticamente após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="612c3-149">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="612c3-150">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-150">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-151">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="612c3-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-154">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="612c3-154">A description of the object.</span></span> <span data-ttu-id="612c3-155">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="612c3-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-157">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-159">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="612c3-159">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="612c3-160">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="612c3-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="612c3-161">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-162">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-163">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-165">O período de tempo em que o trabalho foi executado.</span><span class="sxs-lookup"><span data-stu-id="612c3-165">The length of time that the job has been executing.</span></span> <span data-ttu-id="612c3-166">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="612c3-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-170">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="612c3-170">A display name for the object.</span></span> <span data-ttu-id="612c3-171">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="612c3-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-173">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-175">Um código de erro específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="612c3-175">A vendor-specific error code.</span></span> <span data-ttu-id="612c3-176">O valor deve ser definido como zero se o trabalho for concluído sem erros.</span><span class="sxs-lookup"><span data-stu-id="612c3-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="612c3-177">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="612c3-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-181">Uma cadeia de caracteres que contém a descrição do erro do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="612c3-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="612c3-182">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="612c3-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="612c3-186">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabalho CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="612c3-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="612c3-187">Uma descrição resumida do erro, se presente.</span><span class="sxs-lookup"><span data-stu-id="612c3-187">A summary description of the error, if present.</span></span> <span data-ttu-id="612c3-188">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-188">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="612c3-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-190">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-192">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="612c3-192">The current health of the element.</span></span> <span data-ttu-id="612c3-193">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="612c3-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="612c3-194">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="612c3-194">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="612c3-195">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.</span><span class="sxs-lookup"><span data-stu-id="612c3-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="612c3-196">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="612c3-196">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-197">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-199">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="612c3-199">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="612c3-200">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-201">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="612c3-201">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-204">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="612c3-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="612c3-205">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-206">**JobCompletionStatusCode**</span><span class="sxs-lookup"><span data-stu-id="612c3-206">**JobCompletionStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-207">Tipo de dados: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="612c3-207">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-209">O código **HRESULT** que descreve o status de conclusão da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="612c3-209">The **HRESULT** code that describes the completion status for the asynchronous operation.</span></span>

</dd> <dt>

<span data-ttu-id="612c3-210">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="612c3-210">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-211">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="612c3-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-213">O número de vezes que o trabalho deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="612c3-213">The number of times that the job should be run.</span></span> <span data-ttu-id="612c3-214">Um valor de 1 indica que o trabalho não é recorrente, enquanto qualquer valor diferente de zero indica um limite para o número de vezes que o trabalho será recorrente.</span><span class="sxs-lookup"><span data-stu-id="612c3-214">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="612c3-215">Zero indica que não há nenhum limite para o número de vezes que o trabalho pode ser processado, mas será encerrado após o tempo de espera ter sido atingido **ou o trabalho** será encerrado manualmente.</span><span class="sxs-lookup"><span data-stu-id="612c3-215">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="612c3-216">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-216">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-217">**JobState**</span><span class="sxs-lookup"><span data-stu-id="612c3-217">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-218">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-220">O estado operacional de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="612c3-220">The operational state of a job.</span></span> <span data-ttu-id="612c3-221">Ele também pode indicar transições entre esses Estados, por exemplo, 6 (desligando) e 3 (iniciando).</span><span class="sxs-lookup"><span data-stu-id="612c3-221">It can also indicate transitions between these states, for example, 6 (Shutting Down) and 3 (Starting).</span></span> <span data-ttu-id="612c3-222">Essa propriedade é herdada do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="612c3-222">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="612c3-223">Valor</span><span class="sxs-lookup"><span data-stu-id="612c3-223">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="612c3-224">Significado</span><span class="sxs-lookup"><span data-stu-id="612c3-224">Meaning</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="612c3-225"><dt>**Novo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-225"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                               | <span data-ttu-id="612c3-226">O trabalho nunca foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="612c3-226">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="612c3-227"><dt>**Iniciando**</dt> em <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-227"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                           | <span data-ttu-id="612c3-228">O trabalho está mudando dos Estados "novo", "suspenso" ou "serviço" para o estado "em execução".</span><span class="sxs-lookup"><span data-stu-id="612c3-228">The job is moving from the "New", "Suspended", or "Service" states into the "Running" state.</span></span><br/>                                                                                                                                            |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="612c3-229"><dt>**Executando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-229"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                               | <span data-ttu-id="612c3-230">O trabalho está em execução.</span><span class="sxs-lookup"><span data-stu-id="612c3-230">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="612c3-231"><dt>**Suspenso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-231"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                       | <span data-ttu-id="612c3-232">O trabalho é interrompido, mas pode ser reiniciado de maneira direta.</span><span class="sxs-lookup"><span data-stu-id="612c3-232">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="612c3-233"><dt>**Desligando**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-233"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                       | <span data-ttu-id="612c3-234">O trabalho está mudando para um estado "concluído", "encerrado" ou "eliminado".</span><span class="sxs-lookup"><span data-stu-id="612c3-234">The job is moving to a "Completed", "Terminated", or "Killed" state.</span></span><br/>                                                                                                                                                                    |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="612c3-235"><dt>**Concluído**</dt> em <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-235"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                       | <span data-ttu-id="612c3-236">O trabalho foi concluído normalmente.</span><span class="sxs-lookup"><span data-stu-id="612c3-236">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="612c3-237"><dt>**Terminada**</dt> em <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-237"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                                   | <span data-ttu-id="612c3-238">O trabalho foi interrompido por uma solicitação de alteração de estado "Terminate".</span><span class="sxs-lookup"><span data-stu-id="612c3-238">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="612c3-239">O trabalho e todos os seus processos subjacentes são encerrados e podem ser reiniciados apenas como um novo trabalho.</span><span class="sxs-lookup"><span data-stu-id="612c3-239">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="612c3-240">O requisito de que o trabalho seja reiniciado somente como um novo trabalho é específico do trabalho.</span><span class="sxs-lookup"><span data-stu-id="612c3-240">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="612c3-241"><dt>**Encerrado**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-241"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                                   | <span data-ttu-id="612c3-242">O trabalho foi interrompido por uma solicitação de alteração de estado "Kill".</span><span class="sxs-lookup"><span data-stu-id="612c3-242">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="612c3-243">Os processos subjacentes ainda podem estar em execução, e uma limpeza pode ser necessária para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="612c3-243">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="612c3-244"><dt>**Exceção**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-244"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                      | <span data-ttu-id="612c3-245">O trabalho está em um estado anormal que pode indicar uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="612c3-245">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="612c3-246">O status real do trabalho pode estar disponível por meio de objetos específicos do trabalho.</span><span class="sxs-lookup"><span data-stu-id="612c3-246">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="612c3-247"><dt>**Serviço**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-247"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                              | <span data-ttu-id="612c3-248">O trabalho está em um estado específico do fornecedor que dá suporte à descoberta de problemas ou à resolução, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="612c3-248">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="612c3-249"><dt>**DMTF reservado**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-249"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>                | <span data-ttu-id="612c3-250">Reservado.</span><span class="sxs-lookup"><span data-stu-id="612c3-250">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="612c3-251"><dt> **Fornecedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-251"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="612c3-252">Reservado.</span><span class="sxs-lookup"><span data-stu-id="612c3-252">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="612c3-253">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="612c3-253">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-254">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-256">Uma cadeia de caracteres que representa o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="612c3-256">A string that represents the job status.</span></span> <span data-ttu-id="612c3-257">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-257">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-258">**JobType**</span><span class="sxs-lookup"><span data-stu-id="612c3-258">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-259">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-261">O tipo de operação assíncrona que está sendo rastreada por esta instância de **Msvm \_ StorageJob**.</span><span class="sxs-lookup"><span data-stu-id="612c3-261">The type of asynchronous operation being tracked by this instance of **Msvm\_StorageJob**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="612c3-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="612c3-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>

<span data-ttu-id="612c3-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**Criação de VHD** (1)</span><span class="sxs-lookup"><span data-stu-id="612c3-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD Creation** (1)</span></span>


</dt> <dd>

<span data-ttu-id="612c3-264">Criando uma imagem de VHD (disco rígido virtual).</span><span class="sxs-lookup"><span data-stu-id="612c3-264">Creating a virtual hard disk (VHD) image.</span></span>

</dd> <dt>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>

<span data-ttu-id="612c3-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Criação de disquete** (2)</span><span class="sxs-lookup"><span data-stu-id="612c3-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Floppy Creation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="612c3-266">Criando uma imagem de disquete virtual (VFD).</span><span class="sxs-lookup"><span data-stu-id="612c3-266">Creating a virtual floppy disk image (VFD).</span></span>

</dd> <dt>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>

<span data-ttu-id="612c3-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compactação** (3)</span><span class="sxs-lookup"><span data-stu-id="612c3-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compaction** (3)</span></span>


</dt> <dd>

<span data-ttu-id="612c3-268">Compactando o tamanho de uma imagem VHD.</span><span class="sxs-lookup"><span data-stu-id="612c3-268">Compacting the size of a VHD image.</span></span>

</dd> <dt>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>

<span data-ttu-id="612c3-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansão** (4)</span><span class="sxs-lookup"><span data-stu-id="612c3-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansion** (4)</span></span>


</dt> <dd>

<span data-ttu-id="612c3-270">Expandindo o tamanho de uma imagem VHD.</span><span class="sxs-lookup"><span data-stu-id="612c3-270">Expanding the size of a VHD image.</span></span>

</dd> <dt>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>

<span data-ttu-id="612c3-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Mesclagem** (5)</span><span class="sxs-lookup"><span data-stu-id="612c3-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Merging** (5)</span></span>


</dt> <dd>

<span data-ttu-id="612c3-272">Mesclar várias imagens VHD em uma única imagem.</span><span class="sxs-lookup"><span data-stu-id="612c3-272">Merging multiple VHD images into a single image.</span></span>

</dd> <dt>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>

<span data-ttu-id="612c3-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversão** (6)</span><span class="sxs-lookup"><span data-stu-id="612c3-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="612c3-274">Convertendo o tipo de uma imagem de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="612c3-274">Converting the type of a virtual hard disk image.</span></span>

</dd> <dt>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>

<span data-ttu-id="612c3-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Montagem de auto-retorno** (7)</span><span class="sxs-lookup"><span data-stu-id="612c3-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Loopback Mount** (7)</span></span>


</dt> <dd>

<span data-ttu-id="612c3-276">Montando o disco rígido virtual na partição pai</span><span class="sxs-lookup"><span data-stu-id="612c3-276">Mounting the virtual hard disk on the parent partition</span></span>

</dd> <dt>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>

<span data-ttu-id="612c3-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Obter informações do VHD** (8)</span><span class="sxs-lookup"><span data-stu-id="612c3-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Get VHD Info** (8)</span></span>


</dt> <dd>

<span data-ttu-id="612c3-278">Montar o VHD no sistema operacional de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="612c3-278">Mounting the VHD on the management operating system.</span></span>

</dd> <dt>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>

<span data-ttu-id="612c3-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Validar imagem do VHD** (9)</span><span class="sxs-lookup"><span data-stu-id="612c3-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Validate VHD Image** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="612c3-280">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-280">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-281">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-283">Indica se as horas representadas nas propriedades **RunStartInterval** e **UntilTime** representam horários locais ou horários UTC.</span><span class="sxs-lookup"><span data-stu-id="612c3-283">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="612c3-284">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-284">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="612c3-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Hora local** (1)</span><span class="sxs-lookup"><span data-stu-id="612c3-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Hora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="612c3-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="612c3-287">**Nome**</span><span class="sxs-lookup"><span data-stu-id="612c3-287">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-290">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="612c3-290">The label by which the object is known.</span></span> <span data-ttu-id="612c3-291">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-292">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="612c3-292">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-295">O usuário que é notificado após a conclusão ou falha do trabalho.</span><span class="sxs-lookup"><span data-stu-id="612c3-295">The user who is notified upon job completion or failure.</span></span> <span data-ttu-id="612c3-296">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-296">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-297">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="612c3-297">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-298">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-300">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="612c3-300">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="612c3-301">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="612c3-301">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="612c3-302">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-303">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="612c3-303">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-304">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-304">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="612c3-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-306">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="612c3-306">The current statuses of the object.</span></span> <span data-ttu-id="612c3-307">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-308">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="612c3-308">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-311">Uma cadeia de caracteres que descreve a ação de recuperação quando a propriedade **recoveryaction** da instância é 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="612c3-311">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="612c3-312">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-312">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-313">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="612c3-313">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-314">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-316">O usuário que enviou o trabalho.</span><span class="sxs-lookup"><span data-stu-id="612c3-316">The user who submitted the job.</span></span> <span data-ttu-id="612c3-317">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-317">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-318">**Pai**</span><span class="sxs-lookup"><span data-stu-id="612c3-318">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-321">Em caso de falha da operação assíncrona, essa propriedade contém o caminho do arquivo para o pai do VHD que está sendo afetado por essa operação.</span><span class="sxs-lookup"><span data-stu-id="612c3-321">On failure of the asynchronous operation, this property contains the file path to the parent of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="612c3-322">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="612c3-322">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-323">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="612c3-325">Qualificadores: **MinValue** (0), **MaxValue** (100), **unidades** ("percent")</span><span class="sxs-lookup"><span data-stu-id="612c3-325">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="612c3-326">A porcentagem de conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="612c3-326">The completion percentage of the job.</span></span> <span data-ttu-id="612c3-327">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-327">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-328">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="612c3-328">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-329">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-329">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-331">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="612c3-331">Provides high level status information.</span></span> <span data-ttu-id="612c3-332">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="612c3-332">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="612c3-333">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="612c3-333">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="612c3-334">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-335">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="612c3-335">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-336">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="612c3-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-338">A importância da execução de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="612c3-338">The importance of a job's execution.</span></span> <span data-ttu-id="612c3-339">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-339">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-340">**Recuperação de**</span><span class="sxs-lookup"><span data-stu-id="612c3-340">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-341">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="612c3-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-343">Descreve a ação de recuperação a ser executada para um trabalho que não foi executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="612c3-343">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="612c3-344">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-344">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="612c3-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="612c3-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="612c3-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>Não **continuar** (2)</span><span class="sxs-lookup"><span data-stu-id="612c3-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar com o próximo trabalho** (3)</span><span class="sxs-lookup"><span data-stu-id="612c3-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Executar trabalho novamente** (4)</span><span class="sxs-lookup"><span data-stu-id="612c3-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Executar trabalho de recuperação** (5)</span><span class="sxs-lookup"><span data-stu-id="612c3-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="612c3-351">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="612c3-351">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-352">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="612c3-352">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="612c3-354">Qualificadores: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="612c3-354">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="612c3-355">O dia do mês em que o trabalho deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="612c3-355">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="612c3-356">Há diferentes interpretações para essa propriedade, dependendo do valor de **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="612c3-356">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="612c3-357">Quando **RunDayOfWeek** é 0 e **RunDay** é positivo, **RunDay** define o dia do mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="612c3-357">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="612c3-358">Por exemplo, se **RunDayOfWeek** for 0 e **RunDay** for 12, o trabalho será processado nos <sup>12 dias do</sup> mês.</span><span class="sxs-lookup"><span data-stu-id="612c3-358">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="612c3-359">Quando **RunDayOfWeek** é 0 e **RunDay** é negativo, **RunDay** define o número de dias antes do último dia do mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="612c3-359">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="612c3-360">1 indica o último dia do mês, 2 indica um dia antes do último dia do mês e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="612c3-360">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="612c3-361">Por exemplo, se **RunDayOfWeek** for 0 e **RunDay** for 1, o trabalho será processado no último dia do mês.</span><span class="sxs-lookup"><span data-stu-id="612c3-361">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="612c3-362">Quando **RunDayOfWeek** não for 0, **RunDayOfWeek** será o dia da semana em que o trabalho será processado, em relação a **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="612c3-362">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="612c3-363">Por exemplo, se **RunDay** for 15 e **RunDayOfWeek** for 7 (+ sábado), o trabalho será processado no primeiro sábado, em ou <sup>após 15 dias</sup> do mês.</span><span class="sxs-lookup"><span data-stu-id="612c3-363">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="612c3-364">Se **RunDay** for 20 e **RunDayOfWeek** for 7 (sábado), o trabalho será processado no primeiro sábado, em ou antes <sup>dos 20 dias</sup> do mês.</span><span class="sxs-lookup"><span data-stu-id="612c3-364">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="612c3-365">Se **RunDay** for 1 e **RunDayOfWeek** for 1 (domingo), o trabalho será processado no último domingo do mês.</span><span class="sxs-lookup"><span data-stu-id="612c3-365">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="612c3-366">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-366">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-367">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="612c3-367">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-368">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="612c3-368">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-370">Um inteiro positivo ou negativo usado em conjunto com **RunDay** para indicar o dia da semana ou mês em que o trabalho é processado.</span><span class="sxs-lookup"><span data-stu-id="612c3-370">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="612c3-371">Consulte a descrição da propriedade **RunDay** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="612c3-371">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="612c3-372">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-372">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="612c3-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="612c3-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Sexta** (6)</span><span class="sxs-lookup"><span data-stu-id="612c3-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Quinta** (5)</span><span class="sxs-lookup"><span data-stu-id="612c3-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Quarta** (4)</span><span class="sxs-lookup"><span data-stu-id="612c3-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Terça-feira** (3)</span><span class="sxs-lookup"><span data-stu-id="612c3-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Segunda** (2)</span><span class="sxs-lookup"><span data-stu-id="612c3-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="612c3-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="612c3-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="612c3-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Segunda** (2)</span><span class="sxs-lookup"><span data-stu-id="612c3-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Terça-feira** (3)</span><span class="sxs-lookup"><span data-stu-id="612c3-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Quarta-feira** (4)</span><span class="sxs-lookup"><span data-stu-id="612c3-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Quinta-feira** (5)</span><span class="sxs-lookup"><span data-stu-id="612c3-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Sexta-feira** (6)</span><span class="sxs-lookup"><span data-stu-id="612c3-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="612c3-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="612c3-388">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="612c3-388">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-389">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="612c3-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-391">O mês durante o qual o trabalho deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="612c3-391">The month during which the job should be processed.</span></span> <span data-ttu-id="612c3-392">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="612c3-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Janeiro** (0)</span><span class="sxs-lookup"><span data-stu-id="612c3-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Fevereiro** (1)</span><span class="sxs-lookup"><span data-stu-id="612c3-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Março** (2)</span><span class="sxs-lookup"><span data-stu-id="612c3-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Abril** (3)</span><span class="sxs-lookup"><span data-stu-id="612c3-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Maio** (4)</span><span class="sxs-lookup"><span data-stu-id="612c3-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Junho** (5)</span><span class="sxs-lookup"><span data-stu-id="612c3-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Julho** (6)</span><span class="sxs-lookup"><span data-stu-id="612c3-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="612c3-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Setembro** (8)</span><span class="sxs-lookup"><span data-stu-id="612c3-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Outubro** (9)</span><span class="sxs-lookup"><span data-stu-id="612c3-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembro** (10)</span><span class="sxs-lookup"><span data-stu-id="612c3-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="612c3-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dezembro** (11)</span><span class="sxs-lookup"><span data-stu-id="612c3-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="612c3-405">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="612c3-405">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-406">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-408">O intervalo de tempo após a meia-noite quando o trabalho deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="612c3-408">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="612c3-409">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-409">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-410">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-410">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-411">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-411">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-413">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-414">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-414">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-415">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-417">A hora em que o trabalho começou.</span><span class="sxs-lookup"><span data-stu-id="612c3-417">The time that the job began.</span></span> <span data-ttu-id="612c3-418">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-419">**Status**</span><span class="sxs-lookup"><span data-stu-id="612c3-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-420">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-422">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="612c3-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="612c3-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="612c3-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-424">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="612c3-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="612c3-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-426">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="612c3-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="612c3-427">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="612c3-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-428">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="612c3-428">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-429">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-431">A quantidade de tempo, em minutos, que o trabalho é retido após a conclusão da execução, com êxito ou falha na execução.</span><span class="sxs-lookup"><span data-stu-id="612c3-431">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="612c3-432">O trabalho deve permanecer em existência por algum período de tempo, independentemente do valor da propriedade **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="612c3-432">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="612c3-433">O padrão é de cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="612c3-433">The default is five minutes.</span></span> <span data-ttu-id="612c3-434">Essa propriedade é herdada do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))e é sempre definida como 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="612c3-434">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="612c3-435">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="612c3-435">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-436">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-436">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-438">A hora em que o estado da máquina virtual foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="612c3-438">The time at which the virtual machine's state was last modified.</span></span> <span data-ttu-id="612c3-439">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="612c3-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-440">**Timeenvio**</span><span class="sxs-lookup"><span data-stu-id="612c3-440">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-441">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-443">A hora em que o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="612c3-443">The time that the job was submitted.</span></span> <span data-ttu-id="612c3-444">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-444">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="612c3-445">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-445">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="612c3-446">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-446">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="612c3-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="612c3-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="612c3-448">A hora em que o trabalho não é válido ou deve ser parado.</span><span class="sxs-lookup"><span data-stu-id="612c3-448">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="612c3-449">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="612c3-449">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="612c3-450">Comentários</span><span class="sxs-lookup"><span data-stu-id="612c3-450">Remarks</span></span>

<span data-ttu-id="612c3-451">O acesso à classe **Msvm \_ StorageJob** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="612c3-451">Access to the **Msvm\_StorageJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="612c3-452">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="612c3-452">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="612c3-453">Requisitos</span><span class="sxs-lookup"><span data-stu-id="612c3-453">Requirements</span></span>



| <span data-ttu-id="612c3-454">Requisito</span><span class="sxs-lookup"><span data-stu-id="612c3-454">Requirement</span></span> | <span data-ttu-id="612c3-455">Valor</span><span class="sxs-lookup"><span data-stu-id="612c3-455">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="612c3-456">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="612c3-456">Minimum supported client</span></span><br/> | <span data-ttu-id="612c3-457">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="612c3-457">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="612c3-458">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="612c3-458">Minimum supported server</span></span><br/> | <span data-ttu-id="612c3-459">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="612c3-459">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="612c3-460">Namespace</span><span class="sxs-lookup"><span data-stu-id="612c3-460">Namespace</span></span><br/>                | <span data-ttu-id="612c3-461">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="612c3-461">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="612c3-462">MOF</span><span class="sxs-lookup"><span data-stu-id="612c3-462">MOF</span></span><br/>                      | <dl> <span data-ttu-id="612c3-463"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-463"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="612c3-464">DLL</span><span class="sxs-lookup"><span data-stu-id="612c3-464">DLL</span></span><br/>                      | <dl> <span data-ttu-id="612c3-465"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-465"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="612c3-466">Confira também</span><span class="sxs-lookup"><span data-stu-id="612c3-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="612c3-467">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="612c3-467">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="612c3-468">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="612c3-468">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="612c3-469">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="612c3-469">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

