---
description: São usados para definir um endereço MAC (controle de acesso de mídia) do IEEE.
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828850"
---
# <a name="dot11_mac_address"></a>\_Endereço MAC \_ DOT11

Os tipos de **\_ \_ endereço MAC DOT11** são usados para definir um endereço MAC (controle de acesso de mídia) do IEEE.


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

**\_Endereço MAC \_ DOT11 \[ 6\]**
</dt> <dd>

Um endereço MAC no formato unicast, multicast ou broadcast.

</dd> <dt>

**\_Endereço MAC do PDOT11 \_**
</dt> <dd>

Ponteiro para um endereço MAC no formato unicast, multicast ou broadcast.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                       |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Windot11. h (incluir Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de DOT11 \_ BSSID \_**](dot11-bssid-list.md)
</dt> <dt>

[**\_atributos de associação de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**\_entrada de BSS de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




