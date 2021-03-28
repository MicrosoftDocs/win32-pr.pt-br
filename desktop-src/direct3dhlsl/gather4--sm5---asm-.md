---
title: gather4 (SM5-ASM)
description: Coleta os quatro texels que seriam usados em uma operação de filtragem de bi-linear e os empacota em um único registro. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172694"
---
# <a name="gather4-sm5---asm"></a>gather4 (SM5-ASM)

Coleta os quatro texels que seriam usados em uma operação de filtragem de bi-linear e os empacota em um único registro. Essa instrução só funciona com texturas 2D ou CubeMap, incluindo matrizes. Somente os modos de endereçamento da amostra são usados e o nível superior de qualquer pirâmide MIP é usado.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . selecionar \_ componente\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço dos resultados da operação.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] um conjunto de coordenadas de textura.<br/>                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] um registro de textura.<br/>                          |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] um registro de amostra.<br/>                          |



 

## <a name="remarks"></a>Comentários

Essa instrução se comporta como a instrução de [**exemplo**](sample--sm4---asm-.md) , mas uma amostra filtrada não é gerada. Os quatro exemplos que contribuiria para a filtragem são colocados em xyzw no sentido anti-horário do contador, começando com a amostra para a parte inferior esquerda do local consultado. Isso é o mesmo que a amostragem de ponto com deltas de coordenadas de textura (u, v) nos seguintes locais: (-, +), (+, +), (+,-), (-,-), em que a magnitude dos deltas sempre é meio Texel.

Para texturas CubeMap, quando uma superfície de bi linear abrange uma borda, texels da face vizinha é usado. Os cantos usam as mesmas regras que a instrução de [**exemplo**](sample--sm4---asm-.md) ; ou seja, o canto desconhecido é considerado a média dos três cantos da face do ping.

Há restrições de formato de textura que se aplicam a **gather4** que são expressas na lista de formatos.

O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino.

O componente. Select \_ em *srcSampler* escolhe qual componente da textura de origem (r/g/b/a) para ler 4 texels.

Para formatos com componentes float32, se o valor que está sendo obtido for normalizado, desnormalizado, +-0 ou +-INF, ele será retornado ao sombreador inalterado. NaN é retornado como NaN, mas a representação de bit exata do NaN pode ser alterada. Para TextureCubes, alguma síntese do 4º Texel ausente deve ocorrer nos cantos, portanto, retornar bits inalterados para o Texel sintetizado não se aplica, e as alterações podem ser liberadas.

Para implementações de hardware, otimizações na filtragem biline tradicional que detectam exemplos diretamente em texels e ignoram a leitura de texels que teriam peso 0 não podem ser aproveitadas com essa instrução. *gather4* sempre retorna todos os texels solicitados.

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

 

 





