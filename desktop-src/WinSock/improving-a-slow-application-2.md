---
description: Esta seção examina uma parte de um aplicativo de exemplo que opera pela rede muito lentamente. Ao longo desta seção, são feitas modificações no código inicial para melhorar seu desempenho.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Melhorando um aplicativo lento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff8f996267328805dc120d39218784a08383fb68ae9f6927e8983b6e1bec2d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097886"
---
# <a name="improving-a-slow-application"></a>Melhorando um aplicativo lento

Esta seção examina uma parte de um aplicativo de exemplo que opera pela rede muito lentamente. Ao longo desta seção, são feitas modificações no código inicial para melhorar seu desempenho.

O exemplo de simulação é a parte atualizada para um jogo chamado Life. O aplicativo é escrito de forma que o cliente executa os cálculos das atualizações e os envia para o servidor. Em seguida, o servidor exibe o campo Vida resultante. A saída do cliente é um fluxo de bytes, agrupado em três (triplos), cada um triplo representando uma atualização de célula. Os bytes no tripleto representam a linha, a coluna e o valor, respectivamente, para a célula.

Este exemplo começa como um aplicativo intencionalmente de baixo desempenho, que fornece a linha de base da qual as melhorias de desempenho podem ser ilustradas. A partir daí, o código é aprimorado três vezes para resolver vários problemas que afetam o desempenho. Esses exemplos devem ser lidos em ordem, conforme cada iteração melhora na versão anterior.

O código de linha de base e as revisões que melhoram esse código são os seguintes:

-   [A versão de linha de base: um aplicativo de baixo desempenho](the-baseline-version-a-very-poor-performing-application-2.md)
-   [Revisão 1: limpando o óbvio](revision-1-cleaning-up-the-obvious-2.md)
-   [Revisão 2: Redesigning for Fewer Connects](revision-2-redesigning-for-fewer-connects-2.md)
-   [Revisão 3: Envio de Bloco Compactado](revision-3-compressed-block-send-2.md)
-   [Melhorias futuras](future-improvements-2.md)

> [!WARNING]
> Os primeiros exemplos do aplicativo fornecem desempenho intencionalmente ruim para ilustrar as melhorias de desempenho possíveis com alterações no código. Não use esses exemplos de código em seu aplicativo; eles são apenas para fins de ilustração.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de soquetes Windows de alto desempenho](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



