---
description: Define um algoritmo de codificação para criptografia e descriptografia de dados.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: Enumeração de DOT11_CIPHER_ALGORITHM (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759193"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>Enumeração de algoritmo de \_ codificação DOT11 \_

O tipo enumerado do **\_ \_ algoritmo DOT11 Cipher** define um algoritmo de codificação para criptografia e descriptografia de dados.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11 \_ Cipher \_ algo \_ None**
</dt> <dd>

Especifica que nenhum algoritmo de codificação está habilitado ou com suporte.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ Cipher \_ algo \_ WEP40**
</dt> <dd>

Especifica um algoritmo WEP (Wired Equivalent Privacy), que é o algoritmo baseado em RC4 que é especificado no padrão 802.11-1999. Este enumerador especifica o algoritmo de criptografia WEP com uma chave de codificação de 40 bits.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_ \_ Algo TKIP de codificação DOT11 \_**
</dt> <dd>

Especifica um algoritmo TKIP (Temporal Key Integrity Protocol), que é o conjunto de codificação baseado em RC4, baseado nos algoritmos definidos na especificação WPA e no padrão IEEE 802.11 i-2004. Essa codificação também usa o algoritmo de código de integridade de Michael Message (MIC) para a proteção de falsificação.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11 \_ Cipher \_ algo \_ CCMP**
</dt> <dd>

Especifica um algoritmo AES-CCMP, conforme especificado no padrão IEEE 802.11 i-2004 e RFC 3610. O criptografia AES (AES) é o algoritmo de criptografia definido no FIPS PUB 197.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ Cipher \_ algo \_ WEP104**
</dt> <dd>

Especifica um algoritmo de criptografia WEP com uma chave de codificação de 104 bits.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**\_Grupo de \_ uso de WPA de algo DOT11 Cipher \_ \_ \_**
</dt> <dd>

Especifica um acesso protegido de Wi-Fi (WPA) usando o pacote de codificação de chave de grupo. Para obter mais informações sobre o uso do conjunto de codificação de chave de grupo, consulte a cláusula 7.3.2.25.1 do padrão IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**\_Grupo de \_ uso de RSN de algo \_ \_ de DOT11 Cipher \_**
</dt> <dd>

Especifica uma rede de segurança robusta (RSN) usando o pacote de codificação de chave de grupo. Para obter mais informações sobre o uso do conjunto de codificação de chave de grupo, consulte a cláusula 7.3.2.25.1 do padrão IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**\_ \_ Algo WEP de codificação DOT11 \_**
</dt> <dd>

Especifica um algoritmo de criptografia WEP com uma chave de codificação de qualquer comprimento.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**\_Início de IHV de codificação DOT11 \_ algo \_ \_**
</dt> <dd>

Especifica o início do intervalo que é usado para definir algoritmos de codificação proprietários que são desenvolvidos por um fornecedor de hardware independente (IHV).

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**\_Fim de IHV de codificação DOT11 \_ algo \_ \_**
</dt> <dd>

Especifica o final do intervalo que é usado para definir algoritmos de codificação proprietários que são desenvolvidos por um IHV.

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

 

 




