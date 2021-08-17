---
title: Consultando variáveis de estado
description: A interface IUPnPService fornece o método QueryStateVariable, que retorna o valor de uma variável de estado especificada.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aa3baecf7bd1fd01537f3a461d1e615f539c6c7ce633621a736419942bcd4ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137179"
---
# <a name="querying-state-variables"></a>Consultando variáveis de estado

A interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) fornece o método [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , que retorna o valor de uma variável de estado especificada.

O fórum UPnP não incentiva o uso de [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable). Os gravadores de dispositivos foram incentivados a escrever as ações apropriadas para fornecer essas informações. Os gravadores de dispositivo não têm obrigação de implementar **QueryStateVariable**.

Consulte a seção [chamando ações](invoking-actions.md).

 

 




