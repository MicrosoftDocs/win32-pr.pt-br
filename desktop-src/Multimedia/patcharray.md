---
title: PATCHARRAY (mmsystem. h)
description: PATCHARRAY é um tipo usado para definir uma matriz de patches de MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824820"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY é um tipo usado para definir uma matriz de patches de MIDI.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**PATCHARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Cada elemento na matriz corresponde a um patch com cada um dos 16 bits representando um dos 16 canais MIDI. Os bits são definidos para cada um dos canais que usam esse patch específico. Por exemplo, se o número do patch 0 for usado pelos canais de MIDI física 0 e 8, o elemento 0 da matriz deverá ser definido como 0x0101.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Versão<br/>                  | MIDI (interface digital de instrumento musical), tipos de MIDI<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de MIDI](midi-event-types.md)
</dt> </dl>

 

 





