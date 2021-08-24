---
title: PATCHARRAY (Mmsystem.h)
description: PATCHARRAY é um tipo usado para definir uma matriz de patches MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1d14696d7bb76827f902609cb1411f7890adeac53092e1b66b7eda16604320
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806066"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY é um tipo usado para definir uma matriz de patches MIDI.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**PATCHARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Cada elemento na matriz corresponde a um patch com cada um dos 16 bits que representam um dos 16 canais MIDI. Os bits são definidos para cada um dos canais que usam esse patch específico. Por exemplo, se o patch número 0 for usado pelos canais MIDI físicos 0 e 8, o elemento 0 da matriz deverá ser definido como 0x0101.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Versão<br/>                  | Instrument digital interface (MIDI), tipos MIDI<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos MIDI](midi-event-types.md)
</dt> </dl>

 

 





