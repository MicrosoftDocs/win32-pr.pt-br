---
description: O TAPI 3 dá suporte à integração de interfaces específicas do provedor de serviços aos objetos padrão, permitindo que os aplicativos aproveitem a funcionalidade específica do provedor.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: interfaces Provider-Specific dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09290bf6d2ade55a9e9d2b0f51315acfc5488805b6c19b23679e00708ddaed45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060564"
---
# <a name="provider-specific-interfaces"></a>interfaces Provider-Specific dados

O TAPI 3 dá suporte à integração de interfaces específicas do provedor de serviços aos objetos padrão, permitindo que os aplicativos aproveitem a funcionalidade específica do provedor. Além disso, o TAPI 3 permite que os provedores de serviços entreguem eventos específicos do fornecedor a aplicativos como objetos COM pela mesma interface na qual o aplicativo recebe eventos padrão.

A TAPI atinge essa integração agregando objetos específicos do provedor com os objetos padrão – TAPI, Endereço, Terminal, Chamada e CallHub – e expedindo ou delegando métodos desconhecidos para esses objetos específicos do provedor.

Por exemplo, um provedor de serviços pode permitir que os aplicativos obtenham informações sobre uma chamada além do que é exposto pela interface [**ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) O fornecedor deve definir uma interface que permita que os aplicativos façam essas consultas extras e implementem essa interface em um objeto . Esse objeto também implementa uma interface de consulta de informações do fornecedor para que um aplicativo possa descobrir quais tipos de funções específicas do provedor podem estar disponíveis.

Quando o aplicativo obtém uma referência a um objeto de chamada, o aplicativo pode usar a nova interface específica do provedor e seus métodos como se fossem implementados pelo próprio objeto de chamada.

Confira [Referência da MSPI (Interface](media-service-provider-interface-mspi-reference.md) do Provedor de Serviços de Mídia) para ver uma lista de todas as interfaces padrão do MSP.

Consulte [Interfaces IPConf MSP](ipconf-msp-interfaces.md) para ver uma lista de todas as interfaces específicas para o IPConf MSP.

 

 



