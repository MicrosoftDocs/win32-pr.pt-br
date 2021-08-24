---
title: Considerações sobre programação MGM
description: Ao desenvolver clientes do Gerenciador de grupos de multicast, observe as diretrizes a seguir
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multicast, considerações de programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a749406384068cc7dce54fab237c261926149aaf9b2fbdca23327c7b75f3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029616"
---
# <a name="mgm-programming-considerations"></a>Considerações sobre programação MGM

Ao desenvolver clientes do Gerenciador de grupos de multicast, observe as seguintes diretrizes:

-   As chamadas de função devem ser feitas de dentro do processo do roteador. Se as funções forem chamadas de outro processo, seus resultados não serão válidos; o cliente não irá interagir com o Gerenciador do grupo de multicast.
-   Os clientes que usam a API MGM devem fornecer sua própria verificação de erro, garantindo que apenas os dados válidos sejam passados para o Gerenciador do grupo de multicast. As funções MGM não retornam mensagens de erro detalhadas sobre parâmetros inválidos; o \_ valor de parâmetro inválido do erro \_ é retornado sem explicação.
-   Os clientes devem ter cuidado ao usar bloqueios ao chamar funções MGM. Isso pode impedir deadlocks. Ao chamar as funções MGM, os clientes não devem armazenar nenhum bloqueio que possa ser mantido simultaneamente em um retorno de chamada do Gerenciador de grupos multicast.

 

 




