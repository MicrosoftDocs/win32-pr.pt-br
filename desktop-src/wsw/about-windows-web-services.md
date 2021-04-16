---
title: Sobre os serviços Web do Windows
description: A API de serviços Web do Windows é uma API em camadas e pode ser a imagem a seguir.
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104567295"
---
# <a name="about-windows-web-services"></a>Sobre os serviços Web do Windows

A API de serviços Web do Windows é uma API em camadas e pode ser apresentada da seguinte maneira

![Diagrama mostrando as camadas e áreas de camada cruzada da API dos serviços Web do Windows.](images/apistack.png)

O WWSAPI é uma API em camadas. Esperamos que a maioria dos desenvolvedores direcione o modelo de serviço, que é um modelo de programação baseado em método. No modelo de serviço, o host de serviço fornece o modelo de programação do lado do servidor, enquanto o proxy de serviço fornece o modelo de programação do lado do cliente.

Cada camada expõe um conjunto de APIs e tipos que podem ser usados com APIs dessa camada.

## <a name="service-model"></a>Modelo de serviço

A camada de nível superior chamada [modelo de serviço](service-model-layer-overview.md) fornece um modelo de programação baseado em método e é o modelo mais fácil de usar. No modelo de serviço, o [host de serviço](service-host.md) fornece o modelo de programação do lado do servidor, enquanto o [proxy de serviço](service-proxy.md) fornece o modelo de programação do lado do cliente. O [contexto](context.md) é usado dentro do modelo de serviço para passar um estado relevante disponível para a operação de serviço e/ou o retorno de chamada quando ele é invocado. E o [contrato de serviço](contract.md) é usado para especificar um contrato de serviço em um ponto de extremidade exposto no serviço. Os seguintes componentes e operações fazem parte da camada de serviço:

-   [Host de serviço](service-host.md)
-   [Proxy de serviço](service-proxy.md)
-   [Contexto](context.md)
-   [Contrato](contract.md)
-   [Metadados de serviço](service-metadata.md)

## <a name="channel-layer"></a>Camada de canal

O modelo de serviço é criado com base em uma camada de canal, que fornece flexibilidade total, mas é mais difícil de usar. Os seguintes componentes e operações fazem parte da camada de canal:

-   [Message](message.md)
-   [Channel](channel.md)
-   [Ouvinte](listener.md)
-   [Falhas](faults.md)
-   [URL](url.md)
-   [Segurança](security-overview.md)
-   [Importação de metadados](metadata-import.md)

## <a name="xml-layer"></a>Camada XML

A camada de canal, por sua vez, é criada com base em uma estrutura XML leve, que inclui a desserialização de tipos de dados C. Os seguintes componentes e operações fazem parte da camada XML:

-   [Gravador de XML](xml-writer.md)
-   [Leitor de XML](xml-reader.md)
-   [Buffer XML](xml-buffer.md)
-   [Série](serialization.md)
-   [Suporte à linguagem XML](xml-language-support.md)

## <a name="common-to-all-layers"></a>Comum a todas as camadas

Veja a seguir os tópicos que se aplicam a qualquer uma das três camadas:

-   [Erros](errors.md)
-   [Modelo assíncrono](asynchronous-model.md)
-   [Acesso thread-safe](thread-safety.md)
-   [Rastreamento](tracing.md)
-   [Cancelamento](cancellation.md)
-   [Utilitários](utilities.md)
-   [Depuração](debugging.md)
-   [Ferramenta de compilador do Wsutil](wsutil-compiler-tool.md)
-   [Áreas](heap.md)

## <a name="examples"></a>Exemplos

Para obter mais informações sobre elementos de API, consulte [referência de serviços Web do Windows](windows-web-services-reference.md). Para obter exemplos de como usar a API, consulte [usando os serviços Web do Windows](using-windows-web-services.md).

 

 




