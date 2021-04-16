---
description: O objeto sensor representa um sensor específico.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: O objeto sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754115"
---
# <a name="the-sensor-object"></a>O objeto sensor

O objeto sensor representa um sensor específico.

A API do sensor representa cada sensor como um objeto de sensor. Você pode trabalhar com um objeto de sensor específico por meio de sua interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) . Essa interface permite que você:

-   Recupere metadados sobre o sensor, como sua ID, tipo ou nome amigável.
-   Recupere informações sobre os dados específicos que o sensor pode fornecer.
-   Recupere os dados de forma síncrona.
-   Recuperar informações de estado, como se o sensor está pronto.
-   Especifique quais eventos seu programa receberá.
-   Especifique a interface de retorno de chamada que a API do sensor pode usar para fornecer ao seu programa notificações de eventos.

 

 



