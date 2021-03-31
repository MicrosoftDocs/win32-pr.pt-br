---
description: A API do sensor pode fornecer notificações de eventos.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Sobre eventos de API do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829640"
---
# <a name="about-sensor-api-events"></a>Sobre eventos de API do sensor

A API do sensor pode fornecer notificações de eventos.

Ao se registrar para receber eventos, por meio de [**ISensor:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) ou [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), você deve fornecer um ponteiro para uma interface de retorno de chamada. Você deve implementar os métodos da interface de retorno de chamada em seu código. A API do sensor define as seguintes interfaces de retorno de chamada:

-   [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents). Implemente essa interface para receber eventos de sensores. Os sensores podem notificar seu aplicativo sobre novos dados, alterações no estado do sensor, desconexão do sensor e eventos personalizados definidos pelo fabricante do sensor.
-   [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents). Implemente essa interface para receber eventos do Gerenciador de sensores. O Gerenciador de sensor pode notificar seu aplicativo quando um sensor se conecta e, portanto, pode estar disponível para uso.

Você pode cancelar as notificações de eventos chamando [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) novamente, desta vez passando um valor **nulo** por meio do parâmetro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando eventos de API do sensor](using-sensor-api-events.md)
</dt> </dl>

 

 
