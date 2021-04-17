---
description: Publicação de um evento
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Publicação de um evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782627"
---
# <a name="publishing-an-event"></a>Publicação de um evento

Para publicar um evento, basta criar uma instância de um objeto de evento chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou o método **CreateObject** do Microsoft Visual Basic usando EventClassID ou EventClassName como um argumento. O Publicador chama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto de evento para obter as interfaces suportadas pelo objeto de classe de evento e invoca um método no objeto Event por meio da interface para publicar o evento. Em seguida, o sistema de eventos publica eventos na classe de evento CLSID \_ EventObjectChange com a ID de interface IID \_ IEventObjectChange.

Para dar suporte à entrega de eventos a vários assinantes, os métodos de classe de evento devem conter apenas em parâmetros.

Usando a Propriedade FireInParallel do objeto de [classe de evento](the-com--event-class-object.md) , os editores podem solicitar que o sistema de eventos use vários threads para entregar um evento a mais de um assinante. A seleção de um mecanismo de entrega em paralelo não garante a entrega simultânea do evento a vários assinantes, mas instrui o serviço de eventos COM+ a permitir que isso aconteça.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Publicando e fornecendo eventos no COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
