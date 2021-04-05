---
description: Serviço para criar, aplicar e destruir instantâneos de máquinas virtuais.
ms.assetid: 34efe124-d198-4bad-a3c9-e8457a5faa5e
title: Classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService
- Msvm_VirtualSystemSnapshotService.StartService
- Msvm_VirtualSystemSnapshotService.StopService
- Msvm_VirtualSystemSnapshotService.InstanceID
- Msvm_VirtualSystemSnapshotService.Caption
- Msvm_VirtualSystemSnapshotService.Description
- Msvm_VirtualSystemSnapshotService.ElementName
- Msvm_VirtualSystemSnapshotService.InstallDate
- Msvm_VirtualSystemSnapshotService.Name
- Msvm_VirtualSystemSnapshotService.OperationalStatus
- Msvm_VirtualSystemSnapshotService.StatusDescriptions
- Msvm_VirtualSystemSnapshotService.Status
- Msvm_VirtualSystemSnapshotService.HealthState
- Msvm_VirtualSystemSnapshotService.CommunicationStatus
- Msvm_VirtualSystemSnapshotService.DetailedStatus
- Msvm_VirtualSystemSnapshotService.OperatingStatus
- Msvm_VirtualSystemSnapshotService.PrimaryStatus
- Msvm_VirtualSystemSnapshotService.EnabledState
- Msvm_VirtualSystemSnapshotService.OtherEnabledState
- Msvm_VirtualSystemSnapshotService.RequestedState
- Msvm_VirtualSystemSnapshotService.EnabledDefault
- Msvm_VirtualSystemSnapshotService.TimeOfLastStateChange
- Msvm_VirtualSystemSnapshotService.AvailableRequestedStates
- Msvm_VirtualSystemSnapshotService.TransitioningToState
- Msvm_VirtualSystemSnapshotService.SystemCreationClassName
- Msvm_VirtualSystemSnapshotService.SystemName
- Msvm_VirtualSystemSnapshotService.CreationClassName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerContact
- Msvm_VirtualSystemSnapshotService.StartMode
- Msvm_VirtualSystemSnapshotService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be84d70dd9478012e747626a9a566464d7587789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826855"
---
# <a name="msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="1f845-103">\_Classe Msvm VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="1f845-103">Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="1f845-104">Serviço para criar, aplicar e destruir instantâneos de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="1f845-104">Service to create, apply, and destroy snapshots of virtual machines.</span></span>

<span data-ttu-id="1f845-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1f845-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f845-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f845-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSnapshotService : CIM_VirtualSystemSnapshotService
{
  string   InstanceID;
  string   Caption = "Hyper-V Virtual System Snapshot Service";
  string   Description = "Service for creating, destroying, and applying virtual machine snapshots";
  string   ElementName;
  datetime InstallDate;
  string   Name = "vssnapsvc";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemSnapshotService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="1f845-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1f845-107">Members</span></span>

<span data-ttu-id="1f845-108">A classe **Msvm \_ VirtualSystemSnapshotService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1f845-108">The **Msvm\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="1f845-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f845-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1f845-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f845-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1f845-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f845-111">Methods</span></span>

<span data-ttu-id="1f845-112">A classe **Msvm \_ VirtualSystemSnapshotService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1f845-112">The **Msvm\_VirtualSystemSnapshotService** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1f845-113">Método</span><span class="sxs-lookup"><span data-stu-id="1f845-113">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1f845-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f845-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1f845-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f845-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1f845-116">Aplica um instantâneo de máquina virtual à máquina virtual da qual ele foi criado.</span><span class="sxs-lookup"><span data-stu-id="1f845-116">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1f845-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f845-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1f845-118">Limpa o estado de salvamento de um instantâneo existente.</span><span class="sxs-lookup"><span data-stu-id="1f845-118">Clears save state from an existing snapshot.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1f845-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f845-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1f845-120">Converta um instantâneo do sistema virtual existente em um ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="1f845-120">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="1f845-121">O instantâneo é excluído como um efeito colateral.</span><span class="sxs-lookup"><span data-stu-id="1f845-121">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="1f845-122">Somente instantâneos de recuperação podem ser convertidos em pontos de referência.</span><span class="sxs-lookup"><span data-stu-id="1f845-122">Only recovery snapshots can be converted to reference points.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f845-123">O suporte para esse método foi adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1f845-123">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1f845-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f845-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1f845-125">Cria um instantâneo de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1f845-125">Creates a snapshot of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1f845-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f845-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1f845-127">Destruir um instantâneo de máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="1f845-127">Destroy an existing virtual machine snapshot.</span></span> <span data-ttu-id="1f845-128">Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.</span><span class="sxs-lookup"><span data-stu-id="1f845-128">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1f845-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f845-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1f845-130">Remove um instantâneo existente e todos os seus filhos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1f845-130">Removes an existing snapshot, and all its children, of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1f845-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f845-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1f845-132">Solicita uma alteração de estado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="1f845-132">Requests a state change for the element.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f845-133">O suporte para esse método foi adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1f845-133">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1f845-134"><strong>StartService</strong></span><span class="sxs-lookup"><span data-stu-id="1f845-134"><strong>StartService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1f845-135">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="1f845-135">This method is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1f845-136"><strong>StopService</strong></span><span class="sxs-lookup"><span data-stu-id="1f845-136"><strong>StopService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1f845-137">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="1f845-137">This method is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="1f845-138">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f845-138">Properties</span></span>

<span data-ttu-id="1f845-139">A classe **Msvm \_ VirtualSystemSnapshotService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1f845-139">The **Msvm\_VirtualSystemSnapshotService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f845-140">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="1f845-140">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-141">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1f845-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-143">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="1f845-143">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method used to initiate a state change.</span></span> <span data-ttu-id="1f845-144">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1f845-144">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="1f845-145">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="1f845-145">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="1f845-146">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="1f845-146">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="1f845-147">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f845-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="1f845-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="1f845-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1f845-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="1f845-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="1f845-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="1f845-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="1f845-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="1f845-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="1f845-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="1f845-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="1f845-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="1f845-158">)</span><span class="sxs-lookup"><span data-stu-id="1f845-158">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f845-159">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1f845-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-162">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1f845-162">A short description of the object.</span></span> <span data-ttu-id="1f845-163">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de instantâneo do sistema virtual do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="1f845-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Snapshot Service".</span></span>

</dd> <dt>

<span data-ttu-id="1f845-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1f845-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-167">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="1f845-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1f845-168">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1f845-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1f845-169">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f845-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1f845-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1f845-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="1f845-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="1f845-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="1f845-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="1f845-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1f845-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1f845-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1f845-177">)</span><span class="sxs-lookup"><span data-stu-id="1f845-177">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f845-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1f845-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f845-181">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1f845-181">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1f845-182">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1f845-182">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1f845-183">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ VirtualSystemSnapshotService".</span><span class="sxs-lookup"><span data-stu-id="1f845-183">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemSnapshotService".</span></span>

</dd> <dt>

<span data-ttu-id="1f845-184">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1f845-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-187">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="1f845-187">A description of the object.</span></span> <span data-ttu-id="1f845-188">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço para criar, destruir e aplicar instantâneos de máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="1f845-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, destroying, and applying virtual machine snapshots".</span></span>

</dd> <dt>

<span data-ttu-id="1f845-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1f845-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-190">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-192">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="1f845-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1f845-193">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1f845-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1f845-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f845-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1f845-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="1f845-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="1f845-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="1f845-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="1f845-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="1f845-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="1f845-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1f845-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1f845-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1f845-203">)</span><span class="sxs-lookup"><span data-stu-id="1f845-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f845-204">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1f845-204">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-207">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1f845-207">A display name for the object.</span></span> <span data-ttu-id="1f845-208">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1f845-208">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f845-209">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="1f845-209">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-210">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-212">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1f845-212">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="1f845-213">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="1f845-213">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="1f845-214">Valor</span><span class="sxs-lookup"><span data-stu-id="1f845-214">Value</span></span>                                                                        | <span data-ttu-id="1f845-215">Significado</span><span class="sxs-lookup"><span data-stu-id="1f845-215">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="1f845-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1f845-217">habilitado</span><span class="sxs-lookup"><span data-stu-id="1f845-217">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f845-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1f845-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-219">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-221">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1f845-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1f845-222">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="1f845-222">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="1f845-223">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="1f845-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="1f845-224">Valor</span><span class="sxs-lookup"><span data-stu-id="1f845-224">Value</span></span>                                                                        | <span data-ttu-id="1f845-225">Significado</span><span class="sxs-lookup"><span data-stu-id="1f845-225">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="1f845-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1f845-227">habilitado</span><span class="sxs-lookup"><span data-stu-id="1f845-227">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f845-228">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1f845-228">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-229">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-231">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="1f845-231">The current health of the element.</span></span> <span data-ttu-id="1f845-232">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="1f845-232">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1f845-233">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="1f845-233">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1f845-234">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="1f845-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="1f845-235">Valor</span><span class="sxs-lookup"><span data-stu-id="1f845-235">Value</span></span>                                                                        | <span data-ttu-id="1f845-236">Significado</span><span class="sxs-lookup"><span data-stu-id="1f845-236">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="1f845-237"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-237"><dt>5</dt></span></span> </dl> | <span data-ttu-id="1f845-238">O status de integridade é normal.</span><span class="sxs-lookup"><span data-stu-id="1f845-238">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f845-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1f845-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-240">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1f845-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-242">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="1f845-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="1f845-243">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f845-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f845-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1f845-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-245">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f845-247">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="1f845-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1f845-248">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="1f845-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1f845-249">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1f845-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f845-250">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1f845-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f845-253">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1f845-253">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1f845-254">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="1f845-254">The label by which the object is known.</span></span> <span data-ttu-id="1f845-255">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "vssnapsvc".</span><span class="sxs-lookup"><span data-stu-id="1f845-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vssnapsvc".</span></span>

</dd> <dt>

<span data-ttu-id="1f845-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1f845-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-257">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-259">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="1f845-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1f845-260">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1f845-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1f845-261">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f845-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1f845-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1f845-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="1f845-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="1f845-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="1f845-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="1f845-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="1f845-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="1f845-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="1f845-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="1f845-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="1f845-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="1f845-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="1f845-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="1f845-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="1f845-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="1f845-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="1f845-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="1f845-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1f845-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1f845-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1f845-281">)</span><span class="sxs-lookup"><span data-stu-id="1f845-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f845-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1f845-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-283">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1f845-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-285">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="1f845-285">The current statuses of the object.</span></span> <span data-ttu-id="1f845-286">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="1f845-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="1f845-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="1f845-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-290">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="1f845-290">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1f845-291">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="1f845-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1f845-292">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f845-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f845-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="1f845-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f845-296">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1f845-296">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1f845-297">Todas as informações sobre como o proprietário principal do serviço podem ser atingidas (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="1f845-297">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="1f845-298">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="1f845-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f845-299">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="1f845-299">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f845-302">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1f845-302">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1f845-303">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="1f845-303">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="1f845-304">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="1f845-304">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="1f845-305">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="1f845-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f845-306">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1f845-306">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-307">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-309">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="1f845-309">Provides high level status information.</span></span> <span data-ttu-id="1f845-310">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="1f845-310">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1f845-311">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1f845-311">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1f845-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f845-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1f845-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1f845-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="1f845-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="1f845-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="1f845-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1f845-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1f845-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1f845-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1f845-319">)</span><span class="sxs-lookup"><span data-stu-id="1f845-319">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f845-320">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1f845-320">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-321">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-323">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="1f845-323">The last requested or desired state for the element.</span></span> <span data-ttu-id="1f845-324">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="1f845-324">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="1f845-325">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais para um elemento.</span><span class="sxs-lookup"><span data-stu-id="1f845-325">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="1f845-326">Uma instância específica da classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não oferecer suporte à propriedade **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="1f845-326">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="1f845-327">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="1f845-327">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="1f845-328">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="1f845-328">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="1f845-329">Valor</span><span class="sxs-lookup"><span data-stu-id="1f845-329">Value</span></span>                                                                         | <span data-ttu-id="1f845-330">Significado</span><span class="sxs-lookup"><span data-stu-id="1f845-330">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="1f845-331"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-331"><dt>12</dt></span></span> </dl> | <span data-ttu-id="1f845-332">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="1f845-332">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f845-333">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="1f845-333">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-334">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1f845-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-336">Indica se o serviço está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="1f845-336">Indicates whether the service is currently running.</span></span> <span data-ttu-id="1f845-337">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="1f845-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1f845-338">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="1f845-338">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-339">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f845-341">Qualificadores: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="1f845-341">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="1f845-342">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="1f845-342">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="1f845-343">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="1f845-343">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f845-344">**Status**</span><span class="sxs-lookup"><span data-stu-id="1f845-344">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-347">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f845-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f845-348">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1f845-348">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-349">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1f845-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-351">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="1f845-351">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1f845-352">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), e cada elemento da matriz é sempre definido como "o serviço está sendo executado normalmente".</span><span class="sxs-lookup"><span data-stu-id="1f845-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="1f845-353">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1f845-353">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-354">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f845-356">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1f845-356">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1f845-357">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1f845-357">The scoping system's creation class name.</span></span> <span data-ttu-id="1f845-358">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="1f845-358">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="1f845-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1f845-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f845-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f845-362">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1f845-362">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1f845-363">O nome NetBIOS do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="1f845-363">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="1f845-364">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1f845-364">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1f845-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="1f845-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-366">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1f845-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-368">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="1f845-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1f845-369">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f845-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1f845-370">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="1f845-370">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f845-371">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f845-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f845-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f845-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f845-373">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="1f845-373">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1f845-374">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f845-374">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1f845-375">Valor</span><span class="sxs-lookup"><span data-stu-id="1f845-375">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="1f845-376">Significado</span><span class="sxs-lookup"><span data-stu-id="1f845-376">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="1f845-377"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="1f845-377"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="1f845-378"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-378"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="1f845-379"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-379"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="1f845-380"><dt>**Desligar**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-380"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="1f845-381"><dt>**Nenhuma alteração**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-381"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="1f845-382">Nenhuma transição em andamento.</span><span class="sxs-lookup"><span data-stu-id="1f845-382">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="1f845-383"><dt>**Offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-383"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="1f845-384"><dt>**Teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-384"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="1f845-385"><dt>**Adiar**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-385"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="1f845-386"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-386"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="1f845-387"><dt>**Reinicializar**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-387"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="1f845-388"><dt>**Redefinir**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-388"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="1f845-389"><dt>**Não aplicável**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-389"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="1f845-390">A implementação não dá suporte à representação de transições em andamento.</span><span class="sxs-lookup"><span data-stu-id="1f845-390">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="1f845-391"><dt> **DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-391"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f845-392">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f845-392">Requirements</span></span>



| <span data-ttu-id="1f845-393">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f845-393">Requirement</span></span> | <span data-ttu-id="1f845-394">Valor</span><span class="sxs-lookup"><span data-stu-id="1f845-394">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f845-395">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f845-395">Minimum supported client</span></span><br/> | <span data-ttu-id="1f845-396">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1f845-396">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1f845-397">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f845-397">Minimum supported server</span></span><br/> | <span data-ttu-id="1f845-398">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1f845-398">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f845-399">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f845-399">Namespace</span></span><br/>                | <span data-ttu-id="1f845-400">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1f845-400">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1f845-401">MOF</span><span class="sxs-lookup"><span data-stu-id="1f845-401">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f845-402"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-402"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f845-403">DLL</span><span class="sxs-lookup"><span data-stu-id="1f845-403">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f845-404"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f845-404"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

