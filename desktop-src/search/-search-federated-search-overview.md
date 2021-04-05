---
description: O suporte do Windows 7 para a Federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch permite que os usuários acessem e interajam com seus dados remotos no Windows Explorer.
ms.assetid: 2014b7ac-4885-4f17-b6d4-5fd95872ed59
title: Pesquisa federada no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d7718bb5215072ceeb8786f5728017ed329e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460988"
---
# <a name="federated-search-in-windows"></a>Pesquisa federada no Windows

O suporte do Windows 7 para a Federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch permite que os usuários acessem e interajam com seus dados remotos no Windows Explorer.

A lista de tópicos a seguir descreve como você pode criar um armazenamento de dados baseado na Web que pode ser pesquisado usando a pesquisa federada do Windows e habilitar a integração rica de suas fontes de dados remotas com o Windows Explorer sem precisar escrever ou implantar qualquer código do lado do cliente do Windows.

-   [Introdução com pesquisa federada no Windows](getting-started-with-federated-search-in-windows.md)
-   [Conectando seu serviço Web na pesquisa federada do Windows](-search-federated-search-web-service.md)
-   [Habilitando seu armazenamento de dados na pesquisa federada do Windows](-search-federated-search-data-store.md)
-   [Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)
-   [Seguindo as práticas recomendadas na pesquisa federada do Windows](-search-fedsearch-best.md)
-   [Implantando conectores de pesquisa na pesquisa federada do Windows](-search-federated-search-deploying.md)
-   [Esquema de descrição do conector de pesquisa](search-sconn-desc-schema-entry.md)

## <a name="additional-resources"></a>Recursos adicionais

-   O exemplo de código [OpenSearch](-search-sample-opensearch.md) demonstra como criar um serviço de pesquisa federado usando o protocolo [OpenSearch](https://github.com/dewitt/opensearch) e um arquivo de descritor de OpenSearch (. osdx) (um conector de pesquisa).
-   Para uma demonstração em vídeo de criação de um serviço Web de [OpenSearch](https://github.com/dewitt/opensearch) para um banco de dados SQL, consulte [Windows 7: capacitar os usuários a localizar, Visualizar e organizar seus dados com bibliotecas e o Gerenciador](https://channel9.msdn.com/pdc2008/PC16/).
-   Se você estiver gravando um provedor de [OpenSearch](https://github.com/dewitt/opensearch) do lado do cliente, consulte:
    -   O [desenvolvedor de OpenSearch como guiar](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) para obter mais informações sobre como se conectar a um provedor do lado do cliente usando os protocolos ou as APIs de um repositório de dados proprietário.
    -   A [visão geral da documentação de](search-sconn-desc-schema-entry.md) esquema do esquema de descrição do conector de pesquisa (. searchconnector-MS).
-   Consulte o site do [centro de download da Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) para obter o seguinte recurso para download: search Server 2008 Sample: Federated Search Connector Sample.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Guia do desenvolvedor do Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Referência do Windows Search](-search-reference-entry-page.md)
</dt> <dt>

[Exemplos de código do Windows Search](-search-samples-ovw.md)
</dt> <dt>

[Tecnologias de pesquisa relacionadas](-search-3x-wds-sampleentry.md)
</dt> <dt>

[Glossário do Windows Search](search-glossary.md)
</dt> </dl>

 

 



