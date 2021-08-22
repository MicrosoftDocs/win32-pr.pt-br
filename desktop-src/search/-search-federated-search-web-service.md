---
description: Este tópico descreve as etapas envolvidas na conexão de um serviço Web entre o armazenamento de dados e o Windows Federated Search e como enviar consultas e retornar resultados da pesquisa no RSS ou Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Conectando seu serviço Web Windows Pesquisa Federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4980b2d62f766806cf89856b8ef9e5231284be0dfea3258d2e5d5155e7a46598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456716"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>Conectando seu serviço Web Windows Pesquisa Federada

Este tópico descreve as etapas envolvidas na conexão de um serviço Web entre o armazenamento de dados e o Windows Federated Search e como enviar consultas e retornar resultados da pesquisa no RSS ou Atom.

Este tópico é organizado da seguinte forma:

-   [Conexão Seu serviço Web](#connect-your-web-service)
-   [Registrar um armazenamento de dados remoto existente](#register-an-existing-remote-data-store)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="connect-your-web-service"></a>Conexão Seu serviço Web

**Para conectar o serviço Web do seu armazenamento de dados à pesquisa federada, execute as seguintes etapas:**

1.  Crie um arquivo .osdx.
2.  Fornecer o arquivo .osdx aos usuários para que eles possam adicionar o serviço sob demanda abrindo o arquivo .osdx.
3.  Gere um conector de pesquisa e implante-o ativamente em sua empresa.

## <a name="register-an-existing-remote-data-store"></a>Registrar um armazenamento de dados remoto existente

Um usuário registra um novo armazenamento de dados remoto com Windows Federado abrindo um arquivo OpenSearch Description (.osdx). Quando o usuário faz isso, os seguintes eventos ocorrem:

1.  Um arquivo .searchconnector-ms (conector de pesquisa) é criado na pasta Windows Searches (%userprofile%/Searches).
2.  Um atalho para o arquivo .searchconnector-ms é criado na pasta Links (%userprofile%/Links).
3.  Um atalho é exibido no painel **favoritos** de navegação do Windows Explorer, permitindo que o usuário navegue até o novo armazenamento de dados e consulte o serviço Web.

> [!Note]  
> Um armazenamento de dados que já tem um [serviço](https://github.com/dewitt/opensearch) Web OpenSearch que é compatível com o Windows Federated Search pode ser adicionado ao Windows Explorer quando um usuário abre um arquivo .osdx.

 

## <a name="additional-resources"></a>Recursos adicionais

Para obter informações adicionais sobre como implementar a federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch no Windows 7 e posterior, consulte "Recursos adicionais" em [Pesquisa Federada](/previous-versions//dd742958(v=vs.85))no Windows .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Ponto de Partida com a Pesquisa Federada Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Habilitando seu armazenamento de dados Windows Pesquisa Federada](-search-federated-search-data-store.md)
</dt> <dt>

[Criando um arquivo OpenSearch descrição no Windows Federado](-search-federated-search-osdx-file.md)
</dt> <dt>

[Seguindo as práticas recomendadas Windows pesquisa federada](-search-fedsearch-best.md)
</dt> <dt>

[Implantando conectores de pesquisa Windows Pesquisa Federada](-search-federated-search-deploying.md)
</dt> </dl>

 

 
