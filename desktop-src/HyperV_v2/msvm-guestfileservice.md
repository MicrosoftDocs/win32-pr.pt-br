---
description: Msvm \_ GuestFileService contém um método que pode ser usado para copiar um arquivo para uma máquina virtual do host do Hyper-V.
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Classe Msvm_GuestFileService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ee0f235d7549428ecf02e9c758c83bcea33efe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750842"
---
# <a name="msvm_guestfileservice-class"></a><span data-ttu-id="cc1dd-103">\_Classe Msvm GuestFileService</span><span class="sxs-lookup"><span data-stu-id="cc1dd-103">Msvm\_GuestFileService class</span></span>

<span data-ttu-id="cc1dd-104">**Msvm \_ GuestFileService** contém um método que pode ser usado para copiar um arquivo para uma máquina virtual do host Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-104">**Msvm\_GuestFileService** contains a method that can be used to copy a file to a virtual machine from the Hyper-V host.</span></span> <span data-ttu-id="cc1dd-105">Essa classe deriva de [**Msvm \_ GuestService**](msvm-guestservice.md).</span><span class="sxs-lookup"><span data-stu-id="cc1dd-105">This class derives from [**Msvm\_GuestService**](msvm-guestservice.md).</span></span>

<span data-ttu-id="cc1dd-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc1dd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc1dd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
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
};
```

## <a name="members"></a><span data-ttu-id="cc1dd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cc1dd-108">Members</span></span>

<span data-ttu-id="cc1dd-109">A classe **Msvm \_ GuestFileService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cc1dd-109">The **Msvm\_GuestFileService** class has these types of members:</span></span>

-   [<span data-ttu-id="cc1dd-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc1dd-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="cc1dd-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cc1dd-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cc1dd-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc1dd-112">Methods</span></span>

<span data-ttu-id="cc1dd-113">A classe **Msvm \_ GuestFileService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-113">The **Msvm\_GuestFileService** class has these methods.</span></span>



| <span data-ttu-id="cc1dd-114">Método</span><span class="sxs-lookup"><span data-stu-id="cc1dd-114">Method</span></span>                                                             | <span data-ttu-id="cc1dd-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc1dd-115">Description</span></span>                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc1dd-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md) | <span data-ttu-id="cc1dd-117">Copia arquivos do host Hyper-V para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> <span data-ttu-id="cc1dd-118">**Windows 8.1:** Não há suporte para este método até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-118">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| <span data-ttu-id="cc1dd-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-119">**StartService**</span></span>                                                   | <span data-ttu-id="cc1dd-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-120">This method is not supported.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="cc1dd-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-121">**StopService**</span></span>                                                    | <span data-ttu-id="cc1dd-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-122">This method is not supported.</span></span><br/>                                                                                                                                     |



 

### <a name="properties"></a><span data-ttu-id="cc1dd-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cc1dd-123">Properties</span></span>

<span data-ttu-id="cc1dd-124">A classe **Msvm \_ GuestFileService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-124">The **Msvm\_GuestFileService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc1dd-125">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-128">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-128">Short textual description of the object.</span></span> <span data-ttu-id="cc1dd-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cc1dd-129">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cc1dd-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-133">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cc1dd-134">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="cc1dd-135">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-138">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-138">Textual description of the object.</span></span> <span data-ttu-id="cc1dd-139">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cc1dd-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cc1dd-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-141">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-143">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-143">Date and time the object was installed.</span></span> <span data-ttu-id="cc1dd-144">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-144">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="cc1dd-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cc1dd-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cc1dd-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-149">Identificador exclusivo do serviço que também fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-149">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="cc1dd-150">Para obter mais informações sobre a funcionalidade, consulte a propriedade **Description** do objeto.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-150">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="cc1dd-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cc1dd-151">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cc1dd-152">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-152">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-153">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-155">Se **for true**, o serviço foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-155">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="cc1dd-156">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-156">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-159">Indica se o serviço é iniciado automaticamente (por exemplo, por um sistema operacional) ou iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-159">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="cc1dd-160">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cc1dd-160">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="cc1dd-161">**Automática**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-161">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="cc1dd-162">**Manual**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-162">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cc1dd-163">**Status**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-166">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-166">Current status of the object.</span></span> <span data-ttu-id="cc1dd-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cc1dd-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="cc1dd-168">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cc1dd-168">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="cc1dd-169">**PROBLEMAS**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-169">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="cc1dd-170">**Ao**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-170">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="cc1dd-171">**Degradado**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-171">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="cc1dd-172">**Conhecidos**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-172">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="cc1dd-173">**"Falha de Pred"**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-173">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="cc1dd-174">**Comece**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-174">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="cc1dd-175">**Impedir**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-175">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="cc1dd-176">**Serviço**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-176">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="cc1dd-177">**Analisa**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-177">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="cc1dd-178">**"Não recuperar"**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-178">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="cc1dd-179">**"Sem contato"**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-179">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="cc1dd-180">**"Perda de comunicação"**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-180">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cc1dd-181">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-181">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-184">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-184">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="cc1dd-185">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-185">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc1dd-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc1dd-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc1dd-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc1dd-188">Nome do sistema que hospeda o serviço.</span><span class="sxs-lookup"><span data-stu-id="cc1dd-188">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc1dd-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc1dd-189">Requirements</span></span>



| <span data-ttu-id="cc1dd-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc1dd-190">Requirement</span></span> | <span data-ttu-id="cc1dd-191">Valor</span><span class="sxs-lookup"><span data-stu-id="cc1dd-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc1dd-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc1dd-192">Minimum supported client</span></span><br/> | <span data-ttu-id="cc1dd-193">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc1dd-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="cc1dd-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc1dd-194">Minimum supported server</span></span><br/> | <span data-ttu-id="cc1dd-195">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="cc1dd-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cc1dd-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc1dd-196">Namespace</span></span><br/>                | <span data-ttu-id="cc1dd-197">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="cc1dd-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cc1dd-198">MOF</span><span class="sxs-lookup"><span data-stu-id="cc1dd-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc1dd-199"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc1dd-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc1dd-200">DLL</span><span class="sxs-lookup"><span data-stu-id="cc1dd-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc1dd-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cc1dd-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cc1dd-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc1dd-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc1dd-203">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="cc1dd-203">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

