---
description: Msvm \_ GuestService é a classe base abstrata para serviços no convidado que podem ser acessados do host.
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Classe Msvm_GuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370606"
---
# <a name="msvm_guestservice-class"></a><span data-ttu-id="8ea0d-103">\_Classe Msvm GuestService</span><span class="sxs-lookup"><span data-stu-id="8ea0d-103">Msvm\_GuestService class</span></span>

<span data-ttu-id="8ea0d-104">**Msvm \_ GuestService** é a classe base abstrata para serviços no convidado que podem ser acessados do host.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-104">**Msvm\_GuestService** is the abstract base class for services in the guest that can be accessed from the host.</span></span> <span data-ttu-id="8ea0d-105">Essa classe deriva da classe de [**\_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service) .</span><span class="sxs-lookup"><span data-stu-id="8ea0d-105">This class derives from the [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service) class.</span></span>

<span data-ttu-id="8ea0d-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea0d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ea0d-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="8ea0d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8ea0d-108">Members</span></span>

<span data-ttu-id="8ea0d-109">A classe **Msvm \_ GuestService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8ea0d-109">The **Msvm\_GuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="8ea0d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8ea0d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8ea0d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8ea0d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8ea0d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8ea0d-112">Methods</span></span>

<span data-ttu-id="8ea0d-113">A classe **Msvm \_ GuestService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-113">The **Msvm\_GuestService** class has these methods.</span></span>



| <span data-ttu-id="8ea0d-114">Método</span><span class="sxs-lookup"><span data-stu-id="8ea0d-114">Method</span></span>                                                             | <span data-ttu-id="8ea0d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ea0d-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ea0d-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestservice.md) | <span data-ttu-id="8ea0d-117">Solicita que o estado do serviço convidado seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-117">Requests that the state of the guest service be changed to the specified value.</span></span><br/> |
| [<span data-ttu-id="8ea0d-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-118">**StartService**</span></span>](startservice-msvm-guestservice.md)             | <span data-ttu-id="8ea0d-119">Coloca o serviço convidado em um estado iniciado.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-119">Puts the guest service in a started state.</span></span> <br/>                                     |
| [<span data-ttu-id="8ea0d-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-120">**StopService**</span></span>](stopservice-msvm-guestservice.md)               | <span data-ttu-id="8ea0d-121">Interrompe o serviço convidado.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-121">Stops the guest service.</span></span> <br/>                                                       |



 

### <a name="properties"></a><span data-ttu-id="8ea0d-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8ea0d-122">Properties</span></span>

<span data-ttu-id="8ea0d-123">A classe **Msvm \_ GuestService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-123">The **Msvm\_GuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ea0d-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-127">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-127">Short textual description of the object.</span></span> <span data-ttu-id="8ea0d-128">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ea0d-128">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-132">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-132">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8ea0d-133">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-133">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-137">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-137">Textual description of the object.</span></span> <span data-ttu-id="8ea0d-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ea0d-138">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-140">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-142">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-142">Date and time the object was installed.</span></span> <span data-ttu-id="8ea0d-143">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-143">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="8ea0d-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ea0d-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-145">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-148">Identificador exclusivo do serviço que também fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-148">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="8ea0d-149">Para obter mais informações sobre a funcionalidade, consulte a propriedade **Description** do objeto.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-149">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="8ea0d-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ea0d-150">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-151">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-151">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-152">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-154">Se **for true**, o serviço foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-154">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-155">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-155">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-158">Indica se o serviço é iniciado automaticamente (por exemplo, por um sistema operacional) ou iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-158">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="8ea0d-159">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8ea0d-159">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="8ea0d-160">**Automática**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-160">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="8ea0d-161">**Manual**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-161">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ea0d-162">**Status**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-162">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-165">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-165">Current status of the object.</span></span> <span data-ttu-id="8ea0d-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ea0d-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="8ea0d-167">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8ea0d-167">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="8ea0d-168">**PROBLEMAS**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-168">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="8ea0d-169">**Ao**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-169">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="8ea0d-170">**Degradado**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-170">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="8ea0d-171">**Conhecidos**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-171">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="8ea0d-172">**"Falha de Pred"**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-172">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="8ea0d-173">**Comece**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-173">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="8ea0d-174">**Impedir**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-174">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="8ea0d-175">**Serviço**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-175">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="8ea0d-176">**Analisa**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-176">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="8ea0d-177">**"Não recuperar"**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-177">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="8ea0d-178">**"Sem contato"**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-178">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="8ea0d-179">**"Perda de comunicação"**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-179">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ea0d-180">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-180">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-183">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-183">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="8ea0d-184">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-184">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea0d-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea0d-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ea0d-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea0d-187">Nome do sistema que hospeda o serviço.</span><span class="sxs-lookup"><span data-stu-id="8ea0d-187">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ea0d-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ea0d-188">Requirements</span></span>



| <span data-ttu-id="8ea0d-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea0d-189">Requirement</span></span> | <span data-ttu-id="8ea0d-190">Valor</span><span class="sxs-lookup"><span data-stu-id="8ea0d-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea0d-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ea0d-191">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea0d-192">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8ea0d-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8ea0d-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ea0d-193">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea0d-194">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="8ea0d-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8ea0d-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ea0d-195">Namespace</span></span><br/>                | <span data-ttu-id="8ea0d-196">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8ea0d-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8ea0d-197">MOF</span><span class="sxs-lookup"><span data-stu-id="8ea0d-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ea0d-198"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ea0d-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ea0d-199">DLL</span><span class="sxs-lookup"><span data-stu-id="8ea0d-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ea0d-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ea0d-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8ea0d-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ea0d-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea0d-202">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-202">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="8ea0d-203">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="8ea0d-203">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

