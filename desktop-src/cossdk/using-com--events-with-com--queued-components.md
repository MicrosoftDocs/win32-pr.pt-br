---
description: O serviço de eventos COM+ é usado para gerenciar a entrega de eventos de editores para assinantes.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Usando eventos COM+ com componentes em fila COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762185"
---
# <a name="using-com-events-with-com-queued-components"></a>Usando eventos COM+ com componentes em fila COM+

O serviço de eventos COM+ é usado para gerenciar a entrega de eventos de editores para assinantes. O serviço de componentes na fila COM+ pode ser usado para tornar o Publicador e o tempo de processamento do assinante independentes, colocando a mensagem do Publicador em fila e depois repetindo-o no Assinante. Se você precisa ou não usar o serviço de componentes na fila depende da lógica de negócios subjacente do seu aplicativo. Se você precisar ter eventos independentes de tempo, poderá criá-los usando o serviço de eventos COM+ com o serviço de componentes em fila do COM+.

> [!Note]  
> Para obter informações adicionais sobre como usar o serviço de componentes na fila do COM+, consulte [componentes em fila do com+](com--queued-components.md).

 

O serviço de componentes na fila mantém a invocação de ordem de método em uma única mensagem. O gravador executa em lotes todas as invocações de método em uma mensagem e, em seguida, o Player invoca esses métodos na ordem em que a mensagem é processada.

Um gravador e um player de componentes em fila podem ser posicionados em qualquer um dos dois locais a seguir:

-   Entre o editor e o objeto de evento
-   Entre o objeto de evento e o Assinante

Se você posicionar o gravador e o Player entre o editor e o objeto de evento, estará tornando o componente de [classe de evento](the-com--event-class-object.md) queuable. O componente de classe de evento deve ser marcado para enfileiramento e ser ativado pelo Player em um processo separado do Publicador.

Para entregar eventos de forma assíncrona, redija o gravador e o Player entre o objeto de evento e o Assinante e defina o atributo enfileirado do objeto de assinatura. Isso define SubscriberMoniker da seguinte maneira: "Queue:/New:/ {12345678-1234-1234-1234-123456789012} ".

Há uma ordem de implicação de entrega a ser considerada ao usar componentes enfileirados em uma situação de evento. Como o serviço de componentes na fila registra e reproduz todas as chamadas dentro do tempo de vida de um único objeto em uma mensagem, todas as chamadas são reproduzidas na ordem em que foram feitas. No entanto, se houver mais de uma sessão com mais de um objeto, a ordem não poderá ser garantida. Se a ordem for importante, verifique se as chamadas que precisam ser reproduzidas na ordem residem na mesma instância de objeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtrando eventos no COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publicando e fornecendo eventos no COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Assinaturas](subscriptions.md)
</dt> <dt>

[O objeto de classe de evento COM+](the-com--event-class-object.md)
</dt> </dl>

 

 



