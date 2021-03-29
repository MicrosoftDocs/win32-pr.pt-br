---
title: gather4 (SM 4.1-ASM)
description: Coleta os quatro texels que seriam usados em uma operação de filtragem de bi-linear e os empacota em um único registro. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968402"
---
# <a name="gather4-sm41---asm"></a>gather4 (SM 4.1-ASM)

Coleta os quatro texels que seriam usados em uma operação de filtragem de bi-linear e os empacota em um único registro.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] srcSampler. r |
|--------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço do resultado da operação.<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] contém as coordenadas de textura. <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] um registro de recurso. <br/> O swizzle permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no *dest*. <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] um registro de amostra.<br/> Esse parâmetro deve ter um swizzle. r (vermelho), que indica que o valor do canal R é copiado para *dest*. <br/> |



 

## <a name="remarks"></a>Comentários

Esta operação só funciona com texturas 2D ou CubeMap de canal único. Para texturas 2D, somente os modos de endereçamento da amostra são usados e o nível superior de qualquer pirâmide MIP é usado.

Essa instrução se comporta como a instrução de [exemplo](sample--sm4---asm-.md) , mas uma amostra filtrada não é gerada. Os quatro exemplos que contribuiria para a filtragem são colocados em xyzw no sentido anti-horário do contador, começando com a amostra para a parte inferior esquerda do local consultado. Isso é o mesmo que a amostragem de ponto com deltas de coordenadas de textura (u, v) nos seguintes locais: (-, +), (+, +), (+,-), (-,-), em que a magnitude dos deltas sempre é meio Texel.

Para texturas CubeMap quando um espaço de bi linear abrange um texels de borda da face vizinha, é usado. Os cantos usam as mesmas regras que a instrução de **exemplo** ; Esse é o canto desconhecido, que é considerado a média dos três cantos da face de ping.

As restrições de formato de textura que se aplicam às instruções de **exemplo** também se aplicam à instrução **gather4** .

Para implementações de hardware, otimizações na filtragem biline tradicional que detectam exemplos diretamente em texels e ignoram a leitura de texels que teriam peso 0 não podem ser aproveitadas com **gather4**. **gather4** sempre retorna todos os texels solicitados.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





