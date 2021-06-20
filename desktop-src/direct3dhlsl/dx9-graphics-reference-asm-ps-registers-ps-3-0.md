---
title: ps_3_0 registros
description: Este artigo contém informações de referência para os registros de entrada e saída implementados pelo sombreador de pixel versão 3_0.
ms.assetid: 01bee50a-c1b7-4b15-9df8-1dd52d9ff163
keywords:
- vPos
- Registro de Posição, Sombreador de Pixel
- Registros – ps_3_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1cd0173beabc8fbe21ad15e88e23fc1b6e84892
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405489"
---
# <a name="ps_3_0-registers"></a>ps \_ 3 \_ 0 Registros

Os sombreadores de pixel dependem de registros para obter dados de vértice, para saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura. Há vários tipos de registros, cada um com uma funcionalidade exclusiva. Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de pixel versão 3 \_ 0.

## <a name="new-registers"></a>Novos registros

### <a name="input-register"></a>Registro de Entrada

Os Registros de Entrada (v ) agora são um ponto totalmente flutuante e o Registro de Coordenadas de Textura (t ) foi \# consolidado [](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) \# nele. A [semântica dcl \_ (sm3 – ps asm)](dcl-usage---ps.md) na parte superior do sombreador é usada para descrever o que está contenha em um Registro de \_ Entrada específico. Uma semântica para os tipos de pixel é introduzida (análoga ao lado do vértice) para esse modelo. Nenhuma fixação é executada quando os registros de entrada são definidos como cores (como coordenadas de textura). A avaliação dos registros definidos como cor difere das coordenadas de textura durante a multisampling.

### <a name="face-register"></a>Registro facial

O registro facial (vFace) é novo para esse modelo. Esse é um registro escalar de ponto flutuante que, eventualmente, conterá a área primitiva. No entanto, \_ no ps \_ 3 0, somente o sinal desse registro é válido. Portanto, se o valor for menor que zero (o bit de sinal é definido como negativo), o primitivo será a face traseira (a área é negativa, no sentido anti-horário). Portanto, no ps 3 0, só faz sentido comparar esse registro com \_ \_ 0 (> 0 ou < 0). Dentro do sombreador de pixel, o aplicativo pode tomar uma decisão sobre qual técnica de iluminação usar. A iluminação de dois lados pode ser alcançada dessa maneira. Esse registro requer uma declaração, portanto, o uso não declarado será sinalizado como um erro. Para linhas e primitivos de ponto, esse registro é indefinido. O registro facial só pode ser usado como condição com as seguintes instruções: [setp \_ comp - ps](setp-comp---ps.md), [if comp - \_ ps](if-comp---ps.md)ou [break comp - \_ ps](break-comp---ps.md).

### <a name="loop-counter-register"></a>Registro de contador de loop

O [AL (Registro de](dx9-graphics-reference-asm-ps-registers-loop-counter.md) Contador de Loop) é novo para esse modelo. Ele é incrementado automaticamente em cada execução do [loop – ps](loop---ps.md) / [endloop – bloco ps.](endloop---ps.md) Ele pode ser usado no bloco para endereçamento relativo, se necessário. É inválido usar o Registro de Contador de Loop fora do loop.

### <a name="position-register"></a>Registro de posição

O Registro de Posição (vPos) é novo para esse modelo. Ele contém os pixels atuais (x, y) nos canais correspondentes. Os canais (z, w) são indefinido. Esse registro requer uma declaração, portanto, o uso não declarado será sinalizado como um erro. Quando declarado, esse registro deve ter exatamente uma das seguintes máscaras: .x, .y, .xy.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registrar | Name                                                                                      | Contagem | R/W | \# Ler portas | \# Leituras/inst | Dimensão | RelAddr | Padrões   | Requer DCL |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| V\#      | [Registro de Entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | Ilimitado     | 4         | Al      | Nenhum       | Sim          |
| R\#      | [Registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | R/W | 3             | Ilimitado     | 4         | Não      | Nenhum       | Não           |
| c\#      | [Registro float constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | Ilimitado     | 4         | Não      | 0000       | Não           |
| Eu\#      | [Registro de inteiro constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | Não      | 0000       | Não           |
| b\#      | [Registro booliana constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | Não      | FALSE      | Não           |
| p0       | [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | Não      | Nenhum       | Não           |
| s\#      | [Amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | Não      | Confira a Observação 1 | Sim          |
| vFace    | \_Registro facial                                                                            | 1     | R   | 1             | Ilimitado     | 1         | Não      | Nenhum       | Sim          |
| vPos     | Registro de posição \_                                                                        | 1     | R   | 1             | Ilimitado     | 4         | Não      | Nenhum       | Sim          |
| &       | \_Registro de contador de loop \_                                                                   | 1     | R   | 1             | Ilimitado     | 1         | n/d     | Nenhum       | Não           |



 

Observações:

-   Os padrões para pesquisas de amostra existem, mas os valores dependem do formato de textura.

O número de readports é o número de registros diferentes (para cada tipo de registro) que pode ser lido em uma única instrução.

## <a name="output-register-types"></a>Tipos de registro de saída



| Registrar | Name                                                                              | Contagem                                                                             | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| oC #     | [Registro de cor de saída](dx9-graphics-reference-asm-ps-registers-output-color.md) | Consulte [texturas de vários elementos (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | Não      | Nenhum     | Não           |
| oDepth   | [Registro de profundidade de saída](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | Não      | Nenhum     | Não           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 