---
title: Roteamento de solicitações de entrada
description: A API do servidor HTTP mantém um banco de dados de roteamento para determinar qual aplicativo recebe uma solicitação de entrada.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104366886"
---
# <a name="routing-incoming-requests"></a>Roteamento de solicitações de entrada

A API do servidor HTTP mantém um banco de dados de roteamento para determinar qual aplicativo recebe uma solicitação de entrada. A tabela de roteamento é criada a partir do banco de dados de reserva e contém entradas de reserva, bem como registros atuais. Quando um registro ou reserva é feito, ele é colocado no Bucket do banco de dados de roteamento que corresponde ao tipo de host da seguinte maneira:

-   \+ : os registros de porta são colocados no Bucket "curinga forte"

-   host: os registros de porta são colocados no Bucket "Explicit"

-   IP: os registros de porta são colocados no Bucket "curinga fraco com limite de IP"

-   \* : os registros de porta são colocados no Bucket "curinga fraco"

Essas etapas também se referem à ordem em que as solicitações HTTP de entrada são processadas. As reservas de curinga fortes primeiro, em seguida, a reserva explícita são verificadas, seguidas pelo curinga fraco de IP e por curinga fraco. A pesquisa para quando uma correspondência é encontrada para que os registros em qualquer um dos buckets restantes não sejam encontrados.

O algoritmo de roteamento da API do servidor HTTP localiza a melhor correspondência para o [URLPrefix](urlprefix-strings.md) pesquisando as entradas de registro e as entradas de reserva do banco de dados de roteamento, começando com o Bucket curinga forte e terminando com o Bucket de curinga fraco. A melhor correspondência, dentro de um Bucket, é a correspondência mais longa na parte do URI relativo do UrlPrefix (supondo uma correspondência exata para as partes do host, da porta e do esquema da URL). Depois que uma correspondência for encontrada em um Bucket, o algoritmo de roteamento interromperá sua pesquisa e ignorará todos os buckets de prioridade mais baixa.

Por exemplo, considere os seguintes registros (listados em ordem decrescente de prioridade com base em tipos de Bucket:

-   Registro: `https://+:80/vroot/` é registrado pelo aplicativo 1

-   Registro: `https://adatum.com:80/` é registrado pelo aplicativo 2

-   Registro: `https://\*:80/` é registrado pelo aplicativo 3

Uma solicitação de entrada para `https://adatum.com:80/vroot/subdir/file.htm/` é entregue ao aplicativo 1. Uma solicitação de entrada para `https://adatum.com:80/default.htm/` é entregue ao aplicativo 2. Uma solicitação de entrada para `https://otheradatum.com:80/file.htm/` é entregue ao aplicativo 3.

Se a melhor correspondência for uma entrada de reserva, isso significa que o aplicativo que deve receber a solicitação não está em execução. Por exemplo, considere o seguinte registro e reserva:

-   Registro: `https://\*:80/vroot/` é registrado pelo aplicativo 1, usuário A

-   Reserva: `https://adatum.com:80/` foi reservado para o usuário B

Uma solicitação de entrada para `https://adatum.com:80/vroot/file.htm/` o não é entregue ao aplicativo 1 porque a melhor correspondência leva à entrada de reserva para o usuário B. As regras de precedência são aplicadas nesse caso à reserva que tem uma prioridade mais alta. Se nenhum processo estiver ativo que seja autorizado e registrado para solicitações de serviço para a URL recebida, a solicitação será rejeitada com um código de status 400 (solicitação inadequada).

 

 




