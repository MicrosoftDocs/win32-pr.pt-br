---
title: Registro de erros na API de servidor HTTP
description: Alguns tipos de erros são tratados pela API do servidor HTTP em vez de serem passados de volta para um aplicativo para manipulação, porque a frequência desses erros poderia, de outra forma, inundar um log de eventos ou um manipulador de aplicativos.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API do servidor HTTP, log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105792532"
---
# <a name="error-logging-in-the-http-server-api"></a>Registro de erros na API de servidor HTTP

Alguns tipos de erros são tratados pela API do servidor HTTP em vez de serem passados de volta para um aplicativo para manipulação, porque a frequência desses erros poderia, de outra forma, inundar um log de eventos ou um manipulador de aplicativos.

Os três tópicos a seguir descrevem os diferentes aspectos do log de erros da API do servidor HTTP:

-   [Configuração](configuring-http-server-api-error-logging.md) do As configurações do registro controlam se a API do servidor HTTP registra erros, o tamanho máximo permitido de arquivos de log e onde os arquivos de log são salvos.
-   [Formato do arquivo de log](format-of-the-http-server-api-error-logs.md) A API do servidor HTTP cria arquivos de log que estão em conformidade com as convenções de arquivo de log World Wide Web Consortium (W3C) e podem ser analisadas usando ferramentas padrão. No entanto, diferentemente dos arquivos de log do W3C, os arquivos de log da API do servidor HTTP não contêm nomes das colunas.
-   [Tipos de erros registrados](types-of-errors-logged-by-the-http-server-api.md) A API do servidor HTTP registra uma variedade de erros comuns.

 

 




