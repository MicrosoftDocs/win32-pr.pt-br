---
description: Este tópico descreve as etapas envolvidas na conexão de um serviço Web entre o armazenamento de dados e a pesquisa federada do Windows e como enviar consultas e retornar os resultados da pesquisa em RSS ou Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Conectando seu serviço Web na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090085"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>Conectando seu serviço Web na pesquisa federada do Windows

Este tópico descreve as etapas envolvidas na conexão de um serviço Web entre o armazenamento de dados e a pesquisa federada do Windows e como enviar consultas e retornar os resultados da pesquisa em RSS ou Atom.

Este tópico é organizado da seguinte maneira:

-   [Conectar seu serviço Web](#connect-your-web-service)
-   [Registrar um armazenamento de dados remoto existente](#register-an-existing-remote-data-store)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="connect-your-web-service"></a>Conectar seu serviço Web

**Para conectar o serviço Web do armazenamento de dados à pesquisa federada, execute as seguintes etapas:**

1.  Crie um arquivo. osdx.
2.  Forneça o arquivo. osdx aos usuários para que eles possam adicionar o serviço sob demanda abrindo o arquivo. osdx.
3.  Gere um conector de pesquisa e implante-o ativamente em sua empresa.

## <a name="register-an-existing-remote-data-store"></a>Registrar um armazenamento de dados remoto existente

Um usuário registra um novo armazenamento de dados remoto com a pesquisa federada do Windows abrindo um arquivo de descrição de OpenSearch (. osdx). Quando o usuário faz isso, ocorrem os seguintes eventos:

1.  Um arquivo. searchconnector-MS (conector de pesquisa) é criado na pasta pesquisas do Windows (% USERPROFILE%/Searches).
2.  Um atalho para o arquivo. searchconnector-MS é criado na pasta links (% USERPROFILE%/links).
3.  Um atalho é exibido no painel **favoritos** de navegação do Windows Explorer, permitindo que o usuário navegue até o novo armazenamento de dados e consulte o serviço Web.

> [!Note]  
> Um armazenamento de dados que já tem um serviço Web [OpenSearch](https://github.com/dewitt/opensearch) compatível com a pesquisa federada do Windows pode ser adicionado ao Windows Explorer quando um usuário abre um arquivo. osdx.

 

## <a name="additional-resources"></a>Recursos adicionais

Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introdução com pesquisa federada no Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Habilitando seu armazenamento de dados na pesquisa federada do Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Seguindo as práticas recomendadas na pesquisa federada do Windows](-search-fedsearch-best.md)
</dt> <dt>

[Implantando conectores de pesquisa na pesquisa federada do Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
