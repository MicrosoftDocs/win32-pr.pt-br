---
description: Representa o ponto de conexão lógica para um adaptador de rede. Quando o ponto de extremidade de Wi-Fi está conectado a uma porta de comutador, o adaptador de rede conectado ao ponto de extremidade de Wi-Fi tem conectividade de rede.
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Classe Msvm_WiFiEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f4a0a287d85b7a229b0e8e50a10c402fca734429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920870"
---
# <a name="msvm_wifiendpoint-class"></a><span data-ttu-id="7fa39-104">\_Classe Msvm WiFiEndpoint</span><span class="sxs-lookup"><span data-stu-id="7fa39-104">Msvm\_WiFiEndpoint class</span></span>

<span data-ttu-id="7fa39-105">Representa o ponto de conexão lógica para um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="7fa39-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="7fa39-106">Quando o ponto de extremidade de Wi-Fi está conectado a uma porta de comutador, o adaptador de rede conectado ao ponto de extremidade de Wi-Fi tem conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="7fa39-106">When the Wi-Fi endpoint is connected to a switch port, the network adapter connected to the Wi-Fi endpoint has network connectivity.</span></span>

<span data-ttu-id="7fa39-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7fa39-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa39-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fa39-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
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
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a><span data-ttu-id="7fa39-109">Membros</span><span class="sxs-lookup"><span data-stu-id="7fa39-109">Members</span></span>

<span data-ttu-id="7fa39-110">A classe **Msvm \_ WiFiEndpoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7fa39-110">The **Msvm\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="7fa39-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7fa39-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7fa39-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7fa39-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7fa39-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="7fa39-113">Methods</span></span>

<span data-ttu-id="7fa39-114">A classe **Msvm \_ WiFiEndpoint** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7fa39-114">The **Msvm\_WiFiEndpoint** class has these methods.</span></span>



| <span data-ttu-id="7fa39-115">Método</span><span class="sxs-lookup"><span data-stu-id="7fa39-115">Method</span></span>                 | <span data-ttu-id="7fa39-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fa39-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="7fa39-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="7fa39-117">**RequestStateChange**</span></span> | <span data-ttu-id="7fa39-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="7fa39-118">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7fa39-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7fa39-119">Properties</span></span>

<span data-ttu-id="7fa39-120">A classe **Msvm \_ WiFiEndpoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7fa39-120">The **Msvm\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fa39-121">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="7fa39-121">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-124">Contém o endereço MAC do ponto de acesso ao qual o Wi-Fi ponto de extremidade está associado no momento.</span><span class="sxs-lookup"><span data-stu-id="7fa39-124">Contains the MAC address of the access point with which the Wi-Fi endpoint is currently associated.</span></span> <span data-ttu-id="7fa39-125">Se o ponto de extremidade Wi-Fi não estiver associado no momento, **AccessPointAddress** deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7fa39-125">If the Wi-Fi endpoint is not currently associated, then **AccessPointAddress** should be **Null**.</span></span> <span data-ttu-id="7fa39-126">O endereço MAC deve ser formatado como doze dígitos hexadecimais (por exemplo, "010203040506"), com cada par representando um dos seis octetos do endereço MAC na ordem de bits canônica (por exemplo, o bit de endereço do grupo é encontrado no menor bit de ordem do primeiro caractere da cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="7fa39-126">The MAC address should be formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (for example, the Group address bit is found in the low order bit of the first character of the string).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-127">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="7fa39-127">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-128">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-130">Outros endereços unicast que podem ser usados para se comunicar com o ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="7fa39-130">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="7fa39-131">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-131">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-132">**Associação**</span><span class="sxs-lookup"><span data-stu-id="7fa39-132">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-133">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7fa39-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-135">Indica se o ponto de extremidade Wi-Fi está associado no momento a uma estação de cliente ou ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="7fa39-135">Indicates whether the Wi-Fi endpoint is currently associated to an access point or client station.</span></span>

<span data-ttu-id="7fa39-136">Contém **true** se o ponto de extremidade Wi-Fi estiver associado a uma estação de cliente ou ponto de acesso; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7fa39-136">Contains **True** if the Wi-Fi endpoint is associated to an access point or client station; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-137">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="7fa39-137">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-138">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-140">Especifica o método usado para autenticar o ponto de extremidade de Wi-Fi e a rede entre si.</span><span class="sxs-lookup"><span data-stu-id="7fa39-140">Specifies the method used to authenticate the Wi-Fi endpoint and the network to one another.</span></span>

<dl> <dt>

<span data-ttu-id="7fa39-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7fa39-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7fa39-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Sistema aberto** (2)</span><span class="sxs-lookup"><span data-stu-id="7fa39-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Open System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Chave compartilhada** (3)</span><span class="sxs-lookup"><span data-stu-id="7fa39-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Shared Key** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**PSK WPA** (4)</span><span class="sxs-lookup"><span data-stu-id="7fa39-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="7fa39-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1x** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="7fa39-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="7fa39-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1x** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>Protocolo **CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="7fa39-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1x** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (9..</span><span class="sxs-lookup"><span data-stu-id="7fa39-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (9..</span></span> <span data-ttu-id="7fa39-151">)</span><span class="sxs-lookup"><span data-stu-id="7fa39-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7fa39-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="7fa39-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-153">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-155">Indica os valores possíveis para o parâmetro *requestedstate* do método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="7fa39-155">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="7fa39-156">Os valores listados serão um subconjunto dos valores contidos na propriedade **RequestedStatesSupported** da instância associada do **CIM \_ EnabledLogicalElementCapabilities**, em que os valores selecionados são uma função do estado atual do [**\_ EnabledLogicalElement do CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-156">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="7fa39-157">Essa propriedade pode ser não **nula** se uma implementação for capaz de anunciar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="7fa39-157">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="7fa39-158">Essa propriedade será **nula** se uma implementação não puder determinar o conjunto de valores possíveis como uma função do estado atual.</span><span class="sxs-lookup"><span data-stu-id="7fa39-158">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="7fa39-159">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="7fa39-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="7fa39-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7fa39-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="7fa39-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="7fa39-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="7fa39-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="7fa39-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="7fa39-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="7fa39-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="7fa39-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="7fa39-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="7fa39-170">)</span><span class="sxs-lookup"><span data-stu-id="7fa39-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7fa39-171">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="7fa39-171">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-172">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-174">Indica o tipo de BSS (conjunto de serviços básico) da rede que corresponde à instância.</span><span class="sxs-lookup"><span data-stu-id="7fa39-174">Indicates the Basic Service Set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="7fa39-175">Um conjunto de serviços básico é um conjunto de estações controladas por uma única função de coordenação.</span><span class="sxs-lookup"><span data-stu-id="7fa39-175">A Basic Service Set is a set of stations controlled by a single coordination function.</span></span>



| <span data-ttu-id="7fa39-176">Valor</span><span class="sxs-lookup"><span data-stu-id="7fa39-176">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="7fa39-177">Significado</span><span class="sxs-lookup"><span data-stu-id="7fa39-177">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="7fa39-178"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="7fa39-178"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <span data-ttu-id="7fa39-179"><dt>**Independente**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7fa39-179"><dt>**Independent**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="7fa39-180">O ponto de extremidade Wi-Fi está associado diretamente a outra estação de cliente.</span><span class="sxs-lookup"><span data-stu-id="7fa39-180">The Wi-Fi endpoint is associated directly to another client station.</span></span><br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <span data-ttu-id="7fa39-181"><dt>**Infraestrutura**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7fa39-181"><dt>**Infrastructure**</dt> <dt>3</dt></span></span> </dl>    | <span data-ttu-id="7fa39-182">O ponto de extremidade Wi-Fi está associado a uma rede usando um ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="7fa39-182">The Wi-Fi endpoint is associated to a network by using an access point.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="7fa39-183"><dt> **DMTF reservado**</dt> para <dt>4..</dt></span><span class="sxs-lookup"><span data-stu-id="7fa39-183"><dt>**DMTF Reserved** </dt> <dt>4.. </dt></span></span> </dl> |                                                                                    |



 

</dd> <dt>

<span data-ttu-id="7fa39-184">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="7fa39-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-187">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="7fa39-187">A short description of the object.</span></span> <span data-ttu-id="7fa39-188">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="7fa39-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-190">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-192">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="7fa39-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7fa39-193">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="7fa39-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7fa39-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-195">**Conectado**</span><span class="sxs-lookup"><span data-stu-id="7fa39-195">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-196">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7fa39-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-198">Essa propriedade será definida como **true** se o ponto de extremidade de Wi-Fi estiver conectado a uma porta de comutador.</span><span class="sxs-lookup"><span data-stu-id="7fa39-198">This property is set to **True** if the Wi-Fi endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-199">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7fa39-199">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-202">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7fa39-202">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-203">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="7fa39-203">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7fa39-204">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="7fa39-204">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-205">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7fa39-205">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-208">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="7fa39-208">A description of the object.</span></span> <span data-ttu-id="7fa39-209">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-210">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7fa39-210">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-211">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-213">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="7fa39-213">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7fa39-214">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="7fa39-214">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7fa39-215">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7fa39-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-219">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="7fa39-219">A display name for the object.</span></span> <span data-ttu-id="7fa39-220">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="7fa39-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-222">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-224">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="7fa39-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="7fa39-225">Essa propriedade é herdada de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7fa39-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7fa39-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="7fa39-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7fa39-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="7fa39-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7fa39-229">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7fa39-229">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-230">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-232">Especifica o estado habilitado do sistema planejado.</span><span class="sxs-lookup"><span data-stu-id="7fa39-232">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="7fa39-233">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7fa39-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="7fa39-234">Valor</span><span class="sxs-lookup"><span data-stu-id="7fa39-234">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="7fa39-235">Significado</span><span class="sxs-lookup"><span data-stu-id="7fa39-235">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="7fa39-236"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7fa39-236"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="7fa39-237">O sistema está desligado.</span><span class="sxs-lookup"><span data-stu-id="7fa39-237">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="7fa39-238"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7fa39-238"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="7fa39-239">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7fa39-239">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="7fa39-240"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7fa39-240"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="7fa39-241">O sistema está habilitado, mas offline.</span><span class="sxs-lookup"><span data-stu-id="7fa39-241">The system is enabled, but offline.</span></span> <span data-ttu-id="7fa39-242">Todas as novas solicitações serão descartadas.</span><span class="sxs-lookup"><span data-stu-id="7fa39-242">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7fa39-243">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="7fa39-243">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-244">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-246">Especifica o método de criptografia em uso para proteger a confidencialidade dos dados enviados e recebidos pelo ponto de extremidade Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="7fa39-246">Specifies the encryption method in use to protect the confidentiality of data sent and received by the Wi-Fi endpoint.</span></span>

<dl> <dt>

<span data-ttu-id="7fa39-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7fa39-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7fa39-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="7fa39-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="7fa39-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="7fa39-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (5)</span><span class="sxs-lookup"><span data-stu-id="7fa39-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (6..</span><span class="sxs-lookup"><span data-stu-id="7fa39-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (6..</span></span> <span data-ttu-id="7fa39-254">)</span><span class="sxs-lookup"><span data-stu-id="7fa39-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7fa39-255">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="7fa39-255">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-256">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-258">Endereços multicast para os quais o ponto de extremidade de LAN escuta.</span><span class="sxs-lookup"><span data-stu-id="7fa39-258">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="7fa39-259">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-259">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-260">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7fa39-260">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-261">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-263">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="7fa39-263">The current health of the element.</span></span> <span data-ttu-id="7fa39-264">Essa propriedade expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="7fa39-264">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="7fa39-265">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="7fa39-265">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="7fa39-266">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-267">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="7fa39-267">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-268">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-270">Contém o tipo de protocolo EAP (Extensible Authentication Protocol) se e somente se **AuthenticationMethod** contiver 5 (WPA IEEE 802.1 x), 7 (WPA2 IEEE 802.1 x) ou 8 (CCKM IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="7fa39-270">Contains the Extensible Authentication Protocol (EAP) type if and only if **AuthenticationMethod** contains 5 (WPA IEEE 802.1x), 7 (WPA2 IEEE 802.1x), or 8 (CCKM IEEE 802.1x).</span></span>

<dl> <dt>

<span data-ttu-id="7fa39-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="7fa39-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="7fa39-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="7fa39-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="7fa39-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="7fa39-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="7fa39-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="7fa39-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="7fa39-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-Sim** (8)</span><span class="sxs-lookup"><span data-stu-id="7fa39-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="7fa39-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="7fa39-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (11..</span><span class="sxs-lookup"><span data-stu-id="7fa39-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (11..</span></span> <span data-ttu-id="7fa39-283">)</span><span class="sxs-lookup"><span data-stu-id="7fa39-283">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7fa39-284">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7fa39-284">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-285">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7fa39-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-287">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="7fa39-287">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="7fa39-288">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-289">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7fa39-289">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-290">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-292">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="7fa39-292">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-293">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="7fa39-293">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7fa39-294">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-294">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-295">**LANID**</span><span class="sxs-lookup"><span data-stu-id="7fa39-295">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-296">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-298">Um rótulo ou identificador para o segmento de LAN ao qual o ponto de extremidade está conectado.</span><span class="sxs-lookup"><span data-stu-id="7fa39-298">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="7fa39-299">Se o ponto de extremidade não estiver ativo/conectado no momento ou se essas informações não forem conhecidas, essa propriedade será **nula**.</span><span class="sxs-lookup"><span data-stu-id="7fa39-299">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="7fa39-300">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-300">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-301">**LANType**</span><span class="sxs-lookup"><span data-stu-id="7fa39-301">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-302">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-304">Essa propriedade é preterida no lugar da propriedade **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="7fa39-304">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="7fa39-305">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-305">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-306">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="7fa39-306">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-309">Qualificadores: **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="7fa39-309">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-310">O endereço MAC usado na comunicação com o ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="7fa39-310">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="7fa39-311">O endereço MAC é formatado como doze dígitos hexadecimais (por exemplo, "010203040506"), com cada par representando um dos seis octetos do endereço MAC na ordem de bits canônica de acordo com a RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="7fa39-311">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="7fa39-312">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-312">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-313">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="7fa39-313">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-314">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7fa39-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-316">Qualificadores: **unidades** ("bits")</span><span class="sxs-lookup"><span data-stu-id="7fa39-316">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-317">O maior tamanho, em número de bits, do campo de informações que pode ser enviado ou recebido pelo ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="7fa39-317">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="7fa39-318">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-318">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-319">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7fa39-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-322">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="7fa39-322">The label by which the object is known.</span></span> <span data-ttu-id="7fa39-323">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-324">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="7fa39-324">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-327">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7fa39-327">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-328">Contém a heurística de nomenclatura selecionada para garantir que o valor da propriedade **Name** seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7fa39-328">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="7fa39-329">Essa propriedade é herdada do [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="7fa39-329">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-330">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="7fa39-330">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-331">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-333">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="7fa39-333">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7fa39-334">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="7fa39-334">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7fa39-335">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-335">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7fa39-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-337">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-339">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="7fa39-339">The current statuses of the object.</span></span> <span data-ttu-id="7fa39-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-341">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="7fa39-341">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-344">Especifica o método de autenticação 802,11 se e somente se **AuthenticationMethod** contiver 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="7fa39-344">Specifies the 802.11 authentication method if and only if **AuthenticationMethod** contains 1 (Other).</span></span> <span data-ttu-id="7fa39-345">O formato dessa cadeia de caracteres é específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="7fa39-345">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-346">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="7fa39-346">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-349">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="7fa39-349">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="7fa39-350">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="7fa39-350">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="7fa39-351">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-351">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-352">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="7fa39-352">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-355">Especifica o método de criptografia 802,11 se e somente se **EncryptionMethod** contiver 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="7fa39-355">Specifies the 802.11 encryption method if and only if **EncryptionMethod** contains 1 (Other).</span></span> <span data-ttu-id="7fa39-356">O formato dessa cadeia de caracteres é específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="7fa39-356">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-357">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="7fa39-357">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-360">Essa propriedade é preterida no lugar da propriedade **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="7fa39-360">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="7fa39-361">Essa propriedade é herdada do [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-361">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-362">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="7fa39-362">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-363">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-365">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="7fa39-365">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-366">Uma cadeia de caracteres que descreve o tipo de ponto de extremidade de protocolo quando a propriedade **ProtocolIFType** dessa classe (ou de qualquer uma de suas subclasses) é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="7fa39-366">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="7fa39-367">Essa propriedade deve ser definida como **NULL** quando a propriedade **ProtocolIFType** é qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="7fa39-367">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="7fa39-368">Essa propriedade é herdada do [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="7fa39-368">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-369">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="7fa39-369">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-370">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-372">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="7fa39-372">Provides high level status information.</span></span> <span data-ttu-id="7fa39-373">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="7fa39-373">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="7fa39-374">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="7fa39-374">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7fa39-375">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-376">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="7fa39-376">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-377">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-379">A propriedade é usada para categorizar e classificar instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="7fa39-379">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="7fa39-380">Se **ProtocolIFType** for definido como 1 (outro), as informações de tipo deverão ser fornecidas na propriedade **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="7fa39-380">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="7fa39-381">Essa propriedade é herdada do [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="7fa39-381">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="7fa39-382">**ProtocolIFType** é uma enumeração que é sincronizada com a [MIB ifType da IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="7fa39-382">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="7fa39-383">Os valores adicionais definidos pela DMTF também estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="7fa39-383">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="7fa39-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7fa39-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="7fa39-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA reservado** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="7fa39-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7fa39-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (4301..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (32768..</span><span class="sxs-lookup"><span data-stu-id="7fa39-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="7fa39-389">)</span><span class="sxs-lookup"><span data-stu-id="7fa39-389">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7fa39-390">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="7fa39-390">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-391">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-393">Essa propriedade é preterida no lugar da propriedade **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="7fa39-393">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="7fa39-394">Essa propriedade é herdada do [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="7fa39-394">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="7fa39-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-396">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-398">O último estado solicitado ou desejado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="7fa39-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="7fa39-399">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-400">**Status**</span><span class="sxs-lookup"><span data-stu-id="7fa39-400">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-401">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-403">Descreve o status do elemento.</span><span class="sxs-lookup"><span data-stu-id="7fa39-403">Describes the status of the element.</span></span> <span data-ttu-id="7fa39-404">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-404">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="7fa39-405">PROBLEMAS</span><span class="sxs-lookup"><span data-stu-id="7fa39-405">"OK"</span></span>

<span data-ttu-id="7fa39-406">Ao</span><span class="sxs-lookup"><span data-stu-id="7fa39-406">"Error"</span></span>

<span data-ttu-id="7fa39-407">Degradado</span><span class="sxs-lookup"><span data-stu-id="7fa39-407">"Degraded"</span></span>

<span data-ttu-id="7fa39-408">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="7fa39-408">"Unknown"</span></span>

<span data-ttu-id="7fa39-409">"Falha de Pred"</span><span class="sxs-lookup"><span data-stu-id="7fa39-409">"Pred Fail"</span></span>

<span data-ttu-id="7fa39-410">Comece</span><span class="sxs-lookup"><span data-stu-id="7fa39-410">"Starting"</span></span>

<span data-ttu-id="7fa39-411">Impedir</span><span class="sxs-lookup"><span data-stu-id="7fa39-411">"Stopping"</span></span>

<span data-ttu-id="7fa39-412">Serviço</span><span class="sxs-lookup"><span data-stu-id="7fa39-412">"Service"</span></span>

<span data-ttu-id="7fa39-413">Analisa</span><span class="sxs-lookup"><span data-stu-id="7fa39-413">"Stressed"</span></span>

<span data-ttu-id="7fa39-414">"Não recuperar"</span><span class="sxs-lookup"><span data-stu-id="7fa39-414">"NonRecover"</span></span>

<span data-ttu-id="7fa39-415">"Sem contato"</span><span class="sxs-lookup"><span data-stu-id="7fa39-415">"No Contact"</span></span>

<span data-ttu-id="7fa39-416">"Perda de comunicação"</span><span class="sxs-lookup"><span data-stu-id="7fa39-416">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-417">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7fa39-417">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-418">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-418">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-420">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="7fa39-420">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7fa39-421">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7fa39-421">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-422">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7fa39-422">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-423">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-425">O nome da classe de criação do sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="7fa39-425">The hosting system's creation class name.</span></span> <span data-ttu-id="7fa39-426">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="7fa39-426">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-427">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7fa39-427">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7fa39-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-430">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7fa39-430">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-431">O nome do sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="7fa39-431">The name of the hosting system.</span></span> <span data-ttu-id="7fa39-432">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="7fa39-432">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-433">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="7fa39-433">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-434">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7fa39-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-436">A data e a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="7fa39-436">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="7fa39-437">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-437">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fa39-438">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="7fa39-438">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fa39-439">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fa39-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fa39-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7fa39-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fa39-441">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="7fa39-441">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="7fa39-442">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fa39-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fa39-443">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa39-443">Requirements</span></span>



| <span data-ttu-id="7fa39-444">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa39-444">Requirement</span></span> | <span data-ttu-id="7fa39-445">Valor</span><span class="sxs-lookup"><span data-stu-id="7fa39-445">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa39-446">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fa39-446">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa39-447">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7fa39-447">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7fa39-448">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fa39-448">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa39-449">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7fa39-449">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fa39-450">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fa39-450">Namespace</span></span><br/>                | <span data-ttu-id="7fa39-451">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7fa39-451">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7fa39-452">MOF</span><span class="sxs-lookup"><span data-stu-id="7fa39-452">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fa39-453"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fa39-453"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fa39-454">DLL</span><span class="sxs-lookup"><span data-stu-id="7fa39-454">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fa39-455"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7fa39-455"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

