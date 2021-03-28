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
ms.openlocfilehash: 156367ec08a5f1ecd94181be56558f4ba07005b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005365"
---
# <a name="registers---vs_2_0"></a>Registros-vs \_ 2 \_ 0

Esta seção contém informações de referência para os registros de entrada e saída implementados pelo vertex shader versão 2 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Registre-se | Name                                                                                      | Contagem      | R/W | \# Portas de leitura | \# Leituras/InStr | Dimensão | RelAddr | Padrões     | Requer DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| l\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Ilimitado       | 4         | Não      | Veja a observação 1   | Yes          |
| d\#      | [Registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 12         | R/W | 3             | Ilimitado       | 4         | Não      | Nenhum         | No           |
| c\#      | [Registro de float de constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Confira a observação 2 | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | No           |
| a0       | [Registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | 2               | 4         | Não      | Nenhum         | No           |
| b\#      | [Registro booliano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Não      | FALSE        | No           |
| Encontrei\#      | [Registro de inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Não      | (0, 0, 0, 0) | No           |
| &       | [Registro de contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | Não      | Nenhum         | No           |



 

Observações:

1.  Partial (0, 0, 0, 1) – se apenas um subconjunto de canais for atualizado, os canais restantes padrão serão (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (pelo menos 256 para vs \_ 2 \_ 0).

## <a name="output-registers"></a>Registros de saída



| Registre-se | Name                                                                                          | Contagem | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | [Registro de posição](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | Não      | Nenhum     | No           |
| oFog     | [Registro de neblina](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | Não      | Nenhum     | No           |
| oPts     | [Registro de tamanho do ponto](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | Não      | Nenhum     | No           |
| oD\#     | [Registro de cores](dx9-graphics-reference-asm-vs-registers-color.md); Veja a observação 1               | 2     | W   | 4         | Não      | Nenhum     | No           |
| To\#     | [Registro de coordenadas de textura](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | Não      | Nenhum     | No           |



 

Observações:

-   oD0 é a saída de cor difusa; oD1 é a saída de cor especular.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




