---
description: Representa o ponto de conexão lógica para um adaptador de rede. Quando o ponto de extremidade da LAN está conectado a uma porta de comutador, o adaptador de rede conectado ao ponto de extremidade da LAN tem conectividade de rede.
ms.assetid: 68aad05e-64b5-44dc-ab5b-8f3051fa77ca
title: Classe Msvm_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LANEndpoint
- Msvm_LANEndpoint.InstanceID
- Msvm_LANEndpoint.Caption
- Msvm_LANEndpoint.Description
- Msvm_LANEndpoint.ElementName
- Msvm_LANEndpoint.InstallDate
- Msvm_LANEndpoint.Name
- Msvm_LANEndpoint.OperationalStatus
- Msvm_LANEndpoint.StatusDescriptions
- Msvm_LANEndpoint.Status
- Msvm_LANEndpoint.HealthState
- Msvm_LANEndpoint.CommunicationStatus
- Msvm_LANEndpoint.DetailedStatus
- Msvm_LANEndpoint.OperatingStatus
- Msvm_LANEndpoint.PrimaryStatus
- Msvm_LANEndpoint.EnabledState
- Msvm_LANEndpoint.OtherEnabledState
- Msvm_LANEndpoint.RequestedState
- Msvm_LANEndpoint.EnabledDefault
- Msvm_LANEndpoint.TimeOfLastStateChange
- Msvm_LANEndpoint.AvailableRequestedStates
- Msvm_LANEndpoint.TransitioningToState
- Msvm_LANEndpoint.SystemCreationClassName
- Msvm_LANEndpoint.SystemName
- Msvm_LANEndpoint.CreationClassName
- Msvm_LANEndpoint.NameFormat
- Msvm_LANEndpoint.ProtocolType
- Msvm_LANEndpoint.ProtocolIFType
- Msvm_LANEndpoint.OtherTypeDescription
- Msvm_LANEndpoint.LANID
- Msvm_LANEndpoint.LANType
- Msvm_LANEndpoint.OtherLANType
- Msvm_LANEndpoint.MACAddress
- Msvm_LANEndpoint.AliasAddresses
- Msvm_LANEndpoint.GroupAddresses
- Msvm_LANEndpoint.MaxDataSize
- Msvm_LANEndpoint.Connected
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7585b92461b435b99a05ed198c4c501e10703439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169735"
---
# <a name="msvm_lanendpoint-class"></a><span data-ttu-id="8d549-104">\_Classe Msvm LANEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d549-104">Msvm\_LANEndpoint class</span></span>

<span data-ttu-id="8d549-105">Representa o ponto de conexão lógica para um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="8d549-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="8d549-106">Quando o ponto de extremidade da LAN está conectado a uma porta de comutador, o adaptador de rede conectado ao ponto de extremidade da LAN tem conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="8d549-106">When the LAN endpoint is connected to a switch port, the network adapter connected to the LAN endpoint has network connectivity.</span></span>

<span data-ttu-id="8d549-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8d549-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d549-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d549-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LANEndpoint : CIM_LANEndpoint
{
  string   InstanceID;
  string   Caption = "LAN Endpoint";
  string   Description = "Microsoft Virtual LAN Endpoint";
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
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_LANEndpoint";
  string   NameFormat = "Microsoft Virtual Device ID";
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
};
```

## <a name="members"></a><span data-ttu-id="8d549-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8d549-109">Members</span></span>

<span data-ttu-id="8d549-110">A classe **Msvm \_ LANEndpoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8d549-110">The **Msvm\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="8d549-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8d549-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8d549-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8d549-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8d549-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8d549-113">Methods</span></span>

<span data-ttu-id="8d549-114">A classe **Msvm \_ LANEndpoint** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8d549-114">The **Msvm\_LANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="8d549-115">Método</span><span class="sxs-lookup"><span data-stu-id="8d549-115">Method</span></span>                                                            | <span data-ttu-id="8d549-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d549-116">Description</span></span>                         |
|:------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="8d549-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8d549-117">**RequestStateChange**</span></span>](msvm-lanendpoint-requeststatechange.md) | <span data-ttu-id="8d549-118">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="8d549-118">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8d549-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8d549-119">Properties</span></span>

<span data-ttu-id="8d549-120">A classe **Msvm \_ LANEndpoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8d549-120">The **Msvm\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d549-121">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="8d549-121">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-122">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d549-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-124">Outros endereços unicast que podem ser usados para se comunicar com o ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="8d549-124">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="8d549-125">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d549-125">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-126">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8d549-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-127">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8d549-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-129">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="8d549-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="8d549-130">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d549-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="8d549-131">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="8d549-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="8d549-132">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="8d549-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="8d549-133">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d549-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8d549-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8d549-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8d549-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="8d549-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="8d549-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="8d549-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="8d549-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="8d549-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="8d549-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="8d549-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="8d549-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="8d549-144">)</span><span class="sxs-lookup"><span data-stu-id="8d549-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8d549-145">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8d549-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-148">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8d549-148">A short description of the object.</span></span> <span data-ttu-id="8d549-149">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "ponto de extremidade de LAN".</span><span class="sxs-lookup"><span data-stu-id="8d549-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "LAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="8d549-150">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8d549-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-153">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="8d549-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8d549-154">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="8d549-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8d549-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8d549-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-156">**Conectado**</span><span class="sxs-lookup"><span data-stu-id="8d549-156">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-157">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8d549-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-159">Essa propriedade será definida como **true** se o ponto de extremidade de LAN estiver conectado a uma porta de comutador.</span><span class="sxs-lookup"><span data-stu-id="8d549-159">This property is set to **True** if the LAN endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="8d549-160">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8d549-160">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d549-163">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="8d549-163">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="8d549-164">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="8d549-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8d549-165">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)e é sempre definida como "Msvm \_ LANEndpoint".</span><span class="sxs-lookup"><span data-stu-id="8d549-165">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_LANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="8d549-166">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8d549-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-169">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="8d549-169">A description of the object.</span></span> <span data-ttu-id="8d549-170">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "ponto de extremidade de LAN virtual da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8d549-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual LAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="8d549-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8d549-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-172">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-174">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="8d549-174">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8d549-175">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="8d549-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8d549-176">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8d549-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8d549-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-180">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="8d549-180">A display name for the object.</span></span> <span data-ttu-id="8d549-181">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8d549-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-182">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8d549-182">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-183">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-185">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="8d549-185">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8d549-186">Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8d549-186">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8d549-187"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8d549-187"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-188"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8d549-188"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-189"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="8d549-189"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8d549-190">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8d549-190">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-191">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-193">Especifica o estado habilitado do sistema planejado.</span><span class="sxs-lookup"><span data-stu-id="8d549-193">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="8d549-194">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8d549-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="8d549-195">Valor</span><span class="sxs-lookup"><span data-stu-id="8d549-195">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="8d549-196">Significado</span><span class="sxs-lookup"><span data-stu-id="8d549-196">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="8d549-197"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8d549-197"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="8d549-198">O sistema está desligado.</span><span class="sxs-lookup"><span data-stu-id="8d549-198">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="8d549-199"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8d549-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="8d549-200">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8d549-200">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="8d549-201"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8d549-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="8d549-202">O sistema está habilitado, mas offline.</span><span class="sxs-lookup"><span data-stu-id="8d549-202">The system is enabled, but offline.</span></span> <span data-ttu-id="8d549-203">Todas as novas solicitações serão descartadas.</span><span class="sxs-lookup"><span data-stu-id="8d549-203">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8d549-204">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="8d549-204">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-205">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-205">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d549-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-207">Endereços multicast para os quais o ponto de extremidade de LAN escuta.</span><span class="sxs-lookup"><span data-stu-id="8d549-207">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="8d549-208">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d549-208">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-209">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8d549-209">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-210">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-212">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="8d549-212">The current health of the element.</span></span> <span data-ttu-id="8d549-213">Essa propriedade expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="8d549-213">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8d549-214">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="8d549-214">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8d549-215">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="8d549-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="8d549-216">Valor</span><span class="sxs-lookup"><span data-stu-id="8d549-216">Value</span></span>                                                                        | <span data-ttu-id="8d549-217">Significado</span><span class="sxs-lookup"><span data-stu-id="8d549-217">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="8d549-218"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8d549-218"><dt>5</dt></span></span> </dl> | <span data-ttu-id="8d549-219">O status de integridade é normal.</span><span class="sxs-lookup"><span data-stu-id="8d549-219">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8d549-220">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8d549-220">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-221">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8d549-221">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-223">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="8d549-223">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="8d549-224">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8d549-224">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-225">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8d549-225">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-226">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d549-228">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="8d549-228">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8d549-229">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="8d549-229">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8d549-230">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8d549-230">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-231">**LANID**</span><span class="sxs-lookup"><span data-stu-id="8d549-231">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-234">Um rótulo ou identificador para o segmento de LAN ao qual o ponto de extremidade está conectado.</span><span class="sxs-lookup"><span data-stu-id="8d549-234">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="8d549-235">Se o ponto de extremidade não estiver ativo/conectado no momento ou se essas informações não forem conhecidas, essa propriedade será **nula**.</span><span class="sxs-lookup"><span data-stu-id="8d549-235">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="8d549-236">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d549-236">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-237">**LANType**</span><span class="sxs-lookup"><span data-stu-id="8d549-237">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-238">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-240">Essa propriedade é preterida no lugar da propriedade **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="8d549-240">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="8d549-241">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d549-241">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-242">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="8d549-242">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d549-245">Qualificadores: **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="8d549-245">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="8d549-246">O endereço MAC usado na comunicação com o ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="8d549-246">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="8d549-247">O endereço MAC é formatado como doze dígitos hexadecimais (por exemplo, "010203040506"), com cada par representando um dos seis octetos do endereço MAC na ordem de bits canônica de acordo com a RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="8d549-247">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="8d549-248">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d549-248">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-249">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="8d549-249">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-250">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d549-250">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d549-252">Qualificadores: **unidades** ("bits")</span><span class="sxs-lookup"><span data-stu-id="8d549-252">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="8d549-253">O maior tamanho, em número de bits, do campo de informações que pode ser enviado ou recebido pelo ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="8d549-253">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="8d549-254">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d549-254">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-255">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8d549-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-256">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-258">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="8d549-258">The label by which the object is known.</span></span> <span data-ttu-id="8d549-259">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8d549-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-260">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="8d549-260">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d549-263">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="8d549-263">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="8d549-264">Contém a heurística de nomenclatura selecionada para garantir que o valor da propriedade **Name** seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8d549-264">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="8d549-265">Essa propriedade é herdada de [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)e é definida como "ID do dispositivo virtual da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="8d549-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is set to "Microsoft Virtual Device ID".</span></span>

</dd> <dt>

<span data-ttu-id="8d549-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8d549-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-267">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-269">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="8d549-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8d549-270">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="8d549-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8d549-271">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8d549-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8d549-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-273">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8d549-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-275">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="8d549-275">The current statuses of the object.</span></span> <span data-ttu-id="8d549-276">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="8d549-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-277">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8d549-277">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-280">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="8d549-280">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="8d549-281">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="8d549-281">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8d549-282">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8d549-282">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8d549-283">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="8d549-283">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-286">Essa propriedade é preterida no lugar da propriedade **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="8d549-286">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="8d549-287">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8d549-287">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-288">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="8d549-288">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d549-291">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="8d549-291">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="8d549-292">Uma cadeia de caracteres que descreve o tipo de ponto de extremidade de protocolo quando a propriedade **ProtocolIFType** dessa classe (ou de qualquer uma de suas subclasses) é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="8d549-292">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="8d549-293">Essa propriedade deve ser definida como **NULL** quando a propriedade **ProtocolIFType** é qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="8d549-293">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="8d549-294">Essa propriedade é herdada do [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="8d549-294">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-295">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8d549-295">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-296">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-296">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-298">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="8d549-298">Provides high level status information.</span></span> <span data-ttu-id="8d549-299">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="8d549-299">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="8d549-300">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="8d549-300">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8d549-301">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8d549-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-302">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="8d549-302">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-303">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-305">A propriedade é usada para categorizar e classificar instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="8d549-305">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="8d549-306">Se **ProtocolIFType** for definido como 1 (outro), as informações de tipo deverão ser fornecidas na propriedade **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="8d549-306">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="8d549-307">Essa propriedade é herdada do [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="8d549-307">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="8d549-308">**ProtocolIFType** é uma enumeração que é sincronizada com a [MIB ifType da IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="8d549-308">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="8d549-309">Os valores adicionais definidos pela DMTF também estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="8d549-309">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="8d549-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8d549-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-311"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8d549-311"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-312"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)</span><span class="sxs-lookup"><span data-stu-id="8d549-312"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-313"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span><span class="sxs-lookup"><span data-stu-id="8d549-313"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-314"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X. 25** (4)</span><span class="sxs-lookup"><span data-stu-id="8d549-314"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X.25** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-315"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5)</span><span class="sxs-lookup"><span data-stu-id="8d549-315"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X.25** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-316"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**CSMA/CD de Ethernet** (6)</span><span class="sxs-lookup"><span data-stu-id="8d549-316"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-317"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**CSMA/CD ISO 802,3** (7)</span><span class="sxs-lookup"><span data-stu-id="8d549-317"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-318"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**Barramento de token ISO 802,4** (8)</span><span class="sxs-lookup"><span data-stu-id="8d549-318"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 Token Bus** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-319"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**Token ring ISO 802,5** (9)</span><span class="sxs-lookup"><span data-stu-id="8d549-319"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 Token Ring** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-320"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802,6 Man** (10)</span><span class="sxs-lookup"><span data-stu-id="8d549-320"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-321"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span><span class="sxs-lookup"><span data-stu-id="8d549-321"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-322"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span><span class="sxs-lookup"><span data-stu-id="8d549-322"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-323"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span><span class="sxs-lookup"><span data-stu-id="8d549-323"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-324"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**Hiperchannel** (14)</span><span class="sxs-lookup"><span data-stu-id="8d549-324"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-325"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span><span class="sxs-lookup"><span data-stu-id="8d549-325"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-326"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span><span class="sxs-lookup"><span data-stu-id="8d549-326"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-327"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span><span class="sxs-lookup"><span data-stu-id="8d549-327"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-328"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span><span class="sxs-lookup"><span data-stu-id="8d549-328"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-329"><span id="E1"></span><span id="e1"></span>**E1** (19)</span><span class="sxs-lookup"><span data-stu-id="8d549-329"><span id="E1"></span><span id="e1"></span>**E1** (19)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-330"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**ISDN básico** (20)</span><span class="sxs-lookup"><span data-stu-id="8d549-330"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Basic ISDN** (20)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-331"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**ISDN primário** (21)</span><span class="sxs-lookup"><span data-stu-id="8d549-331"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primary ISDN** (21)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-332"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Serial ponto a ponto proprietário** (22)</span><span class="sxs-lookup"><span data-stu-id="8d549-332"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietary Point-to-Point Serial** (22)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-333"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span><span class="sxs-lookup"><span data-stu-id="8d549-333"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-334"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Auto-retorno de software** (24)</span><span class="sxs-lookup"><span data-stu-id="8d549-334"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software Loopback** (24)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-335"><span id="EON"></span><span id="eon"></span>**EON** (25)</span><span class="sxs-lookup"><span data-stu-id="8d549-335"><span id="EON"></span><span id="eon"></span>**EON** (25)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-336"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**3Mbit Ethernet** (26)</span><span class="sxs-lookup"><span data-stu-id="8d549-336"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-337"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span><span class="sxs-lookup"><span data-stu-id="8d549-337"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-338"><span id="SLIP"></span><span id="slip"></span>**Guia** (28)</span><span class="sxs-lookup"><span data-stu-id="8d549-338"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-339"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span><span class="sxs-lookup"><span data-stu-id="8d549-339"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-340"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span><span class="sxs-lookup"><span data-stu-id="8d549-340"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-341"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span><span class="sxs-lookup"><span data-stu-id="8d549-341"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-342"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span><span class="sxs-lookup"><span data-stu-id="8d549-342"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-343"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span><span class="sxs-lookup"><span data-stu-id="8d549-343"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-344"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Paralelo** (34)</span><span class="sxs-lookup"><span data-stu-id="8d549-344"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-345"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span><span class="sxs-lookup"><span data-stu-id="8d549-345"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-346"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span><span class="sxs-lookup"><span data-stu-id="8d549-346"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-347"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span><span class="sxs-lookup"><span data-stu-id="8d549-347"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-348"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**Mio X. 25** (38)</span><span class="sxs-lookup"><span data-stu-id="8d549-348"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**MIO X.25** (38)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-349"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span><span class="sxs-lookup"><span data-stu-id="8d549-349"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-350"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X. 25 PLE** (40)</span><span class="sxs-lookup"><span data-stu-id="8d549-350"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X.25 PLE** (40)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-351"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211 c** (41)</span><span class="sxs-lookup"><span data-stu-id="8d549-351"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211c** (41)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-352"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span><span class="sxs-lookup"><span data-stu-id="8d549-352"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-353"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXi** (43)</span><span class="sxs-lookup"><span data-stu-id="8d549-353"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-354"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Serviço de Frame Relay** (44)</span><span class="sxs-lookup"><span data-stu-id="8d549-354"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay Service** (44)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-355"><span id="V.35"></span><span id="v.35"></span>**V. 35** (45)</span><span class="sxs-lookup"><span data-stu-id="8d549-355"><span id="V.35"></span><span id="v.35"></span>**V.35** (45)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-356"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span><span class="sxs-lookup"><span data-stu-id="8d549-356"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-357"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span><span class="sxs-lookup"><span data-stu-id="8d549-357"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-358"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span><span class="sxs-lookup"><span data-stu-id="8d549-358"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-359"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span><span class="sxs-lookup"><span data-stu-id="8d549-359"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-360"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**Caminho de SONET** (50)</span><span class="sxs-lookup"><span data-stu-id="8d549-360"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET Path** (50)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-361"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span><span class="sxs-lookup"><span data-stu-id="8d549-361"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-362"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span><span class="sxs-lookup"><span data-stu-id="8d549-362"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-363"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Virtual/interna proprietária** (53)</span><span class="sxs-lookup"><span data-stu-id="8d549-363"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietary Virtual/Internal** (53)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-364"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Multiplexador proprietário** (54)</span><span class="sxs-lookup"><span data-stu-id="8d549-364"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietary Multiplexor** (54)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-365"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802,12** (55)</span><span class="sxs-lookup"><span data-stu-id="8d549-365"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-366"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span><span class="sxs-lookup"><span data-stu-id="8d549-366"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-367"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**Interface HIPPI** (57)</span><span class="sxs-lookup"><span data-stu-id="8d549-367"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI Interface** (57)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-368"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Interconexão de Frame Relay** (58)</span><span class="sxs-lookup"><span data-stu-id="8d549-368"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay Interconnect** (58)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-369"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**LAN emulada ATM para 802,3** (59)</span><span class="sxs-lookup"><span data-stu-id="8d549-369"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM Emulated LAN for 802.3** (59)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-370"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**LAN emulada ATM para 802,5** (60)</span><span class="sxs-lookup"><span data-stu-id="8d549-370"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM Emulated LAN for 802.5** (60)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-371"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**Circuito emulado ATM** (61)</span><span class="sxs-lookup"><span data-stu-id="8d549-371"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM Emulated Circuit** (61)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-372"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span><span class="sxs-lookup"><span data-stu-id="8d549-372"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-373"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span><span class="sxs-lookup"><span data-stu-id="8d549-373"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-374"><span id="V.11"></span><span id="v.11"></span>**V. 11** (64)</span><span class="sxs-lookup"><span data-stu-id="8d549-374"><span id="V.11"></span><span id="v.11"></span>**V.11** (64)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-375"><span id="V.36"></span><span id="v.36"></span>**V. 36** (65)</span><span class="sxs-lookup"><span data-stu-id="8d549-375"><span id="V.36"></span><span id="v.36"></span>**V.36** (65)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-376"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 em 64K** (66)</span><span class="sxs-lookup"><span data-stu-id="8d549-376"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 at 64K** (66)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-377"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 em 2 MB** (67)</span><span class="sxs-lookup"><span data-stu-id="8d549-377"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 at 2Mb** (67)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-378"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span><span class="sxs-lookup"><span data-stu-id="8d549-378"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-379"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span><span class="sxs-lookup"><span data-stu-id="8d549-379"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-380"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Canal** (70)</span><span class="sxs-lookup"><span data-stu-id="8d549-380"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-381"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="8d549-381"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-382"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**Canal IBM 260/370 OEMI** (72)</span><span class="sxs-lookup"><span data-stu-id="8d549-382"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-383"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span><span class="sxs-lookup"><span data-stu-id="8d549-383"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-384"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Alternância de link de dados** (74)</span><span class="sxs-lookup"><span data-stu-id="8d549-384"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Data Link Switching** (74)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-385"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**Interface ISDN S/T** (75)</span><span class="sxs-lookup"><span data-stu-id="8d549-385"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T Interface** (75)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-386"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**Interface ISDN U** (76)</span><span class="sxs-lookup"><span data-stu-id="8d549-386"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U Interface** (76)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-387"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span><span class="sxs-lookup"><span data-stu-id="8d549-387"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-388"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**Opção de IP** (78)</span><span class="sxs-lookup"><span data-stu-id="8d549-388"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP Switch** (78)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-389"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Ponte de rota de origem remota** (79)</span><span class="sxs-lookup"><span data-stu-id="8d549-389"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote Source Route Bridging** (79)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-390"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM lógico** (80)</span><span class="sxs-lookup"><span data-stu-id="8d549-390"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-391"><span id="DS0"></span><span id="ds0"></span>**Ds0** (81)</span><span class="sxs-lookup"><span data-stu-id="8d549-391"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-392"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**Pacote ds0** (82)</span><span class="sxs-lookup"><span data-stu-id="8d549-392"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-393"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span><span class="sxs-lookup"><span data-stu-id="8d549-393"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-394"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span><span class="sxs-lookup"><span data-stu-id="8d549-394"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-395"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat net radio** (85)</span><span class="sxs-lookup"><span data-stu-id="8d549-395"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat Net Radio** (85)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-396"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**DTR r 802.5 ISO** (86)</span><span class="sxs-lookup"><span data-stu-id="8d549-396"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5r DTR** (86)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-397"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Sistema de relatório Loc do PDV de extensão** (87)</span><span class="sxs-lookup"><span data-stu-id="8d549-397"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc Report System** (87)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-398"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**Protocolo de acesso remoto AppleTalk** (88)</span><span class="sxs-lookup"><span data-stu-id="8d549-398"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk Remote Access Protocol** (88)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-399"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>Sem **conexão proprietária** (89)</span><span class="sxs-lookup"><span data-stu-id="8d549-399"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietary Connectionless** (89)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-400"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**Painel de host ITU X. 29** (90)</span><span class="sxs-lookup"><span data-stu-id="8d549-400"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X.29 Host PAD** (90)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-401"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X. 3 terminal pad** (91)</span><span class="sxs-lookup"><span data-stu-id="8d549-401"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X.3 Terminal PAD** (91)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-402"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**MPI de Frame Relay** (92)</span><span class="sxs-lookup"><span data-stu-id="8d549-402"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-403"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X. 213** (93)</span><span class="sxs-lookup"><span data-stu-id="8d549-403"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X.213** (93)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-404"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span><span class="sxs-lookup"><span data-stu-id="8d549-404"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-405"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span><span class="sxs-lookup"><span data-stu-id="8d549-405"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-406"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span><span class="sxs-lookup"><span data-stu-id="8d549-406"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-407"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span><span class="sxs-lookup"><span data-stu-id="8d549-407"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-408"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802,5 CRFP** (98)</span><span class="sxs-lookup"><span data-stu-id="8d549-408"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-409"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span><span class="sxs-lookup"><span data-stu-id="8d549-409"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-410"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Recebimento e transmissão de voz** (100)</span><span class="sxs-lookup"><span data-stu-id="8d549-410"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Voice Receive and Transmit** (100)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-411"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Escritório de troca de voz estrangeira** (101)</span><span class="sxs-lookup"><span data-stu-id="8d549-411"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Voice Foreign Exchange Office** (101)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-412"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Serviço de troca de voz estrangeira** (102)</span><span class="sxs-lookup"><span data-stu-id="8d549-412"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Voice Foreign Exchange Service** (102)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-413"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Encapsulamento de voz** (103)</span><span class="sxs-lookup"><span data-stu-id="8d549-413"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Voice Encapsulation** (103)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-414"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voz sobre IP** (104)</span><span class="sxs-lookup"><span data-stu-id="8d549-414"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-415"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**DXi ATM** (105)</span><span class="sxs-lookup"><span data-stu-id="8d549-415"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-416"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**FUNI ATM** (106)</span><span class="sxs-lookup"><span data-stu-id="8d549-416"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-417"><span id="ATM_IMA"></span><span id="atm_ima"></span>**IMA ATM** (107)</span><span class="sxs-lookup"><span data-stu-id="8d549-417"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-418"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**Pacote PPP Multilink** (108)</span><span class="sxs-lookup"><span data-stu-id="8d549-418"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP Multilink Bundle** (108)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-419"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP sobre CDLC** (109)</span><span class="sxs-lookup"><span data-stu-id="8d549-419"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP over CDLC** (109)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-420"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP sobre Claw** (110)</span><span class="sxs-lookup"><span data-stu-id="8d549-420"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over CLAW** (110)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-421"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Pilha para pilha** (111)</span><span class="sxs-lookup"><span data-stu-id="8d549-421"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack to Stack** (111)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-422"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Endereço IP virtual** (112)</span><span class="sxs-lookup"><span data-stu-id="8d549-422"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtual IP Address** (112)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-423"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span><span class="sxs-lookup"><span data-stu-id="8d549-423"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-424"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP sobre ATM** (114)</span><span class="sxs-lookup"><span data-stu-id="8d549-424"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP over ATM** (114)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-425"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**Anel de Fibre token do ISO 802.5 j** (115)</span><span class="sxs-lookup"><span data-stu-id="8d549-425"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5j Fibre Token Ring** (115)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-426"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span><span class="sxs-lookup"><span data-stu-id="8d549-426"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-427"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span><span class="sxs-lookup"><span data-stu-id="8d549-427"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-428"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span><span class="sxs-lookup"><span data-stu-id="8d549-428"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-429"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span><span class="sxs-lookup"><span data-stu-id="8d549-429"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-430"><span id="V.37"></span><span id="v.37"></span>**V. 37** (120)</span><span class="sxs-lookup"><span data-stu-id="8d549-430"><span id="V.37"></span><span id="v.37"></span>**V.37** (120)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-431"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X. 25 MLP** (121)</span><span class="sxs-lookup"><span data-stu-id="8d549-431"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X.25 MLP** (121)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-432"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**Grupo de busca X. 25** (122)</span><span class="sxs-lookup"><span data-stu-id="8d549-432"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X.25 Hunt Group** (122)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-433"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span><span class="sxs-lookup"><span data-stu-id="8d549-433"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-434"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Intercalar canal** (124)</span><span class="sxs-lookup"><span data-stu-id="8d549-434"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave Channel** (124)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-435"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**Canal rápido** (125)</span><span class="sxs-lookup"><span data-stu-id="8d549-435"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-436"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (para APPN HPR em redes IP)** (126)</span><span class="sxs-lookup"><span data-stu-id="8d549-436"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (for APPN HPR in IP Networks)** (126)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-437"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**Camada Mac CATV** (127)</span><span class="sxs-lookup"><span data-stu-id="8d549-437"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC Layer** (127)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-438"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV downstream** (128)</span><span class="sxs-lookup"><span data-stu-id="8d549-438"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV Downstream** (128)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-439"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV upstream** (129)</span><span class="sxs-lookup"><span data-stu-id="8d549-439"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV Upstream** (129)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-440"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Opção Avalon 12MPP** (130)</span><span class="sxs-lookup"><span data-stu-id="8d549-440"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Avalon 12MPP Switch** (130)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-441"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Túnel** (131)</span><span class="sxs-lookup"><span data-stu-id="8d549-441"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-442"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Café** (132)</span><span class="sxs-lookup"><span data-stu-id="8d549-442"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Coffee** (132)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-443"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Serviço de emulação de circuito** (133)</span><span class="sxs-lookup"><span data-stu-id="8d549-443"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation Service** (133)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-444"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**Subinterface ATM** (134)</span><span class="sxs-lookup"><span data-stu-id="8d549-444"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM SubInterface** (134)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-445"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**VLAN de camada 2 usando 802.1 q** (135)</span><span class="sxs-lookup"><span data-stu-id="8d549-445"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2 VLAN using 802.1Q** (135)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-446"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**VLAN de camada 3 usando IP** (136)</span><span class="sxs-lookup"><span data-stu-id="8d549-446"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3 VLAN using IP** (136)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-447"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**VLAN de camada 3 usando IPX** (137)</span><span class="sxs-lookup"><span data-stu-id="8d549-447"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3 VLAN using IPX** (137)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-448"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Linha de alimentação digital** (138)</span><span class="sxs-lookup"><span data-stu-id="8d549-448"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digital Power Line** (138)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-449"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Email multimídia sobre IP** (139)</span><span class="sxs-lookup"><span data-stu-id="8d549-449"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia Mail over IP** (139)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-450"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span><span class="sxs-lookup"><span data-stu-id="8d549-450"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-451"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span><span class="sxs-lookup"><span data-stu-id="8d549-451"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-452"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**Encaminhamento de IP** (142)</span><span class="sxs-lookup"><span data-stu-id="8d549-452"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP Forwarding** (142)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-453"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span><span class="sxs-lookup"><span data-stu-id="8d549-453"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-454"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span><span class="sxs-lookup"><span data-stu-id="8d549-454"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-455"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**If-GSN/HIPPI-6400** (145)</span><span class="sxs-lookup"><span data-stu-id="8d549-455"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-456"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**Camada Mac de RCC de DVB** (146)</span><span class="sxs-lookup"><span data-stu-id="8d549-456"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**DVB-RCC MAC Layer** (146)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-457"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC downstream** (147)</span><span class="sxs-lookup"><span data-stu-id="8d549-457"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC Downstream** (147)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-458"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC upstream** (148)</span><span class="sxs-lookup"><span data-stu-id="8d549-458"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC Upstream** (148)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-459"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM virtual** (149)</span><span class="sxs-lookup"><span data-stu-id="8d549-459"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM Virtual** (149)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-460"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**Túnel MPLS** (150)</span><span class="sxs-lookup"><span data-stu-id="8d549-460"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS Tunnel** (150)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-461"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span><span class="sxs-lookup"><span data-stu-id="8d549-461"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-462"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voz sobre ATM** (152)</span><span class="sxs-lookup"><span data-stu-id="8d549-462"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-463"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Retransmissão de quadros de voz sobre** (153)</span><span class="sxs-lookup"><span data-stu-id="8d549-463"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-464"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span><span class="sxs-lookup"><span data-stu-id="8d549-464"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-465"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Link composto** (155)</span><span class="sxs-lookup"><span data-stu-id="8d549-465"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Composite Link** (155)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-466"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**Link de sinalização do SS7** (156)</span><span class="sxs-lookup"><span data-stu-id="8d549-466"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signaling Link** (156)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-467"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Sem fio P2P proprietário** (157)</span><span class="sxs-lookup"><span data-stu-id="8d549-467"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietary P2P Wireless** (157)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-468"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Encaminhar quadro** (158)</span><span class="sxs-lookup"><span data-stu-id="8d549-468"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame Forward** (158)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-469"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 multiprotocolo sobre ATM** (159)</span><span class="sxs-lookup"><span data-stu-id="8d549-469"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol over ATM** (159)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-470"><span id="USB"></span><span id="usb"></span>**USB** (160)</span><span class="sxs-lookup"><span data-stu-id="8d549-470"><span id="USB"></span><span id="usb"></span>**USB** (160)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-471"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**Agregação de link do AD 802.3 IEEE** (161)</span><span class="sxs-lookup"><span data-stu-id="8d549-471"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3ad Link Aggregate** (161)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-472"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**Contabilização de política BGP** (162)</span><span class="sxs-lookup"><span data-stu-id="8d549-472"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP Policy Accounting** (162)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-473"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**Multilink fr .16 do FRF** (163)</span><span class="sxs-lookup"><span data-stu-id="8d549-473"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink FR** (163)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-474"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**Gatekeeper H. 323** (164)</span><span class="sxs-lookup"><span data-stu-id="8d549-474"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H.323 Gatekeeper** (164)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-475"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**Proxy H. 323** (165)</span><span class="sxs-lookup"><span data-stu-id="8d549-475"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H.323 Proxy** (165)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-476"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span><span class="sxs-lookup"><span data-stu-id="8d549-476"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-477"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Link de sinalização de várias frequências** (167)</span><span class="sxs-lookup"><span data-stu-id="8d549-477"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Multi-Frequency Signaling Link** (167)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-478"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span><span class="sxs-lookup"><span data-stu-id="8d549-478"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-479"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span><span class="sxs-lookup"><span data-stu-id="8d549-479"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-480"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**Link de dados de recursos do DS1** (170)</span><span class="sxs-lookup"><span data-stu-id="8d549-480"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 Facility Data Link** (170)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-481"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Pacote sobre SONET/SDH** (171)</span><span class="sxs-lookup"><span data-stu-id="8d549-481"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-482"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**Entrada de DVB-ASI** (172)</span><span class="sxs-lookup"><span data-stu-id="8d549-482"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**DVB-ASI Input** (172)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-483"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**Saída de DVB-ASI** (173)</span><span class="sxs-lookup"><span data-stu-id="8d549-483"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**DVB-ASI Output** (173)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-484"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Linha de alimentação** (174)</span><span class="sxs-lookup"><span data-stu-id="8d549-484"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Power Line** (174)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-485"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Sinalização associada ao não recurso** (175)</span><span class="sxs-lookup"><span data-stu-id="8d549-485"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Non Facility Associated Signaling** (175)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-486"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span><span class="sxs-lookup"><span data-stu-id="8d549-486"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-487"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span><span class="sxs-lookup"><span data-stu-id="8d549-487"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-488"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span><span class="sxs-lookup"><span data-stu-id="8d549-488"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-489"><span id="ISUP"></span><span id="isup"></span>**IsUp** (179)</span><span class="sxs-lookup"><span data-stu-id="8d549-489"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-490"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Camada Mac sem fio proprietária** (180)</span><span class="sxs-lookup"><span data-stu-id="8d549-490"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietary Wireless MAC Layer** (180)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-491"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Downstream sem fio patenteado** (181)</span><span class="sxs-lookup"><span data-stu-id="8d549-491"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietary Wireless Downstream** (181)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-492"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Upstream sem fio patenteado** (182)</span><span class="sxs-lookup"><span data-stu-id="8d549-492"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietary Wireless Upstream** (182)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-493"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN tipo 2** (183)</span><span class="sxs-lookup"><span data-stu-id="8d549-493"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN Type 2** (183)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-494"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Ponto de acesso sem fio de banda larga proprietária para MultiPoint** (184)</span><span class="sxs-lookup"><span data-stu-id="8d549-494"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Proprietary Broadband Wireless Access Point to Multipoint** (184)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-495"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**Canal de sobrecarga de SONET** (185)</span><span class="sxs-lookup"><span data-stu-id="8d549-495"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET Overhead Channel** (185)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-496"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Canal de sobrecarga de wrapper digital** (186)</span><span class="sxs-lookup"><span data-stu-id="8d549-496"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Digital Wrapper Overhead Channel** (186)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-497"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**Camada de adaptação ATM 2** (187)</span><span class="sxs-lookup"><span data-stu-id="8d549-497"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM Adaptation Layer 2** (187)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-498"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Mac de rádio** (188)</span><span class="sxs-lookup"><span data-stu-id="8d549-498"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio MAC** (188)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-499"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**Rádio ATM** (189)</span><span class="sxs-lookup"><span data-stu-id="8d549-499"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-500"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Tronco entre máquinas** (190)</span><span class="sxs-lookup"><span data-stu-id="8d549-500"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Inter Machine Trunk** (190)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-501"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span><span class="sxs-lookup"><span data-stu-id="8d549-501"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-502"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**DSL de leitura longa** (192)</span><span class="sxs-lookup"><span data-stu-id="8d549-502"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long Read DSL** (192)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-503"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Ponto de extremidade DLCI de Frame Relay** (193)</span><span class="sxs-lookup"><span data-stu-id="8d549-503"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Frame Relay DLCI Endpoint** (193)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-504"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**Ponto de extremidade VCI ATM** (194)</span><span class="sxs-lookup"><span data-stu-id="8d549-504"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI Endpoint** (194)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-505"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Canal óptico** (195)</span><span class="sxs-lookup"><span data-stu-id="8d549-505"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optical Channel** (195)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-506"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Transporte óptico** (196)</span><span class="sxs-lookup"><span data-stu-id="8d549-506"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optical Transport** (196)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-507"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**ATM proprietário** (197)</span><span class="sxs-lookup"><span data-stu-id="8d549-507"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietary ATM** (197)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-508"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Cabo de voz sobre** (198)</span><span class="sxs-lookup"><span data-stu-id="8d549-508"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice over Cable** (198)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-509"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**InfiniBand** (199)</span><span class="sxs-lookup"><span data-stu-id="8d549-509"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**Infiniband** (199)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-510"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**Link de te** (200)</span><span class="sxs-lookup"><span data-stu-id="8d549-510"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**TE Link** (200)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-511"><span id="Q.2931"></span><span id="q.2931"></span>**P. 2931** (201)</span><span class="sxs-lookup"><span data-stu-id="8d549-511"><span id="Q.2931"></span><span id="q.2931"></span>**Q.2931** (201)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-512"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Grupo de troncos virtuais** (202)</span><span class="sxs-lookup"><span data-stu-id="8d549-512"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtual Trunk Group** (202)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-513"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**Grupo de troncos SIP** (203)</span><span class="sxs-lookup"><span data-stu-id="8d549-513"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP Trunk Group** (203)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-514"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**Sinalização de SIP** (204)</span><span class="sxs-lookup"><span data-stu-id="8d549-514"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP Signaling** (204)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-515"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**Canal de upstream do CATV** (205)</span><span class="sxs-lookup"><span data-stu-id="8d549-515"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV Upstream Channel** (205)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-516"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span><span class="sxs-lookup"><span data-stu-id="8d549-516"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-517"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**Fsan 155MB Pon** (207)</span><span class="sxs-lookup"><span data-stu-id="8d549-517"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155Mb PON** (207)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-518"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**Fsan 622MB Pon** (208)</span><span class="sxs-lookup"><span data-stu-id="8d549-518"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622Mb PON** (208)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-519"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Ponte transparente** (209)</span><span class="sxs-lookup"><span data-stu-id="8d549-519"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparent Bridge** (209)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-520"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Grupo de linhas** (210)</span><span class="sxs-lookup"><span data-stu-id="8d549-520"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Line Group** (210)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-521"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Grupo de recursos de & de voz** (211)</span><span class="sxs-lookup"><span data-stu-id="8d549-521"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Voice & Feature Group** (211)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-522"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**EANA de FGD de voz** (212)</span><span class="sxs-lookup"><span data-stu-id="8d549-522"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-523"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voz did** (213)</span><span class="sxs-lookup"><span data-stu-id="8d549-523"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice DID** (213)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-524"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**Transporte MPEG** (214)</span><span class="sxs-lookup"><span data-stu-id="8d549-524"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG Transport** (214)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-525"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215)</span><span class="sxs-lookup"><span data-stu-id="8d549-525"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6To4** (215)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-526"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span><span class="sxs-lookup"><span data-stu-id="8d549-526"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-527"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span><span class="sxs-lookup"><span data-stu-id="8d549-527"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-528"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span><span class="sxs-lookup"><span data-stu-id="8d549-528"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-529"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Grupo de canais ópticos** (219)</span><span class="sxs-lookup"><span data-stu-id="8d549-529"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optical Channel Group** (219)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-530"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span><span class="sxs-lookup"><span data-stu-id="8d549-530"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-531"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span><span class="sxs-lookup"><span data-stu-id="8d549-531"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-532"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span><span class="sxs-lookup"><span data-stu-id="8d549-532"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-533"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span><span class="sxs-lookup"><span data-stu-id="8d549-533"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-534"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**FCIP** (224)</span><span class="sxs-lookup"><span data-stu-id="8d549-534"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-535"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA reservado** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="8d549-535"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-536"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="8d549-536"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-537"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="8d549-537"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-538"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="8d549-538"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-539"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span><span class="sxs-lookup"><span data-stu-id="8d549-539"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-540"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span><span class="sxs-lookup"><span data-stu-id="8d549-540"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-541"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span><span class="sxs-lookup"><span data-stu-id="8d549-541"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-542"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span><span class="sxs-lookup"><span data-stu-id="8d549-542"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-543"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span><span class="sxs-lookup"><span data-stu-id="8d549-543"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-544"><span id="VINES"></span><span id="vines"></span>**Vines** (4104)</span><span class="sxs-lookup"><span data-stu-id="8d549-544"><span id="VINES"></span><span id="vines"></span>**VINES** (4104)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-545"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span><span class="sxs-lookup"><span data-stu-id="8d549-545"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-546"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**Ponto de extremidade do canal do ISDN B** (4106)</span><span class="sxs-lookup"><span data-stu-id="8d549-546"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B Channel Endpoint** (4106)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-547"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**Ponto de extremidade do canal ISDN D** (4107)</span><span class="sxs-lookup"><span data-stu-id="8d549-547"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN D Channel Endpoint** (4107)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-548"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span><span class="sxs-lookup"><span data-stu-id="8d549-548"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-549"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span><span class="sxs-lookup"><span data-stu-id="8d549-549"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-550"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span><span class="sxs-lookup"><span data-stu-id="8d549-550"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-551"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span><span class="sxs-lookup"><span data-stu-id="8d549-551"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-552"><span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112)</span><span class="sxs-lookup"><span data-stu-id="8d549-552"><span id="802.11a"></span><span id="802.11A"></span>**802.11a** (4112)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-553"><span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113)</span><span class="sxs-lookup"><span data-stu-id="8d549-553"><span id="802.11b"></span><span id="802.11B"></span>**802.11b** (4113)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-554"><span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114)</span><span class="sxs-lookup"><span data-stu-id="8d549-554"><span id="802.11g"></span><span id="802.11G"></span>**802.11g** (4114)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-555"><span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115)</span><span class="sxs-lookup"><span data-stu-id="8d549-555"><span id="802.11h"></span><span id="802.11H"></span>**802.11h** (4115)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-556"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span><span class="sxs-lookup"><span data-stu-id="8d549-556"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-557"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span><span class="sxs-lookup"><span data-stu-id="8d549-557"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-558"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span><span class="sxs-lookup"><span data-stu-id="8d549-558"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-559"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span><span class="sxs-lookup"><span data-stu-id="8d549-559"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-560"><span id="HTTP"></span><span id="http"></span>**Http** (4204)</span><span class="sxs-lookup"><span data-stu-id="8d549-560"><span id="HTTP"></span><span id="http"></span>**HTTP** (4204)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-561"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span><span class="sxs-lookup"><span data-stu-id="8d549-561"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-562"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span><span class="sxs-lookup"><span data-stu-id="8d549-562"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-563"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span><span class="sxs-lookup"><span data-stu-id="8d549-563"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-564"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span><span class="sxs-lookup"><span data-stu-id="8d549-564"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-565"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span><span class="sxs-lookup"><span data-stu-id="8d549-565"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-566"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span><span class="sxs-lookup"><span data-stu-id="8d549-566"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-567"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span><span class="sxs-lookup"><span data-stu-id="8d549-567"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-568"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span><span class="sxs-lookup"><span data-stu-id="8d549-568"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-569"><span id="HTTPS"></span><span id="https"></span>**Https** (4406)</span><span class="sxs-lookup"><span data-stu-id="8d549-569"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-570"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8d549-570"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8d549-571"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (32768..</span><span class="sxs-lookup"><span data-stu-id="8d549-571"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="8d549-572">)</span><span class="sxs-lookup"><span data-stu-id="8d549-572">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8d549-573">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="8d549-573">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-574">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-574">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-575">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-575">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-576">Essa propriedade é preterida no lugar da propriedade **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="8d549-576">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="8d549-577">Essa propriedade é herdada do [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="8d549-577">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-578">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8d549-578">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-579">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-579">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-580">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-580">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-581">O último estado solicitado ou desejado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="8d549-581">The last requested or desired state for the management service.</span></span> <span data-ttu-id="8d549-582">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="8d549-582">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="8d549-583">Valor</span><span class="sxs-lookup"><span data-stu-id="8d549-583">Value</span></span>                                                                         | <span data-ttu-id="8d549-584">Significado</span><span class="sxs-lookup"><span data-stu-id="8d549-584">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="8d549-585"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="8d549-585"><dt>12</dt></span></span> </dl> | <span data-ttu-id="8d549-586">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="8d549-586">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8d549-587">**Status**</span><span class="sxs-lookup"><span data-stu-id="8d549-587">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-588">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-589">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-589">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-590">Descreve o status do elemento.</span><span class="sxs-lookup"><span data-stu-id="8d549-590">Describes the status of the element.</span></span> <span data-ttu-id="8d549-591">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8d549-591">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="8d549-592">PROBLEMAS</span><span class="sxs-lookup"><span data-stu-id="8d549-592">"OK"</span></span>

<span data-ttu-id="8d549-593">Ao</span><span class="sxs-lookup"><span data-stu-id="8d549-593">"Error"</span></span>

<span data-ttu-id="8d549-594">Degradado</span><span class="sxs-lookup"><span data-stu-id="8d549-594">"Degraded"</span></span>

<span data-ttu-id="8d549-595">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="8d549-595">"Unknown"</span></span>

<span data-ttu-id="8d549-596">"Falha de Pred"</span><span class="sxs-lookup"><span data-stu-id="8d549-596">"Pred Fail"</span></span>

<span data-ttu-id="8d549-597">Comece</span><span class="sxs-lookup"><span data-stu-id="8d549-597">"Starting"</span></span>

<span data-ttu-id="8d549-598">Impedir</span><span class="sxs-lookup"><span data-stu-id="8d549-598">"Stopping"</span></span>

<span data-ttu-id="8d549-599">Serviço</span><span class="sxs-lookup"><span data-stu-id="8d549-599">"Service"</span></span>

<span data-ttu-id="8d549-600">Analisa</span><span class="sxs-lookup"><span data-stu-id="8d549-600">"Stressed"</span></span>

<span data-ttu-id="8d549-601">"Não recuperar"</span><span class="sxs-lookup"><span data-stu-id="8d549-601">"NonRecover"</span></span>

<span data-ttu-id="8d549-602">"Sem contato"</span><span class="sxs-lookup"><span data-stu-id="8d549-602">"No Contact"</span></span>

<span data-ttu-id="8d549-603">"Perda de comunicação"</span><span class="sxs-lookup"><span data-stu-id="8d549-603">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="8d549-604">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8d549-604">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-605">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-605">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8d549-606">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-607">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8d549-607">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8d549-608">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="8d549-608">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="8d549-609">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8d549-609">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-610">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-611">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-612">O nome da classe de criação do sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="8d549-612">The hosting system's creation class name.</span></span> <span data-ttu-id="8d549-613">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="8d549-613">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-614">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8d549-614">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-615">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8d549-615">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-616">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-616">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d549-617">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="8d549-617">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="8d549-618">O nome do sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="8d549-618">The name of the hosting system.</span></span> <span data-ttu-id="8d549-619">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="8d549-619">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="8d549-620">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8d549-620">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-621">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8d549-621">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-622">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-623">A data e a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="8d549-623">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8d549-624">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é suportada.</span><span class="sxs-lookup"><span data-stu-id="8d549-624">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8d549-625">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8d549-625">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d549-626">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8d549-626">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8d549-627">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8d549-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d549-628">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="8d549-628">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8d549-629">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="8d549-629">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d549-630">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d549-630">Requirements</span></span>



| <span data-ttu-id="8d549-631">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d549-631">Requirement</span></span> | <span data-ttu-id="8d549-632">Valor</span><span class="sxs-lookup"><span data-stu-id="8d549-632">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d549-633">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d549-633">Minimum supported client</span></span><br/> | <span data-ttu-id="8d549-634">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8d549-634">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8d549-635">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d549-635">Minimum supported server</span></span><br/> | <span data-ttu-id="8d549-636">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8d549-636">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8d549-637">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d549-637">Namespace</span></span><br/>                | <span data-ttu-id="8d549-638">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8d549-638">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8d549-639">MOF</span><span class="sxs-lookup"><span data-stu-id="8d549-639">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d549-640"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d549-640"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d549-641">DLL</span><span class="sxs-lookup"><span data-stu-id="8d549-641">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d549-642"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8d549-642"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

