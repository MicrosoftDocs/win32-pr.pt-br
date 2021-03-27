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
ms.openlocfilehash: e6776fef206f9ced0608e86cbf596585399d4a12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822849"
---
# <a name="registers---vs_1_1"></a>Registros-vs \_ 1 \_ 1

Esta seção contém informações de referência para os registros de entrada e saída implementados pelo vertex shader versão 1 \_ 1.

## <a name="input-registers"></a>Registros de entrada



| Registre-se | Name                                                                                  | Contagem      | R/W | \# Portas de leitura | \# Leituras/InStr | Dimensão  | RelAddr | Padrões     | Requer DCL |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [Registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | R/W | 1             | Ilimitado       | Veja a observação 3 | Não      | Nenhum         | No           |
| c\#      | [Registro de float de constante](dx9-graphics-reference-asm-vs-registers-constant-float.md) | Confira a observação 2 | R   | 1             | Ilimitado       | 4          | a0 x    | (0, 0, 0, 0) | No           |
| l\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | Ilimitado       | 4          | Não      | Veja a observação 1   | Yes          |
| d\#      | [Registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | R/W | 3             | Ilimitado       | 4          | Não      | Nenhum         | No           |



 

Observações:

1.  Partial (0, 0, 0, 1) – se apenas um subconjunto de canais for atualizado, os canais restantes padrão serão (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (pelo menos 96 para vs \_ 1 \_ 1).
3.  Somente o canal. x está disponível.

## <a name="output-registers"></a>Registros de saída



| Registre-se | Name                        | Contagem | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | Registro de posição           | 1     | W   | 4         | Não      | Nenhum     | No           |
| oFog     | Registro de neblina                | 1     | W   | 1         | Não      | Nenhum     | No           |
| oPts     | Registro de tamanho do ponto         | 1     | W   | 1         | Não      | Nenhum     | No           |
| oD\#     | Registro de cores; Veja a observação 1  | 2     | W   | 4         | Não      | Nenhum     | No           |
| To\#     | Registro de coordenadas de textura | 8     | W   | 4         | Não      | Nenhum     | No           |



 

Observações:

-   oD0 é a saída de cor difusa; oD1 é a saída de cor especular.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




