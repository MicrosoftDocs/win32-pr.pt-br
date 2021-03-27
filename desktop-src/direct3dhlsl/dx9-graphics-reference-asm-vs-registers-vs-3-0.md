---
title: Registros-vs_3_0
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pela versão 3 0 do sombreador de vértice \_ .
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47353a3f312a2abbd6f4fe5ea1dcd1ed9495a9d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636660"
---
# <a name="registers---vs_3_0"></a>Registros-vs \_ 3 \_ 0

Esta seção contém informações de referência para os registros de entrada e saída implementados pela versão 3 0 do sombreador de vértice \_ .

## <a name="input-registers"></a>Registros de entrada



| Registre-se | Name                                                                                      | Contagem      | R/W | \# Portas de leitura | \# Leituras/InStr | Dimensão | RelAddr | Padrões     | Requer DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| l\#      | [Registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Ilimitado       | 4         | a0/aL   | Veja a observação 1   | Yes          |
| d\#      | [Registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | R/W | 3             | Ilimitado       | 4         | Não      | Nenhum         | No           |
| c\#      | [Registro de float de constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Confira a observação 2 | R   | 1             | Ilimitado       | 4         | a0/aL   | (0, 0, 0, 0) | No           |
| a0       | [Registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | Ilimitado       | 4         | Não      | Nenhum         | No           |
| b\#      | [Registro booliano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Não      | FALSE        | No           |
| Encontrei\#      | [Registro de inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Não      | (0, 0, 0, 0) | No           |
| &       | [Registro de contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | Ilimitado       | 1         | Não      | Nenhum         | No           |
| P0       | [Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W | 1             | 1               | 4         | não      | nenhum         | não           |
| s\#      | [Amostra (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | Não      | Veja a observação 3   | Yes          |



 

Observações:

1.  Partial (0, 0, 0, 1) – se apenas um subconjunto de canais for atualizado, os canais restantes padrão serão (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (pelo menos 256 para vs \_ 3 \_ 0).
3.  Os padrões para a pesquisa de amostra existem, mas os valores dependem do formato de textura.

## <a name="output-registers"></a>Registros de saída

Os registros de saída foram recolhidos em \# registros de 12 o (saída). Eles podem ser usados para qualquer coisa que o usuário deseja interpolar para o sombreador de pixel: coordenadas de textura, cores, neblina, etc.



| Registre-se | Name            | Contagem | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| minúscula\#      | Registro de saída | 12    | W   | 4         | &      | Nenhum     | Yes          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




