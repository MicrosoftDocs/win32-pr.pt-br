---
title: A necessidade de informações de erro estendidas
description: Uma dificuldade principal associada à solução de problemas de RPC é o mapeamento de um código de erro RPC para o problema subjacente.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce13e2cb30c7cd9f2db4d7f518eb0a747cd15b2ba1ff7962cf5f41fbc9cf552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016796"
---
# <a name="the-need-for-extended-error-information"></a>A necessidade de informações de erro estendidas

Uma dificuldade principal associada à solução de problemas de RPC é o mapeamento de um código de erro RPC para o problema subjacente. Um erro de configuração ou um problema de rede pode resultar em uma ou mais estações de trabalho recebendo \_ erros RPC S \_ \* , mas essa estação de trabalho pode exibir apenas o erro, parafrasea ou salvá-lo em algum arquivo de log. Seja qual for a abordagem usada, a pessoa que está solucionando o problema é deprived de informações essenciais:

-   Onde o erro ocorreu. Ele pode ter ocorrido no computador local, em um computador remoto chamado pelo computador local ou em um computador remoto chamado por outro computador remoto.
-   O código de erro original que causou o problema. Para estar em conformidade com o padrão uso, MS RPC mapeia códigos de erro para \_ códigos RPC S \_ \* . Os \_ \_ \* códigos de RPC S são muito genéricos, no entanto, e oferecem poucas informações úteis de solução de problemas.
-   Quaisquer informações de contexto relacionadas à ocorrência do problema. Com erros não RPC, os depuradores podem parar o processo e examinar o contexto no qual ocorreu o erro. Os erros de RPC geralmente são gerados por um processo ou computador remoto, o que continua o processamento depois de retornar o erro e substitui qualquer contexto relativo ao erro.

 

 




