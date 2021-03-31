---
title: A necessidade de informações de erro estendidas
description: Uma dificuldade principal associada à solução de problemas de RPC é o mapeamento de um código de erro RPC para o problema subjacente.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82fbbcaf0fac427b2bf64fbacbf1e85aeb4d06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005256"
---
# <a name="the-need-for-extended-error-information"></a>A necessidade de informações de erro estendidas

Uma dificuldade principal associada à solução de problemas de RPC é o mapeamento de um código de erro RPC para o problema subjacente. Um erro de configuração ou um problema de rede pode resultar em uma ou mais estações de trabalho recebendo \_ erros RPC S \_ \* , mas essa estação de trabalho pode exibir apenas o erro, parafrasea ou salvá-lo em algum arquivo de log. Seja qual for a abordagem usada, a pessoa que está solucionando o problema é deprived de informações essenciais:

-   Onde o erro ocorreu. Ele pode ter ocorrido no computador local, em um computador remoto chamado pelo computador local ou em um computador remoto chamado por outro computador remoto.
-   O código de erro original que causou o problema. Para estar em conformidade com o padrão uso, MS RPC mapeia códigos de erro para \_ códigos RPC S \_ \* . Os \_ \_ \* códigos de RPC S são muito genéricos, no entanto, e oferecem poucas informações úteis de solução de problemas.
-   Quaisquer informações de contexto relacionadas à ocorrência do problema. Com erros não RPC, os depuradores podem parar o processo e examinar o contexto no qual ocorreu o erro. Os erros de RPC geralmente são gerados por um processo ou computador remoto, o que continua o processamento depois de retornar o erro e substitui qualquer contexto relativo ao erro.

 

 




