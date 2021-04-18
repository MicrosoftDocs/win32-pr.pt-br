---
description: Representa o ponto de extremidade de VLAN de uma porta de comutador.
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Classe Msvm_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5606e18fd1327f17feaac07570e5bf8c0c8eb59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750837"
---
# <a name="msvm_vlanendpoint-class"></a><span data-ttu-id="ece8b-103">\_Classe Msvm VLANEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece8b-103">Msvm\_VLANEndpoint class</span></span>

<span data-ttu-id="ece8b-104">Representa o ponto de extremidade de VLAN de uma porta de comutador.</span><span class="sxs-lookup"><span data-stu-id="ece8b-104">Represents the VLAN endpoint of a switch port.</span></span> <span data-ttu-id="ece8b-105">A configuração desse ponto de extremidade mudará a maneira como a porta do comutador envia pacotes de VLAN por meio do comutador.</span><span class="sxs-lookup"><span data-stu-id="ece8b-105">The configuration of this endpoint will change the way the switch port sends VLAN packets through the switch.</span></span>

<span data-ttu-id="ece8b-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ece8b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ece8b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ece8b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
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
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a><span data-ttu-id="ece8b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ece8b-108">Members</span></span>

<span data-ttu-id="ece8b-109">A classe **Msvm \_ VLANEndpoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ece8b-109">The **Msvm\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="ece8b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ece8b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ece8b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ece8b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ece8b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ece8b-112">Methods</span></span>

<span data-ttu-id="ece8b-113">A classe **Msvm \_ VLANEndpoint** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ece8b-113">The **Msvm\_VLANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="ece8b-114">Método</span><span class="sxs-lookup"><span data-stu-id="ece8b-114">Method</span></span>                                                             | <span data-ttu-id="ece8b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ece8b-115">Description</span></span>                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="ece8b-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ece8b-116">**RequestStateChange**</span></span>](msvm-vlanendpoint-requeststatechange.md) | <span data-ttu-id="ece8b-117">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="ece8b-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ece8b-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ece8b-118">Properties</span></span>

<span data-ttu-id="ece8b-119">A classe **Msvm \_ VLANEndpoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ece8b-119">The **Msvm\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ece8b-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="ece8b-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-121">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-123">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="ece8b-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="ece8b-124">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ece8b-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="ece8b-125">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="ece8b-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="ece8b-126">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="ece8b-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="ece8b-127">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ece8b-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="ece8b-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="ece8b-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="ece8b-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="ece8b-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="ece8b-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="ece8b-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="ece8b-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="ece8b-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="ece8b-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="ece8b-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="ece8b-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="ece8b-138">)</span><span class="sxs-lookup"><span data-stu-id="ece8b-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ece8b-139">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ece8b-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-140">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-142">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="ece8b-142">A short description of the object.</span></span> <span data-ttu-id="ece8b-143">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "ponto de extremidade de VLAN".</span><span class="sxs-lookup"><span data-stu-id="ece8b-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-144">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ece8b-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-145">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-147">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="ece8b-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ece8b-148">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="ece8b-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ece8b-149">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ece8b-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-150">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ece8b-150">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-151">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-153">O nome da classe ou da subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="ece8b-153">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="ece8b-154">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)e é sempre definida como "Msvm \_ VLANEndpoint".</span><span class="sxs-lookup"><span data-stu-id="ece8b-154">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VLANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-155">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ece8b-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-158">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="ece8b-158">A description of the object.</span></span> <span data-ttu-id="ece8b-159">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "Microsoft VLAN Endpoint".</span><span class="sxs-lookup"><span data-stu-id="ece8b-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-160">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="ece8b-160">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-162">Tipo de acesso: somente gravação</span><span class="sxs-lookup"><span data-stu-id="ece8b-162">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-163">O modo de VLAN desejado que é solicitado para uso.</span><span class="sxs-lookup"><span data-stu-id="ece8b-163">The desired VLAN mode that is requested for use.</span></span> <span data-ttu-id="ece8b-164">O modo atual é fornecido pela propriedade **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="ece8b-164">The current mode is given by the **OperationalEndpointMode** property.</span></span> <span data-ttu-id="ece8b-165">Essa propriedade é herdada do [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="ece8b-165">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="ece8b-166">Valor</span><span class="sxs-lookup"><span data-stu-id="ece8b-166">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="ece8b-167">Significado</span><span class="sxs-lookup"><span data-stu-id="ece8b-167">Meaning</span></span>                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="ece8b-168"><dt>**DMTF reservado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-168"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="ece8b-169"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-169"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="ece8b-170"><dt>**Acesso**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-170"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="ece8b-171">Coloca a porta do ponto de extremidade/comutador em modo de não entroncamento permanente e negocia para converter o link em um link de não tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-171">Puts the endpoint/switch port into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="ece8b-172">O ponto de extremidade se torna uma interface de não tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-172">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="ece8b-173"><dt>**Auto 3 dinâmicos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-173"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="ece8b-174">Torna o ponto de extremidade capaz de converter o link para um link de tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-174">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="ece8b-175">O ponto de extremidade se tornará uma interface de tronco se a interface vizinha estiver definida para o modo trunk ou desejável.</span><span class="sxs-lookup"><span data-stu-id="ece8b-175">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="ece8b-176"><dt>**Dinâmicos desejáveis**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-176"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="ece8b-177">Torna o ponto de extremidade uma tentativa ativa de converter o link para um link de tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-177">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="ece8b-178">O ponto de extremidade se tornará uma interface de tronco se a interface vizinha estiver definida para o modo Trunk, desejável ou auto.</span><span class="sxs-lookup"><span data-stu-id="ece8b-178">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="ece8b-179">O modo padrão de porta de comutador para todas as interfaces Ethernet é dinâmico, desejável.</span><span class="sxs-lookup"><span data-stu-id="ece8b-179">The default switch-port mode for all Ethernet interfaces is dynamic desirable.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="ece8b-180"><dt>**Tronco**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-180"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="ece8b-181">Coloca o ponto de extremidade no modo de entroncamento permanente e negocia para converter o link em um link de tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-181">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="ece8b-182">O ponto de extremidade se torna uma interface de tronco, mesmo se a interface vizinha não for uma interface de tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-182">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="ece8b-183"><dt>**Túnel Dot1Q**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-183"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="ece8b-184">Configura a interface como um ponto de extremidade/porta de túnel (sem tronco) a ser conectado em um link assimétrico com uma porta de tronco 802.1 Q.</span><span class="sxs-lookup"><span data-stu-id="ece8b-184">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="ece8b-185">o túnel 802.1 q é usado para manter a integridade da VLAN do cliente em uma rede do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="ece8b-185">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="ece8b-186"><dt>**DMTF reservado**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-186"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="ece8b-187"><dt> **Fornecedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-187"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="ece8b-188">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="ece8b-188">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-189">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-191">O tipo de encapsulamento de VLAN que é solicitado para uso.</span><span class="sxs-lookup"><span data-stu-id="ece8b-191">The type of VLAN encapsulation that is requested for use.</span></span> <span data-ttu-id="ece8b-192">O encapsulamento em uso no momento é fornecido pela propriedade **OperationalVLANTrunkEncapsulation** .</span><span class="sxs-lookup"><span data-stu-id="ece8b-192">The encapsulation currently in use is given by the **OperationalVLANTrunkEncapsulation** property.</span></span> <span data-ttu-id="ece8b-193">Essa propriedade só é aplicável quando o ponto de extremidade está operando em um modo de entroncamento (consulte a propriedade **OperationalEndpointMode** para obter detalhes adicionais).</span><span class="sxs-lookup"><span data-stu-id="ece8b-193">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="ece8b-194">Essa propriedade é 2 (não aplicável) (ou seja, o ponto de extremidade nunca será colocado em um modo de Entroncamento), um tipo específico (802.1 Q ou Cisco ISL) ou 5 (Negotiate) (ou seja, o resultado da negociação entre essa interface e seu vizinho).</span><span class="sxs-lookup"><span data-stu-id="ece8b-194">This property is either 2 (Not Applicable) (that is, the endpoint will never be placed in a trunking mode), a particular type (802.1Q or Cisco ISL), or 5 (Negotiate) (that is, the result of the negotiation between this interface and its neighbor).</span></span> <span data-ttu-id="ece8b-195">O valor 5 (Negotiate) não será permitido se o ponto de extremidade não oferecer suporte à negociação.</span><span class="sxs-lookup"><span data-stu-id="ece8b-195">The value, 5 (Negotiate) is not allowed if the endpoint does not support negotiation.</span></span> <span data-ttu-id="ece8b-196">Esse recurso é dependente de hardware e fornecedor.</span><span class="sxs-lookup"><span data-stu-id="ece8b-196">This capability is hardware and vendor dependent.</span></span> <span data-ttu-id="ece8b-197">Essa propriedade é herdada do [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="ece8b-197">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="ece8b-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="ece8b-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ece8b-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (2)</span><span class="sxs-lookup"><span data-stu-id="ece8b-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="ece8b-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="ece8b-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negociar** (5)</span><span class="sxs-lookup"><span data-stu-id="ece8b-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="ece8b-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="ece8b-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ece8b-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ece8b-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-207">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-209">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="ece8b-209">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ece8b-210">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="ece8b-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ece8b-211">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ece8b-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-212">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ece8b-212">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-213">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-215">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="ece8b-215">A display name for the object.</span></span> <span data-ttu-id="ece8b-216">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ece8b-216">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-217">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="ece8b-217">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-218">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-220">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="ece8b-220">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ece8b-221">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="ece8b-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ece8b-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-223">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-225">Os Estados habilitado e desabilitado deste elemento.</span><span class="sxs-lookup"><span data-stu-id="ece8b-225">The enabled and disabled states of this element.</span></span> <span data-ttu-id="ece8b-226">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="ece8b-226">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-227">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="ece8b-227">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-228">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-230">Indica se o GVRP (protocolo de registro de VLAN GARP) está habilitado ou desabilitado no ponto de extremidade/porta do tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-230">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint/port.</span></span> <span data-ttu-id="ece8b-231">Essa propriedade é 2 (não aplicável), a menos que GVRP seja suportado pelo ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ece8b-231">This property is 2 (Not Applicable) unless GVRP is supported by the endpoint.</span></span> <span data-ttu-id="ece8b-232">Essa propriedade é aplicável somente quando o ponto de extremidade está operando no modo de entroncamento (consulte a propriedade **OperationalEndpointMode** para obter detalhes adicionais).</span><span class="sxs-lookup"><span data-stu-id="ece8b-232">This property is applicable only when the endpoint is operating in trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="ece8b-233">Essa propriedade é herdada do [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="ece8b-233">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="ece8b-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="ece8b-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (2)</span><span class="sxs-lookup"><span data-stu-id="ece8b-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="ece8b-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="ece8b-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Disabled** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ece8b-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ece8b-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-239">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-241">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="ece8b-241">The current health of the element.</span></span> <span data-ttu-id="ece8b-242">Essa propriedade expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="ece8b-242">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="ece8b-243">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="ece8b-243">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="ece8b-244">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="ece8b-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-245">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ece8b-245">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-246">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ece8b-246">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-248">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="ece8b-248">The date and time when the object was installed.</span></span> <span data-ttu-id="ece8b-249">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ece8b-249">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-250">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ece8b-250">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-253">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="ece8b-253">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-254">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="ece8b-254">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ece8b-255">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ece8b-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-256">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ece8b-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-259">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="ece8b-259">The label by which the object is known.</span></span> <span data-ttu-id="ece8b-260">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ece8b-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-261">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="ece8b-261">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-262">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-262">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-264">A heurística de nomenclatura selecionada para garantir que o valor da propriedade **Name** seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ece8b-264">The naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="ece8b-265">Essa propriedade é herdada de [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ece8b-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ece8b-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-267">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-269">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="ece8b-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ece8b-270">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="ece8b-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ece8b-271">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ece8b-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-272">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="ece8b-272">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-273">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-275">O modo de configuração para o ponto de extremidade de VLAN.</span><span class="sxs-lookup"><span data-stu-id="ece8b-275">The configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="ece8b-276">Essa propriedade é herdada do [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="ece8b-276">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="ece8b-277">Valor</span><span class="sxs-lookup"><span data-stu-id="ece8b-277">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="ece8b-278">Significado</span><span class="sxs-lookup"><span data-stu-id="ece8b-278">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="ece8b-279"><dt>**DMTF reservado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-279"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="ece8b-280"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-280"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       | <span data-ttu-id="ece8b-281">O ponto de extremidade não reconhece VLAN.</span><span class="sxs-lookup"><span data-stu-id="ece8b-281">The endpoint is not VLAN aware.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="ece8b-282"><dt>**Acesso**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-282"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="ece8b-283">Coloca o ponto de extremidade em modo de não entroncamento permanente e negocia para converter o link em um link não tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-283">Puts the endpoint into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="ece8b-284">O ponto de extremidade se torna uma interface de não tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-284">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="ece8b-285"><dt>**Auto 3 dinâmicos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-285"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="ece8b-286">Torna o ponto de extremidade capaz de converter o link para um link de tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-286">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="ece8b-287">O ponto de extremidade se tornará uma interface de tronco se a interface vizinha estiver definida para o modo trunk ou desejável.</span><span class="sxs-lookup"><span data-stu-id="ece8b-287">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="ece8b-288"><dt>**Dinâmicos desejáveis**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-288"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="ece8b-289">Torna o ponto de extremidade uma tentativa ativa de converter o link para um link de tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-289">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="ece8b-290">O ponto de extremidade se tornará uma interface de tronco se a interface vizinha estiver definida para o modo Trunk, desejável ou auto.</span><span class="sxs-lookup"><span data-stu-id="ece8b-290">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="ece8b-291">Esse é o modo padrão de porta de comutador para todas as interfaces Ethernet.</span><span class="sxs-lookup"><span data-stu-id="ece8b-291">This is the default switch-port mode for all Ethernet interfaces.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="ece8b-292"><dt>**Tronco**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-292"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="ece8b-293">Coloca o ponto de extremidade no modo de entroncamento permanente e negocia para converter o link em um link de tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-293">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="ece8b-294">O ponto de extremidade se torna uma interface de tronco, mesmo se a interface vizinha não for uma interface de tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-294">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="ece8b-295"><dt>**Túnel Dot1Q**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-295"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="ece8b-296">Configura a interface como um ponto de extremidade/porta de túnel (sem tronco) a ser conectado em um link assimétrico com uma porta de tronco 802.1 Q.</span><span class="sxs-lookup"><span data-stu-id="ece8b-296">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="ece8b-297">o túnel 802.1 q é usado para manter a integridade da VLAN do cliente em uma rede do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="ece8b-297">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="ece8b-298"><dt>**DMTF reservado**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-298"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="ece8b-299"><dt> **Fornecedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-299"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="ece8b-300">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ece8b-300">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-301">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-301">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-303">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="ece8b-303">The current statuses of the object.</span></span> <span data-ttu-id="ece8b-304">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="ece8b-304">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-305">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="ece8b-305">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-306">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-308">O tipo de encapsulamento de VLAN em uso em um ponto de extremidade/porta de tronco.</span><span class="sxs-lookup"><span data-stu-id="ece8b-308">The type of VLAN encapsulation in use on a trunk endpoint/port.</span></span> <span data-ttu-id="ece8b-309">Essa propriedade é 2 (não aplicável) (ou seja, o ponto de extremidade não está operando no modo de Entroncamento), um tipo específico (3-802.1 Q ou 4-Cisco ISL), 5 (Negotiate) (ou seja, os pontos de extremidade estão negociando o tipo de encapsulamento).</span><span class="sxs-lookup"><span data-stu-id="ece8b-309">This property is either 2 (Not Applicable) (that is, the endpoint is not operating in trunking mode), a particular type (3 - 802.1Q or 4 - Cisco ISL), 5 (Negotiate) (that is, the endpoints are negotiating the encapsulation type).</span></span> <span data-ttu-id="ece8b-310">Essa propriedade só é aplicável quando o ponto de extremidade está operando em um modo de entroncamento (consulte a propriedade **OperationalEndpointMode** para obter detalhes adicionais).</span><span class="sxs-lookup"><span data-stu-id="ece8b-310">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="ece8b-311">Essa propriedade é herdada do [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="ece8b-311">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="ece8b-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="ece8b-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ece8b-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (2)</span><span class="sxs-lookup"><span data-stu-id="ece8b-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="ece8b-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="ece8b-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negociando** (5)</span><span class="sxs-lookup"><span data-stu-id="ece8b-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negotiating** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="ece8b-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="ece8b-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ece8b-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="ece8b-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-321">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-323">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="ece8b-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="ece8b-324">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="ece8b-324">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="ece8b-325">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ece8b-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-326">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="ece8b-326">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-327">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-329">O tipo de modelo de ponto de extremidade de VLAN com suporte por esse ponto de extremidade de VLAN, quando o valor da propriedade **OperationalEndpointMode** é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="ece8b-329">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the **OperationalEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="ece8b-330">Essa propriedade deve ser definida como **NULL** quando a propriedade **OperationalEndpointMode** é qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="ece8b-330">This property should be set to **Null** when the **OperationalEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="ece8b-331">Essa propriedade é herdada do [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="ece8b-331">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-332">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="ece8b-332">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-335">O tipo de encapsulamento de VLAN com suporte por esse ponto de extremidade de VLAN, quando o valor da propriedade **OperationalVLANTrunkEncapsulation** é definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="ece8b-335">The type of VLAN encapsulation that is supported by this VLAN endpoint, when the value of the **OperationalVLANTrunkEncapsulation** property is set to 1 (Other).</span></span> <span data-ttu-id="ece8b-336">Essa propriedade deve ser definida como **NULL** quando a propriedade de encapsulamento desejada for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="ece8b-336">This property should be set to **Null** when the desired encapsulation property is any value other than 1.</span></span> <span data-ttu-id="ece8b-337">Essa propriedade é herdada do [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="ece8b-337">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-338">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="ece8b-338">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-339">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-339">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-341">O tipo de ponto de extremidade de protocolo quando a propriedade **Type** dessa classe (ou de qualquer uma de suas subclasses) é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="ece8b-341">The type of protocol endpoint when the **Type** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="ece8b-342">Essa propriedade é herdada do [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)e é sempre definida como "virtual Ethernet".</span><span class="sxs-lookup"><span data-stu-id="ece8b-342">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ece8b-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-344">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-346">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="ece8b-346">Provides high level status information.</span></span> <span data-ttu-id="ece8b-347">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="ece8b-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="ece8b-348">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="ece8b-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ece8b-349">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ece8b-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-350">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="ece8b-350">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-351">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-353">A [MIB ifType da IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="ece8b-353">The [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="ece8b-354">Essa propriedade é herdada do [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)e é sempre definida como 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="ece8b-354">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-355">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="ece8b-355">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-356">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-358">Essa propriedade é herdada de [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ece8b-358">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-359">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ece8b-359">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-360">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-362">O último estado solicitado ou desejado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ece8b-362">The last requested or desired state for the management service.</span></span> <span data-ttu-id="ece8b-363">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="ece8b-363">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="ece8b-364">Valor</span><span class="sxs-lookup"><span data-stu-id="ece8b-364">Value</span></span>                                                                         | <span data-ttu-id="ece8b-365">Significado</span><span class="sxs-lookup"><span data-stu-id="ece8b-365">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="ece8b-366"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-366"><dt>12</dt></span></span> </dl> | <span data-ttu-id="ece8b-367">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="ece8b-367">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ece8b-368">**Status**</span><span class="sxs-lookup"><span data-stu-id="ece8b-368">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-369">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-371">Descreve o status do elemento.</span><span class="sxs-lookup"><span data-stu-id="ece8b-371">Describes the status of the element.</span></span> <span data-ttu-id="ece8b-372">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ece8b-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="ece8b-373">PROBLEMAS</span><span class="sxs-lookup"><span data-stu-id="ece8b-373">"OK"</span></span>

<span data-ttu-id="ece8b-374">Ao</span><span class="sxs-lookup"><span data-stu-id="ece8b-374">"Error"</span></span>

<span data-ttu-id="ece8b-375">Degradado</span><span class="sxs-lookup"><span data-stu-id="ece8b-375">"Degraded"</span></span>

<span data-ttu-id="ece8b-376">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="ece8b-376">"Unknown"</span></span>

<span data-ttu-id="ece8b-377">"Falha de Pred"</span><span class="sxs-lookup"><span data-stu-id="ece8b-377">"Pred Fail"</span></span>

<span data-ttu-id="ece8b-378">Comece</span><span class="sxs-lookup"><span data-stu-id="ece8b-378">"Starting"</span></span>

<span data-ttu-id="ece8b-379">Impedir</span><span class="sxs-lookup"><span data-stu-id="ece8b-379">"Stopping"</span></span>

<span data-ttu-id="ece8b-380">Serviço</span><span class="sxs-lookup"><span data-stu-id="ece8b-380">"Service"</span></span>

<span data-ttu-id="ece8b-381">Analisa</span><span class="sxs-lookup"><span data-stu-id="ece8b-381">"Stressed"</span></span>

<span data-ttu-id="ece8b-382">"Não recuperar"</span><span class="sxs-lookup"><span data-stu-id="ece8b-382">"NonRecover"</span></span>

<span data-ttu-id="ece8b-383">"Sem contato"</span><span class="sxs-lookup"><span data-stu-id="ece8b-383">"No Contact"</span></span>

<span data-ttu-id="ece8b-384">"Perda de comunicação"</span><span class="sxs-lookup"><span data-stu-id="ece8b-384">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-385">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ece8b-385">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-386">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-388">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ece8b-388">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ece8b-389">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="ece8b-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-390">**SupportedEndpointModes**</span><span class="sxs-lookup"><span data-stu-id="ece8b-390">**SupportedEndpointModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-391">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-393">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="ece8b-393">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-394">Os modos de ponto de extremidade com suporte nesta porta.</span><span class="sxs-lookup"><span data-stu-id="ece8b-394">The endpoint modes supported by this port.</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-395">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ece8b-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-396">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-398">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="ece8b-398">The creation class name of the scoping system.</span></span> <span data-ttu-id="ece8b-399">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)e é sempre definida como "Msvm \_ comutador virtual"</span><span class="sxs-lookup"><span data-stu-id="ece8b-399">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VirtualSwitch"</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-400">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ece8b-400">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-401">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ece8b-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-403">O nome do sistema do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="ece8b-403">The system name of the scoping system.</span></span> <span data-ttu-id="ece8b-404">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="ece8b-404">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-405">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="ece8b-405">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-406">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ece8b-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-408">A data e a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="ece8b-408">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ece8b-409">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é suportada.</span><span class="sxs-lookup"><span data-stu-id="ece8b-409">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ece8b-410">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="ece8b-410">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ece8b-411">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ece8b-411">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ece8b-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ece8b-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ece8b-413">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="ece8b-413">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ece8b-414">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="ece8b-414">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ece8b-415">Comentários</span><span class="sxs-lookup"><span data-stu-id="ece8b-415">Remarks</span></span>

<span data-ttu-id="ece8b-416">O acesso à classe **Msvm \_ VLANEndpoint** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="ece8b-416">Access to the **Msvm\_VLANEndpoint** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ece8b-417">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ece8b-417">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ece8b-418">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ece8b-418">Examples</span></span>

<span data-ttu-id="ece8b-419">Consulte [consultando objetos de rede](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ece8b-419">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ece8b-420">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ece8b-420">Requirements</span></span>



| <span data-ttu-id="ece8b-421">Requisito</span><span class="sxs-lookup"><span data-stu-id="ece8b-421">Requirement</span></span> | <span data-ttu-id="ece8b-422">Valor</span><span class="sxs-lookup"><span data-stu-id="ece8b-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece8b-423">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece8b-423">Minimum supported client</span></span><br/> | <span data-ttu-id="ece8b-424">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ece8b-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ece8b-425">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece8b-425">Minimum supported server</span></span><br/> | <span data-ttu-id="ece8b-426">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ece8b-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ece8b-427">Namespace</span><span class="sxs-lookup"><span data-stu-id="ece8b-427">Namespace</span></span><br/>                | <span data-ttu-id="ece8b-428">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ece8b-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ece8b-429">MOF</span><span class="sxs-lookup"><span data-stu-id="ece8b-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ece8b-430"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ece8b-431">DLL</span><span class="sxs-lookup"><span data-stu-id="ece8b-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ece8b-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ece8b-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ece8b-433">Confira também</span><span class="sxs-lookup"><span data-stu-id="ece8b-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece8b-434">**\_VLANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="ece8b-434">**CIM\_VLANEndpoint**</span></span>](cim-vlanendpoint.md)
</dt> <dt>

[<span data-ttu-id="ece8b-435">**\_VLANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="ece8b-435">**CIM\_VLANEndpoint**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

