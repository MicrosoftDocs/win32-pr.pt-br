---
description: Os identificadores opacos são usados no TSPI para fazer referência às estruturas de dados que representam linhas, telefones e aparências de chamada.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Identificadores opacos e estruturas de dados privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921084"
---
# <a name="opaque-handles-and-private-data-structures"></a>Identificadores opacos e estruturas de dados privadas

Os identificadores opacos são usados no TSPI para fazer referência às estruturas de dados que representam linhas, telefones e aparências de chamada. Eles aparecem como parâmetros para a maioria das funções e retornos de chamada. Há poucas funções que se referem ao dispositivo usando um identificador de dispositivo em vez de um identificador opaco. Nesse caso, a referência é para o dispositivo em si, e não para uma estrutura de dados. Funções que funcionam dessa maneira normalmente são aquelas chamadas em tempos de inicialização antecipados antes que as estruturas de dados sejam criadas e identificadores opacos sejam trocados.

O provedor de serviços deve decidir como interpretar esses identificadores. Um provedor de serviços normalmente usa o ponteiro para sua estrutura de dados ou para o índice em uma matriz de estruturas de dados como seu identificador opaco. A única restrição é que o provedor de serviços não pode usar o valor 0 como um [HDRVLINE](hdrvline.md), HDRVCALL ou [HDRVPHONE](hdrvphone.md). O valor 0 ou **NULL** para um identificador tem um significado especial em algumas operações.

 

 



