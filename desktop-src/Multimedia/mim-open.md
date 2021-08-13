---
title: MIM_OPEN mensagem (Mmsystem.h)
description: A MIM open é enviada para uma função de retorno de chamada de entrada \_ MIDI quando um dispositivo de entrada MIDI é aberto.
ms.assetid: c7a8b856-aedd-457d-8a21-0ec2e9303960
keywords:
- MIM_OPEN mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15cacc21fd31810adf3188cb1ba267c9727715a0426c98d18f231eeec19b9691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428116"
---
# <a name="mim_open-message"></a>\_MIM Mensagem OPEN

A **MIM \_ open** é enviada para uma função de retorno de chamada de entrada MIDI quando um dispositivo de entrada MIDI é aberto.


```C++
MIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*Dwparam1*
</dt> <dd>

Reservado; não use.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*Dwparam2*
</dt> <dd>

Reservado; não use.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MIDI (Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Mensagens MIDI](midi-messages.md)
</dt> </dl>

 

 





