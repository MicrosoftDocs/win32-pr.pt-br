---
title: Implementando um sistema distribuído
description: Uma maneira de implementar o software em um sistema distribuído é usar o suporte à rede bruta.
ms.assetid: 46abbbec-caa1-4fee-a713-4a4a2b462051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098263f916129115f41840e15ac689fab7e4544621989d1a4d3179e50ef17d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020525"
---
# <a name="implementing-a-distributed-system"></a>Implementando um sistema distribuído

Uma maneira de implementar o software em um sistema distribuído é usar o suporte à rede bruta. Essa abordagem inclui soquetes, pipes nomeados ou postagens HTTP, GETs e assim por diante. Todos esses modelos forçam o desenvolvedor a usar primitivos de programação de baixo nível, de uma maneira ou de outra, o que força o desenvolvedor a lidar com a NDR (representação de dados de rede), empacotar dados, gerenciar o tráfego de rede e as condições de falha, proteção e criptografia de integridade de dados e assim por diante.

O RPC oferece um modelo de programação em que o desenvolvedor retém o controle granular da interação de rede entre o cliente e o servidor por meio de uma API avançada, ao mesmo tempo em que poupa os desenvolvedores dos detalhes e das cargas que um sistema distribuído tende a introduzir.

Por exemplo, considere a sobrecarga associada a várias abordagens para proteger a integridade e a privacidade das trocas de mensagens em um sistema distribuído. Ao considerar a segurança de rede para trocas de pacotes, algumas proteções são mais fracas e mais seguras. Não há segurança de rede verdadeira, somente vários mecanismos de segurança baseados em pacote; segurança que identifica o chamador (que tende a ser fraco também, já que o conteúdo do pacote geralmente pode ser alterado em trânsito), segurança protegendo a integridade do pacote sem proteger sua privacidade (várias assinaturas e hashes) e segurança protegendo a privacidade da troca de mensagens (vários mecanismos de criptografia).

Outro fardo da implementação de um sistema distribuído seguro são os algoritmos necessários para implementar primitivos de segurança, como criptografia, assinatura, autenticação e assim por diante. Um desenvolvedor pode implementar esses algoritmos, mas isso é difícil, propenso a erros e até mesmo arriscado, pois os algoritmos resultantes geralmente têm falhas sutis de segurança. Como alternativa, um desenvolvedor pode usar um provedor de segurança disponível para implementar a proteção para as interações de rede em um sistema distribuído.

Usando RPC, essas cargas são resolvidas muito facilmente. Um desenvolvedor simplesmente precisa informar ao RPC qual pacote de segurança usar e qual proteção de segurança deve ser aplicada à troca de mensagens (em termos de autenticação, criptografia, autenticação mútua, controle de identidade do chamador e assim por diante). O RPC cuida de todos os detalhes nos bastidores de maneira eficiente, embora forneça ao desenvolvedor controle total sobre como os dados serão protegidos.

 

 




