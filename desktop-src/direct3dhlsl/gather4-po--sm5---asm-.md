---
title: gather4_po (sm5 – asm)
description: Uma variante de gather4, mas em vez de dar suporte a um deslocamento imediato \ -8,7\, o deslocamento vem como um parâmetro para a instrução e também tem um intervalo maior de \ -32..31\ .
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e18859c2df7b26511f89e6e791573fe74a69f6bd548706ac65e6b268ca08e2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089886"
---
# <a name="gather4_po-sm5---asm"></a>gather4 \_ po (sm5 - asm)

Uma variante de [gather4](gather4--sm5---asm-.md), mas em vez de dar suporte a um deslocamento imediato -8..7 , o deslocamento vem como um parâmetro para a instrução e também tem um intervalo maior de \[ \] \[ -32,.31 \] .



| gather4 \_ po dest \[ .mask , \] srcAddress \[ .swizzle \] , srcOffset \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler \[ .select \_ component\] |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[em \] O endereço do resultado da operação.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] Um conjunto de coordenadas de textura.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*Srcoffset*<br/>         | \[em \] O deslocamento.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] Um registro de textura.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] Um registro de exemplo.<br/>                         |



 

## <a name="remarks"></a>Comentários

Os dois primeiros componentes do parâmetro de deslocamento de 4 vetores fornecem deslocamentos inteiros de 32 bits. Os outros componentes desse parâmetro são ignorados.

Os 6 bits menos significativos de cada valor de deslocamento são honorados como um valor assinado, produtividade de \[ -32,.31 \] intervalo.

Essa instrução funciona apenas com texturas 2D, ao contrário **de gather4,** que também funciona com TextureCubes.

Os únicos modos honorados no exemplo são os modos de endereçamento. Somente o mip mais detalhado na exibição de recursos é usado.

Se o endereço estiver em um centro de texel, isso não significa que os outros texels poderão ser zerados.

O *parâmetro srcSampler* inclui o componente .select, permitindo que qualquer componente de uma textura seja recuperado, incluindo o retorno de padrões \[ para \_ \] componentes ausentes.

Para formatos com componentes float32, se o valor que está sendo buscado for normalizado, desnormalizado, +-0 ou +-INF, ele será retornado ao sombreador inalterado. NaN é retornado como NaN, mas a representação exata de bit do NaN pode ser alterada. Para TextureCubes, alguma síntese do 4º texel ausente deve ocorrer em cantos, portanto, a noção de retorno de bits inalterados para o texel sintetizado não se aplica e desnorms podem ser liberados.

Use esta instrução para estender o intervalo de deslocamento **de gather4** para ser maior e programável. O sufixo "po" no nome significa "deslocamento programável".

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

 

 





