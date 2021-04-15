---
description: Este tópico explica como um usuário registra um novo armazenamento de dados remoto com pesquisa federada abrindo um arquivo de descrição de OpenSearch (. osdx), como implantar um arquivo. osdx e como acompanhar o uso do serviço OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Implantar conectores de pesquisa na pesquisa federada do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460989"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a>Implantando conectores de pesquisa na pesquisa federada do Windows

Este tópico explica como um usuário registra um novo armazenamento de dados remoto com pesquisa federada abrindo um arquivo de descrição de OpenSearch (. osdx), como implantar um arquivo. osdx e como acompanhar o uso do serviço [OpenSearch](https://github.com/dewitt/opensearch) .

Este tópico é organizado da seguinte maneira:

-   [O arquivo. searchconnector-MS (conector de pesquisa)](#the-searchconnector-ms-search-connector-file)
-   [Métodos de implantação](#deployment-methods)
    -   [Implantação de pull](#pull-deployment)
    -   [Implantação por push](#push-deployment)
-   [Controlando o uso](#tracking-usage)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a>O arquivo. searchconnector-MS (conector de pesquisa)

Simplesmente abrir o arquivo. osdx que descreve como se conectar ao serviço Web e como mapear quaisquer elementos personalizados em seu RSS ou Atom XML registra seu novo armazenamento de dados remoto com pesquisa federada. Um armazenamento de dados que já tem um serviço Web do [OpenSearch](https://github.com/dewitt/opensearch) compatível com a pesquisa federada pode ser adicionado ao Windows Explorer quando um usuário abre um arquivo. osdx.

Depois de ter dado o. osdx ao usuário e o usuário abrir o arquivo. osdx, os eventos a seguir ocorrerão.

1.  Um arquivo. searchconnector-MS é criado na pasta **pesquisas do Windows** (% USERPROFILE%/Searches).
2.  Um atalho para o arquivo. searchconnector-MS é criado na pasta **links** (% USERPROFILE%/links).
3.  Um atalho é exibido no painel **favoritos** de navegação do Windows Explorer, permitindo que o usuário navegue até o novo repositório de dados e consulte o serviço Web.

## <a name="deployment-methods"></a>Métodos de implantação

Há duas maneiras de implantar conectores de pesquisa, implantação de pull e implantação por push.

### <a name="pull-deployment"></a>Implantação de pull

A implantação de pull descreve qualquer tipo de implantação na qual o usuário final usa a iniciativa para instalar os conectores de pesquisa. Os métodos comuns de implantação pull são:

-   Anexando o arquivo. osdx em um email.
-   Postando o arquivo em uma página da Web.
-   Fornecendo um link dinâmico no site da intranet; por exemplo, um que gera arquivos. osdx personalizados com base nas opções do usuário ou no escopo atual no site.

Para o arquivo a ser baixado quando o usuário clica no link em seu navegador, o servidor Web que hospeda o serviço Web deve ser configurado para entregar o. osdx como um arquivo. Portanto, você deve configurar os tipos MIME no servidor Web para tratar arquivos. osdx como `"application/opensearchdescription+xml"` . Opcionalmente, você pode usar o ícone fornecido pela Microsoft para identificar o link do conector de pesquisa.

### <a name="push-deployment"></a>Implantação por push

A implantação por push descreve qualquer tipo de implantação que não depende da iniciativa de usuário para instalar os conectores de pesquisa. Os métodos comuns de implantação por push são:

-   Preferências de Política de Grupo (GPP)
-   Script de logon
-   Perfis móveis
-   Geração de imagens

## <a name="tracking-usage"></a>Controlando o uso

Para acompanhar o uso do serviço [OpenSearch](https://github.com/dewitt/opensearch) por usuários pesquisando no Windows Explorer, filtre os arquivos de log do servidor Web para esta cadeia de caracteres do agente do usuário: `Windows-Search+(Windows+NT+6.1)` .

## <a name="additional-resources"></a>Recursos adicionais

Para obter informações adicionais sobre como implementar a Federação de pesquisa em armazenamentos de dados remotos usando as tecnologias OpenSearch no Windows 7 e versões posteriores, consulte "recursos adicionais" em [pesquisa federada no Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introdução com pesquisa federada no Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Conectando seu serviço Web na pesquisa federada do Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Habilitando seu armazenamento de dados na pesquisa federada do Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Criando um arquivo de descrição do OpenSearch na pesquisa federada do Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Seguindo as práticas recomendadas na pesquisa federada do Windows](-search-fedsearch-best.md)
</dt> </dl>

 

 
