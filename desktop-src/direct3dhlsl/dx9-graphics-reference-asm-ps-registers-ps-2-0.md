---
title: ps_2_0 registros
description: Este artigo contém informações de referência para os registros de entrada e saída implementados pelo sombreador de pixel versão 2_0.
ms.assetid: 8002e3eb-b9d4-4ecb-a9e5-ae58a9e20ace
keywords:
- Registros – ps_2_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 328eb1b0247c2c2c514ca9116a04e9add23f596d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406719"
---
# <a name="ps_2_0-registers"></a>ps \_ 2 \_ 0 Registros

Os sombreadores de pixel dependem de registros para obter dados de vértice, para saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura. Há vários tipos de registros, cada um com uma funcionalidade exclusiva. Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de pixel versão 2 \_ x.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registrar | Name                                                                                          | Contagem      | R/W        | \# Ler portas | \# Leituras/inst | Dimensão | RelAddr | Padrões                  | Requer DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| V\#      | [Registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Ilimitado     | 4         | N       | Partial(0001). confira a Observação 4 | Y            |
| R\#      | [Registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Confira a Observação 1 | R/W        | 3             | Ilimitado     | 4         | N       | Nenhum                      | N            |
| c\#      | [Registro float constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| Eu\#      | [Registro de inteiro constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Confira a observação 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| b\#      | [Registro booliana constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Confira a observação 2 | 1             | 1             | 1         | N       | FALSE                     | N            |
| p0       | [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Confira a observação 2 | 1             | 1             | 1         | N       | Nenhum                      | Y            |
| s\#      | [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Consulte a observação 3 | 1             | 1             | 4         | N       | confira a Observação 5                | Y            |
| T\#      | [Registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | Nenhum                      | Y            |



 

Observações:

1.  12 min/32 máx: o número de registros de r \# é determinado por D3DPSHADERCAPS2 \_ 0. NumTemps (que varia de 12 a 32).
2.  Utilizável somente por uma instrução de controle de fluxo.
3.  Utilizável somente por uma instrução de amostragem de textura.
4.  Partial (x, y, z, w) – se apenas um subconjunto de canais for atualizado no registro, os canais restantes usarão como padrão os valores especificados (x, y, z, w).
5.  Os padrões para pesquisas de amostra existem, mas os valores dependem do formato de textura.

O número de readports é o número de registros diferentes (para cada tipo de registro) que pode ser lido em uma única instrução.

## <a name="output-register-types"></a>Tipos de registro de saída



| Registrar | Name                                                                              | Contagem                                                                             | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| oC #     | [Registro de cor de saída](dx9-graphics-reference-asm-ps-registers-output-color.md) | Consulte [texturas de vários elementos (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Nenhum     | N            |
| oDepth   | [Registro de profundidade de saída](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Nenhum     | N            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 