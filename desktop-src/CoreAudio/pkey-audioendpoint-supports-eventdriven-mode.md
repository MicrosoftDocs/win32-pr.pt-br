---
description: O PKEY \_ AudioEndpoint \_ dá suporte à \_ propriedade de modo EventDriven que \_ indica se o ponto de extremidade dá suporte ao modo controlado por evento.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 280be65d4ae8e0b557bd96320ea31f67ba75657ecb5b685608bd2c314e10836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758916"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>PKEY \_ AudioEndpoint \_ dá suporte ao \_ \_ modo EventDriven

O **PKEY \_ AudioEndpoint \_ dá suporte à propriedade de \_ \_ modo EventDriven** que indica se o ponto de extremidade dá suporte ao modo controlado por evento.

O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ UI4.

O membro **uintVal** da estrutura **PROPVARIANT** é um **DWORD** que indica se o ponto de extremidade dá suporte ao modo controlado por evento.

## <a name="remarks"></a>Comentários

Esse valor de propriedade é preenchido por um OEM de áudio em um arquivo. inf para indicar que o hardware HDAudio dá suporte ao modo controlado por eventos de acordo com o requisito do WHQL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio de núcleo](core-audio-properties.md)
</dt> </dl>

 

 




