---
description: Este tópico explica como um usuário registra um novo armazenamento de dados remoto com pesquisa federada abrindo um arquivo de Descrição do OpenSearch (.osdx), como implantar um arquivo .osdx e como acompanhar o uso do serviço OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Implantar conectores de pesquisa Windows Pesquisa Federada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7515fa905abf3767696457f30a52abdb0a36d78883e9649cb2bf42e77e8b8c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463131"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>Implantando conectores de pesquisa Windows Pesquisa Federada

Este tópico explica como um usuário registra um novo armazenamento de dados remoto com pesquisa federada abrindo um arquivo de Descrição do OpenSearch (.osdx), como implantar um arquivo .osdx e como acompanhar o uso do [serviço OpenSearch.](https://github.com/dewitt/opensearch)

Este tópico é organizado da seguinte forma:

-   [O arquivo .searchconnector-ms (Search Connector)](#the-searchconnector-ms-search-connector-file)
-   [Métodos de implantação](#deployment-methods)
    -   [Implantação pull](#pull-deployment)
    -   [Implantação por push](#push-deployment)
-   [Acompanhamento de uso](#tracking-usage)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>O arquivo .searchconnector-ms (Search Connector)

Simplesmente abrir o arquivo .osdx que descreve como se conectar ao serviço Web e como mapear quaisquer elementos personalizados em seu RSS ou Atom XML registra seu novo armazenamento de dados remoto com pesquisa federada. Um armazenamento de dados que já tem um [OpenSearch](https://github.com/dewitt/opensearch) Web compatível com a pesquisa federada pode ser adicionado ao Windows Explorer quando um usuário abre um arquivo .osdx.

Depois de ter dado o .osdx ao usuário e o usuário abrir o arquivo .osdx, os eventos a seguir ocorrerão.

1.  Um arquivo .searchconnector-ms é criado na **pasta Windows Searches** (%userprofile%/Searches).
2.  Um atalho para o arquivo .searchconnector-ms é criado na **pasta Links** (%userprofile%/Links).
3.  Um atalho é exibido no painel  Windows de navegação do Explorer, permitindo que o usuário navegue até o novo armazenamento de dados e consulte o serviço Web.

## <a name="deployment-methods"></a>Métodos de implantação

Há duas maneiras de implantar conectores de pesquisa, implantação de pull e implantação por push.

### <a name="pull-deployment"></a>Implantação pull

A implantação pull descreve qualquer tipo de implantação na qual o usuário final toma a iniciativa de instalar os conectores de pesquisa. Métodos comuns de implantação de pull são:

-   Anexando o arquivo .osdx em um email.
-   Postando o arquivo em uma página da Web.
-   Fornecendo um link dinâmico em seu site da intranet; por exemplo, um que gera arquivos .osdx personalizados com base nas opções do usuário ou no escopo atual dentro do site.

Para que o arquivo seja baixado quando o usuário clicar no link no navegador, o servidor Web que hospeda o serviço Web deverá ser configurado para entregar o .osdx como um arquivo. Portanto, você deve configurar os Tipos MIME no servidor Web para tratar arquivos .osdx como `"application/opensearchdescription+xml"` . Opcionalmente, você pode usar o ícone fornecido pela Microsoft para identificar o link do conector de pesquisa.

### <a name="push-deployment"></a>Implantação por push

A implantação por push descreve qualquer tipo de implantação que não dependa da iniciativa do usuário para instalar os conectores de pesquisa. Métodos comuns de implantação por push são:

-   GPP (Política de Grupo de Política de Grupo)
-   Script de logon
-   Perfis móveis
-   Geração de imagens

## <a name="tracking-usage"></a>Acompanhamento de uso

Para acompanhar o uso do serviço [OpenSearch](https://github.com/dewitt/opensearch) por usuários que pesquisam no Windows Explorer, filtre os arquivos de log do servidor Web para essa cadeia de caracteres do agente do usuário: `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Recursos adicionais

Para obter informações adicionais sobre como implementar a federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch no Windows 7 e posterior, consulte "Recursos adicionais" em [Pesquisa Federada](/previous-versions//dd742958(v=vs.85))no Windows .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Ponto de Partida com a Pesquisa Federada Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conectando seu serviço Web Windows Pesquisa Federada](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitando seu armazenamento de dados Windows Pesquisa Federada](-search-federated-search-data-store.md)
</dt> <dt>

[Criando um arquivo OpenSearch descrição no Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Seguindo as práticas recomendadas Windows pesquisa federada](-search-fedsearch-best.md)
</dt> </dl>

 

 
