---
title: Tipos de dados da API do servidor HTTP versão 1,0
description: A API do servidor HTTP usa vários tipos de identificador de finalidade especial declarados no arquivo de cabeçalho http. h como inteiros de 64 bits sem sinal.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- Tipo de HTTP_CONNECTION_ID HTTP
- Tipo de HTTP_RAW_CONNECTION_ID HTTP
- Tipo de HTTP_REQUEST_ID HTTP
- Tipo de HTTP_URL_CONTEXT HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151ef975470ca21c6e82e5bc7bd7bd8b99a70573385375e8552b6660ce78f631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950795"
---
# <a name="http-server-api-version-10-data-types"></a>Tipos de dados da API do servidor HTTP versão 1,0

A API do servidor HTTP usa vários tipos de identificador de finalidade especial declarados no arquivo de cabeçalho http. h como inteiros de 64 bits sem sinal (**ULONGLONGs**):

-   \_ID da conexão http \_
-   \_ID de \_ conexão \_ bruta http
-   \_ID da solicitação HTTP \_
-   \_contexto de URL http \_

Um aplicativo não deve tentar gerar ou modificar nenhum identificador que pertença a um desses tipos.

 

 




