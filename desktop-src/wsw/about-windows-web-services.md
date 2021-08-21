---
title: Sobre Windows Web services
description: O Windows API de Serviços Web é uma API em camadas e pode ser figurada da seguinte forma.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ed82d21568b407d3fc4fd33b561f238fc21f8ce4a38fbb6bf197016d0c4f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026230"
---
# <a name="about-windows-web-services"></a>Sobre Windows Web services

A Windows API de Serviços Web é uma API em camadas e pode ser figurada da seguinte forma

![Diagrama mostrando as camadas e áreas entre camadas da API Windows Web Services.](images/apistack.png)

O WWSAPI é uma API em camadas. Esperamos que a maioria dos desenvolvedores direciona o Modelo de Serviço, que é um modelo de programação baseado em método. No Modelo de Serviço, o Host do Serviço fornece o modelo de programação do lado do servidor, enquanto o Proxy de Serviço fornece o modelo de programação do lado do cliente.

Cada camada expõe um conjunto de APIs e tipos que podem ser usados com APIs dessa camada.

## <a name="service-model"></a>Modelo de serviço

A camada de nível superior chamada [Modelo de Serviço](service-model-layer-overview.md) fornece um modelo de programação baseado em método e é o modelo mais fácil de usar. No Modelo de Serviço, o Host do [Serviço](service-host.md) fornece o modelo de programação do lado do servidor, enquanto o [Proxy](service-proxy.md) de Serviço fornece o modelo de programação do lado do cliente. [O](context.md) contexto é usado no Modelo de Serviço para passar um estado relevante disponível para a operação de serviço e/ou o retorno de chamada quando ele é invocado. E [o Contrato de](contract.md) Serviço é usado para especificar um contrato de serviço em um ponto de extremidade exposto no serviço. Os seguintes componentes e operações fazem parte da Camada de Serviço:

-   [Host de Serviço](service-host.md)
-   [Proxy de Serviço](service-proxy.md)
-   [Contexto](context.md)
-   [Contrato](contract.md)
-   [Metadados de serviço](service-metadata.md)

## <a name="channel-layer"></a>Camada de canal

O Modelo de Serviço é criado com base em uma camada de canal, que fornece flexibilidade total, mas é mais difícil de usar. Os seguintes componentes e operações fazem parte da Camada de Canal:

-   [Message](message.md)
-   [Channel](channel.md)
-   [Ouvinte](listener.md)
-   [Falhas](faults.md)
-   [URL](url.md)
-   [Segurança](security-overview.md)
-   [Importação de metadados](metadata-import.md)

## <a name="xml-layer"></a>Camada XML

A Camada de Canal é, por sua vez, criada com base em uma estrutura XML leve, que inclui a desserlização de tipos de dados C. Os seguintes componentes e operações fazem parte da camada XML:

-   [XML Writer](xml-writer.md)
-   [Leitor de XML](xml-reader.md)
-   [XML Buffer](xml-buffer.md)
-   [Serialização](serialization.md)
-   [Suporte à linguagem XML](xml-language-support.md)

## <a name="common-to-all-layers"></a>Comum a todas as camadas

Veja a seguir tópicos que se aplicam a qualquer uma das três camadas:

-   [Erros](errors.md)
-   [Modelo assíncrono](asynchronous-model.md)
-   [Acesso thread-safe](thread-safety.md)
-   [Rastreamento](tracing.md)
-   [Cancelamento](cancellation.md)
-   [Utilitários](utilities.md)
-   [Depuração](debugging.md)
-   [Ferramenta do compilador Wsutil](wsutil-compiler-tool.md)
-   [Pilha](heap.md)

## <a name="examples"></a>Exemplos

Para obter mais informações sobre elementos de API, [consulte Windows Web Services Reference](windows-web-services-reference.md). Para ver exemplos de como usar a API, consulte [Usando Windows Web Services.](using-windows-web-services.md)

 

 




