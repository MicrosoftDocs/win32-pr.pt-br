---
description: Essa classe de tipo de evento é usada para indicar que os eventos foram perdidos em uma sessão em tempo real. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: Classe RT_LostEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: d0944b843c8deb38012242111b6c5057ccf7cb8557c69caefe9a87283d2ae418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328736"
---
# <a name="rt_lostevent-class"></a>\_Classe RT LostEvent

Essa classe de tipo de evento é usada para indicar que os eventos foram perdidos em uma sessão em tempo real.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a>Membros

A classe **RT \_ LostEvent** não define nenhum membro.

## <a name="remarks"></a>Comentários

O tipo de evento RTLostEvent indica que um ou mais eventos foram perdidos. O tipo de evento RTLostBuffer indica que um ou mais buffers foram perdidos. Os tipos de evento RTLostEvent e RTLostBuffer são entregues antes de processar eventos do buffer.

O RTLostFile indica que o arquivo de backup usado pelo autologger para capturar eventos foi perdido.

Os eventos perder dependem da frequência com que os eventos são registrados e de quanto tempo o consumidor gasta processando os eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Evento perdido**](lost-event.md)
</dt> </dl>

 

 




