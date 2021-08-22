---
title: gather4_c (sm5 – asm)
description: O mesmo que gather4, exceto que essa instrução executa a comparação em texels, semelhante à amostra \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b300e27743d08f3bbdf813de200b5a749a4ac25f16ab10458968731b9918c493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488686"
---
# <a name="gather4_c-sm5---asm"></a>gather4 \_ c (sm5 – asm)

O mesmo [**que gather4**](gather4--sm5---asm-.md), exceto que essa instrução executa a comparação em texels, semelhante ao [**exemplo \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ c \[ \_ aoffimmi(u,v) \] dest \[ \] .mask, srcAddress \[ .swizzle, \] srcResource \[ .swizzle, \] srcSampler \[ . R, \] srcReferenceValue |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                                       | Descrição                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[em \] O endereço do resultado da operação<br/>                                    |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[em \] Um conjunto de coordenadas de textura.<br/>                                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[em \] Um registro de textura.<br/>                                                           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[em \] Um registro de exemplo.<br/>                                                           |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[em \] Um registro com um único componente selecionado, que é usado na comparação.<br/> |



 

## <a name="remarks"></a>Comentários

Consulte [**o \_ exemplo c**](sample-c--sm4---asm-.md) para obter uma descrição de como *srcReferenceValue* é comparado com cada texel buscado. Ao contrário **do \_ exemplo c**, **gather4 \_ c** retorna cada resultado de comparação, em vez de filtre-os.

Para cantos textureCube, em que há três reais texels e um quarto deve ser sintetizado, a síntese deve ocorrer após a etapa de comparação. Isso significa que o resultado de comparação retornado para o texel sintesizado pode ser 0, 0,33 , 0,66 ou 1. Algumas implementações só podem retornar 0 ou 1 para o texel sintetizado. Além dessa listagem de possíveis resultados, o método para sintetizar o texel não é especificado.

Para formatos com componentes float32, se o valor que está sendo buscado for normalizado ou +-INF, ele será usado na operação de comparação inalterado. NaN é usado na operação de comparação como NaN, mas a representação exata de bit do NaN pode ser alterada. Os desnorms são liberados para zero entrando na comparação. Para TextureCubes, alguma síntese do 4º texel ausente deve ocorrer em cantos, portanto, a noção de retorno de bits inalterados para o texel sintetizado não se aplica.

Os formatos com suporte *para gather4 \_ c* são os mesmos que os com suporte para o *exemplo \_ c*. Esses são formatos de componente único, portanto, o . R em *srcSampler*, em vez de um swizzle arbitrário. **gather4 \_ c** em um recurso nãobound retorna 0.

Use esta instrução para filtragem de mapa de sombra personalizada.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





