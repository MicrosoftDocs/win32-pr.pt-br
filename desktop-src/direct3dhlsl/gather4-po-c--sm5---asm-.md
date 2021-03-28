---
title: gather4_po_c (SM5-ASM)
description: Comporta-se da mesma forma que gather4 \_ Po, exceto realiza a comparação em texels, semelhante ao exemplo \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365264"
---
# <a name="gather4_po_c-sm5---asm"></a>gather4 \_ po \_ c (SM5-ASM)

Comporta-se da mesma forma que [**gather4 \_ po**](gather4-po--sm5---asm-.md), exceto realiza a comparação em texels, semelhante ao [**exemplo \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ po \_ c dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcOffset \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . R \] , srcReferenceValue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                                       | Descrição                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[no \] endereço do resultado da operação.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[em \] um conjunto de coordenadas de textura.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>                                 | \[no \] deslocamento.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[em \] um registro de textura.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[em \] um registro de amostra.<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[em \] um único componente selecionado.<br/>                  |



 

## <a name="remarks"></a>Comentários

Consulte [**exemplo \_ c**](sample-c--sm4---asm-.md) para obter informações sobre como o *srcReferenceValue* é comparado com cada Texel buscada. Ao contrário do **exemplo \_ c**, o *gather4 \_ po \_ c* retorna cada resultado da comparação, em vez de filtrá-los.

Essa instrução, como o **gather4 \_ po**, funciona apenas com texturas 2D. Isso é diferente de [**gather4 \_ c**](gather4-c--sm5---asm-.md), que também funciona com TextureCubes.

Para formatos com componentes float32, se o valor que está sendo obtido for normalizado, ou +-INF, ele será usado na operação de comparação inalterada. NaN é usado na operação de comparação como NaN, mas a representação de bit exata do NaN pode ser alterada. As desnormas são liberadas para zero, indo para a comparação. Para TextureCubes, alguma síntese do 4º Texel ausente deve ocorrer nos cantos, portanto a noção de retorno de bits inalterado para o Texel sintetizado não se aplica.

Os formatos com suporte para a **\_ OC \_ c gather4** são iguais aos compatíveis com o **exemplo \_ c**. Esses são formatos de componente único, portanto, o. R em srcSampler, em vez de um swizzle arbitrário.

o **gather4 \_ po \_ c** em um recurso não associado retorna 0.

Use este método para filtragem de mapa de sombra.

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

 

 





