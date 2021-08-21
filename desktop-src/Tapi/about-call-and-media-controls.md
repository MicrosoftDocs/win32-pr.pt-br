---
description: Os controles de mídia e de chamada TAPI 3 são um conjunto genérico de objetos COM, interfaces e métodos para fazer chamadas entre dois ou mais computadores.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: Sobre controles de chamada e de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5405dce096c1f2e4a9eeffa4625ad0aa557b141ea4f6004f6c4283a97cc04d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872947"
---
# <a name="about-call-and-media-controls"></a>Sobre controles de chamada e de mídia

Os controles de mídia e de chamada TAPI 3 são um conjunto genérico de objetos COM, interfaces e métodos para fazer chamadas entre dois ou mais computadores. No contexto da TAPI 3, a *chamada* se refere não apenas à transmissão de voz pela PSTN (rede telefônica pública comutada), mas a qualquer mecanismo de médio e transporte para o qual os provedores de serviço existem: por exemplo, uma conferência de multicast de multimídia em execução em uma intranet corporativa.

Os cinco objetos principais na arquitetura de controle de mídia e chamada TAPI 3 são [TAPI](tapi-object.md), [endereço](address-object.md), [terminal](terminal-object.md), [Call](call-object.md)e [CallHub](callhub-object.md). Além disso, o provisionamento foi feito para [interfaces específicas do provedor](provider-specific-interfaces.md).

O diagrama a seguir ilustra como esses objetos interagem.

![interações entre os objetos de controle de mídia e de chamada TAPI 3,0](images/sdkobj2.png)

## <a name="features"></a>Recursos

-   Abstrai a funcionalidade de chamada e de mídia para permitir que protocolos de comunicação diferentes e aparentemente incompatíveis exponham uma interface comum aos aplicativos.
-   Com base no Component Object Model (COM), para que os aplicativos possam ser escritos em praticamente qualquer linguagem. Se você precisar de informações adicionais sobre COM, consulte o SDK (Software Development Kit) da plataforma.
-   Controle de chamada fornecido por TSPs (provedores de serviços de telefonia), que implementam mecanismos específicos de transporte.
-   Controle de mídia fornecido pelos provedores de serviços de mídia (MSPs). MSPs atual use DirectShow. DirectShow é um sistema modular de componentes conectáveis chamados filtros, organizados em uma configuração chamada de grafo de filtro. O Gerenciador de gráfico de filtro supervisiona a conexão desses filtros e controla o fluxo de dados do fluxo. se você precisar de informações adicionais sobre DirectShow, consulte o SDK da plataforma.

 

 



