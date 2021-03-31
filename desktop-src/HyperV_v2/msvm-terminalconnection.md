---
description: Indica o estado de uma sessão remota ativa que interage com uma máquina virtual.
ms.assetid: EAE6082F-A0CB-4E75-8029-51E20649C0A8
title: Classe Msvm_TerminalConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalConnection
- Msvm_TerminalConnection.InstanceID
- Msvm_TerminalConnection.Caption
- Msvm_TerminalConnection.Description
- Msvm_TerminalConnection.ElementName
- Msvm_TerminalConnection.InstallDate
- Msvm_TerminalConnection.Name
- Msvm_TerminalConnection.OperationalStatus
- Msvm_TerminalConnection.StatusDescriptions
- Msvm_TerminalConnection.Status
- Msvm_TerminalConnection.HealthState
- Msvm_TerminalConnection.CommunicationStatus
- Msvm_TerminalConnection.DetailedStatus
- Msvm_TerminalConnection.OperatingStatus
- Msvm_TerminalConnection.PrimaryStatus
- Msvm_TerminalConnection.EnabledState
- Msvm_TerminalConnection.OtherEnabledState
- Msvm_TerminalConnection.RequestedState
- Msvm_TerminalConnection.EnabledDefault
- Msvm_TerminalConnection.TimeOfLastStateChange
- Msvm_TerminalConnection.AvailableRequestedStates
- Msvm_TerminalConnection.TransitioningToState
- Msvm_TerminalConnection.ConnectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66be5000fb7fdd4404e07c87673e3359065af6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663006"
---
# <a name="msvm_terminalconnection-class"></a><span data-ttu-id="3230f-103">\_Classe Msvm TerminalConnection</span><span class="sxs-lookup"><span data-stu-id="3230f-103">Msvm\_TerminalConnection class</span></span>

<span data-ttu-id="3230f-104">Indica o estado de uma sessão remota ativa que interage com uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3230f-104">Indicates the state of an active remote session interacting with a virtual machine.</span></span> <span data-ttu-id="3230f-105">Só pode haver uma conexão por vez.</span><span class="sxs-lookup"><span data-stu-id="3230f-105">There can only be one connection at a time.</span></span>

<span data-ttu-id="3230f-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3230f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3230f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3230f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalConnection : CIM_EnabledLogicalElement
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
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   ConnectionID;
};
```

## <a name="members"></a><span data-ttu-id="3230f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3230f-108">Members</span></span>

<span data-ttu-id="3230f-109">A classe **Msvm \_ TerminalConnection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3230f-109">The **Msvm\_TerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="3230f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3230f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3230f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3230f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3230f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3230f-112">Methods</span></span>

<span data-ttu-id="3230f-113">A classe **Msvm \_ TerminalConnection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3230f-113">The **Msvm\_TerminalConnection** class has these methods.</span></span>



| <span data-ttu-id="3230f-114">Método</span><span class="sxs-lookup"><span data-stu-id="3230f-114">Method</span></span>                                                                   | <span data-ttu-id="3230f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="3230f-115">Description</span></span>                         |
|:-------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="3230f-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3230f-116">**RequestStateChange**</span></span>](msvm-terminalconnection-requeststatechange.md) | <span data-ttu-id="3230f-117">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="3230f-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3230f-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3230f-118">Properties</span></span>

<span data-ttu-id="3230f-119">A classe **Msvm \_ TerminalConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3230f-119">The **Msvm\_TerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3230f-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="3230f-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-121">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3230f-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-123">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="3230f-123">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="3230f-124">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3230f-124">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3230f-125">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="3230f-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3230f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-128">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="3230f-128">A short description of the object.</span></span> <span data-ttu-id="3230f-129">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3230f-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3230f-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-133">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="3230f-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3230f-134">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="3230f-134">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3230f-135">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-135">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3230f-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3230f-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="3230f-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="3230f-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="3230f-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="3230f-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3230f-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3230f-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3230f-143">)</span><span class="sxs-lookup"><span data-stu-id="3230f-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3230f-144">**ConnectionID**</span><span class="sxs-lookup"><span data-stu-id="3230f-144">**ConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3230f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3230f-147">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3230f-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3230f-148">O identificador exclusivo de uma instância do objeto de conexão de terminal.</span><span class="sxs-lookup"><span data-stu-id="3230f-148">The unique identifier for an instance of the terminal connection object.</span></span> <span data-ttu-id="3230f-149">O identificador é do formato "Microsoft:*VMID* \\ *index*".</span><span class="sxs-lookup"><span data-stu-id="3230f-149">The identifier is of the form "Microsoft:*VMID*\\*Index*".</span></span> <span data-ttu-id="3230f-150">Por exemplo, "Microsoft: 67A5D397-A02D-11DB-AC13-001676AA34F0 \\ 0".</span><span class="sxs-lookup"><span data-stu-id="3230f-150">For example, "Microsoft:67A5D397-A02D-11DB-AC13-001676AA34F0\\0".</span></span>

</dd> <dt>

<span data-ttu-id="3230f-151">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3230f-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3230f-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-154">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="3230f-154">A description of the object.</span></span> <span data-ttu-id="3230f-155">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3230f-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3230f-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-157">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-159">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="3230f-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3230f-160">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="3230f-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3230f-161">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3230f-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="3230f-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="3230f-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="3230f-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="3230f-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="3230f-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="3230f-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3230f-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3230f-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3230f-170">)</span><span class="sxs-lookup"><span data-stu-id="3230f-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3230f-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3230f-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3230f-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-174">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="3230f-174">A display name for the object.</span></span> <span data-ttu-id="3230f-175">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3230f-176">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="3230f-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-177">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-179">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="3230f-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="3230f-180">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3230f-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3230f-181">Valor</span><span class="sxs-lookup"><span data-stu-id="3230f-181">Value</span></span>                                                                        | <span data-ttu-id="3230f-182">Significado</span><span class="sxs-lookup"><span data-stu-id="3230f-182">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="3230f-183"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3230f-183"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3230f-184">habilitado</span><span class="sxs-lookup"><span data-stu-id="3230f-184">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="3230f-185"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3230f-185"><dt>3</dt></span></span> </dl> | <span data-ttu-id="3230f-186">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="3230f-186">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3230f-187">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3230f-187">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-188">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-190">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="3230f-190">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3230f-191">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="3230f-191">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="3230f-192">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3230f-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3230f-193">Valor</span><span class="sxs-lookup"><span data-stu-id="3230f-193">Value</span></span>                                                                        | <span data-ttu-id="3230f-194">Significado</span><span class="sxs-lookup"><span data-stu-id="3230f-194">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3230f-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3230f-195"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3230f-196">habilitado</span><span class="sxs-lookup"><span data-stu-id="3230f-196">Enabled</span></span><br/>        |
| <dl> <span data-ttu-id="3230f-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3230f-197"><dt>3</dt></span></span> </dl> | <span data-ttu-id="3230f-198">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="3230f-198">Disabled</span></span><br/>       |
| <dl> <span data-ttu-id="3230f-199"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3230f-199"><dt>5</dt></span></span> </dl> | <span data-ttu-id="3230f-200">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="3230f-200">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3230f-201">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3230f-201">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-202">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-204">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="3230f-204">The current health of the element.</span></span> <span data-ttu-id="3230f-205">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="3230f-205">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="3230f-206">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="3230f-206">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="3230f-207">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="3230f-207">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3230f-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3230f-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-209">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3230f-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-211">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="3230f-211">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="3230f-212">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3230f-213">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3230f-213">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3230f-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3230f-216">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="3230f-216">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3230f-217">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="3230f-217">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3230f-218">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3230f-219">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3230f-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3230f-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-222">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="3230f-222">The label by which the object is known.</span></span> <span data-ttu-id="3230f-223">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é a mesma que a propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="3230f-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="3230f-224">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3230f-224">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-225">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-227">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="3230f-227">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3230f-228">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="3230f-228">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3230f-229">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3230f-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3230f-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="3230f-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="3230f-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="3230f-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="3230f-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="3230f-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="3230f-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="3230f-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="3230f-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="3230f-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="3230f-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="3230f-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="3230f-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="3230f-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="3230f-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="3230f-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="3230f-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3230f-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3230f-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3230f-249">)</span><span class="sxs-lookup"><span data-stu-id="3230f-249">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3230f-250">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3230f-250">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-251">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-251">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3230f-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-253">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="3230f-253">The current statuses of the object.</span></span> <span data-ttu-id="3230f-254">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3230f-255">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="3230f-255">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-256">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3230f-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-258">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="3230f-258">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="3230f-259">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="3230f-259">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="3230f-260">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3230f-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3230f-261">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3230f-261">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-262">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-264">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="3230f-264">Provides high level status information.</span></span> <span data-ttu-id="3230f-265">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="3230f-265">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3230f-266">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="3230f-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3230f-267">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3230f-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3230f-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="3230f-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="3230f-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="3230f-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3230f-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3230f-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3230f-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3230f-274">)</span><span class="sxs-lookup"><span data-stu-id="3230f-274">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3230f-275">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3230f-275">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-276">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-278">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="3230f-278">The last requested or desired state for the element.</span></span> <span data-ttu-id="3230f-279">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="3230f-279">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="3230f-280">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="3230f-280">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="3230f-281">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte A **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="3230f-281">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="3230f-282">Se isso ocorrer, o valor 12 será usado.</span><span class="sxs-lookup"><span data-stu-id="3230f-282">If this occurs, the value 12 is used.</span></span> <span data-ttu-id="3230f-283">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="3230f-283">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>



| <span data-ttu-id="3230f-284">Valor</span><span class="sxs-lookup"><span data-stu-id="3230f-284">Value</span></span>                                                                         | <span data-ttu-id="3230f-285">Significado</span><span class="sxs-lookup"><span data-stu-id="3230f-285">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3230f-286"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3230f-286"><dt>12</dt></span></span> </dl> | <span data-ttu-id="3230f-287">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="3230f-287">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3230f-288">**Status**</span><span class="sxs-lookup"><span data-stu-id="3230f-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3230f-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-291">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3230f-291">The current status of the object.</span></span> <span data-ttu-id="3230f-292">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="3230f-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3230f-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3230f-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-294">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3230f-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3230f-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-296">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="3230f-296">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3230f-297">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3230f-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3230f-298">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3230f-298">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-299">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3230f-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-301">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="3230f-301">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3230f-302">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3230f-302">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3230f-303">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="3230f-303">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3230f-304">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3230f-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3230f-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3230f-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3230f-306">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="3230f-306">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3230f-307">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3230f-307">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3230f-308">Valor</span><span class="sxs-lookup"><span data-stu-id="3230f-308">Value</span></span>                                                                         | <span data-ttu-id="3230f-309">Significado</span><span class="sxs-lookup"><span data-stu-id="3230f-309">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3230f-310"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3230f-310"><dt>12</dt></span></span> </dl> | <span data-ttu-id="3230f-311">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="3230f-311">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3230f-312">Comentários</span><span class="sxs-lookup"><span data-stu-id="3230f-312">Remarks</span></span>

<span data-ttu-id="3230f-313">O acesso à classe **Msvm \_ TerminalConnection** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="3230f-313">Access to the **Msvm\_TerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3230f-314">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3230f-314">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3230f-315">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3230f-315">Requirements</span></span>



| <span data-ttu-id="3230f-316">Requisito</span><span class="sxs-lookup"><span data-stu-id="3230f-316">Requirement</span></span> | <span data-ttu-id="3230f-317">Valor</span><span class="sxs-lookup"><span data-stu-id="3230f-317">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3230f-318">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3230f-318">Minimum supported client</span></span><br/> | <span data-ttu-id="3230f-319">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3230f-319">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3230f-320">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3230f-320">Minimum supported server</span></span><br/> | <span data-ttu-id="3230f-321">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3230f-321">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3230f-322">Namespace</span><span class="sxs-lookup"><span data-stu-id="3230f-322">Namespace</span></span><br/>                | <span data-ttu-id="3230f-323">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3230f-323">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3230f-324">MOF</span><span class="sxs-lookup"><span data-stu-id="3230f-324">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3230f-325"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3230f-325"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3230f-326">DLL</span><span class="sxs-lookup"><span data-stu-id="3230f-326">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3230f-327"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3230f-327"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3230f-328">Confira também</span><span class="sxs-lookup"><span data-stu-id="3230f-328">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3230f-329">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3230f-329">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> <dt>

<span data-ttu-id="3230f-330">[**\_ENABLEDLOGICALELEMENT CIM**](/previous-versions//cc136818(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3230f-330">[**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3230f-331">Classes de vídeo</span><span class="sxs-lookup"><span data-stu-id="3230f-331">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

