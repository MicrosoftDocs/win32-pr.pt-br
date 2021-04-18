---
description: Define um algoritmo de autenticação de LAN sem fio.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: Enumeração de DOT11_AUTH_ALGORITHM (Wlantypes. h)
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
ms.openlocfilehash: 1b14886c62448194b79eab2e0302ce5608ad282d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770153"
---
# <a name="dot11_auth_algorithm-enumeration"></a>Enumeração de algoritmo de \_ autenticação DOT11 \_

O tipo enumerado do **\_ \_ algoritmo DOT11 auth** define um algoritmo de autenticação de LAN sem fio.

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

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ auth \_ algo \_ 80211 \_ abrir**
</dt> <dd>

Especifica um algoritmo de autenticação do sistema aberto IEEE 802,11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**\_Chave compartilhada DOT11 auth \_ algo \_ 80211 \_ \_**
</dt> <dd>

Especifica um algoritmo de autenticação de chave compartilhada 802,11 que requer o uso de uma chave WEP (Wired Equivalent Privacy) pré-compartilhada para a autenticação 802,11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**\_WPA de \_ algo de autenticação DOT11 \_**
</dt> <dd>

Especifica um algoritmo de WPA (acesso protegido Wi-Fi). A autenticação de porta IEEE 802.1 X é executada pelo suplicante, autenticador e servidor de autenticação. As chaves de codificação são derivadas dinamicamente por meio do processo de autenticação.

Esse algoritmo é válido somente para tipos de BSS da \_ infraestrutura de tipo BSS dot11 \_ \_ .

Quando o algoritmo WPA estiver habilitado, a estação 802,11 será associada somente a um ponto de acesso cujas respostas de Beacon ou Probe contenham o conjunto de autenticação do tipo 1 (802.1 X) no elemento de informações WPA (ou seja).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ auth \_ algo \_ WPA \_ PSK**
</dt> <dd>

Especifica um algoritmo WPA que usa chaves pré-compartilhadas (PSK). A autenticação de porta IEEE 802.1 X é executada pelo suplicante e pelo autenticador. As chaves de codificação são derivadas dinamicamente por meio de uma chave pré-compartilhada que é usada no suplicante e no autenticador.

Esse algoritmo é válido somente para tipos de BSS **da \_ \_ \_ infraestrutura de tipo BSS dot11**.

Quando o algoritmo WPA PSK estiver habilitado, a estação 802,11 será associada somente a um ponto de acesso cujas respostas de Beacon ou investigação contenham o conjunto de autenticação do tipo 2 (chave pré-compartilhada) no IE do WPA.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ auth \_ algo \_ WPA \_ None**
</dt> <dd>

Não há suporte para esse valor.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**\_Algo de autenticação DOT11 \_ \_ RSNA**
</dt> <dd>

Especifica um algoritmo RSNA (Associação de rede de segurança robusta) 802.11. O WPA2 é um desses algoritmos. A autenticação de porta IEEE 802.1 X é executada pelo suplicante, autenticador e servidor de autenticação. As chaves de codificação são derivadas dinamicamente por meio do processo de autenticação.

Esse algoritmo é válido somente para tipos de BSS **da \_ \_ \_ infraestrutura de tipo BSS dot11**.

Quando o algoritmo RSNA estiver habilitado, a estação 802,11 será associada somente a um ponto de acesso cujas respostas de Beacon ou Probe contenham o conjunto de autenticação do tipo 1 (802.1 X) dentro do RSN IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ auth \_ algo \_ RSNA \_ PSK**
</dt> <dd>

Especifica um algoritmo 802.11 i RSNA que usa PSK. A autenticação de porta IEEE 802.1 X é executada pelo suplicante e pelo autenticador. As chaves de codificação são derivadas dinamicamente por meio de uma chave pré-compartilhada que é usada no suplicante e no autenticador.

Esse algoritmo é válido somente para tipos de BSS **da \_ \_ \_ infraestrutura de tipo BSS dot11**.

Quando o algoritmo PSK RSNA estiver habilitado, a estação 802,11 será associada somente a um ponto de acesso cujas respostas de Beacon ou investigação contenham o conjunto de autenticação do tipo 2 (chave pré-compartilhada) dentro do RSN IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**\_Início do IHV da autenticação DOT11 \_ algo \_ \_**
</dt> <dd>

Indica o início do intervalo que especifica os algoritmos de autenticação proprietários desenvolvidos por um IHV.

O enumerador de **\_ inicialização DOT11 auth \_ algo \_ IHV \_** é válido somente quando o driver de miniporta está operando no modo de estação extensível (ExtSTA).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**\_Fim de IHV da autenticação DOT11 \_ algo \_ \_**
</dt> <dd>

Indica o final do intervalo que especifica os algoritmos de autenticação proprietários que são desenvolvidos por um IHV.

O enumerador de **\_ \_ \_ \_ extremidade de IHV algo DOT11 auth** é válido somente quando o driver de miniporta está operando no modo ExtSTA.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                        |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Wlantypes. h (incluir Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Par de codificação de DOT11 \_ auth \_ \_**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**rede de WLAN \_ disponível \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**\_atributos de segurança de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




