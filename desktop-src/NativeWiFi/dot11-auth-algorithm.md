---
description: Define um algoritmo de autenticação de LAN sem fio.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: DOT11_AUTH_ALGORITHM enumeração (Wlantypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 774b2218a451f4cbaa85e6b77559c0d5761b0b132ebdf9d3f11c15ea6658e7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798466"
---
# <a name="dot11_auth_algorithm-enumeration"></a>Enumeração DE ALGORITMO \_ DE AUTH DOT11 \_

O **tipo enumerado DOT11 \_ AUTH \_ ALGORITHM** define um algoritmo de autenticação de LAN sem fio.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ OPEN**
</dt> <dd>

Especifica um algoritmo de autenticação IEEE 802.11 Open System.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ SHARED \_ KEY**
</dt> <dd>

Especifica um algoritmo de autenticação de Chave Compartilhada 802.11 que requer o uso de uma chave WEP (Privacidade Equivalente com Fio) pré-compartilhada para a autenticação 802.11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA**
</dt> <dd>

Especifica um algoritmo Wi-Fi WPA (Acesso Protegido). A autenticação de porta IEEE 802.1X é executada pelo servidor de autenticação, autenticador e flexível. As chaves de criptografia são derivadas dinamicamente por meio do processo de autenticação.

Esse algoritmo é válido somente para tipos BSS da infraestrutura de tipo \_ BSS dot11. \_ \_

Quando o algoritmo WPA estiver habilitado, a estação 802.11 associará somente a um ponto de acesso cujas respostas de sonda ou sinalizador contêm o pacote de autenticação do tipo 1 (802.1X) dentro do elemento de informações do WPA (IE).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ PSK**
</dt> <dd>

Especifica um algoritmo WPA que usa PSK (chaves pré-compartilhadas). A autenticação de porta IEEE 802.1X é executada pelo autenticador e pelo flexível. As chaves de criptografia são derivadas dinamicamente por meio de uma chave pré-compartilhada que é usada tanto no flexível quanto no autenticador.

Esse algoritmo é válido somente para tipos BSS da infraestrutura de tipo **\_ dot11 BSS \_ \_**.

Quando o algoritmo PSK do WPA estiver habilitado, a estação 802.11 associará somente a um ponto de acesso cujas respostas de sonda ou sinalizador contêm o pacote de autenticação do tipo 2 (chave pré-compartilhada) no IE do WPA.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ NONE**
</dt> <dd>

Não há suporte para esse valor.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA**
</dt> <dd>

Especifica um algoritmo RSNA (Associação de Rede de Segurança Robusta) 802.11i. WPA2 é um algoritmo desse tipo. A autenticação de porta IEEE 802.1X é executada pelo servidor de autenticação, autenticador e flexível. As chaves de criptografia são derivadas dinamicamente por meio do processo de autenticação.

Esse algoritmo é válido somente para tipos BSS da infraestrutura de tipo **\_ dot11 BSS \_ \_**.

Quando o algoritmo RSNA estiver habilitado, a estação 802.11 associará somente a um ponto de acesso cujas respostas de sonda ou sinalizador contêm o pacote de autenticação do tipo 1 (802.1X) no IE do RSN.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA \_ PSK**
</dt> <dd>

Especifica um algoritmo RSNA 802.11i que usa PSK. A autenticação de porta IEEE 802.1X é executada pelo autenticador e pelo flexível. As chaves de criptografia são derivadas dinamicamente por meio de uma chave pré-compartilhada que é usada tanto no flexível quanto no autenticador.

Esse algoritmo é válido somente para tipos BSS da infraestrutura de tipo **\_ dot11 BSS \_ \_**.

Quando o algoritmo PSK RSNA estiver habilitado, a estação 802.11 será associada somente a um ponto de acesso cujas respostas de sonda ou sinalizador contêm o pacote de autenticação do tipo 2 (chave pré-compartilhada) no IE do RSN.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ START**
</dt> <dd>

Indica o início do intervalo que especifica algoritmos de autenticação proprietários desenvolvidos por um IHV.

O **enumerador DOT11 \_ AUTH \_ ALGO \_ IHV \_ START** é válido somente quando o driver de miniporte está operando no modo ExtSTA (Estação Extensível).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ END**
</dt> <dd>

Indica o final do intervalo que especifica algoritmos de autenticação proprietários desenvolvidos por um IHV.

O **enumerador DOT11 \_ AUTH \_ ALGO \_ IHV \_ END** é válido somente quando o driver de miniporte está operando no modo ExtSTA.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, Windows XP somente com aplicativos da área de trabalho SP3 \[\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                        |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Wlantypes.h (inclua Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PAR DE CRIPTOGRAFIA \_ DOT11 \_ AUTH \_**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**REDE DISPONÍVEL DO WLAN \_ \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**ATRIBUTOS DE SEGURANÇA \_ WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




