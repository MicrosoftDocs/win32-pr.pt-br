---
description: Calculando valores de parâmetro
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Calculando valores de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105748237"
---
# <a name="calculating-parameter-values"></a>Calculando valores de parâmetro

Potencialmente, um buffer de entrada poderia ser muito grande. O ideal é que, quando o DMO processa o buffer, os parâmetros sigam exatamente suas curvas em todo o lote de dados. No entanto, um DMO tem algumas reserva em como calcula esses valores.

-   A abordagem mais precisa é calcular o valor exato de cada unidade atômica de dados; por exemplo, cada amostra de áudio. Essa abordagem é a mais cara em termos computacionais.
-   Outra abordagem é dividir os dados em unidades menores de algum tamanho fixo, como exemplos de 100. Essa abordagem cria um efeito de "etapa de escada". Para alguns parâmetros, isso pode ser aceitável. Em efeitos de áudio, ele pode criar artefatos audíveis.
-   Um comprometimento é usar a técnica anterior, mas em cada lote, executar uma interpolação linear do valor do parâmetro para cada amostra.

Esses problemas são especialmente importantes para o processamento de áudio. Um segundo de áudio pode conter 48.000 amostras de áudio por canal, que são muitos cálculos a serem executados, mas o Ear é sensível a artefatos como alias.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Parâmetros de mídia](media-parameters.md)
</dt> </dl>

 

 



