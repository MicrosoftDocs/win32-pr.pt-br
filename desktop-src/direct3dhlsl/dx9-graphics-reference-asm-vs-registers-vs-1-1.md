---
title: Registros-vs_1_1
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo vertex shader versão 1 \_ 1.
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4bcfadae2b1dca70298ffed188de2e6075892563b27bf6f624f2139e441600cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908000"
---
# <a name="registers---vs_1_1"></a>Registros-vs \_ 1 \_ 1

Esta seção contém informações de referência para os registros de entrada e saída implementados pelo vertex shader versão 1 \_ 1.

## <a name="input-registers"></a>Registros de entrada



| Registre-se | Nome                                                                                  | Contagem      | R/W | \# Portas de leitura | \# Leituras/InStr | Dimensão  | RelAddr | Padrões     | Requer DCL |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [Registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | R/W | 1             | Ilimitado       | Veja a observação 3 | Não      | Nenhum         | Não           |
| c\#      | [Registro de float de constante](dx9-graphics-reference-asm-vs-registers-constant-float.md) | Confira a observação 2 | R   | 1             | Ilimitado       | 4          | a0 x    | (0, 0, 0, 0) | Não           |
| l\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | Ilimitado       | 4          | Não      | Confira a Observação 1   | Sim          |
| d\#      | [Registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | R/W | 3             | Ilimitado       | 4          | Não      | Nenhum         | Não           |



 

Observações:

1.  Partial (0, 0, 0, 1) – se apenas um subconjunto de canais for atualizado, os canais restantes padrão serão (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (pelo menos 96 para vs \_ 1 \_ 1).
3.  Somente o canal. x está disponível.

## <a name="output-registers"></a>Registros de saída



| Registre-se | Nome                        | Contagem | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | Registro de posição           | 1     | W   | 4         | Não      | Nenhum     | Não           |
| oFog     | Registro de neblina                | 1     | W   | 1         | Não      | Nenhum     | Não           |
| oPts     | Registro de tamanho do ponto         | 1     | W   | 1         | Não      | Nenhum     | Não           |
| oD\#     | Registro de cores; Veja a observação 1  | 2     | W   | 4         | Não      | Nenhum     | Não           |
| Ot\#     | Registro de coordenadas de textura | 8     | W   | 4         | Não      | Nenhum     | Não           |



 

Observações:

-   oD0 é a saída de cor difusa; oD1 é a saída de cor especular.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




