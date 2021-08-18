---
description: criando um filtro de Publisher
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: criando um filtro de Publisher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2cf3391cd331f7d81c3bb7ff467c140a78b0c8e30fb609ea655596dfe745a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128788"
---
# <a name="creating-a-publisher-filter"></a>criando um filtro de Publisher

Há dois métodos para estabelecer o filtro de editor: usando a propriedade MultiPublisherFilterCLSID da classe de evento ou usando [**IEventControl:: SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter).

-   Como ele permite compor o objeto de evento com o serviço de [componentes em fila com+](com--queued-components.md) , o método preferencial é usar a propriedade MultiPublisherFilterCLSID na classe de evento para definir o filtro de editor. Isso estabelece um objeto de filtro para todos os métodos das interfaces de evento de um objeto de evento. O objeto de evento ativa o filtro do Publicador quando o objeto da classe de evento é instanciado usando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).
-   Você também pode usar [**SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter). No entanto, se você escolher esse método, a interface não será queuable e, portanto, não poderá usar o objeto de evento com o serviço de componentes em fila COM+ entre o Publicador e o objeto de classe de evento. Para obter informações adicionais sobre como usar o serviço de componentes na fila com eventos COM+, consulte [usando eventos com+ com componentes em fila com+](using-com--events-with-com--queued-components.md).

Um evento pode ter um ou mais objetos de filtro ou nenhum. Os objetos de filtro do Publicador devem dar suporte a [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) ou [**IMultiInterfacePublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter), dependendo se você tiver uma única interface de acionamento ou várias interfaces de acionamento no objeto da classe de evento. As interfaces **IPublisherFilter** e **IMultiInterfacePublisherFilter** especificam um método **Initialize** . O método **Initialize** é chamado pelo objeto da classe de evento imediatamente após a criação do objeto Filter.

Os eventos COM+ tentam invocar dois métodos no filtro. Primeiro, ele chama [**IPublisherFilter::P reparetofire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) e passa um ponteiro de interface [**IFiringControl**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) para o filtro. Em seguida, ele consulta o objeto de filtro para a interface de evento. Se o filtro oferecer suporte à interface de evento, ele invocará um método nele. Isso fornece acesso aos parâmetros do Publicador para um evento. O filtro pode usar esses parâmetros para determinar quais assinaturas são acionadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtrando eventos no COM+](filtering-events-in-com-.md)
</dt> </dl>

 

 
