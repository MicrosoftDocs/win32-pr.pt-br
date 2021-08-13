---
description: Representa um ponto de extremidade de comunicação sem fio, que pode enviar e receber quadros de dados quando seu dispositivo de interface associado estiver conectado a uma LAN sem fio IEEE 802.11.
ms.assetid: 61743402-f333-4501-ba17-e676d85f72f3
title: CIM_WiFiEndpoint classe
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
ms.openlocfilehash: 5b188c59be8ca6fc6c1d171c4c030fa222e0fb8d4ac22622979304d975d74a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646319"
---
# <a name="cim_wifiendpoint-class"></a>Classe CIM \_ WiFiEndpoint

Representa um ponto de extremidade de comunicação sem fio, que pode enviar e receber quadros de dados quando seu dispositivo de interface associado estiver conectado a uma LAN sem fio IEEE 802.11.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A **classe CIM \_ WiFiEndpoint** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ WiFiEndpoint** tem essas propriedades.

<dl> <dt>

**AccessPointAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O endereço MAC do ponto de acesso associado ao ponto de Wi-Fi de acesso; caso contrário, **NULL.**

</dd> <dt>

**Associação**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**true** se o ponto de extremidade WiFi estiver associado atualmente a um ponto de acesso ou estação de cliente; caso contrário, **false.**

</dd> <dt>

**AuthenticationMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**", "**CIM \_ WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**", "**CIM \_ WiFiEndpoint**.**OtherAuthenticationMethod**")
</dt> </dl>

O tipo de autenticação usado entre Wi-Fi ponto de extremidade e a rede.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>

**Abrir Sistema** (2)


</dt> <dd></dd> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>

**Chave Compartilhada** (3)


</dt> <dd></dd> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>

**WPA PSK** (4)


</dt> <dd></dd> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>

**WPA IEEE 802.1x** (5)


</dt> <dd></dd> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>

**WPA2 PSK** (6)


</dt> <dd></dd> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>

**WPA2 IEEE 802.1x** (7)


</dt> <dd></dd> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>

**CCKM IEEE 802.1x** (8)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (9..)


</dt> <dd></dd> </dl>

</dd> <dt>

**BSSType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3.16")
</dt> </dl>

O tipo BSS (conjunto de serviços básico) da rede que corresponde à instância. Um BSS é um conjunto de estações controladas por uma única função de coordenação.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Independente** (2)


</dt> <dd></dd> <dt>

<span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span>

**Infraestrutura** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (4..)


</dt> <dd></dd> </dl>

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**", "**CIM \_ WiFiEndpoint**.**OtherEncryptionMethod**")
</dt> </dl>

O tipo de criptografia usado ao enviar e receber dados por meio Wi-Fi ponto de extremidade.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="WEP"></span><span id="wep"></span>

**WEP** (2)


</dt> <dd></dd> <dt>

<span id="TKIP"></span><span id="tkip"></span>

**TKIP** (3)


</dt> <dd></dd> <dt>

<span id="CCMP"></span><span id="ccmp"></span>

**CCMP** (4)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (6..)


</dt> <dd></dd> </dl>

</dd> <dt>

**IEEE8021xAuthenticationProtocol**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017. IETF", "RFC2716. IETF", "draft-ietf-pppext-eap-ttls. IETF", "draft-kamath-pppext-peapv0. IETF", "draft-draft-draftsson-pppext-eap-tls-eap", "RFC4851. IETF", "RFC3748. IETF", "RFC4764. IETF", "RFC4186. IETF", "RFC4187. IETF"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")
</dt> </dl>

O tipo EAP (Protocolo de Autenticação Extensível) para o ponto de extremidade Wi-Fi quando **AuthenticationMethod** contém "7" (WPA IEEE 802.1x) ou "8" (CCKM IEEE 802.1x).

<dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>

**EAP-TLS** (0)


</dt> <dd></dd> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>

**EAP-TTLS/MSCHAPv2** (1)


</dt> <dd></dd> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>

**PEAPv0/EAP-MSCHAPv2** (2)


</dt> <dd></dd> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>

**PEAPv1/EAP-GTC** (3)


</dt> <dd></dd> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>

**EAP-FAST/MSCHAPv2** (4)


</dt> <dd></dd> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>

**EAP-FAST/GTC** (5)


</dt> <dd></dd> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>

**EAP-MD5** (6)


</dt> <dd></dd> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>

**EAP-PSK** (7)


</dt> <dd></dd> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>

**EAP-SIM** (8)


</dt> <dd></dd> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>

**EAP-AKA** (9)


</dt> <dd></dd> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>

**EAP-FAST/TLS** (10)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (11..)


</dt> <dd></dd> </dl>

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")
</dt> </dl>

O SSID (identificador de conjunto de serviços) da LAN sem fio associada ao ponto de extremidade Wi-Fi serviço; caso contrário, **NULL.**

</dd> <dt>

**OtherAuthenticationMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")
</dt> </dl>

O tipo de autenticação usado entre o ponto Wi-Fi e a rede quando **AuthenticationMethod** contém "1" (Outro).

</dd> <dt>

**OtherEncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**")
</dt> </dl>

Descreve o tipo de criptografia para o ponto de Wi-Fi quando **EncryptionMethod** contém "1" (Outro).

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")
</dt> </dl>

A categoria ou classificação dessa instância. Os valores possíveis são limitados aos valores Wi-Fi e reservados do MIB DMTF e [IANA ifType](https://www.iana.org/assignments/ianaiftype-mib).

Se **ProtocolIFType** for definido como "1" (Outro), as informações de tipo deverão ser fornecidas na **propriedade OtherTypeDescription.**

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

**IEEE 802.11** (71)


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

**IANA Reservado** (225..4095)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (4301..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor Reservado** (32768..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ LANEndpoint**](cim-lanendpoint.md)
</dt> </dl>

 

