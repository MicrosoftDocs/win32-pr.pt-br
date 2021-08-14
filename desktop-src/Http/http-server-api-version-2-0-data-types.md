---
title: Tipos de dados da API do servidor HTTP versão 2,0
description: Tipos de dados da API do servidor HTTP versão 2,0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a347b58a97ad89e499136c07f85e18ee2ce1bddc31b5c6d67b8f14a2348a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950765"
---
# <a name="http-server-api-version-20-data-types"></a>Tipos de dados da API do servidor HTTP versão 2,0

A API do servidor HTTP usa vários tipos de identificador de finalidade especial declarados no cabeçalho http. h da seguinte maneira:

-   **UShort** parâmetro \_ \_ \_ de tempo limite de configuração do serviço http \_ , \* \_ parâmetro de \_ \_ tempo limite da configuração do serviço PHTTP \_
-   **ULONGLONG** ID opaca HTTP \_ \_ , \* \_ ID opaca \_ PHTTP
-   **Http \_ ID \_** \_ de solicitação HTTP \_ de ID opaca, \* \_ ID de solicitação PHTTP \_
-   **Http \_ ID \_** \_ de conexão http \_ de ID opaca, \* \_ ID de conexão PHTTP \_
-   **Http \_ ID \_** \_ de conexão bruta http de ID opaca \_ \_ , \* ID de \_ conexão bruta PHTTP \_ \_
-   **UShort** parâmetro \_ \_ \_ de tempo limite de configuração do serviço http \_ , \* \_ parâmetro de \_ \_ tempo limite da configuração do serviço PHTTP \_

Um aplicativo não deve tentar gerar ou modificar nenhum identificador que pertença a um desses tipos.

 

 




