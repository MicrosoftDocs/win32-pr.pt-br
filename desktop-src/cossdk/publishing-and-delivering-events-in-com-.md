---
description: Para publicar um evento, basta criar uma instância de um objeto de classe de evento e invocar o método desejado; para obter instruções detalhadas sobre como fazer isso no código, consulte publicando um evento.
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: Publicando e fornecendo eventos no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646488"
---
# <a name="publishing-and-delivering-events-in-com"></a>Publicando e fornecendo eventos no COM+

Para publicar um evento, basta criar uma instância de um objeto de [classe de evento](the-com--event-class-object.md) e invocar o método desejado; para obter instruções detalhadas sobre como fazer isso no código, consulte [publicando um evento](publishing-an-event.md).

Quando um Publicador dispara um evento, o serviço de eventos COM+ pesquisa o banco de dados de assinatura para localizar todos os assinantes que registraram assinaturas na classe de evento instanciado. Ele se conecta a esses assinantes (por criação direta, monikers ou componentes enfileirados) e chama o método. Para dar suporte a mais de uma notificação de assinante para um evento, os métodos podem conter apenas em parâmetros e devem retornar apenas valores de êxito ou falha de **HRESULT** .

> [!Note]  
> Esta versão dos eventos COM+ não dá suporte a um repositório de eventos distribuído. Um Assinante deve assinar um evento em cada computador do qual deseja receber a notificação. Como alternativa, você pode registrar o objeto de classe de evento e as assinaturas em um computador central e instanciar esse objeto de classe de evento a partir dos computadores remotos nos quais você publica eventos. A entrega de eventos é fornecida pelo DCOM ou pelo serviço de componentes em fila do COM+. Para obter mais informações sobre como usar o serviço de componentes na fila COM+, consulte [usando eventos com+ com componentes em fila do com+](using-com--events-with-com--queued-components.md).

 

Por padrão, o serviço de eventos COM+ dispara eventos um de cada vez, em nenhuma ordem determinada ou repetitiva. Os Publicadores que precisam controlar a ordem em que os assinantes recebem um evento podem implementar um filtro de editor. (Para obter mais informações, consulte [Filtering Events in com+](filtering-events-in-com-.md).)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtrando eventos no COM+](filtering-events-in-com-.md)
</dt> <dt>

[Assinaturas](subscriptions.md)
</dt> <dt>

[O objeto de classe de evento COM+](the-com--event-class-object.md)
</dt> <dt>

[Usando eventos COM+ com componentes em fila COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



