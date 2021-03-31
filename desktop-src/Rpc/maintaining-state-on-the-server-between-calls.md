---
title: Mantendo o estado no servidor entre as chamadas
description: Geralmente, é necessário manter o estado no servidor entre chamadas RPC separadas \ 8212; usar identificadores de contexto é a melhor maneira de fazer isso. Algumas palavras sobre como os identificadores de contexto operam internamente ajudam a entender quando os identificadores de contexto funcionam melhor.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, manutenção do estado entre chamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634797"
---
# <a name="maintaining-state-on-the-server-between-calls"></a>Mantendo o estado no servidor entre as chamadas

Geralmente, é necessário manter o estado no servidor entre chamadas RPC separadas — o uso de identificadores de contexto é a melhor maneira de fazer isso. Algumas palavras sobre como os identificadores de contexto operam internamente ajudam a entender quando os identificadores de contexto funcionam melhor.

O cliente nunca recebe o estado mantido no servidor. Geralmente, o estado no servidor é um ponteiro para um bloco de memória e o cliente não tem informações sobre ele. Tudo o que o cliente recebe é um grande número exclusivo, com outras informações associadas a ele, que o servidor envia para o cliente e que representa o identificador de contexto em todas as operações subsequentes. Sempre que o cliente se refere a um identificador aberto, ele envia o grande número recebido do servidor quando esse identificador de contexto foi aberto.

O servidor mantém o controle de todos os grandes números que envia a um cliente. Quando o servidor recebe um grande número que representa um identificador de contexto, ele pesquisa o número na coleção de identificadores de contexto válidos e pendentes para esse cliente e localiza o contexto do lado do servidor correspondente a um determinado número grande. Isso é passado para a rotina do servidor. Se o número grande não for encontrado, uma \_ exceção de \_ incompatibilidade de contexto X SS de RPC \_ \_ será gerada e propagada para o cliente.

Os coregistros desse design são os seguintes:

-   Um identificador de contexto é válido somente no contexto da sessão de cliente/servidor existente. Ele não pode ser passado para outro cliente.
-   Um identificador de contexto torna-se inválido se o servidor for reinicializado ou perder sua conexão com o cliente.
-   O cliente não pode interpretar o que o identificador de contexto representa no servidor. Para um cliente, todos os identificadores de contexto são simplesmente números grandes.

Se o cliente falhar, o servidor receberá uma notificação e limpará seus identificadores de contexto usando o mecanismo de execução.

 

 




