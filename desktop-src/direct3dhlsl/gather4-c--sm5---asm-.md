---
title: gather4_c (SM5-ASM)
description: O mesmo que gather4, exceto que esse instruting executa a comparação em texels, semelhante ao exemplo \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988597"
---
# <a name="gather4_c-sm5---asm"></a>gather4 \_ c (SM5-ASM)

O mesmo que [**gather4**](gather4--sm5---asm-.md), exceto que esse instruting executa a comparação em texels, semelhante ao [**exemplo \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ c \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . R \] , srcReferenceValue |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                                       | Descrição                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[no \] endereço do resultado da operação<br/>                                    |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[em \] um conjunto de coordenadas de textura.<br/>                                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[em \] um registro de textura.<br/>                                                           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[em \] um registro de amostra.<br/>                                                           |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[em \] um registro com um único componente selecionado, que é usado na comparação.<br/> |



 

## <a name="remarks"></a>Comentários

Consulte [**exemplo \_ c**](sample-c--sm4---asm-.md) para obter uma descrição de como o *srcReferenceValue* é comparado com cada Texel buscada. Ao contrário do **exemplo \_ c**, **gather4 \_ c** retorna cada resultado da comparação, em vez de filtrá-los.

Para os cantos TextureCube, onde há três texels reais e a quarta deve ser sintetizada, a síntese deve ocorrer após a etapa de comparação. Isso significa que o resultado de comparação retornado para o syntesized Texel pode ser 0, 0,33, 0,66 ou 1. Algumas implementações só podem retornar 0 ou 1 para o Texel sintetizado. Além dessa listagem de possíveis resultados, o método para sintetizar o Texel não é especificado.

Para formatos com componentes float32, se o valor que está sendo obtido for normalizado, ou +-INF, ele será usado na operação de comparação inalterada. NaN é usado na operação de comparação como NaN, mas a representação de bit exata do NaN pode ser alterada. As desnormas são liberadas para zero, indo para a comparação. Para TextureCubes, alguma síntese do 4º Texel ausente deve ocorrer nos cantos, portanto a noção de retorno de bits inalterado para o Texel sintetizado não se aplica.

Os formatos com suporte para *gather4 \_ c* são iguais aos compatíveis com o *exemplo \_ c*. Esses são formatos de componente único, portanto, o. R em *srcSampler*, em vez de um swizzle arbitrário. **gather4 \_ c** em um recurso não associado retorna 0.

Use esta instrução para filtrar o mapa de sombra personalizado.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





