---
title: sample (sm4 - asm)
description: Exemplos de dados do Elemento/textura especificados usando o endereço especificado e o modo de filtragem identificado pelo exemplo especificado. | sample (sm4 - asm)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b6fabb75c819bb2a95fcf500799fd1e8153d6dabfe66d33ba04c518c949fa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671876"
---
# <a name="sample-sm4---asm"></a>sample (sm4 - asm)

Exemplos de dados do Elemento/textura especificados usando o endereço especificado e o modo de filtragem identificado pelo exemplo especificado.



| sample \[ \_ aoffimmi(u,v,w) \] dest \[ .mask \] , srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler |
|--------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[em \] O endereço do resultado da operação.<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] Um conjunto de coordenadas de textura. Para obter mais informações, consulte a **seção Comentários.**<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] Um registro de textura. Para obter mais informações, consulte a **seção Comentários.**<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] Um registro de exemplo. Para obter mais informações, consulte a **seção Comentários.**<br/>           |



 

## <a name="remarks"></a>Comentários

Os dados de origem podem vir de qualquer Tipo de Recurso, diferente de Buffers.

*srcAddress fornece* o conjunto de coordenadas de textura necessárias para executar a amostra, como valores de ponto flutuante que fazem referência ao espaço normalizado na textura. Os modos de empacotamento de endereço (wrap/mirror/fix/border etc.) são aplicados para coordenadas de textura fora do intervalo de 0...1, retirados do estado de amostra (s) e aplicados depois que qualquer deslocamento de endereço é aplicado às coordenadas de \[ \] \# textura.

*srcResource é* um registro de textura (t \# ). Isso é simplesmente um espaço reservado para uma textura, incluindo o tipo de dados de retorno do recurso que está sendo amostrado. Todas essas informações são declaradas no preâmbulo sombreador. O recurso real a ser amostrado é vinculado ao Sombreador externamente no slot \# (para t \# ).

*srcSampler* é um (s) registro (s) de amostra. Isso é simplesmente um espaço reservado para uma coleção de controles de filtragem, como pontos versus lineares, mipmapping e controles de quebra de endereço.

O conjunto de informações necessário para o hardware executar a amostragem é dividido em duas partes ortogonais. Primeiro, o registro de textura fornece informações de tipo de dados de origem, incluindo, por exemplo, informações sobre se a textura contém dados SRGB. Ele também faz referência à memória real que está sendo amostrada. Em segundo lugar, o registro de amostra define o modo de filtragem a ser aplicado.

### <a name="array-resources"></a>Recursos de matriz

Para Matrizes Texture1D, o *componente srcAddress* g (POS-swizzle) seleciona de qual Fatia de Matriz buscar. Isso sempre é tratado como um valor float dimensionado, em vez do espaço normalizado para coordenadas de textura padrão, e um intervalo arredondado para o mais próximo é aplicado ao valor, seguido por um fixador ao intervalo BufferArray disponível.

Para Matrizes Texture2D, o componente *srcAddress* b (POS-swizzle) seleciona de qual Fatia de Matriz buscar, caso contrário, usando a mesma semântica descrita para Matrizes Texture1D .

### <a name="address-offset"></a>Deslocamento de endereço

O sufixo \[ \_ opcional aoffimmi(u,v,w) (deslocamento de endereço por inteiro imediato) indica que as coordenadas de textura para a amostra devem ser deslocadas por um conjunto de valores constantes de inteiro de espaço \] de espaço imediatamente fornecidos. Os valores literais são um conjunto de números de complemento de 4 bits 2, com intervalo de \[ inteiros -8,7 \] . Esse modificador é definido para todos os Recursos, incluindo matrizes Texture1D/2D e Texture3D, mas é indefinido para TextureCube.

O hardware pode aproveitar o conhecimento imediato de que uma travessia sobre algumas áreas de dados sobre um local comum está sendo executada por um conjunto de instruções de exemplo. Isso pode ser transmitido usando \_ aoffimmi(u,v,w).

Os deslocamentos são adicionados às coordenadas de textura, no espaço texel, em relação a cada miplevel que está sendo acessado. Portanto, embora as coordenadas de textura sejam fornecidas como valores float normalizados, o deslocamento aplica um deslocamento inteiro de espaço de texel.

Deslocamentos de endereço não são aplicados ao longo do eixo de matriz de Matrizes Texture1D/2D.

\_Os componentes aoffimmi v,w são ignorados para Texture1Ds.

\_O componente aoffimmi w é ignorado para Texture2Ds.

Os modos de empacotamento de endereço (wrap/mirror/fix/border etc.) do estado de amostra (s ) são aplicados depois que qualquer deslocamento de endereço é aplicado às \# coordenadas de textura.

### <a name="return-type-control"></a>Controle de tipo de retorno

O formato de dados retornado pelo exemplo para o registro de destino é determinado pelo formato de recurso (FORMATO DXGI ) vinculado ao parâmetro \_ \* *srcResource* (t \# ). Por exemplo, se o t especificado tiver sido vinculado a um recurso com o formato \# DXGI \_ FORMAT A8B8G8R8 UNORM SRGB, a operação de amostragem converterá os texels de amostra de \_ \_ gama \_ 2.0 para 1,0, aplicará a filtragem e o resultado será gravado no registro de destino como valores de ponto flutuante no intervalo \[ 0,1 \] .

Os valores retornados são quatro vetores (com padrões específicos ao formato para componentes não presentes no formato). O swizzle em *srcResource* determina como fazer swizzle do resultado de quatro componentes que volta da amostra/filtro de textura, após o qual .mask em *dest* determina quais componentes no *dest* são atualizados.

Quando  o exemplo lê um valor float de 32 bits em um registro de 32 bits, com amostragem de ponto (sem filtragem), ele pode ou não liberar valores desnormais, mas, caso contrário, os números não são modificados. Se a incerteza com valores desnormais de amostragem de ponto for um problema para um aplicativo, use a instrução [ld,](ld--sm4---asm-.md) que garante que os valores float de 32 bits sejam lidos sem modificações.

### <a name="lod-calculation"></a>Cálculo de LOD

Para obter detalhes sobre como os derivados são calculados no processo de determinar LOD para filtragem, consulte [ \_ rtx](deriv-rtx--sm4---asm-.md) derivar [e \_ derivar rty](deriv-rty--sm4---asm-.md). A **instrução** de exemplo calcula implicitamente derivados nas coordenadas de textura usando a mesma definição que as **instruções de** sombreador derivadas usam. Isso não se aplica às [instruções \_ de exemplo l](sample-l--sm4---asm-.md) ou d [ \_ de](sample-d--sm4---asm-.md) exemplo. Para essas instruções, LOD ou derivados são fornecidos diretamente pelo aplicativo.

Para  a instrução de exemplo, as implementações podem optar por compartilhar o mesmo cálculo lod entre todos os 4 pixels em um carimbo 2x2 (mas nenhuma área maior) ou executar cálculos LOD por pixel.

### <a name="miscellaneous-details"></a>Detalhes diversos

Para Buffer & Texture1D, os componentes .gba *do srcAddress* (POS-swizzle) são ignorados. Para matrizes Texture1D, *os componentes .ba srcAddress* (POS-swizzle) são ignorados. Para Texture2Ds, *o componente srcAddress* .a (POS-swizzle) é ignorado.

Buscar de um slot de entrada que não tem nada vinculado a ele retorna 0 para todos os componentes.

### <a name="restrictions"></a>Restrições

-   *srcResource* deve ser um registro \# t. *srcResource não* pode ser um ConstantBuffer, que não pode ser vinculado a \# registros t.
-   *srcSampler* deve ser um registro \# s.
-   O *endereçamento relativo em srcResource* *ou srcSampler* não é permitido.
-   *srcAddress* deve ser um temp (r \# /x \# ), constantBuffer (cb ), input (v ) register ou \# immediate \# value(s).
-   *dest* deve ser um registro temporário (r \# /x \# ) ou de saída (o \* \# ).
-   \_Aoffimmi(u,v,w) não é permitida para TextureCubes.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





