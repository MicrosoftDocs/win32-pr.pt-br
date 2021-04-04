---
title: Considerações sobre programação MGM
description: Ao desenvolver clientes do Gerenciador de grupos de multicast, observe as diretrizes a seguir
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multicast, considerações de programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822812"
---
# <a name="mgm-programming-considerations"></a>Considerações sobre programação MGM

Ao desenvolver clientes do Gerenciador de grupos de multicast, observe as seguintes diretrizes:

-   As chamadas de função devem ser feitas de dentro do processo do roteador. Se as funções forem chamadas de outro processo, seus resultados não serão válidos; o cliente não irá interagir com o Gerenciador do grupo de multicast.
-   Os clientes que usam a API MGM devem fornecer sua própria verificação de erro, garantindo que apenas os dados válidos sejam passados para o Gerenciador do grupo de multicast. As funções MGM não retornam mensagens de erro detalhadas sobre parâmetros inválidos; o \_ valor de parâmetro inválido do erro \_ é retornado sem explicação.
-   Os clientes devem ter cuidado ao usar bloqueios ao chamar funções MGM. Isso pode impedir deadlocks. Ao chamar as funções MGM, os clientes não devem armazenar nenhum bloqueio que possa ser mantido simultaneamente em um retorno de chamada do Gerenciador de grupos multicast.

 

 




