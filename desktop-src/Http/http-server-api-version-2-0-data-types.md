---
title: Tipos de dados da API do servidor HTTP versão 2,0
description: Tipos de dados da API do servidor HTTP versão 2,0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105787530"
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

 

 




