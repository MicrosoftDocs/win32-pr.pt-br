---
description: A classe CAMSchedule implementa um Agendador para relógios de referência.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Classe CAMSchedule (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2236eb66086bb590892401cab052f39d81a41941db38d2a73dedd5edb4c53ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955405"
---
# <a name="camschedule-class"></a>Classe CAMSchedule

A `CAMSchedule` classe implementa um Agendador para relógios de referência.



| Métodos públicos                                             | Descrição                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**CAMSchedule**](camschedule-camschedule.md)             | Método de construtor.                                                                  |
| [**~ CAMSchedule**](camschedule--camschedule.md)           | Método destruidor. VirtuaisLUNs.                                                          |
| [**GetAdviseCount**](camschedule-getadvisecount.md)       | Recupera o número de solicitações de aviso pendentes.                                     |
| [**GetNextAdviseTime**](camschedule-getnextadvisetime.md) | Recupera a hora da próxima solicitação de aviso.                                       |
| [**AddAdvisePacket**](camschedule-addadvisepacket.md)     | Adiciona uma solicitação de aviso à lista de solicitações pendentes.                              |
| [**Cancelar**](camschedule-unadvise.md)                   | Remove uma solicitação de aviso.                                                           |
| [**Aconselhamos**](camschedule-advise.md)                       | Despacha todas as solicitações agendadas para um período especificado ou anterior.          |
| [**GetEvent**](camschedule-getevent.md)                   | Recupera um identificador de evento, que é usado para sinalizar uma alteração no próximo horário de aviso. |



 

## <a name="remarks"></a>Comentários

Esse objeto auxiliar mantém uma lista de solicitações de aviso para um relógio de referência. A classe [**CBaseReferenceClock**](cbasereferenceclock.md) a usa para ajudar a agendar solicitações de aviso. Os relógios usam esse objeto da seguinte maneira:

1.  O relógio cria um thread de trabalho para lidar com o agendamento.
2.  O thread de trabalho chama o método [**CAMSchedule:: getuniforme**](camschedule-getevent.md) para recuperar um identificador de evento do Agendador. Ele aguarda esse evento, inicialmente com um tempo limite infinito.
3.  Para agendar uma nova solicitação de aviso, o relógio chama o método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) . Uma solicitação de aviso pode ser uma única imagem ou periódica. O Agendador mantém a lista de solicitações na ordem de tempo.
4.  Se uma solicitação for adicionada à frente da lista, o Agendador sinalizará o evento. (A lista está vazia a princípio, portanto, a primeira solicitação é garantida para sinalizar o evento.)
5.  Quando o evento é sinalizado, o thread de trabalho chama o método [**CAMSchedule:: Advise**](camschedule-advise.md) , especificando o tempo de referência atual. Se todas as solicitações pendentes tiverem expirado, o Agendador as expedirá.
6.  O método Advise retorna a hora da próxima solicitação. O thread de trabalho usa esse valor para calcular um novo valor de tempo limite.
7.  As etapas 2 6 repetim indefinidamente.
8.  Para encerrar o thread de trabalho, o relógio define um sinalizador interno e sinaliza o evento.

Na etapa 2, o evento é sinalizado ou a espera atinge o tempo limite. Se o evento for sinalizado, significa que uma nova solicitação foi adicionada à frente da lista. O thread de trabalho deve calcular um novo valor de tempo limite. Por outro lado, se a espera atingir o tempo limite, significa que uma solicitação de aviso já chegou e deve ser expedida. A chamada para Advise na etapa 5 lida com ambos os casos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dsschedule. h (incluir Fluxos. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




