---
title: Recursos da API do Servidor HTTP
description: Este tópico oferece suporte a recursos sem suporte da API do Servidor HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Recursos da API do Servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaf567d4576618b07ef5ad8dec91b360f37ab46eb820ff52e2bca896ca91a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014774"
---
# <a name="http-server-api-features"></a>Recursos da API do Servidor HTTP

As listas a seguir descrevem os recursos com suporte e sem suporte da API do servidor HTTP.

## <a name="features-supported"></a>Recursos com suporte

O HTTP dá suporte aos seguintes recursos:

-   Funcionalidade de servidor HTTP v1.0 e v1.1.
-   protocolo SSL SSL (3.0) com suporte para certificados de cliente e servidor.
-   Caching de fragmentos de dados para uso em respostas subsequentes.
-   Suporte para endereçamento IPv6 e IPv4.
-   Reservas de namespace de URL para segurança do aplicativo.
-   Verdadeiros alças para todos os objetos.
-   Modelos de E/S síncronos e assíncronos.
-   Suporte para WOW64 em computadores em execução em Windows de 64 bits a partir do Windows Server 2003 com o Service Pack 1 (SP1).

## <a name="features-not-supported"></a>Recursos sem suporte

A API do Servidor HTTP não dá suporte à seguinte funcionalidade:

-   A API do Servidor HTTP não executa a autenticação de cliente ou servidor com base no conteúdo dos cabeçalhos de solicitação HTTP. Qualquer autenticação necessária deve ser implementada pelo aplicativo.
-   Não há suporte para WOW64 em computadores em execução no Windows de 64 bits no Windows Server 2003 e no Windows XP com o Service Pack 2 (SP2) e anteriores.
-   A API do Servidor HTTP não dá suporte ao registro em log de solicitações e respostas HTTP.
-   A API do Servidor HTTP não faz a parte das respostas HTTP de saída. O aplicativo deve implementar a replicação em partes de resposta, se necessário.

 

 




