---
description: A TAPI 3 dá suporte à integração de interfaces específicas do provedor de serviço nos objetos padrão, permitindo que os aplicativos tirem proveito da funcionalidade específica do provedor.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Interfaces Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011548"
---
# <a name="provider-specific-interfaces"></a>Interfaces Provider-Specific

A TAPI 3 dá suporte à integração de interfaces específicas do provedor de serviço nos objetos padrão, permitindo que os aplicativos tirem proveito da funcionalidade específica do provedor. Além disso, a TAPI 3 permite que os provedores de serviços forneçam eventos específicos do fornecedor a aplicativos como objetos COM na mesma interface em que o aplicativo recebe eventos padrão.

A TAPI alcança essa integração por meio da agregação de objetos específicos do provedor com os objetos padrão – TAPI, endereço, terminal, chamada e CallHub – e expedição ou delegação de métodos desconhecidos a esses objetos específicos do provedor.

Por exemplo, um provedor de serviços pode permitir que os aplicativos obtenham informações sobre uma chamada além do que é exposto pela interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) . O fornecedor deve definir uma interface que permita que os aplicativos façam essas consultas adicionais e implementem essa interface em um objeto. Esse objeto também implementa uma interface de consulta de informações de fornecedor para que um aplicativo possa descobrir quais tipos de funções específicas do provedor podem estar disponíveis.

Quando o aplicativo obtém uma referência a um objeto de chamada, o aplicativo pode usar a nova interface específica do provedor e seus métodos como se eles estivessem implementados pelo próprio objeto de chamada.

Consulte [referência da MSPI (interface do provedor de serviços de mídia)](media-service-provider-interface-mspi-reference.md) para obter uma lista de todas as interfaces padrão msp.

Consulte [IPConf MSP interfaces](ipconf-msp-interfaces.md) para obter uma lista de todas as interfaces específicas para o IPConf msp.

 

 



