---
title: Recursos da API do servidor HTTP
description: Este tópico tem suporte e recursos sem suporte da API do servidor HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Recursos da API do servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292668"
---
# <a name="http-server-api-features"></a>Recursos da API do servidor HTTP

As listas a seguir descrevem os recursos com e sem suporte da API do servidor HTTP.

## <a name="features-supported"></a>Recursos com suporte

O HTTP dá suporte aos seguintes recursos:

-   Funcionalidade de servidor HTTP v 1.0 e v 1.1.
-   Protocolo SSL 3,0 (SSL) com suporte para certificados de cliente e de servidor.
-   Cache de fragmentos de dados para uso em respostas subsequentes.
-   Suporte para IPv6 e endereçamento IPv4.
-   Reservas de namespace de URL para segurança de aplicativo.
-   Identificadores verdadeiros para todos os objetos.
-   Modelos de e/s síncronos e assíncronos.
-   Suporte para WOW64 em computadores executados em Windows de 64 bits a partir do Windows Server 2003 com Service Pack 1 (SP1).

## <a name="features-not-supported"></a>Recursos sem suporte

A API do servidor HTTP não oferece suporte para a seguinte funcionalidade:

-   A API do servidor HTTP não executa a autenticação de cliente ou de servidor com base no conteúdo dos cabeçalhos de solicitação HTTP. Qualquer autenticação necessária deve ser implementada pelo aplicativo.
-   O WOW64 em computadores que executam o Windows de 64 bits não tem suporte no Windows Server 2003 e no Windows XP com Service Pack 2 (SP2) e versões anteriores.
-   A API do servidor HTTP não dá suporte ao log de solicitações e respostas HTTP.
-   A API do servidor HTTP não faz a parte das respostas HTTP de saída. O aplicativo deve implementar o agrupamento de respostas, se necessário.

 

 




