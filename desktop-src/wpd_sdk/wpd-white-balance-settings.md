---
description: O \_ tipo de \_ Enumeração configurações de balanço de branco WPD \_ descreve como um dispositivo de vídeo ou imagem tem como peso os canais de cores para atingir um equilíbrio de branco adequado.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Enumeração de WPD_WHITE_BALANCE_SETTINGS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751712"
---
# <a name="wpd_white_balance_settings-enumeration"></a>\_Enumeração de \_ configurações de balanço de branco WPD \_

O tipo de enumeração **\_ configurações de \_ balanço \_ de branco WPD** descreve como um dispositivo de vídeo ou imagem tem como peso os canais de cores para atingir um equilíbrio de branco adequado.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_balanço de branco WPD \_ \_ indefinido**
</dt> <dd>

Este valor não foi definido.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_manual de \_ saldo de branco WPD \_**
</dt> <dd>

O equilíbrio de branco é definido explicitamente usando a propriedade de [ \_ \_ \_ \_ lucro RGB da imagem ainda](still-image-properties.md) mais e não será alterado por si só.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**saldo de branco WPD- \_ \_ \_ automático**
</dt> <dd>

O dispositivo definirá o equilíbrio de branco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**pressão branca de WPD de \_ \_ \_ um \_ Push \_ automático**
</dt> <dd>

O dispositivo definirá o equilíbrio de branco, mas somente quando o usuário enviar por push o botão de captura do dispositivo enquanto mira o dispositivo em um campo branco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**\_horário de \_ Verão de saldo branco WPD \_**
</dt> <dd>

O dispositivo usará números de saldo branco apropriados para uso na maioria das configurações de horário de verão.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**\_Tungsten de \_ saldo de branco WPD \_**
</dt> <dd>

O dispositivo usará números de saldo branco apropriados para uso na maioria das configurações de iluminação de incandescentes.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**\_flash de \_ proporção de branco WPD \_**
</dt> <dd>

O dispositivo usará números de balanço de branco apropriados para uso com um flash.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [de \_ \_ balanço de \_ branco \_ de imagem ainda WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




