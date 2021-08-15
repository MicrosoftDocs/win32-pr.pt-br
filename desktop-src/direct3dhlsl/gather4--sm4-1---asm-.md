---
title: gather4 (sm4.1 – asm)
description: Coleta os quatro texels que seriam usados em uma operação de filtragem bi-linear e os empacota em um único registro. | gather4 (sm4.1 – asm)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb39918bdb421123cb3e2bfe41931740e271f85a27cf36b8994d493656d91c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457576"
---
# <a name="gather4-sm41---asm"></a>gather4 (sm4.1 – asm)

Coleta os quatro texels que seriam usados em uma operação de filtragem bi-linear e os empacota em um único registro.



| gather4 \[ \_ aoffimmi(u,v) \] dest \[ \] .mask, srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] srcSampler.r |
|--------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[em \] O endereço do resultado da operação.<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] Contém as coordenadas de textura. <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] Um registro de recurso. <br/> O swizzle permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados *no dest.* <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] Um registro de exemplo.<br/> Esse parâmetro deve ter um swizzle .r (vermelho), que indica que o valor do canal R é copiado para *dest.* <br/> |



 

## <a name="remarks"></a>Comentários

Essa operação só funciona com texturas de canal único 2D ou CubeMap. Para texturas 2D, somente os modos de endereçamento do amostrador são usados e o nível superior de qualquer pirâmide mip é usado.

Essa instrução se comporta como a [instrução de](sample--sm4---asm-.md) exemplo, mas uma amostra filtrada não é gerada. Os quatro exemplos que contribuem para a filtragem são colocados em xyzw em ordem anti-horário, começando com o exemplo no canto inferior esquerdo do local consultado. Isso é o mesmo que a amostragem de pontos com deltas de coordenadas de textura (u,v) nos seguintes locais: (-,+),(+,+),(+,-),(-,-), em que a magnitude dos deltas sempre é metade de um texel.

Para texturas CubeMap quando um espaço bi linear abrange um edge texels do rosto vizinho são usados. Os cantos usam as mesmas regras que a **instrução de** exemplo; que é o canto sem-proprietário é considerado a média dos três cantos de rosto impinging.

As restrições de formato de textura que se aplicam às **instruções de** exemplo também se aplicam à **instrução gather4.**

Para implementações de hardware, otimizações na filtragem bilinear tradicional que detectam amostras diretamente em texels e ignoram a leitura de texels que teriam peso 0 não podem ser aproveitadas com **gather4**. **gather4** sempre retorna todos os texels solicitados.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





