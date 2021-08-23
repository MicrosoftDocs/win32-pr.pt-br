---
title: gather4_po_c (sm5 – asm)
description: Comporta-se da mesma forma que gather4 \_ po, exceto que executa a comparação em texels, semelhante à amostra \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83342aed97663c027b0915f612b13b288192d937d29d364257004cfc8966aec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743866"
---
# <a name="gather4_po_c-sm5---asm"></a>gather4 \_ po \_ c (sm5 - asm)

Comporta-se da mesma forma [**que gather4 \_ po**](gather4-po--sm5---asm-.md), exceto que executa a comparação em texels, semelhante ao [**exemplo \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ po \_ c dest \[ .mask , \] srcAddress \[ .swizzle \] , srcOffset \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler \[ . R, \] srcReferenceValue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                                       | Descrição                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[em \] O endereço do resultado da operação.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[em \] Um conjunto de coordenadas de textura.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*Srcoffset*<br/>                                 | \[em \] O deslocamento.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[em \] Um registro de textura.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[em \] Um registro de exemplo.<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[em \] Componente único selecionado.<br/>                  |



 

## <a name="remarks"></a>Comentários

Consulte [**o \_ exemplo c**](sample-c--sm4---asm-.md) para obter informações sobre como *srcReferenceValue* é comparado com cada texel buscado. Ao **contrário do exemplo \_ c**, *gather4 po \_ \_ c* retorna cada resultado de comparação, em vez de filtre-os.

Essa instrução, como **gather4 \_ po**, funciona apenas com texturas 2D. Isso é diferente [**de gather4 \_ c**](gather4-c--sm5---asm-.md), que também funciona com TextureCubes.

Para formatos com componentes float32, se o valor que está sendo buscado for normalizado ou +-INF, ele será usado na operação de comparação inalterado. NaN é usado na operação de comparação como NaN, mas a representação exata de bit do NaN pode ser alterada. Os desnorms são liberados para zero entrando na comparação. Para TextureCubes, alguma síntese do 4º texel ausente deve ocorrer em cantos, portanto, a noção de retorno de bits inalterados para o texel sintetizado não se aplica.

Os formatos com suporte **para gather4 \_ po \_ c** são os mesmos que os com suporte para o **exemplo \_ c**. Esses são formatos de componente único, portanto, o . R em srcSampler, em vez de um swizzle arbitrário.

**gather4 \_ po \_ c** em um recurso nãobound retorna 0.

Use esse método para filtragem de mapa de sombra.

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

 

 





