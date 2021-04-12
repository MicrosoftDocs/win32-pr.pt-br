---
title: Desempenho e consumo de memória no WOW64
description: O consumo de desempenho e de memória sob o WOW64 é determinado pelos seguintes fatores.
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- desempenho sob programação WOW64 de 64 bits do Windows
- consumo de memória sob programação WOW64 de 64 bits do Windows
- Programação WOW64 para Windows de 64 bits, desempenho
- Programação WOW64 de 64 bits do Windows, consumo de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8928e7d50c8396aa2b5b34081af3e4ee2719e044
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366572"
---
# <a name="performance-and-memory-consumption-under-wow64"></a>Desempenho e consumo de memória no WOW64

O consumo de desempenho e de memória sob o WOW64 é determinado pelos seguintes fatores:

-   Hardware do processador. A emulação de instrução é executada no chip. No processador x64, as instruções x86 são executadas nativamente pelo processador. Portanto, a velocidade de execução sob WOW64 em x64 é semelhante à sua velocidade em janelas de 32 bits. No processador Intel Itanium e em qualquer processador de ARM64, mais software está envolvido na emulação e o desempenho é afetado como resultado.
-   Sobrecarga de conversão de API. Essa sobrecarga é pequena em comparação com as chamadas do sistema para o kernel do NT. As funções do kernel NT devem ser chamadas com pouca frequência.
-   Tamanho da memória virtual. No processador Intel Itanium, o WOW64 adiciona sobrecarga significativa se duas ou mais instâncias do mesmo aplicativo de 32 bits estiverem em execução simultaneamente. Isso se deve às páginas nativas de 8 KB no Intel Itanium, o que complica a emulação das páginas nativas de 4 KB na arquitetura x86 (mais páginas são marcadas como graváveis; todas as páginas graváveis são privadas para o processo). Isso pode afetar negativamente a escalabilidade dos serviços de terminal em determinados processadores. Esse não é o caso do processador x64.
-   Conjunto de trabalho. O WOW64 aumenta o tamanho do conjunto de trabalho do aplicativo.

O WOW64 permite que os aplicativos de 32 bits tirem proveito do kernel de 64 bits. Portanto, os aplicativos de 32 bits podem usar um número maior de identificadores de kernel e identificadores de janela. No entanto, os aplicativos de 32 bits podem não ser capazes de criar tantos segmentos no WOW64 quanto podem ser executados nativamente em sistemas baseados em x86, pois o WOW64 aloca uma pilha de 64 bits adicional (geralmente 512 KB) para cada thread. Além disso, alguma quantidade de espaço de endereço é reservada para o WOW64 em si e as estruturas de dados que ele usa. A quantidade reservada depende do processador; mais é reservado no Intel Itanium do que nos processadores x64 ou ARM64.

Se o aplicativo tiver o sinalizador de [**\_ \_ \_ \_ reconhecimento de endereço grande do arquivo de imagem**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) definido no cabeçalho da imagem, cada aplicativo de 32 bits receberá 4 GB de espaço de endereço virtual no ambiente WOW64. Se o sinalizador de **\_ \_ \_ \_ reconhecimento de endereço grande do arquivo de imagem** não estiver definido, cada aplicativo de 32 bits receberá 2 GB de espaço de endereço virtual no ambiente WOW64.

 

 