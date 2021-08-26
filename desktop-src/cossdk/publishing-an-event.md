---
description: Publicação de um evento
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Publicação de um evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724dc94ddf9cc25ec3b11cc31376805241e9d6d67250f8a494f8b417b9d201a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990496"
---
# <a name="publishing-an-event"></a>Publicação de um evento

Para publicar um evento, basta criar uma instanância de um objeto de evento chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou o método **CreateObject** do Microsoft Visual Basic usando EventClassID ou EventClassName como um argumento. O editor chama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto de evento para obter as interfaces com suporte pelo objeto de classe de evento e invoca um método no objeto de evento por meio da interface para publicar o evento. Em seguida, o sistema de eventos publica eventos na classe de evento CLSID \_ EventObjectChange com a ID da interface \_ IID IEventObjectChange.

Para dar suporte à entrega de eventos para vários assinantes, os métodos de classe de evento devem conter somente em parâmetros.

Usando a propriedade FireInParallel [](the-com--event-class-object.md) do objeto de classe de evento, os editores podem solicitar que o sistema de eventos use vários threads para entregar um evento a mais de um assinante. Selecionar um mecanismo de entrega em paralelo não garante a entrega simultânea do evento para vários assinantes, mas instrui o serviço de eventos COM+ a permitir que isso aconteça.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Publicando e entregando eventos em COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
