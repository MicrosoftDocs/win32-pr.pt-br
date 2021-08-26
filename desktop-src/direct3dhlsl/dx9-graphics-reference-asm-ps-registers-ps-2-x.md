---
title: ps_2_x registros
description: Este artigo contém informações de referência para os registros de entrada e saída implementados pela versão do sombreador de pixel 2_x.
ms.assetid: 52bb6290-46e2-4d7d-9b96-b4c3e2abfe43
keywords:
- Registros – ps_2_x
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c9f3c71ab6308ad921b5cce27f2c078ad980da17daa7c0045228d27ef0579ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024116"
---
# <a name="ps_2_x-registers"></a>ps \_ 2 \_ x Registers

Os sombreadores de pixel dependem de registros para obter dados de vértice, para saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura. Há vários tipos de registros, cada um com uma funcionalidade exclusiva. Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de pixel versão 2 \_ x.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registre-se | Nome                                                                                          | Contagem      | R/W        | \# Ler portas | \# Leituras/inst | Dimensão | RelAddr | Padrões                  | Requer DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| v\#      | [Registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Ilimitado     | 4         | N       | Partial(0001). confira a Observação 4 | Y            |
| R\#      | [Registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Consulte a observação 1 | R/W        | 3             | Ilimitado     | 4         | N       | Nenhum                      | N            |
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



| Registre-se | Nome                                                                              | Contagem                                                                             | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| oC #     | [Registro de cor de saída](dx9-graphics-reference-asm-ps-registers-output-color.md) | Consulte [texturas de vários elementos (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Nenhum     | N            |
| oDepth   | [Registro de profundidade de saída](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Nenhum     | N            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 