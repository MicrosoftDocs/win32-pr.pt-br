---
title: Keyarray (mmsystem. h)
description: Keyarray especifica um tipo usado para definir uma matriz de chaves.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- MIDIPATCHSIZE DE KEYARRAY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c5f578b912a7b184f9f455bc4a730132b2316472d061532c48847c312302d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140036"
---
# <a name="keyarray"></a>Keyarray

Keyarray especifica um tipo usado para definir uma matriz de chaves.


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**MIDIPATCHSIZE de keyarray \[\]**
</dt> <dd>

Cada elemento na matriz corresponde a um patch de percussão baseado em chave com cada um dos 16 bits representando um dos 16 canais MIDI. Os bits são definidos para cada um dos canais que usam esse patch específico. Por exemplo, se o patch de percussão para o número de chave 60 for usado pelos canais de MIDI física 9 e 15, o elemento 60 da matriz deverá ser definido como 0x8200.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Versão<br/>                  | MIDI (interface digital de instrumento musical), tipos de MIDI<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de MIDI](midi-event-types.md)
</dt> </dl>

 

 





