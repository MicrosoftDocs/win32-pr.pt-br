---
title: Registro de erros na API de servidor HTTP
description: Alguns tipos de erros são tratados pela API do servidor HTTP em vez de serem passados de volta para um aplicativo para tratamento, porque a frequência desses erros poderia inundar um log de eventos ou manipulador de aplicativos.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API do Servidor HTTP, log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c92c071929b61020b456d8ecabc81ebc0f05503c2f385b235afc323cf8dea33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130676"
---
# <a name="error-logging-in-the-http-server-api"></a>Registro de erros na API de servidor HTTP

Alguns tipos de erros são tratados pela API do servidor HTTP em vez de serem passados de volta para um aplicativo para tratamento, porque a frequência desses erros poderia inundar um log de eventos ou manipulador de aplicativos.

Os três tópicos a seguir descrevem os diferentes aspectos do log de erros da API do servidor HTTP:

-   [Configuração](configuring-http-server-api-error-logging.md) As configurações do Registro controlam se a API do Servidor HTTP registra erros, o tamanho máximo permitida dos arquivos de log e onde os arquivos de log são salvos.
-   [Formato de arquivo de log](format-of-the-http-server-api-error-logs.md) A API do Servidor HTTP cria arquivos de log que estão em conformidade com as convenções de arquivo de log World Wide Web Consortium (W3C) e podem ser analisados usando ferramentas padrão. No entanto, ao contrário dos arquivos de log do W3C, os arquivos de log da API do servidor HTTP não contêm nomes das colunas.
-   [Tipos de erros registrados](types-of-errors-logged-by-the-http-server-api.md) A API do Servidor HTTP registra uma variedade de erros comuns.

 

 




