---
title: gather4_po (SM5-ASM)
description: Uma variante de gather4, mas em vez de dar suporte a um deslocamento imediato \-8.. 7 \, o deslocamento é fornecido como um parâmetro para a instrução e também tem um intervalo maior de \-32.. 31 \.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967119"
---
# <a name="gather4_po-sm5---asm"></a>gather4 \_ po (SM5-ASM)

Uma variante de [gather4](gather4--sm5---asm-.md), mas em vez de dar suporte a um deslocamento imediato \[ -8.. 7 \] , o deslocamento é fornecido como um parâmetro para a instrução e também tem um intervalo maior de \[ -32.. 31 \] .



| gather4 \_ po dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcOffset \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . selecionar \_ componente\] |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço do resultado da operação.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] um conjunto de coordenadas de textura.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>         | \[no \] deslocamento.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] um registro de textura.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] um registro de amostra.<br/>                         |



 

## <a name="remarks"></a>Comentários

Os dois primeiros componentes do parâmetro de deslocamento de quatro vetores fornecem deslocamentos de inteiro de 32 bits. Os outros componentes desse parâmetro são ignorados.

Os 6 bits menos significativos de cada valor de deslocamento são respeitados como um valor assinado, produzindo \[ -32.. 31 \] Range.

Essa instrução só funciona com texturas 2D, ao contrário de **gather4**, que também funciona com TextureCubes.

Os únicos modos honrados na amostra são os modos de endereçamento. Somente o MIP mais detalhado no modo de exibição de recursos é usado.

Se o endereço cair em um Texel Center, isso não significa que o outro texels pode ser zerado.

O parâmetro *srcSampler* inclui o \[ componente. Select \_ \] , permitindo que qualquer componente individual de uma textura seja recuperado, incluindo o retorno de padrões para componentes ausentes.

Para formatos com componentes float32, se o valor que está sendo obtido for normalizado, desnormalizado, +-0 ou +-INF, ele será retornado ao sombreador inalterado. NaN é retornado como NaN, mas a representação de bit exata do NaN pode ser alterada. Para TextureCubes, alguma síntese do 4º Texel ausente deve ocorrer nos cantos, portanto, a noção de retornar bits inalterado para o Texel sintetizado não se aplica, e as desnormas podem ser liberadas.

Use esta instrução para estender o intervalo de deslocamento de **gather4** para ser maior e programável. O sufixo "po" no nome significa "deslocamento programável".

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

 

 





