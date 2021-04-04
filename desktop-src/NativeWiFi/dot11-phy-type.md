---
description: Define um tipo de mídia e PHY 802,11.
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: Enumeração de DOT11_PHY_TYPE (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_PHY_TYPE
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 4e8fc4a1154b9f95fad5024607435861b9e98ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828848"
---
# <a name="dot11_phy_type-enumeration"></a>\_Enumeração de \_ tipo DOT11 PHY

A enumeração de **\_ \_ tipo DOT11 PHY** define um tipo de mídia e PHY 802,11.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = 0,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11 \_ PHY \_ tipo \_ desconhecido**
</dt> <dd>

Especifica um tipo PHY desconhecido ou não inicializado.

</dd> <dt>

<span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11 \_ PHY \_ tipo \_ any**
</dt> <dd>

Especifica qualquer tipo de PHY.

</dd> <dt>

<span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11 \_ PHY \_ Type \_ FHSS**
</dt> <dd>

Especifica um PHY (FHSS) de espectro de dispersão de frequência. Os dispositivos Bluetooth podem usar FHSS ou uma adaptação de FHSS.

</dd> <dt>

<span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11 \_ PHY \_ tipo \_ DSSS**
</dt> <dd>

Especifica um tipo PHY de espectro de espalhamento de sequência direta (DSSS).

</dd> <dt>

<span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11 \_ PHY \_ Type \_ irbaseband**
</dt> <dd>

Especifica um tipo de PHY de banda de infravermelho (IR).

</dd> <dt>

<span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11 \_ PHY \_ Type \_ OFDM**
</dt> <dd>

Especifica um tipo PHY de OFDM (multiplexação de divisão de frequência ortogonal). dispositivos 802.11 a podem usar o OFDM.

</dd> <dt>

<span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11 \_ PHY \_ Type \_ hrdsss**
</dt> <dd>

Especifica um tipo PHY de HRDSSS (DSSS de alta taxa).

</dd> <dt>

<span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11 \_ PHY \_ tipo \_ ERP**
</dt> <dd>

Especifica um tipo PHY de taxa estendida (ERP). dispositivos 802.11 g podem usar ERP.

</dd> <dt>

<span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11 \_ PHY \_ tipo \_ HT**
</dt> <dd>

Especifica o tipo PHY 802.11 n.

</dd> <dt>

<span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11 \_ PHY \_ Type \_ vht**
</dt> <dd>

Especifica o tipo PHY de AC 802.11. Este é o tipo PHY de taxa de transferência muito alta especificado em IEEE 802.11 AC.

Esse valor tem suporte em Windows 8.1, Windows Server 2012 R2 e posterior.

</dd> <dt>

<span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11 \_ PHY \_ tipo \_ de \_ início de IHV**
</dt> <dd>

Especifica o início do intervalo que é usado para definir os tipos de PHY que são desenvolvidos por um fornecedor de hardware independente (IHV).

</dd> <dt>

<span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11 \_ PHY \_ tipo \_ de \_ fim de IHV**
</dt> <dd>

Especifica o início do intervalo que é usado para definir os tipos de PHY que são desenvolvidos por um fornecedor de hardware independente (IHV).

</dd> </dl>

## <a name="remarks"></a>Comentários

Um IHV pode atribuir um valor para seus tipos de PHY proprietários de **dot11 \_ PHY \_ tipo \_ IHV \_ início** por meio de **dot11 \_ PHY \_ tipo \_ IHV \_ end**. O IHV deve atribuir um número exclusivo a partir desse intervalo para cada um de seus tipos de PHY proprietários.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/>                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Windot11. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_atributos de associação de WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**\_funcionalidade da interface WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




