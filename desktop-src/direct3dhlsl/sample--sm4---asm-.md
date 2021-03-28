---
title: exemplo (sm4-ASM)
description: Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo. | exemplo (sm4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930433"
---
# <a name="sample-sm4---asm"></a>exemplo (sm4-ASM)

Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo.



| aoffimmi de exemplo \[ \_ (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler |
|--------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço do resultado da operação.<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] um conjunto de coordenadas de textura. Para obter mais informações, consulte a seção **comentários** .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] um registro de textura. Para obter mais informações, consulte a seção **comentários** .<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] um registro de amostra. Para obter mais informações, consulte a seção **comentários** .<br/>           |



 

## <a name="remarks"></a>Comentários

Os dados de origem podem vir de qualquer tipo de recurso, além de buffers.

o *srcAddress* fornece o conjunto de coordenadas de textura necessárias para executar o exemplo, como valores de ponto flutuante referenciando o espaço normalizado na textura. Os modos de disposição de endereço (Wrap/espelho/fixe/Border etc.) são aplicados para coordenadas de textura fora de \[ 0... 1 \] intervalo, extraído dos Estados de amostra \# e aplicados depois que qualquer deslocamento de endereço é aplicado às coordenadas de textura.

*srcResource* é um registro de textura (t \# ). Isso é simplesmente um espaço reservado para uma textura, incluindo o tipo de dados de retorno do recurso que está sendo amostrado. Todas essas informações são declaradas no preâmbulo do sombreador. O recurso real a ser amostrado é associado ao sombreador externamente no slot \# (para t \# ).

*srcSampler* é um ou mais registros de amostra. Trata-se simplesmente de um espaço reservado para uma coleção de controles de filtragem como controles Point vs. linear, mipmapping e address entorno.

O conjunto de informações necessárias para que o hardware execute a amostragem é dividido em duas partes ortogonal. Primeiro, o registro de textura fornece informações de tipo de dados de origem, incluindo, por exemplo, informações sobre se a textura contém dados SRGB. Ele também faz referência à memória real que está sendo amostrada. Em segundo lugar, o registro de amostra define o modo de filtragem a ser aplicado.

### <a name="array-resources"></a>Recursos de matriz

Para matrizes Texture1D, o componente g do *srcAddress* (pos-swizzle) seleciona a fatia da matriz da qual buscar. Isso é sempre tratado como um valor float dimensionado, em vez do espaço normalizado para coordenadas de textura padrão, e um ponto de arredondamento para mais próximo é aplicado ao valor, seguido por um fixe para o intervalo BufferArray disponível.

Para matrizes Texture2D, o componente *srcAddress* b (pos-swizzle) seleciona a fatia da matriz da qual buscar, caso contrário, usando a mesma semântica descrita para matrizes Texture1D.

### <a name="address-offset"></a>Deslocamento de endereço

O \[ \_ sufixo opcional aoffimmi (u, v, w) \] (deslocamento de endereço por inteiro imediato) indica que as coordenadas de textura do exemplo devem ser deslocadas por um conjunto de valores de constante de inteiro de espaço de Texel imediato fornecido. Os valores literais são um conjunto de números de complemento de 4 bits 2, com intervalo de números inteiros \[ -8, 7 \] . Esse modificador é definido para todos os recursos, incluindo matrizes Texture1D/2D e Texture3D, mas não é definido para TextureCube.

O hardware pode aproveitar o conhecimento imediato de que uma passagem em uma superfície de texels sobre um local comum está sendo executada por um conjunto de instruções de exemplo. Isso pode ser transmitido usando \_ aoffimmi (u, v, w).

Os deslocamentos são adicionados às coordenadas de textura, no espaço Texel, em relação a cada MipLevel que está sendo acessado. Portanto, embora as coordenadas de textura sejam fornecidas como valores float normalizados, o deslocamento aplica um deslocamento de inteiro de Texel de espaço.

Deslocamentos de endereço não são aplicados ao longo do eixo de matriz de matrizes Texture1D/2D.

\_os componentes aoffimmi v, w são ignorados para Texture1Ds.

\_o componente aoffimmi w é ignorado para Texture2Ds.

Os modos de quebra de endereço (quebra/espelho/fixe/borda etc.) dos Estados de amostra \# são aplicados depois que qualquer deslocamento de endereço é aplicado às coordenadas de textura.

### <a name="return-type-control"></a>Controle de tipo de retorno

O formato de dados retornado pelo exemplo para o registro de destino é determinado pelo formato de recurso ( \_ formato dxgi \* ) associado ao parâmetro *srcResource* (t \# ). Por exemplo, se o t especificado \# tiver sido associado a um recurso com formato de formato dxgi \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, a operação de amostragem converterá texels de amostra de gama 2,0 para 1,0, aplicará a filtragem e o resultado será gravado no registro de destino como valores de ponto flutuante no intervalo \[ 0.. 1 \] .

Os valores retornados são de 4 vetores (com padrões específicos de formato para componentes que não estão presentes no formato). O swizzle em *srcResource* determina como swizzle o resultado de 4 componentes de volta do exemplo de textura/filtro, após o qual. Mask no *dest* determina quais componentes no *dest* são atualizados.

Quando o **exemplo** lê um valor float de 32 bits em um registro de 32 bits, com amostragem de ponto (sem filtragem), ele pode ou não liberar valores desnormals, mas os números não são modificados. Se a incerteza com valores desnormals de amostragem de ponto for um problema para um aplicativo, use a instrução [LD](ld--sm4---asm-.md) , que garante que os valores float de 32 bits sejam lidos sem modificações.

### <a name="lod-calculation"></a>Cálculo de LOD

Para obter detalhes sobre como os derivativos são calculados no processo de determinação de LOD para filtragem, consulte [derivar \_ RTX](deriv-rtx--sm4---asm-.md) e [derivar \_ rty](deriv-rty--sm4---asm-.md). A instrução de **exemplo** computa implicitamente as derivações nas coordenadas de textura usando a mesma definição que as instruções **derivadas** do sombreador usam. Isso não se aplica às [instruções \_ l](sample-l--sm4---asm-.md) ou [ \_ d](sample-d--sm4---asm-.md) de exemplo. Para essas instruções, LOD ou derivativos são fornecidos diretamente pelo aplicativo.

Para a instrução de **exemplo** , as implementações podem optar por compartilhar o mesmo cálculo de LOD em todos os quatro pixels em um carimbo 2x2 (mas sem área maior) ou executar cálculos de LOD por pixel.

### <a name="miscellaneous-details"></a>Detalhes diversos

Para o buffer & Texture1D, os componentes *srcAddress* . GBA (pos-swizzle) são ignorados. Para matrizes Texture1D, os componentes *srcAddress* . BA (pos-swizzle) são ignorados. Para Texture2Ds, *srcAddress* . a Component (pos-swizzle) é ignorado.

A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.

### <a name="restrictions"></a>Restrições

-   *srcResource* deve ser um \# registro t. *srcResource* não pode ser um ConstantBuffer, que não pode ser associado a \# registros t.
-   *srcSampler* deve ser um registro de s \# .
-   O endereçamento relativo em *srcResource* ou *srcSampler* não é permitido.
-   *srcAddress* deve ser temp (r \# /X \# ), constantBuffer (CB \# ), registro de entrada (v \# ) ou valor (es) imediato (s).
-   *dest* deve ser um registro temporário (r \# /x \# ) ou saída (o \* \# ).
-   \_aoffimmi (u, v, w) não é permitido para TextureCubes.

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

 

 





