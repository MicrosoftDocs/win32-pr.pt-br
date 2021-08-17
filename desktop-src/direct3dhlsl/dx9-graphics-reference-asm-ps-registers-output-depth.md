---
title: Registro de profundidade de saída
description: O oDepth (registro de profundidade de saída) do sombreador de pixel é um registro escalar somente gravação com o intervalo \ 0.. 1 \ que retorna um novo valor de profundidade para um teste de profundidade no buffer do estêncil de profundidade.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 041ffccb3301831c91554ef3cda835d3f2e79204730e838b25f26660e76d9a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119720"
---
# <a name="output-depth-register"></a>Registro de profundidade de saída

O oDepth (registro de profundidade de saída) do sombreador de pixel é um registro escalar somente gravação com o intervalo \[ 0.. 1 \] que retorna um novo valor de profundidade para um teste de profundidade em relação ao buffer do estêncil de profundidade.

Syntax



| oDepth |
|--------|



 

Em que:



| Nome   | Descrição                                                       |
|--------|-------------------------------------------------------------------|
| oDepth | Novo valor de profundidade para um teste de profundidade no buffer de estêncil de profundidade |



 

É importante estar ciente de que a gravação em oDepth causa a perda de qualquer algoritmo de otimização de buffer de profundidade específico do hardware (ou seja, a Z hierárquico) que acelera o desempenho do teste de profundidade.

Replicar swizzle de origem (. x \| . y \| . z \| . w) é necessário ao gravar em oDepth. Não são permitidas máscaras de gravação explícitas.

Gravar no registro oDepth substitui o valor de profundidade interpolado (e ignora qualquer tendência de profundidade/slopescale renderstates). Se nenhum buffer de profundidade tiver sido criado ou anexado ao dispositivo, então gravar em oDepth será ignorado.

Se você for multiamostrar e gravar em oDepth, como o sombreador de pixel só é executado uma vez por pixel, o valor de profundidade é replicado para todos os locais de subamostras cobertos. O teste de profundidade ainda acontece por exemplo, mas você não tem um valor de profundidade por amostra na comparação do sombreador de pixel como você teria se não escrever oDepth.

Se um aplicativo tiver um conjunto de buffer w como seu buffer de profundidade, ele precisa levar isso em conta ao gravar no oDepth. Ele potencialmente precisa enviar informações de intervalo w para o sombreador de pixel e calcular o intervalo w para dimensionar os valores w gravados em oDepth.

### <a name="ps_2_0-and-ps_2_x-restrictions"></a>\_restrições PS 2 \_ 0 e PS \_ 2 \_ x

-   oDepth só pode ser escrito com a instrução [Mov-PS](mov---ps.md) e só pode ser feito uma vez.
-   Nenhum modificador de origem é permitido ao gravar em oDepth.
-   Nenhum modificador de instrução é permitido ao gravar em oDepth.
-   Não há gravação no oDepth de dentro de uma construção de controle de fluxo ou ao usar predicação.

### <a name="ps_3_0-restrictions"></a>Restrições do PS \_ 3 \_ 0

-   Para o PS \_ 3 \_ 0, os registros de saída OC # e OD \# podem ser gravados várias vezes. A saída do sombreador de pixel é proveniente do conteúdo dos registros de saída no final da execução do sombreador. Se uma gravação em um registro de saída não ocorrer, talvez devido ao controle de fluxo ou se o sombreador simplesmente não o escreveu, o destino de renderização correspondente também não será atualizado. Se um subconjunto dos canais em um registro de saída for gravado, os valores indefinidos serão gravados nos canais restantes.
-   Você pode gravar em oDepth no controle de fluxo ou predicação, desde que todos os caminhos possíveis eventualmente gravem no registro.
-   Você não pode executar cálculos de gradiente (ou operações que invocam implicitamente cálculos de gradiente, como [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) dentro de instruções de controle de fluxo cujas condições de ramificação variam em uma base por primitiva (isto é: instruções de controle de fluxo dinâmico). Instrução predicação não é considerada controle de fluxo dinâmico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




