---
description: Um objeto de evento é um objeto de sincronização cujo estado pode ser definido explicitamente como sinalizado pelo uso da função SetEvent. A seguir estão os dois tipos de objeto de evento.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Objetos de evento (sincronização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ef4f5102df91cabb76529c9d4a9958859418aa
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102125"
---
# <a name="event-objects-synchronization"></a>Objetos de evento (sincronização)

Um *objeto de* evento é um objeto de sincronização cujo estado pode ser definido explicitamente como sinalizado pelo uso da função [**SetEvent.**](/windows/win32/api/synchapi/nf-synchapi-setevent) A seguir estão os dois tipos de objeto de evento.



| Objeto             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento de redefinição manual | Um objeto de evento cujo estado permanece sinalizado até que seja redefinido explicitamente para não sinalizado pela [**função ResetEvent.**](/windows/win32/api/synchapi/nf-synchapi-resetevent) Embora seja sinalizado, qualquer número de threads em espera ou threads que especifiquem subsequentemente o mesmo objeto de evento em uma das funções [de](wait-functions.md)espera , pode ser liberado.                                                                                                        |
| Evento de redefinição automática   | Um objeto de evento cujo estado permanece sinalizado até que um único thread em espera seja liberado, momento em que o sistema define automaticamente o estado como não sinalizado. Se nenhum thread estiver aguardando, o estado do objeto de evento permanecerá sinalizado. Se mais de um thread estiver aguardando, um thread em espera será selecionado. Não suponha uma ordem FIFO (primeiro a entrar, primeiro a sair). Eventos externos, como APCs de modo kernel, podem alterar a ordem de espera.<br/> |



 

O objeto de evento é útil no envio de um sinal para um thread que indica que ocorreu um evento específico. Por exemplo, na entrada e na saída sobrepondo, o sistema define um objeto de evento especificado para o estado sinalizado quando a operação sobreexplorada foi concluída. Um único thread pode especificar objetos de evento diferentes em várias operações sobrecarradas [simultâneas](wait-functions.md) e, em seguida, usar uma das funções de espera de vários objetos para aguardar o estado de qualquer um dos objetos de evento a ser sinalizado.

Um thread usa a [**função CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) ou [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) para criar um objeto de evento. O thread de criação especifica o estado inicial do objeto e se ele é um objeto de evento de redefinição manual ou de redefinição automática. O thread de criação também pode especificar um nome para o objeto de evento. Threads em outros processos podem abrir um identificador para um objeto de evento existente especificando seu nome em uma chamada para a [**função OpenEvent.**](/windows/win32/api/synchapi/nf-synchapi-openeventa) Para obter informações adicionais sobre nomes para objetos mutex, evento, semáforo e temporizador, consulte [Sincronização entre processos](interprocess-synchronization.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando objetos de evento](using-event-objects.md)
</dt> </dl>

 

 
