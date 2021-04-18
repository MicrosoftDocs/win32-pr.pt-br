---
description: Representa uma instância de um componente de extensão associado a um comutador Ethernet virtual.
ms.assetid: 5b3e26e3-4cb9-47c9-865e-2f3232bbfc8e
title: Classe Msvm_EthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtension
- Msvm_EthernetSwitchExtension.InstanceID
- Msvm_EthernetSwitchExtension.Caption
- Msvm_EthernetSwitchExtension.Description
- Msvm_EthernetSwitchExtension.ElementName
- Msvm_EthernetSwitchExtension.InstallDate
- Msvm_EthernetSwitchExtension.OperationalStatus
- Msvm_EthernetSwitchExtension.StatusDescriptions
- Msvm_EthernetSwitchExtension.Status
- Msvm_EthernetSwitchExtension.HealthState
- Msvm_EthernetSwitchExtension.CommunicationStatus
- Msvm_EthernetSwitchExtension.DetailedStatus
- Msvm_EthernetSwitchExtension.OperatingStatus
- Msvm_EthernetSwitchExtension.PrimaryStatus
- Msvm_EthernetSwitchExtension.EnabledState
- Msvm_EthernetSwitchExtension.OtherEnabledState
- Msvm_EthernetSwitchExtension.RequestedState
- Msvm_EthernetSwitchExtension.EnabledDefault
- Msvm_EthernetSwitchExtension.TimeOfLastStateChange
- Msvm_EthernetSwitchExtension.AvailableRequestedStates
- Msvm_EthernetSwitchExtension.TransitioningToState
- Msvm_EthernetSwitchExtension.SystemCreationClassName
- Msvm_EthernetSwitchExtension.SystemName
- Msvm_EthernetSwitchExtension.CreationClassName
- Msvm_EthernetSwitchExtension.Name
- Msvm_EthernetSwitchExtension.ExtensionType
- Msvm_EthernetSwitchExtension.Vendor
- Msvm_EthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a6d760737ded1a12cf369ccb3a46595627d8e38e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757145"
---
# <a name="msvm_ethernetswitchextension-class"></a><span data-ttu-id="c7deb-103">\_Classe Msvm EthernetSwitchExtension</span><span class="sxs-lookup"><span data-stu-id="c7deb-103">Msvm\_EthernetSwitchExtension class</span></span>

<span data-ttu-id="c7deb-104">Representa uma instância de um componente de extensão associado a um comutador Ethernet virtual.</span><span class="sxs-lookup"><span data-stu-id="c7deb-104">Represents an instance of an extension component bound to a virtual Ethernet switch.</span></span>

<span data-ttu-id="c7deb-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c7deb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7deb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7deb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtension : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption = "Virtual Switch Extension";
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchExtension";
  string   Name;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="c7deb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c7deb-107">Members</span></span>

<span data-ttu-id="c7deb-108">A classe **Msvm \_ EthernetSwitchExtension** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c7deb-108">The **Msvm\_EthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="c7deb-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c7deb-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c7deb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7deb-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c7deb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c7deb-111">Methods</span></span>

<span data-ttu-id="c7deb-112">A classe **Msvm \_ EthernetSwitchExtension** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c7deb-112">The **Msvm\_EthernetSwitchExtension** class has these methods.</span></span>



| <span data-ttu-id="c7deb-113">Método</span><span class="sxs-lookup"><span data-stu-id="c7deb-113">Method</span></span>                                                                        | <span data-ttu-id="c7deb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7deb-114">Description</span></span>                         |
|:------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="c7deb-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c7deb-115">**RequestStateChange**</span></span>](msvm-ethernetswitchextension-requeststatechange.md) | <span data-ttu-id="c7deb-116">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="c7deb-116">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c7deb-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7deb-117">Properties</span></span>

<span data-ttu-id="c7deb-118">A classe **Msvm \_ EthernetSwitchExtension** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c7deb-118">The **Msvm\_EthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7deb-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c7deb-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-120">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-122">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="c7deb-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="c7deb-123">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7deb-123">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="c7deb-124">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="c7deb-124">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="c7deb-125">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="c7deb-125">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="c7deb-126">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7deb-126">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c7deb-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c7deb-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c7deb-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="c7deb-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="c7deb-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="c7deb-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="c7deb-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="c7deb-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="c7deb-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="c7deb-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="c7deb-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="c7deb-137">)</span><span class="sxs-lookup"><span data-stu-id="c7deb-137">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c7deb-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c7deb-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-141">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7deb-141">A short description of the object.</span></span> <span data-ttu-id="c7deb-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "extensão do comutador virtual".</span><span class="sxs-lookup"><span data-stu-id="c7deb-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch Extension".</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-143">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c7deb-143">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-146">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="c7deb-146">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c7deb-147">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c7deb-147">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c7deb-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-148">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-149">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c7deb-149">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-152">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7deb-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-153">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c7deb-153">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="c7deb-154">Essa propriedade é sempre definida como "Msvm \_ EthernetSwitchExtension".</span><span class="sxs-lookup"><span data-stu-id="c7deb-154">This property is always set to "Msvm\_EthernetSwitchExtension".</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-155">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c7deb-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-158">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="c7deb-158">A description of the object.</span></span> <span data-ttu-id="c7deb-159">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-160">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c7deb-160">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-163">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="c7deb-163">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c7deb-164">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c7deb-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c7deb-165">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-166">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c7deb-166">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-169">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c7deb-169">A display name for the object.</span></span> <span data-ttu-id="c7deb-170">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-171">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c7deb-171">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-172">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-174">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="c7deb-174">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c7deb-175">Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7deb-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c7deb-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c7deb-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c7deb-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="c7deb-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c7deb-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c7deb-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-180">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-182">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="c7deb-182">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c7deb-183">Essa propriedade também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="c7deb-183">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c7deb-184">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7deb-184">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c7deb-185">Valor</span><span class="sxs-lookup"><span data-stu-id="c7deb-185">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="c7deb-186">Significado</span><span class="sxs-lookup"><span data-stu-id="c7deb-186">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="c7deb-187"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="c7deb-187"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="c7deb-188"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="c7deb-189"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-189"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="c7deb-190">O elemento é ou pode estar executando comandos, processará qualquer comando na fila e enfileirará novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="c7deb-190">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="c7deb-191"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="c7deb-192">O elemento não executará comandos e descartará as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="c7deb-192">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="c7deb-193"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-193"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="c7deb-194">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c7deb-194">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="c7deb-195"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-195"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="c7deb-196">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c7deb-196">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="c7deb-197"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-197"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="c7deb-198">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="c7deb-198">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="c7deb-199"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-199"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="c7deb-200">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="c7deb-200">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="c7deb-201"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-201"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="c7deb-202">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="c7deb-202">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="c7deb-203"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-203"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="c7deb-204">O elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="c7deb-204">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="c7deb-205">O comportamento do elemento é semelhante ao estado habilitado, mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="c7deb-205">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="c7deb-206">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="c7deb-206">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="c7deb-207"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-207"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="c7deb-208">O elemento está no processo de ir para um estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="c7deb-208">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="c7deb-209">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="c7deb-209">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="c7deb-210"><dt>**DMTF reservado**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-210"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="c7deb-211">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c7deb-211">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="c7deb-212"><dt>**Fornecedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-212"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="c7deb-213">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c7deb-213">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="c7deb-214">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="c7deb-214">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-215">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="c7deb-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-217">Indica o tipo do componente de extensão.</span><span class="sxs-lookup"><span data-stu-id="c7deb-217">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7deb-218">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c7deb-218">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="c7deb-219">**Captura** (1)</span><span class="sxs-lookup"><span data-stu-id="c7deb-219">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="c7deb-220">**Filtro** (2)</span><span class="sxs-lookup"><span data-stu-id="c7deb-220">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="c7deb-221">**Encaminhamento** (3)</span><span class="sxs-lookup"><span data-stu-id="c7deb-221">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="c7deb-222">**Monitoramento** (4)</span><span class="sxs-lookup"><span data-stu-id="c7deb-222">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="c7deb-223">**Nativo** (5)</span><span class="sxs-lookup"><span data-stu-id="c7deb-223">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7deb-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c7deb-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-225">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-227">Especifica a integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="c7deb-227">Specifies the current health of the element.</span></span> <span data-ttu-id="c7deb-228">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c7deb-228">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="c7deb-229">Quando ocorrer um erro crítico, verifique o log de eventos para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="c7deb-229">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="c7deb-230">A propriedade **enabledstate** também pode conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c7deb-230">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="c7deb-231">Por exemplo, quando o espaço em disco está muito baixo, o **HealthState** é definido como 25, a máquina virtual pausa e **enabledstate** é definido como 32768 (em pausa).</span><span class="sxs-lookup"><span data-stu-id="c7deb-231">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="c7deb-232">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="c7deb-233">Valor</span><span class="sxs-lookup"><span data-stu-id="c7deb-233">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="c7deb-234">Significado</span><span class="sxs-lookup"><span data-stu-id="c7deb-234">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="c7deb-235"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-235"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="c7deb-236">O elemento é totalmente funcional e está operando em parâmetros operacionais normais e sem erros.</span><span class="sxs-lookup"><span data-stu-id="c7deb-236">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="c7deb-237"><dt>**Maior falha**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-237"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="c7deb-238">O elemento sofreu uma falha grave.</span><span class="sxs-lookup"><span data-stu-id="c7deb-238">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="c7deb-239"><dt>**Falha crítica**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-239"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="c7deb-240">O elemento não é funcional e a recuperação pode não ser possível.</span><span class="sxs-lookup"><span data-stu-id="c7deb-240">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="c7deb-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c7deb-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-242">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c7deb-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-244">A data e a hora em que a configuração de máquina virtual foi criada para uma máquina virtual, ou **nula**, para um sistema operacional de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="c7deb-244">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="c7deb-245">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c7deb-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-249">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c7deb-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-250">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c7deb-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c7deb-251">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-252">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c7deb-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-253">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-255">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7deb-255">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-256">O nome exclusivo do componente de extensão.</span><span class="sxs-lookup"><span data-stu-id="c7deb-256">The unique name of the extension component.</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-257">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c7deb-257">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-258">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-260">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="c7deb-260">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c7deb-261">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c7deb-261">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c7deb-262">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-262">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-263">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c7deb-263">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-264">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-264">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-266">Uma matriz que contém os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7deb-266">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="c7deb-267">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-268">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c7deb-268">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-269">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-271">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="c7deb-271">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="c7deb-272">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="c7deb-272">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c7deb-273">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c7deb-273">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-274">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c7deb-274">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-275">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-277">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="c7deb-277">Provides high level status information.</span></span> <span data-ttu-id="c7deb-278">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c7deb-278">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="c7deb-279">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="c7deb-279">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c7deb-280">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-281">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c7deb-281">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-282">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-284">O último estado solicitado ou desejado para o elemento como passado para o método **RequestStateChange** , ou 12 (não aplicável) se nenhuma alteração de estado estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="c7deb-284">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="c7deb-285">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="c7deb-285">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="c7deb-286">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="c7deb-286">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="c7deb-287">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7deb-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-288">**Status**</span><span class="sxs-lookup"><span data-stu-id="c7deb-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-291">Uma cadeia de caracteres que especifica o status do elemento.</span><span class="sxs-lookup"><span data-stu-id="c7deb-291">A string that specifies the status of the element.</span></span> <span data-ttu-id="c7deb-292">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c7deb-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-294">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-296">Qualificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c7deb-296">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-297">Uma matriz que contém cadeias de caracteres que descrevem os valores correspondentes da matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c7deb-297">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="c7deb-298">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c7deb-298">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-299">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c7deb-299">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-302">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7deb-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-303">O nome da classe de criação do sistema.</span><span class="sxs-lookup"><span data-stu-id="c7deb-303">The system creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-304">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c7deb-304">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-305">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-307">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c7deb-307">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-308">O nome do comutador virtual ao qual a instância de extensão está associada.</span><span class="sxs-lookup"><span data-stu-id="c7deb-308">The name of the virtual switch to which the extension instance is bound to.</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-309">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c7deb-309">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-310">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c7deb-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-312">A data e a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="c7deb-312">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c7deb-313">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7deb-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-314">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c7deb-314">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-315">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7deb-315">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-317">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="c7deb-317">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c7deb-318">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c7deb-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-319">**Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="c7deb-319">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-322">Indica o fornecedor que fornece a extensão.</span><span class="sxs-lookup"><span data-stu-id="c7deb-322">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="c7deb-323">**Versão**</span><span class="sxs-lookup"><span data-stu-id="c7deb-323">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7deb-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7deb-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7deb-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7deb-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7deb-326">A versão da extensão em um formato de "*Major*. *Minor*", por exemplo," 2,0 ".</span><span class="sxs-lookup"><span data-stu-id="c7deb-326">The version of the extension in a format of "*major*.*minor*", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7deb-327">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7deb-327">Requirements</span></span>



| <span data-ttu-id="c7deb-328">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7deb-328">Requirement</span></span> | <span data-ttu-id="c7deb-329">Valor</span><span class="sxs-lookup"><span data-stu-id="c7deb-329">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7deb-330">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7deb-330">Minimum supported client</span></span><br/> | <span data-ttu-id="c7deb-331">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c7deb-331">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7deb-332">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7deb-332">Minimum supported server</span></span><br/> | <span data-ttu-id="c7deb-333">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c7deb-333">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7deb-334">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7deb-334">Namespace</span></span><br/>                | <span data-ttu-id="c7deb-335">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c7deb-335">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7deb-336">MOF</span><span class="sxs-lookup"><span data-stu-id="c7deb-336">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7deb-337"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-337"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7deb-338">DLL</span><span class="sxs-lookup"><span data-stu-id="c7deb-338">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7deb-339"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7deb-339"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

