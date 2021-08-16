---
description: O tipo de enumeração WPD WHITE BALANCE SETTINGS descreve como um dispositivo de vídeo ou imagem pondera os canais de cores para obter \_ um equilíbrio de branco \_ \_ adequado.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: WPD_WHITE_BALANCE_SETTINGS enumeração (PortableDevice.h)
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
ms.openlocfilehash: 1b596dd6d8fbcc2b2a875b70d80e8eb4040c966590642a004c551ec159c9f5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842043"
---
# <a name="wpd_white_balance_settings-enumeration"></a>\_Enumeração WPD WHITE \_ \_ BALANCE SETTINGS

O **tipo de enumeração WPD \_ WHITE BALANCE \_ \_ SETTINGS** descreve como um dispositivo de vídeo ou imagem pondera os canais de cores para obter um equilíbrio de branco adequado.

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

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD \_ WHITE \_ BALANCE \_ UNDEFINED**
</dt> <dd>

Esse valor não foi definido.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD \_ WHITE \_ BALANCE \_ MANUAL**
</dt> <dd>

O saldo em branco é definido explicitamente usando a propriedade [WPD \_ STILL IMAGE \_ \_ RGB \_ GAIN](still-image-properties.md) e não será alterado por si só.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD \_ WHITE \_ BALANCE \_ AUTOMATIC**
</dt> <dd>

O dispositivo definirá o saldo em branco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD \_ WHITE \_ BALANCE \_ ONE \_ PUSH \_ AUTOMATIC**
</dt> <dd>

O dispositivo definirá o saldo em branco, mas somente quando o usuário efetuar push do botão de captura do dispositivo enquanto estiver pressionando o dispositivo em um campo branco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ WHITE \_ BALANCE \_ DAYLIGHT**
</dt> <dd>

O dispositivo usará números de saldo em branco apropriados para uso na maioria das configurações de verão.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD \_ WHITE \_ BALANCE \_ LTDEN**
</dt> <dd>

O dispositivo usará números de saldo em branco apropriados para uso na maioria das configurações de iluminação interna e incandescente.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD \_ WHITE \_ BALANCE \_ FLASH**
</dt> <dd>

O dispositivo usará números de saldo em branco apropriados para uso com um flash.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela [propriedade WPD \_ STILL IMAGE \_ WHITE \_ \_ BALANCE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




