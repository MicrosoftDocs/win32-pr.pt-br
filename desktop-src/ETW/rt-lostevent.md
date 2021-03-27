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
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501766"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Evento perdido**](lost-event.md)
</dt> </dl>

 

 




