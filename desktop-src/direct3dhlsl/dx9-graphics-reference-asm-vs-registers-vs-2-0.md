---
title: Registros-vs_2_0
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo vertex shader versão 2 \_ 0.
ms.assetid: e5ef015e-1e4d-41b3-95da-3b44ef0bd73e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd31f4ce5cac538624fe736642b30cbee9ba54579ee50da9a2ccd027847e9ecc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067966"
---
# <a name="registers---vs_2_0"></a>Registros-vs \_ 2 \_ 0

Esta seção contém informações de referência para os registros de entrada e saída implementados pelo vertex shader versão 2 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Registre-se | Nome                                                                                      | Contagem      | R/W | \# Portas de leitura | \# Leituras/InStr | Dimensão | RelAddr | Padrões     | Requer DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Ilimitado       | 4         | Não      | Confira a Observação 1   | Sim          |
| d\#      | [Registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 12         | R/W | 3             | Ilimitado       | 4         | Não      | Nenhum         | Não           |
| c\#      | [Registro de float de constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Confira a observação 2 | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | Não           |
| a0       | [Registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | 2               | 4         | Não      | Nenhum         | Não           |
| b\#      | [Registro booliano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Não      | FALSE        | Não           |
| Encontrei\#      | [Registro de inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Não      | (0, 0, 0, 0) | Não           |
| &       | [Registro de contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | Não      | Nenhum         | Não           |



 

Observações:

1.  Partial (0, 0, 0, 1) – se apenas um subconjunto de canais for atualizado, os canais restantes padrão serão (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (pelo menos 256 para vs \_ 2 \_ 0).

## <a name="output-registers"></a>Registros de saída



| Registre-se | Nome                                                                                          | Contagem | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | [Registro de posição](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | Não      | Nenhum     | Não           |
| oFog     | [Registro de neblina](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | Não      | Nenhum     | Não           |
| oPts     | [Registro de tamanho do ponto](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | Não      | Nenhum     | Não           |
| oD\#     | [Registro de cores](dx9-graphics-reference-asm-vs-registers-color.md); Veja a observação 1               | 2     | W   | 4         | Não      | Nenhum     | Não           |
| To\#     | [Registro de coordenadas de textura](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | Não      | Nenhum     | Não           |



 

Observações:

-   oD0 é a saída de cor difusa; oD1 é a saída de cor especular.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




