---
title: Registros de ps_2_x
description: Sombreadores de pixel dependem de registros para obter dados de vértice, de saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura.
ms.assetid: 52bb6290-46e2-4d7d-9b96-b4c3e2abfe43
keywords:
- Registros-ps_2_x
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 880c897aa3d812d1e94e5dc408e97ec18b5de106
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967183"
---
# <a name="ps_2_x-registers"></a>\_registros PS 2 \_ x

Sombreadores de pixel dependem de registros para obter dados de vértice, de saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura. Há vários tipos de registradores, cada um com uma funcionalidade exclusiva. Esta seção contém informações de referência para os registros de entrada e saída implementados pelo pixel shader versão 2 \_ x.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registre-se | Name                                                                                          | Contagem      | R/W        | \# Portas de leitura | \# Leituras/InStr | Dimensão | RelAddr | Padrões                  | Requer DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| l\#      | [Registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Ilimitado     | 4         | N       | Partial (0001). Veja a observação 4 | S            |
| d\#      | [Registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Veja a observação 1 | R/W        | 3             | Ilimitado     | 4         | N       | Nenhum                      | N            |
| c\#      | [Registro de float de constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| Encontrei\#      | [Registro de inteiro constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Confira a observação 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| b\#      | [Registro booliano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Confira a observação 2 | 1             | 1             | 1         | N       | FALSE                     | N            |
| P0       | [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Confira a observação 2 | 1             | 1             | 1         | N       | Nenhum                      | S            |
| s\#      | [Amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Veja a observação 3 | 1             | 1             | 4         | N       | Consulte a observação 5                | S            |
| t\#      | [Registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | Nenhum                      | S            |



 

Observações:

1.  12 min/32 máx: o número de registros de r \# é determinado por D3DPSHADERCAPS2 \_ 0. NumTemps (que varia de 12 a 32).
2.  Utilizável somente por uma instrução de controle de fluxo.
3.  Utilizável somente por uma instrução de amostragem de textura.
4.  Partial (x, y, z, w) – se apenas um subconjunto de canais for atualizado no registro, os canais restantes usarão como padrão os valores especificados (x, y, z, w).
5.  Os padrões para pesquisas de amostra existem, mas os valores dependem do formato de textura.

O número de readports é o número de registros diferentes (para cada tipo de registro) que pode ser lido em uma única instrução.

## <a name="output-register-types"></a>Tipos de registro de saída



| Registre-se | Name                                                                              | Contagem                                                                             | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| oC #     | [Registro de cor de saída](dx9-graphics-reference-asm-ps-registers-output-color.md) | Consulte [texturas de vários elementos (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Nenhum     | N            |
| oDepth   | [Registro de profundidade de saída](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Nenhum     | N            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 