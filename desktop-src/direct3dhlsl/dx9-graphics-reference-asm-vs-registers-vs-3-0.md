---
title: Registros – vs_3_0
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de vértice versão 3 \_ 0.
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d658d2d14d149d5d83d673269f2a414d7feaa22f13f1b32f57c4b80500fb1398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673096"
---
# <a name="registers---vs_3_0"></a>Registros – vs \_ 3 \_ 0

Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de vértice versão 3 \_ 0.

## <a name="input-registers"></a>Registros de entrada



| Registre-se | Nome                                                                                      | Contagem      | R/W | \# Ler portas | \# Leituras/inst | Dimensão | RelAddr | Padrões     | Requer DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registro de Entrada](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Ilimitado       | 4         | a0/aL   | Consulte a observação 1   | Sim          |
| R\#      | [Registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | R/W | 3             | Ilimitado       | 4         | Não      | Nenhum         | Não           |
| c\#      | [Registro float constante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Confira a observação 2 | R   | 1             | Ilimitado       | 4         | a0/aL   | (0, 0, 0, 0) | Não           |
| a0       | [Registro de endereço](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | Ilimitado       | 4         | Não      | Nenhum         | Não           |
| b\#      | [Registro booliana constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Não      | FALSE        | Não           |
| Eu\#      | [Registro de inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | Não      | (0, 0, 0, 0) | Não           |
| Al       | [Registro de contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | Ilimitado       | 1         | Não      | Nenhum         | Não           |
| p0       | [Registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W | 1             | 1               | 4         | não      | nenhum         | não           |
| s\#      | [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | Não      | Consulte a observação 3   | Sim          |



 

Observações:

1.  Parcial (0, 0, 0, 1) – se apenas um subconjunto de canais for atualizado, os canais restantes terão como padrão (0, 0, 0, 1).
2.  Igual a D3DCAPS9. MaxVertexShaderConst (pelo menos 256 para \_ versus 3 \_ 0).
3.  Existem padrões para a busca de amostra, mas os valores dependem do formato de textura.

## <a name="output-registers"></a>Registros de saída

Os registros de saída foram recolhidos em 12 registros \# (saída). Eles podem ser usados para qualquer coisa que o usuário deseja interpolar para o sombreador de pixel: coordenadas de textura, cores, etc.



| Registre-se | Nome            | Contagem | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| o\#      | Registro de Saída | 12    | W   | 4         | Al      | Nenhum     | Sim          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




