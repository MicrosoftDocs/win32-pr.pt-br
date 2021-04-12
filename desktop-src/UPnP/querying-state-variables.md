---
title: Consultando variáveis de estado
description: A interface IUPnPService fornece o método QueryStateVariable, que retorna o valor de uma variável de estado especificada.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292087"
---
# <a name="querying-state-variables"></a>Consultando variáveis de estado

A interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) fornece o método [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , que retorna o valor de uma variável de estado especificada.

O fórum UPnP não incentiva o uso de [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable). Os gravadores de dispositivos foram incentivados a escrever as ações apropriadas para fornecer essas informações. Os gravadores de dispositivo não têm obrigação de implementar **QueryStateVariable**.

Consulte a seção [chamando ações](invoking-actions.md).

 

 




