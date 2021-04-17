---
description: A classe CBaseReferenceClock Implementa um relógio de referência.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: Classe CBaseReferenceClock (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770293"
---
# <a name="cbasereferenceclock-class"></a>Classe CBaseReferenceClock

![hierarquia de classe CBaseReferenceClock](images/rclock01.png)

A `CBaseReferenceClock` classe implementa um relógio de referência.



| Variáveis de membro protegido                                                         | Descrição                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_pSchedule m**](cbasereferenceclock-m-pschedule.md)                            | Objeto [**CAMSchedule**](camschedule.md) que lida com tarefas de agendamento para o relógio. |
| Métodos Protegidos                                                                  | Descrição                                                                            |
| [**~ CBaseReferenceClock**](cbasereferenceclock--cbasereferenceclock.md)           | Método destruidor.                                                                     |
| Métodos públicos                                                                     | Descrição                                                                            |
| [**CBaseReferenceClock**](cbasereferenceclock-cbasereferenceclock.md)             | Método de construtor.                                                                    |
| [**Getparticulartime**](cbasereferenceclock-getprivatetime.md)                       | Recupera o tempo real do relógio.                                                |
| [**SetTimeDelta**](cbasereferenceclock-settimedelta.md)                           | Ajusta a hora interna do relógio.                                                       |
| [**Getschedule**](cbasereferenceclock-getschedule.md)                             | Recupera um ponteiro para o objeto de agendamento do relógio.                                  |
| [**TriggerThread**](cbasereferenceclock-triggerthread.md)                         | Ativa o thread de trabalho que lida com o agendamento.                                    |
| Métodos IReferenceClock                                                            | Descrição                                                                            |
| [**GetTime**](cbasereferenceclock-gettime.md)                                     | Recupera o tempo de referência atual.                                                  |
| [**Aviso de**](cbasereferenceclock-advisetime.md)                               | Cria uma solicitação de aviso de uma imagem.                                                     |
| [**AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md)                       | Cria uma solicitação de aviso periódica.                                                     |
| [**Cancelar**](cbasereferenceclock-unadvise.md)                                   | Remove uma solicitação de aviso pendente.                                                      |
| Métodos IReferenceClockTimerControl                                                | Descrição                                                                            |
| [**GetDefaultTimerResolution**](cbasereferenceclock-getdefaulttimerresolution.md) | Retorna a resolução atual do temporizador do relógio de referência.                         |
| [**SetDefaultTimerResolution**](cbasereferenceclock-setdefaulttimerresolution.md) | Define a resolução do timer do relógio de referência.                                    |
| Funções auxiliares                                                                   | Descrição                                                                            |
| [**ConvertToMilliseconds**](converttomilliseconds.md)                             | Converte um tempo de referência em milissegundos.                                             |



 

## <a name="remarks"></a>Comentários

Essa classe implementa um relógio de referência que dá suporte às interfaces [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) e [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) . Se um filtro puder fornecer um relógio de referência para o grafo de filtro, por exemplo, ao acessar um dispositivo de hardware, ele poderá usar essa classe para implementar o relógio.

O `CBaseReferenceClock` objeto mantém dois valores de hora distintos:

-   Internamente, o método [**CBaseReferenceClock:: Getparticulartime**](cbasereferenceclock-getprivatetime.md) retorna o tempo real mantido pelo relógio.
-   Externamente, o método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) retorna o tempo de referência para o grafo de filtro.

É válido para a execução do relógio interno em breves períodos. Por exemplo, se o relógio for para frente, o filtro poderá ajustá-lo para trás. (Consulte [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md).) O método **getTime** usa os valores de tempo relatados por **getprivadotime**. No entanto, o tempo de referência é um aumento monotônico; em outras palavras, ele nunca é executado retroativamente. Portanto, se o relógio interno for executado retroativamente, **getTime** continuará relatando o tempo antigo até que o relógio interno se ajuste.

Por exemplo, os dois métodos podem retornar as seguintes sequências:

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

No terceiro tique do relógio, o relógio interno salta para o 103. O método **getTime** continua a relatar 106 até que o relógio interno seja atualizado.

Por padrão, **GetPrivateTime** retorna a hora do sistema, por meio de uma chamada para a função **timeGetTime** . Um filtro que está fornecendo um relógio de referência de um dispositivo externo pode executar um dos seguintes procedimentos:

-   Substitua **GetPrivateTime** para retornar a hora do dispositivo.
-   Monitore a discrepância entre a hora do dispositivo e a hora do sistema e chame **SetTimeDelta** para fazer correções.

Essa classe usa um objeto [**CAMSchedule**](camschedule.md) para lidar com o agendamento de solicitações de aviso. Para obter detalhes, consulte a documentação da classe **CAMSchedule** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




