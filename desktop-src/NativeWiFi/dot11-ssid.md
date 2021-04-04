---
description: Contém o SSID de uma interface.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: Estrutura de DOT11_SSID (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828846"
---
# <a name="dot11_ssid-structure"></a>\_Estrutura DOT11 SSID

Uma estrutura **DOT11 \_ SSID** contém o SSID de uma interface.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a>Membros

<dl> <dt>

**uSSIDLength**
</dt> <dd>

O comprimento, em bytes, da matriz **ucSSID** .

</dd> <dt>

**ucSSID**
</dt> <dd>

O SSID. O \_ \_ comprimento máximo \_ de DOT11 SSID é definido como 32.

</dd> </dl>

## <a name="remarks"></a>Comentários

O SSID especificado pelo membro **ucSSID** não é uma cadeia de caracteres ASCII terminada em nulo. O comprimento do SSID é determinado pelo membro **uSSIDLength** .

Um SSID curinga é um SSID cujo membro **uSSIDLength** está definido como zero. Quando o SSID desejado é definido como o caractere curinga SSID, a estação 802,11 pode se conectar a qualquer rede de BSS (conjunto de serviços) básica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                        |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Wlantypes. h (incluir Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_parâmetros de conexão WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




