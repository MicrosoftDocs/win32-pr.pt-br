---
description: Esta seção examina uma parte de um aplicativo de exemplo que opera na rede muito devagar. Ao longo desta seção, são feitas modificações no código inicial para melhorar seu desempenho.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Melhorando um aplicativo lento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782614"
---
# <a name="improving-a-slow-application"></a>Melhorando um aplicativo lento

Esta seção examina uma parte de um aplicativo de exemplo que opera na rede muito devagar. Ao longo desta seção, são feitas modificações no código inicial para melhorar seu desempenho.

O exemplo fictício é a parte atualizada de um jogo chamado Life. O aplicativo é escrito de modo que o cliente executa os cálculos para as atualizações e as envia para o servidor. Em seguida, o servidor exibe o campo de vida resultante. A saída do cliente é um fluxo de bytes, agrupados em três (tercetos), cada terceto representando uma atualização de célula. Os bytes no terceto representam a linha, a coluna e o valor, respectivamente, para a célula.

Este exemplo começa como um aplicativo de desempenho intencionalmente insatisfatório, que fornece a linha de base da qual as melhorias de desempenho podem ser ilustradas. A partir daí, o código é melhorado três vezes para resolver vários problemas que afetam o desempenho. Esses exemplos devem ser lidos em ordem, uma vez que cada iteração melhora na versão anterior.

O código de linha de base e as revisões que melhoram esse código são os seguintes:

-   [A versão de linha de base: um aplicativo com muito mau desempenho](the-baseline-version-a-very-poor-performing-application-2.md)
-   [Revisão 1: limpando o óbvio](revision-1-cleaning-up-the-obvious-2.md)
-   [Revisão 2: redesignação para menos conexões](revision-2-redesigning-for-fewer-connects-2.md)
-   [Revisão 3: envio de bloco compactado](revision-3-compressed-block-send-2.md)
-   [Aprimoramentos futuros](future-improvements-2.md)

> [!WARNING]
> Os primeiros exemplos do aplicativo fornecem um desempenho intencionalmente insatisfatório, a fim de ilustrar as melhorias de desempenho possíveis com alterações no código. Não use esses exemplos de código em seu aplicativo; Eles são apenas para fins ilustrativos.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de alto desempenho do Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



