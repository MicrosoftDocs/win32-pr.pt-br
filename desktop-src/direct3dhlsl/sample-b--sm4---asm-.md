---
title: sample_b (sm4-ASM)
description: Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo. | sample_b (sm4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172811"
---
# <a name="sample_b-sm4---asm"></a>exemplo \_ b (sm4-ASM)

Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo.



| exemplo \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler e srcLODBias. Select \_ componente |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço do resultado da operação.<br/>                                                              |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] um conjunto de coordenadas de textura. Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] um registro de textura. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] um registro de amostra. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                 |
| <span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*<br/>     | \[em \] consulte a seção **comentários** para obter informações sobre esse parâmetro.<br/>                                        |



 

## <a name="remarks"></a>Comentários

Os dados de origem podem vir de qualquer tipo de recurso, além de buffers. Uma diferença adicional é aplicada ao nível de detalhes calculados como parte da execução da instrução.

Essa instrução se comporta como a instrução de [exemplo](sample--sm4---asm-.md) com a adição de aplicar o valor *srcLODBias* especificado ao nível de valor de detalhe calculado como parte da execução de instrução antes de selecionar o (s) mapa (es) MIP. O valor de *srcLODBias* é adicionado ao LOD computado por pixel, juntamente com o valor de MipLODBias de amostra, antes do fixe para MinLOD e MaxLOD.

### <a name="restrictions"></a>Restrições

-   o **exemplo \_ b** herda as mesmas restrições que a instrução de [exemplo](sample--sm4---asm-.md) , além de restrições adicionais para seu parâmetro adicional.
-   O intervalo de *srcLODBias* é (-16.0 f a 15.99 f); os valores fora desse intervalo produzirão resultados indefinidos.
-   *srcLODBias* deve usar um seletor de componente único se não for um escalar imediato.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





