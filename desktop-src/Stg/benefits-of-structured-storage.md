---
title: Benefícios do armazenamento estruturado
description: O COM fornece um conjunto de serviços coletivamente chamado de armazenamento estruturado.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Strctd de armazenamento estruturado STG, benefícios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635138"
---
# <a name="benefits-of-structured-storage"></a>Benefícios do armazenamento estruturado

O COM fornece um conjunto de serviços coletivamente chamado de armazenamento estruturado. Entre os benefícios desses serviços está a redução das penalidades de desempenho e a sobrecarga associada ao armazenamento de objetos separados em um arquivo simples. Em vez de um arquivo simples, o COM armazena os objetos separados em um único arquivo estruturado, que consiste em dois elementos principais: objetos de armazenamento e objetos de fluxo. Juntos, eles funcionam como um sistema de arquivos em um arquivo.

O armazenamento estruturado resolve problemas de desempenho, eliminando a necessidade de reescrever totalmente um arquivo no armazenamento sempre que um novo objeto for adicionado a um arquivo composto ou um objeto existente aumentar de tamanho. Os novos dados são gravados no próximo local disponível no armazenamento permanente, e o objeto de armazenamento atualiza a tabela de ponteiros que ele mantém para rastrear os locais de seus objetos de armazenamento e objetos de fluxo. Ao mesmo tempo, o armazenamento estruturado permite que os usuários finais interajam e gerenciem um arquivo composto como se fosse um único arquivo em vez de uma hierarquia aninhada de objetos separados.

O armazenamento estruturado também tem outros benefícios:

-   **Acesso incremental**. Se um usuário precisar de acesso a um objeto em um arquivo composto, o usuário poderá carregar e salvar apenas esse objeto, em vez de todo o arquivo.
-   **Uso múltiplo**. Mais de um usuário final ou aplicativo pode ler e gravar informações simultaneamente no mesmo arquivo composto.
-   **Processamento de transações**. Os usuários podem ler ou gravar em arquivos compostos COM no modo transacionado, em que as alterações feitas no arquivo são armazenadas em buffer e podem ser subseqüentemente confirmadas no arquivo ou invertidas.
-   **Economia de memória insuficiente**. O armazenamento estruturado fornece recursos para salvar arquivos em situações de baixa memória.

 

 




