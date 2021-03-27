---
title: LD (sm4-ASM)
description: Busca dados do buffer ou da textura especificada sem nenhuma filtragem (por exemplo, amostragem de ponto) usando o endereço inteiro fornecido. Os dados de origem podem vir de qualquer tipo de recurso, diferente de TextureCube.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293574"
---
# <a name="ld-sm4---asm"></a>LD (sm4-ASM)

Busca dados do buffer ou da textura especificada sem nenhuma filtragem (por exemplo, amostragem de ponto) usando o endereço inteiro fornecido. Os dados de origem podem vir de qualquer tipo de recurso, diferente de TextureCube.



| LD \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço do resultado da operação.<br/>                                                               |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[nas \] coordenadas de textura necessárias para executar o exemplo.<br/>                                                     |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] um registro de textura (t \# ) que deve ter sido declarado identificando de qual textura ou buffer deve ser obtido.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução é uma alternativa simplificada para a instrução de [exemplo](sample--sm4---asm-.md) . Ao contrário de **Sample**, **LD** também é capaz de buscar dados de buffers. **LD** também pode buscar de recursos de várias amostras (somente no sombreador de pixel).

o *srcAddress* fornece o conjunto de coordenadas de textura necessárias para executar o exemplo na forma de inteiros sem sinal. Se *srcAddress* estiver fora do intervalo \[ 0... ( \# texels na dimensão-1) \] , o comportamento fora dos limites é invocado, em que **LD** retorna 0 em todos os componentes não ausentes do formato do *srcResource* e o padrão para componentes ausentes. Um aplicativo que deseja ter um controle mais flexível sobre o comportamento de endereço fora do intervalo deve usar a instrução de **exemplo** , pois ele honra o comportamento de encapsulamento/espelho/fixe/Border definido como um estado de amostra.

*srcAddress. a* (pos-swizzle) sempre fornece um nível de mipmap inteiro sem sinal. Se o valor estiver fora do intervalo \[ 0... ( num miplevels no Resource-1) \] ), o comportamento fora dos limites é invocado. Se o recurso for um buffer, que não pode ter nenhum mipmaps, então *srcAddress. a* será ignorada

*srcAddress. GB* (pos-swizzle) é ignorado para buffers e texture1D (não matriz). *srcAddress. b* (pos-swizzle) é ignorado para matrizes Texture1D e texture2Ds.

Para matrizes texture1D, *srcAddress. g* (pos-swizzle) fornece o índice de matriz como um inteiro sem sinal. Se o valor estiver fora do intervalo de índices de matriz disponíveis \[ 0... ( tamanho da matriz-1) \] , então o comportamento fora dos limites é invocado.

Para matrizes texture2D, *srcAddress. b* (pos-swizzle) fornece o índice de matriz, caso contrário, com a mesma semântica que para texture1D.

A busca de *t \#* que não tem nada associado retorna 0 para todos os componentes.

### <a name="address-offset"></a>Deslocamento de endereço

O \[ \_ sufixo opcional aoffimmi (u, v, w) \] (deslocamento de endereço por inteiro imediato) indica que as coordenadas de textura para o **LD** devem ser deslocadas por um conjunto de valores de constante de inteiro de espaço de Texel imediato fornecido. Os valores literais são um conjunto de números de complemento de 4 bits 2, com intervalo de números inteiros \[ -8, 7 \] . Esse modificador é definido somente para texture1D/2D/3D, incluindo matrizes, e não para buffers.

Os deslocamentos são adicionados às coordenadas de textura, no espaço Texel, em relação ao MipLevel que está sendo acessado pela **LD**.

Deslocamentos de endereço não são aplicados ao longo do eixo de matriz de matrizes texture1D/2D.

Os componentes *\_ aoffimmi v, w* são ignorados para texture1Ds.

O componente *\_ aoffimmi w* é ignorado para texture2Ds.

Como as coordenadas de textura para **LD** são inteiros não assinados, se o deslocamento fizer com que o endereço fique abaixo de zero, ele será encapsulado em um endereço grande e resultará em um acesso fora dos limites.

### <a name="return-type-control"></a>Controle de tipo de retorno

O formato de dados retornado por **LD** para o registro de destino é determinado da mesma maneira que descrito para a instrução de **exemplo** ; Ele se baseia no formato associado ao parâmetro *srcResource* (*t \#*).

Assim como acontece com a instrução de **exemplo** , os valores retornados para **LD** são 4 vetores com padrões específicos de formato para componentes que não estão presentes no formato. O swizzle em *srcResource* determina como swizzle o resultado de 4 componentes de volta da carga de textura, após o qual. Mask no *dest* determina quais componentes no *dest* são atualizados.

Quando um valor float de 32 bits é lido por *LD* em um registro de 32 bits, os bits são intocados; ou seja, os valores desnormals permanecem desnormalizados. Isso é diferente da instrução de **exemplo** .

### <a name="miscellaneous-details"></a>Detalhes diversos

Como não há nenhuma filtragem associada à instrução **LD** , conceitos como LOD Bias não se aplicam a **LD**. Portanto, não há nenhum parâmetro de *s \#* de amostra.

### <a name="restrictions"></a>Restrições

-   *srcResource* deve ser um \# registro t e não um TextureCube. *srcResource* não pode ser um constantbuffer, que não pode ser associado a \# registros t.
-   O endereçamento relativo em *srcResource* não é permitido.
-   *srcAddress* deve ser um registro temporário (r \# /x \# ), uma constante (CB \# ) ou de entrada (v \# ).
-   *dest* deve ser um registro temporário (r \# /x \# ) ou saída (o \* \# ).

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
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





