---
title: benefícios do Armazenamento estruturado
description: O COM fornece um conjunto de serviços coletivamente chamado de armazenamento estruturado.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- estruturada Armazenamento Strctd Stg, benefícios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a52159f37b3bf443419beaadbcf9f76aa9c5d7209e04b25506eea850c4d3d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663556"
---
# <a name="benefits-of-structured-storage"></a>benefícios do Armazenamento estruturado

O COM fornece um conjunto de serviços coletivamente chamado de armazenamento estruturado. Entre os benefícios desses serviços está a redução das penalidades de desempenho e a sobrecarga associada ao armazenamento de objetos separados em um arquivo simples. Em vez de um arquivo simples, o COM armazena os objetos separados em um único arquivo estruturado, que consiste em dois elementos principais: objetos de armazenamento e objetos de fluxo. Juntos, eles funcionam como um sistema de arquivos em um arquivo.

O armazenamento estruturado resolve problemas de desempenho, eliminando a necessidade de reescrever totalmente um arquivo no armazenamento sempre que um novo objeto for adicionado a um arquivo composto ou um objeto existente aumentar de tamanho. Os novos dados são gravados no próximo local disponível no armazenamento permanente, e o objeto de armazenamento atualiza a tabela de ponteiros que ele mantém para rastrear os locais de seus objetos de armazenamento e objetos de fluxo. Ao mesmo tempo, o armazenamento estruturado permite que os usuários finais interajam e gerenciem um arquivo composto como se fosse um único arquivo em vez de uma hierarquia aninhada de objetos separados.

O armazenamento estruturado também tem outros benefícios:

-   **Acesso incremental**. Se um usuário precisar de acesso a um objeto em um arquivo composto, o usuário poderá carregar e salvar apenas esse objeto, em vez de todo o arquivo.
-   **Uso múltiplo**. Mais de um usuário final ou aplicativo pode ler e gravar informações simultaneamente no mesmo arquivo composto.
-   **Processamento de transações**. Os usuários podem ler ou gravar em arquivos compostos COM no modo transacionado, em que as alterações feitas no arquivo são armazenadas em buffer e podem ser subseqüentemente confirmadas no arquivo ou invertidas.
-   **Economia de memória insuficiente**. O armazenamento estruturado fornece recursos para salvar arquivos em situações de baixa memória.

 

 




