---
description: Um objeto de evento é um objeto de sincronização cujo estado pode ser definido explicitamente para sinalizado pelo uso da função SetEvent. A seguir estão os dois tipos de objeto de evento.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Objetos de evento (sincronização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365b42bb7550507fe3522f07d950dac74c88843d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753701"
---
# <a name="event-objects-synchronization"></a>Objetos de evento (sincronização)

Um *objeto de evento* é um objeto de sincronização cujo estado pode ser definido explicitamente para sinalizado pelo uso da função [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) . A seguir estão os dois tipos de objeto de evento.



| Objeto             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento de redefinição manual | Um objeto de evento cujo estado permanece sinalizado até que seja explicitamente redefinido para não sinalizado pela função [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) . Enquanto ele é sinalizado, qualquer número de threads em espera ou threads que especificam posteriormente o mesmo objeto de evento em uma das [funções de espera](wait-functions.md)podem ser liberados.                                                                                                        |
| Evento de redefinição automática   | Um objeto de evento cujo estado permanece sinalizado até que um único thread de espera seja liberado, quando o sistema automaticamente define o estado como não sinalizado. Se nenhum thread estiver aguardando, o estado do objeto de evento permanecerá sinalizado. Se mais de um thread estiver aguardando, um thread em espera será selecionado. Não assuma uma ordem FIFO (primeiro a entrar, primeiro a sair). Eventos externos, como APCs de modo kernel, podem alterar a ordem de espera.<br/> |



 

O objeto de evento é útil ao enviar um sinal para um thread indicando que ocorreu um evento específico. Por exemplo, em entrada e saída sobrepostas, o sistema define um objeto de evento especificado para o estado sinalizado quando a operação sobreposta foi concluída. Um único thread pode especificar objetos de evento diferentes em várias operações de Overlapped simultâneas e, em seguida, usar uma das [funções de espera](wait-functions.md) de vários objetos para aguardar o estado de qualquer um dos objetos de evento ser sinalizado.

Um thread usa a função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) ou [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) para criar um objeto de evento. O thread de criação especifica o estado inicial do objeto e se é um objeto de evento de redefinição manual ou de redefinição automática. O thread de criação também pode especificar um nome para o objeto de evento. Os threads em outros processos podem abrir um identificador para um objeto de evento existente especificando seu nome em uma chamada para a função [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa) . Para obter informações adicionais sobre nomes de mutex, evento, semáforo e objetos de temporizador, consulte [sincronização entre processos](interprocess-synchronization.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando objetos de evento](using-event-objects.md)
</dt> </dl>

 

 
