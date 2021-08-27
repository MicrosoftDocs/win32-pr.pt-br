---
title: Registros de ps_2_0
description: Este artigo contém informações de referência para os registros de entrada e saída implementados pelo pixel shader versão 2_0.
ms.assetid: 8002e3eb-b9d4-4ecb-a9e5-ae58a9e20ace
keywords:
- Registros-ps_2_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b8e4300765f340b99da5d06b7651c4daaae4c97b043c6ceb5017aa43b2e2dcb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024146"
---
# <a name="ps_2_0-registers"></a>\_registros PS 2 \_ 0

Sombreadores de pixel dependem de registros para obter dados de vértice, de saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura. Há vários tipos de registradores, cada um com uma funcionalidade exclusiva. Esta seção contém informações de referência para os registros de entrada e saída implementados pelo pixel shader versão 2 \_ x.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registre-se | Nome                                                                                          | Contagem      | R/W        | \# Portas de leitura | \# Leituras/InStr | Dimensão | RelAddr | Padrões                  | Requer DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| v\#      | [Registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Ilimitado     | 4         | N       | Partial (0001). confira a Observação 4 | Y            |
| d\#      | [Registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Veja a observação 1 | R/W        | 3             | Ilimitado     | 4         | N       | Nenhum                      | N            |
| c\#      | [Registro de float de constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| Encontrei\#      | [Registro de inteiro constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Confira a observação 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| b\#      | [Registro booliano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Confira a observação 2 | 1             | 1             | 1         | N       | FALSE                     | N            |
| P0       | [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Confira a observação 2 | 1             | 1             | 1         | N       | Nenhum                      | Y            |
| s\#      | [Amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Veja a observação 3 | 1             | 1             | 4         | N       | confira a Observação 5                | Y            |
| t\#      | [Registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | Nenhum                      | Y            |



 

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

 

 