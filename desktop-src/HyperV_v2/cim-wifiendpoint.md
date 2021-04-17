---
description: Representa um ponto de extremidade de comunicação sem fio, que pode enviar e receber quadros de dados quando seu dispositivo de interface associado está conectado a uma LAN sem fio IEEE 802,11.
ms.assetid: 61743402-f333-4501-ba17-e676d85f72f3
title: Classe CIM_WiFiEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiEndpoint
- CIM_WiFiEndpoint.LANID
- CIM_WiFiEndpoint.ProtocolIFType
- CIM_WiFiEndpoint.EncryptionMethod
- CIM_WiFiEndpoint.OtherEncryptionMethod
- CIM_WiFiEndpoint.AuthenticationMethod
- CIM_WiFiEndpoint.OtherAuthenticationMethod
- CIM_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- CIM_WiFiEndpoint.AccessPointAddress
- CIM_WiFiEndpoint.BSSType
- CIM_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e09d040f9d4530bee4347528d704cfe2e9403b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812950"
---
# <a name="cim_wifiendpoint-class"></a><span data-ttu-id="7eedc-103">\_Classe CIM WiFiEndpoint</span><span class="sxs-lookup"><span data-stu-id="7eedc-103">CIM\_WiFiEndpoint class</span></span>

<span data-ttu-id="7eedc-104">Representa um ponto de extremidade de comunicação sem fio, que pode enviar e receber quadros de dados quando seu dispositivo de interface associado está conectado a uma LAN sem fio IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="7eedc-104">Represents a wireless communication endpoint, which can send and receive data frames when its associated interface device is connected with an IEEE 802.11 wireless LAN.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eedc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7eedc-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Network::Wireless"), AMENDMENT]
class CIM_WiFiEndpoint : CIM_LANEndpoint
{
  string  LANID;
  uint16  ProtocolIFType = 71;
  uint16  EncryptionMethod;
  string  OtherEncryptionMethod;
  uint16  AuthenticationMethod;
  string  OtherAuthenticationMethod;
  uint16  IEEE8021xAuthenticationProtocol;
  string  AccessPointAddress;
  uint16  BSSType;
  boolean Associated;
};
```

## <a name="members"></a><span data-ttu-id="7eedc-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7eedc-106">Members</span></span>

<span data-ttu-id="7eedc-107">A classe **CIM \_ WiFiEndpoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7eedc-107">The **CIM\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="7eedc-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7eedc-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7eedc-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7eedc-109">Properties</span></span>

<span data-ttu-id="7eedc-110">A classe **CIM \_ WiFiEndpoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7eedc-110">The **CIM\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7eedc-111">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="7eedc-111">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7eedc-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-114">O endereço MAC do ponto de acesso associado ao ponto de extremidade de Wi-Fi; caso contrário, **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7eedc-114">The MAC address of the access point that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7eedc-115">**Associação**</span><span class="sxs-lookup"><span data-stu-id="7eedc-115">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7eedc-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-118">**true** se o ponto de extremidade WiFi estiver atualmente associado a um ponto de acesso ou estação de cliente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7eedc-118">**true** if the WiFi endpoint is currently associated with an access point or client station; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7eedc-119">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="7eedc-119">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-120">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eedc-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-122">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**","**CIM \_ WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**","**CIM \_ WiFiEndpoint**.**OtherAuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="7eedc-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**", "**CIM\_WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**", "**CIM\_WiFiEndpoint**.**OtherAuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-123">O tipo de autenticação usado entre o ponto de extremidade Wi-Fi e a rede.</span><span class="sxs-lookup"><span data-stu-id="7eedc-123">The authentication type used between the Wi-Fi endpoint and the network.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7eedc-124">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7eedc-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7eedc-125">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7eedc-125">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>

<span data-ttu-id="7eedc-126">**Sistema aberto** (2)</span><span class="sxs-lookup"><span data-stu-id="7eedc-126">**Open System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>

<span data-ttu-id="7eedc-127">**Chave compartilhada** (3)</span><span class="sxs-lookup"><span data-stu-id="7eedc-127">**Shared Key** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>

<span data-ttu-id="7eedc-128">**PSK WPA** (4)</span><span class="sxs-lookup"><span data-stu-id="7eedc-128">**WPA PSK** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>

<span data-ttu-id="7eedc-129">**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="7eedc-129">**WPA IEEE 802.1x** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>

<span data-ttu-id="7eedc-130">**WPA2 PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="7eedc-130">**WPA2 PSK** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>

<span data-ttu-id="7eedc-131">**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="7eedc-131">**WPA2 IEEE 802.1x** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>

<span data-ttu-id="7eedc-132">Protocolo **CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="7eedc-132">**CCKM IEEE 802.1x** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7eedc-133">**DMTF reservado** (9..)</span><span class="sxs-lookup"><span data-stu-id="7eedc-133">**DMTF Reserved** (9..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7eedc-134">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="7eedc-134">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eedc-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-137">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3,16")</span><span class="sxs-lookup"><span data-stu-id="7eedc-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3.16")</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-138">O tipo de BSS (conjunto de serviços básico) da rede que corresponde à instância.</span><span class="sxs-lookup"><span data-stu-id="7eedc-138">The basic service set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="7eedc-139">Um BSS é um conjunto de estações controladas por uma única função de coordenação.</span><span class="sxs-lookup"><span data-stu-id="7eedc-139">A BSS is a set of stations controlled by a single coordination function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7eedc-140">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7eedc-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="7eedc-141">**Independente** (2)</span><span class="sxs-lookup"><span data-stu-id="7eedc-141">**Independent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span>

<span data-ttu-id="7eedc-142">**Infraestrutura** (3)</span><span class="sxs-lookup"><span data-stu-id="7eedc-142">**Infrastructure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7eedc-143">**DMTF reservado** (4..)</span><span class="sxs-lookup"><span data-stu-id="7eedc-143">**DMTF Reserved** (4..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7eedc-144">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="7eedc-144">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-145">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eedc-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-147">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**","**CIM \_ WiFiEndpoint**.**OtherEncryptionMethod**")</span><span class="sxs-lookup"><span data-stu-id="7eedc-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**", "**CIM\_WiFiEndpoint**.**OtherEncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-148">O tipo de criptografia usado ao enviar e receber dados por meio do ponto de extremidade Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="7eedc-148">The encryption type used when sending and receiving data through the Wi-Fi endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7eedc-149">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7eedc-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7eedc-150">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7eedc-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WEP"></span><span id="wep"></span>

<span data-ttu-id="7eedc-151">**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="7eedc-151">**WEP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TKIP"></span><span id="tkip"></span>

<span data-ttu-id="7eedc-152">**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="7eedc-152">**TKIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CCMP"></span><span id="ccmp"></span>

<span data-ttu-id="7eedc-153">**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="7eedc-153">**CCMP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="7eedc-154">**Nenhum** (5)</span><span class="sxs-lookup"><span data-stu-id="7eedc-154">**None** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7eedc-155">**DMTF reservado** (6..)</span><span class="sxs-lookup"><span data-stu-id="7eedc-155">**DMTF Reserved** (6..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7eedc-156">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="7eedc-156">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-157">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eedc-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-159">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017. IETF "," RFC2716. IETF "," draft-ietf-pppext-EAP-TTLS. IETF "," Draft-kamath-pppext-PEAPv0. IETF "," Draft-Josefsson-pppext-EAP-TLS-EAP "," RFC4851. IETF "," RFC3748. IETF "," RFC4764. IETF "," RFC4186. IETF "," RFC4187. IETF "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="7eedc-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017.IETF", "RFC2716.IETF", "draft-ietf-pppext-eap-ttls.IETF", "draft-kamath-pppext-peapv0.IETF", "draft-josefsson-pppext-eap-tls-eap", "RFC4851.IETF", "RFC3748.IETF", "RFC4764.IETF", "RFC4186.IETF", "RFC4187.IETF"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-160">O tipo de EAP (protocolo de autenticação extensível) para o ponto de extremidade Wi-Fi quando **AuthenticationMethod** contém "7" (WPA IEEE 802.1 x) ou "8" (CCKM IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="7eedc-160">The EAP (Extensible Authentication Protocol) type for the Wi-Fi endpoint when **AuthenticationMethod** contains "7" (WPA IEEE 802.1x) or "8" (CCKM IEEE 802.1x).</span></span>

<dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>

<span data-ttu-id="7eedc-161">**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="7eedc-161">**EAP-TLS** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>

<span data-ttu-id="7eedc-162">**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="7eedc-162">**EAP-TTLS/MSCHAPv2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>

<span data-ttu-id="7eedc-163">**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="7eedc-163">**PEAPv0/EAP-MSCHAPv2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>

<span data-ttu-id="7eedc-164">**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="7eedc-164">**PEAPv1/EAP-GTC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>

<span data-ttu-id="7eedc-165">**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="7eedc-165">**EAP-FAST/MSCHAPv2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>

<span data-ttu-id="7eedc-166">**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="7eedc-166">**EAP-FAST/GTC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>

<span data-ttu-id="7eedc-167">**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="7eedc-167">**EAP-MD5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>

<span data-ttu-id="7eedc-168">**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="7eedc-168">**EAP-PSK** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>

<span data-ttu-id="7eedc-169">**EAP-Sim** (8)</span><span class="sxs-lookup"><span data-stu-id="7eedc-169">**EAP-SIM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>

<span data-ttu-id="7eedc-170">**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="7eedc-170">**EAP-AKA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>

<span data-ttu-id="7eedc-171">**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="7eedc-171">**EAP-FAST/TLS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7eedc-172">**DMTF reservado** (11..)</span><span class="sxs-lookup"><span data-stu-id="7eedc-172">**DMTF Reserved** (11..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7eedc-173">**LANID**</span><span class="sxs-lookup"><span data-stu-id="7eedc-173">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7eedc-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-176">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span><span class="sxs-lookup"><span data-stu-id="7eedc-176">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-177">O SSID (identificador de conjunto de serviços) da LAN sem fio que está associado ao ponto de extremidade de Wi-Fi; caso contrário, **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7eedc-177">The service set identifier (SSID) of the wireless LAN that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7eedc-178">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="7eedc-178">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7eedc-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-181">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="7eedc-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-182">O tipo de autenticação usado entre o ponto de extremidade Wi-Fi e a rede quando **AuthenticationMethod** contém "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="7eedc-182">The authentication type used between the Wi-Fi endpoint and the network when **AuthenticationMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="7eedc-183">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="7eedc-183">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7eedc-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-186">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**")</span><span class="sxs-lookup"><span data-stu-id="7eedc-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-187">Descreve o tipo de criptografia para o ponto de extremidade Wi-Fi quando **EncryptionMethod** contém "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="7eedc-187">Describes the encryption type for the Wi-Fi endpoint when **EncryptionMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="7eedc-188">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="7eedc-188">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eedc-189">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eedc-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eedc-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7eedc-191">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span><span class="sxs-lookup"><span data-stu-id="7eedc-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span></span>
</dt> </dl>

<span data-ttu-id="7eedc-192">A categoria ou classificação dessa instância.</span><span class="sxs-lookup"><span data-stu-id="7eedc-192">The category or classification of this instance.</span></span> <span data-ttu-id="7eedc-193">Os valores possíveis são limitados à Wi-Fi e valores reservados da MIB e da [IANA ifType](https://www.iana.org/assignments/ianaiftype-mib)</span><span class="sxs-lookup"><span data-stu-id="7eedc-193">The possible values are limited to the Wi-Fi and reserved values from the DMTF and [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span>

<span data-ttu-id="7eedc-194">Se **ProtocolIFType** for definido como "1" (outro), as informações de tipo deverão ser fornecidas na propriedade **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="7eedc-194">If the **ProtocolIFType** is set to "1" (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7eedc-195">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7eedc-195">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

<span data-ttu-id="7eedc-196">**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="7eedc-196">**IEEE 802.11** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

<span data-ttu-id="7eedc-197">**IANA reservado** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="7eedc-197">**IANA Reserved** (225..4095)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7eedc-198">**DMTF reservado** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7eedc-198">**DMTF Reserved** (4301..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7eedc-199">**Fornecedor reservado** (32768..)</span><span class="sxs-lookup"><span data-stu-id="7eedc-199">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="7eedc-200"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7eedc-200"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7eedc-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eedc-201">Requirements</span></span>



| <span data-ttu-id="7eedc-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eedc-202">Requirement</span></span> | <span data-ttu-id="7eedc-203">Valor</span><span class="sxs-lookup"><span data-stu-id="7eedc-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eedc-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eedc-204">Minimum supported client</span></span><br/> | <span data-ttu-id="7eedc-205">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7eedc-205">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7eedc-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eedc-206">Minimum supported server</span></span><br/> | <span data-ttu-id="7eedc-207">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7eedc-207">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7eedc-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="7eedc-208">Namespace</span></span><br/>                | <span data-ttu-id="7eedc-209">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7eedc-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7eedc-210">MOF</span><span class="sxs-lookup"><span data-stu-id="7eedc-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eedc-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eedc-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eedc-212">DLL</span><span class="sxs-lookup"><span data-stu-id="7eedc-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eedc-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7eedc-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7eedc-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="7eedc-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eedc-215">**\_LANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="7eedc-215">**CIM\_LANEndpoint**</span></span>](cim-lanendpoint.md)
</dt> </dl>

 

