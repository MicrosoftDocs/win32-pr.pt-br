---
title: Registros de ps_3_0
description: Sombreadores de pixel dependem de registros para obter dados de vértice, de saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura.
ms.assetid: 01bee50a-c1b7-4b15-9df8-1dd52d9ff163
keywords:
- vPos
- Registro de posição, sombreador de pixel
- Registros-ps_3_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ef4eef435857968246ab0413841ef072b5391a5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366164"
---
# <a name="ps_3_0-registers"></a>\_registros PS 3 \_ 0

Sombreadores de pixel dependem de registros para obter dados de vértice, de saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura. Há vários tipos de registradores, cada um com uma funcionalidade exclusiva. Esta seção contém informações de referência para os registros de entrada e saída implementados pelo pixel shader versão 3 \_ 0.

## <a name="new-registers"></a>Novos registros

### <a name="input-register"></a>Registro de entrada

Os registros de entrada (v \# ) agora são de ponto totalmente flutuante e o s (t) [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) \# foi consolidado nele. A [semântica de DCL \_ (SM3-PS ASM)](dcl-usage---ps.md) na parte superior do sombreador é usada para descrever o que está contratado em um registro de entrada específico \_ . Uma semântica para os tipos de pixel é introduzida (análoga ao lado do vértice) para esse modelo. Nenhum fixação MSS é executado quando os registros de entrada são definidos como cores (como coordenadas de textura). A avaliação dos registros definidos como cor difere das coordenadas de textura quando há multiamostragens.

### <a name="face-register"></a>Registro facial

O vFace (registro facial) é novo para esse modelo. Esse é um registro escalar de ponto flutuante que eventualmente conterá a área primitiva. No \_ \_ entanto, no PS 3 0, somente o sinal desse registro é válido. Portanto, se o valor for menor que zero (o bit de sinal é definido como negativo), o primitivo será o verso (a área é negativa, no sentido anti-horário). Portanto, no PS \_ 3 \_ 0, faz sentido comparar esse registro com relação a 0 (> 0 ou < 0). Dentro do sombreador de pixel, o aplicativo pode tomar uma decisão sobre qual técnica de iluminação usar. A iluminação de dois lados pode ser obtida dessa forma. Esse registro requer uma declaração, portanto, o uso não declarado será sinalizado como um erro. Para linhas e primitivas de ponto, esse registro é indefinido. O registro facial só pode ser usado como condição com as seguintes instruções: [setp \_ comp-PS](setp-comp---ps.md), [se \_ comp-PS](if-comp---ps.md)ou [Break \_ comp-PS](break-comp---ps.md).

### <a name="loop-counter-register"></a>Registro de contador de loop

O [registro do contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) é novo para este modelo. Ele é incrementado automaticamente em cada execução do bloco de [bits do loop PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) . Ele pode ser usado no bloco para endereçamento relativo, se necessário. Não é válido usar o registro de contador de loop fora do loop.

### <a name="position-register"></a>Registro de posição

O vPos (registro de posição) é novo para este modelo. Ele contém os pixels atuais (x, y) nos canais correspondentes. Os canais (z, w) são indefinidos. Esse registro requer uma declaração, portanto, o uso não declarado será sinalizado como um erro. Quando declarado, esse registro deve ter exatamente uma das seguintes máscaras:. x,. y,. XY.

## <a name="input-register-types"></a>Tipos de registro de entrada



| Registre-se | Name                                                                                      | Contagem | R/W | \# Portas de leitura | \# Leituras/InStr | Dimensão | RelAddr | Padrões   | Requer DCL |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| l\#      | [Registro de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | Ilimitado     | 4         | &      | Nenhum       | Yes          |
| d\#      | [Registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | R/W | 3             | Ilimitado     | 4         | Não      | Nenhum       | No           |
| c\#      | [Registro de float de constante](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | Ilimitado     | 4         | Não      | 0000       | No           |
| Encontrei\#      | [Registro de inteiro constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | Não      | 0000       | No           |
| b\#      | [Registro booliano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | Não      | FALSE      | No           |
| P0       | [Registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | Não      | Nenhum       | No           |
| s\#      | [Amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | Não      | Veja a observação 1 | Yes          |
| vFace    | \_Registro facial                                                                            | 1     | R   | 1             | Ilimitado     | 1         | Não      | Nenhum       | Yes          |
| vPos     | Registro de posição \_                                                                        | 1     | R   | 1             | Ilimitado     | 4         | Não      | Nenhum       | Yes          |
| &       | \_Registro de contador de loop \_                                                                   | 1     | R   | 1             | Ilimitado     | 1         | n/d     | Nenhum       | No           |



 

Observações:

-   Os padrões para pesquisas de amostra existem, mas os valores dependem do formato de textura.

O número de readports é o número de registros diferentes (para cada tipo de registro) que pode ser lido em uma única instrução.

## <a name="output-register-types"></a>Tipos de registro de saída



| Registre-se | Name                                                                              | Contagem                                                                             | R/W | Dimensão | RelAddr | Padrões | Requer DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| oC #     | [Registro de cor de saída](dx9-graphics-reference-asm-ps-registers-output-color.md) | Consulte [texturas de vários elementos (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | Não      | Nenhum     | No           |
| oDepth   | [Registro de profundidade de saída](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | Não      | Nenhum     | No           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 