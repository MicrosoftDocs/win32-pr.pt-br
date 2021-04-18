---
description: Representa um trabalho de operação do serviço de arquivo convidado.
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Classe Msvm_CopyFileToGuestJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766896"
---
# <a name="msvm_copyfiletoguestjob-class"></a><span data-ttu-id="e6673-103">\_Classe Msvm CopyFileToGuestJob</span><span class="sxs-lookup"><span data-stu-id="e6673-103">Msvm\_CopyFileToGuestJob class</span></span>

<span data-ttu-id="e6673-104">Representa um trabalho de operação do serviço de arquivo convidado.</span><span class="sxs-lookup"><span data-stu-id="e6673-104">Represents a guest file service operation job.</span></span> <span data-ttu-id="e6673-105">Essa classe deriva de [**Msvm \_ GuestFileService**](msvm-guestfileservice.md).</span><span class="sxs-lookup"><span data-stu-id="e6673-105">This class derives from [**Msvm\_GuestFileService**](msvm-guestfileservice.md).</span></span>

<span data-ttu-id="e6673-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e6673-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6673-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6673-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a><span data-ttu-id="e6673-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e6673-108">Members</span></span>

<span data-ttu-id="e6673-109">A classe **Msvm \_ CopyFileToGuestJob** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e6673-109">The **Msvm\_CopyFileToGuestJob** class has these types of members:</span></span>

-   [<span data-ttu-id="e6673-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6673-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6673-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6673-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6673-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6673-112">Methods</span></span>

<span data-ttu-id="e6673-113">A classe **Msvm \_ CopyFileToGuestJob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e6673-113">The **Msvm\_CopyFileToGuestJob** class has these methods.</span></span>



| <span data-ttu-id="e6673-114">Método</span><span class="sxs-lookup"><span data-stu-id="e6673-114">Method</span></span>                                                                   | <span data-ttu-id="e6673-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6673-115">Description</span></span>                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="e6673-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="e6673-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md)       | <span data-ttu-id="e6673-117">Copia arquivos do host Hyper-V para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6673-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> |
| [<span data-ttu-id="e6673-118">**GetError**</span><span class="sxs-lookup"><span data-stu-id="e6673-118">**GetError**</span></span>](geterror-msvm-copyfiletoguestjob.md)                     | <span data-ttu-id="e6673-119">Recupera o objeto de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e6673-119">Retrieves the error object for the job.</span></span><br/>                    |
| [<span data-ttu-id="e6673-120">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="e6673-120">**GetErrorEx**</span></span>](geterrorex-msvm-copyfiletoguestjob.md)                 | <span data-ttu-id="e6673-121">Recupera os objetos de erro para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e6673-121">Retrieves the error objects for the job.</span></span><br/>                   |
| [<span data-ttu-id="e6673-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e6673-122">**RequestStateChange**</span></span>](requeststatechange-msvm-copyfiletoguestjob.md) | <span data-ttu-id="e6673-123">Altera o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e6673-123">Changes the state of the job.</span></span><br/>                              |
| <span data-ttu-id="e6673-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="e6673-124">**StartService**</span></span>                                                         | <span data-ttu-id="e6673-125">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e6673-125">This method is not supported.</span></span><br/>                              |
| <span data-ttu-id="e6673-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="e6673-126">**StopService**</span></span>                                                          | <span data-ttu-id="e6673-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="e6673-127">This method is not supported.</span></span><br/>                              |



 

### <a name="properties"></a><span data-ttu-id="e6673-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6673-128">Properties</span></span>

<span data-ttu-id="e6673-129">A classe **Msvm \_ CopyFileToGuestJob** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e6673-129">The **Msvm\_CopyFileToGuestJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6673-130">**Cancelável**</span><span class="sxs-lookup"><span data-stu-id="e6673-130">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-131">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e6673-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-133">Indica se o trabalho pode ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="e6673-133">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="e6673-134">O valor dessa propriedade não garante que uma solicitação para cancelar o trabalho seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="e6673-134">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span> <span data-ttu-id="e6673-135">Se **for true**, o trabalho poderá ser cancelado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e6673-135">If **TRUE**, the job can be cancelled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e6673-136">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e6673-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-139">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e6673-139">Short textual description of the object.</span></span> <span data-ttu-id="e6673-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6673-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6673-141">**CopyFileToGuestSettingData**</span><span class="sxs-lookup"><span data-stu-id="e6673-141">**CopyFileToGuestSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-142">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e6673-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-144">Definindo dados que são usados para copiar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e6673-144">Setting data that is used to copy a file.</span></span>

</dd> <dt>

<span data-ttu-id="e6673-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e6673-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-148">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="e6673-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e6673-149">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="e6673-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="e6673-150">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e6673-150">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-153">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e6673-153">Textual description of the object.</span></span> <span data-ttu-id="e6673-154">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6673-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6673-155">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="e6673-155">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6673-158">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabalho CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="e6673-158">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="e6673-159">Uma descrição resumida do erro, se presente.</span><span class="sxs-lookup"><span data-stu-id="e6673-159">A summary description of the error, if present.</span></span> <span data-ttu-id="e6673-160">Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="e6673-160">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="e6673-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e6673-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-162">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6673-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-164">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e6673-164">Date and time the object was installed.</span></span> <span data-ttu-id="e6673-165">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e6673-165">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="e6673-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6673-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6673-167">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e6673-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-170">Identificador exclusivo do serviço que também fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e6673-170">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="e6673-171">Para obter mais informações sobre a funcionalidade, consulte a propriedade **Description** do objeto.</span><span class="sxs-lookup"><span data-stu-id="e6673-171">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="e6673-172">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6673-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6673-173">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="e6673-173">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-174">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e6673-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-176">Se **for true**, o serviço foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="e6673-176">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="e6673-177">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="e6673-177">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-180">Indica se o serviço é iniciado automaticamente (por exemplo, por um sistema operacional) ou iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="e6673-180">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="e6673-181">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e6673-181">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="e6673-182">**Automática**</span><span class="sxs-lookup"><span data-stu-id="e6673-182">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="e6673-183">**Manual**</span><span class="sxs-lookup"><span data-stu-id="e6673-183">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6673-184">**Status**</span><span class="sxs-lookup"><span data-stu-id="e6673-184">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-187">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e6673-187">Current status of the object.</span></span> <span data-ttu-id="e6673-188">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6673-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="e6673-189">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e6673-189">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="e6673-190">**PROBLEMAS**</span><span class="sxs-lookup"><span data-stu-id="e6673-190">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="e6673-191">**Ao**</span><span class="sxs-lookup"><span data-stu-id="e6673-191">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="e6673-192">**Degradado**</span><span class="sxs-lookup"><span data-stu-id="e6673-192">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="e6673-193">**Conhecidos**</span><span class="sxs-lookup"><span data-stu-id="e6673-193">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="e6673-194">**"Falha de Pred"**</span><span class="sxs-lookup"><span data-stu-id="e6673-194">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="e6673-195">**Comece**</span><span class="sxs-lookup"><span data-stu-id="e6673-195">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="e6673-196">**Impedir**</span><span class="sxs-lookup"><span data-stu-id="e6673-196">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="e6673-197">**Serviço**</span><span class="sxs-lookup"><span data-stu-id="e6673-197">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="e6673-198">**Analisa**</span><span class="sxs-lookup"><span data-stu-id="e6673-198">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="e6673-199">**"Não recuperar"**</span><span class="sxs-lookup"><span data-stu-id="e6673-199">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="e6673-200">**"Sem contato"**</span><span class="sxs-lookup"><span data-stu-id="e6673-200">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="e6673-201">**"Perda de comunicação"**</span><span class="sxs-lookup"><span data-stu-id="e6673-201">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6673-202">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e6673-202">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-205">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e6673-205">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="e6673-206">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e6673-206">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-209">Nome do sistema que hospeda o serviço.</span><span class="sxs-lookup"><span data-stu-id="e6673-209">Name of the system that hosts the service.</span></span>

</dd> <dt>

<span data-ttu-id="e6673-210">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="e6673-210">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6673-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e6673-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6673-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e6673-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6673-213">GUID do sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="e6673-213">GUID of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e6673-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6673-214">Requirements</span></span>



| <span data-ttu-id="e6673-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6673-215">Requirement</span></span> | <span data-ttu-id="e6673-216">Valor</span><span class="sxs-lookup"><span data-stu-id="e6673-216">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6673-217">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6673-217">Minimum supported client</span></span><br/> | <span data-ttu-id="e6673-218">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6673-218">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e6673-219">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6673-219">Minimum supported server</span></span><br/> | <span data-ttu-id="e6673-220">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="e6673-220">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e6673-221">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6673-221">Namespace</span></span><br/>                | <span data-ttu-id="e6673-222">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e6673-222">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6673-223">MOF</span><span class="sxs-lookup"><span data-stu-id="e6673-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6673-224"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6673-224"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6673-225">DLL</span><span class="sxs-lookup"><span data-stu-id="e6673-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6673-226"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6673-226"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6673-227">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6673-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6673-228">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="e6673-228">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

[<span data-ttu-id="e6673-229">**Msvm \_ GuestFileService**</span><span class="sxs-lookup"><span data-stu-id="e6673-229">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> <dt>

[<span data-ttu-id="e6673-230">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="e6673-230">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

