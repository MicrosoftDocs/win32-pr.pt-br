---
title: ld2dms (SM 4.1-ASM)
description: Lê exemplos individuais fora de texturas com várias amostras bidimensionais.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084267"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (SM 4.1-ASM)

Lê exemplos individuais fora de texturas com várias amostras bidimensionais.



| ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , sampleIndex (operando escalar) |
|------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço do resultado da operação. <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[nas \] coordenadas de textura necessárias para executar o exemplo.<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] um registro de textura (t \# ) que deve ter sido declarado identificando a textura ou o buffer a ser obtido<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[em \] Idendifies, os exemplos a serem lidos em *srcResource*.<br/>                                                       |



 

## <a name="remarks"></a>Comentários

Essa instrução é uma alternativa simplificada para a instrução de [exemplo](sample--sm4---asm-.md) . Ele busca dados da textura especificada sem nenhuma filtragem (por exemplo, amostragem de ponto) usando o inteiro fornecido *srcAddress* e *sampleIndex*.

o *srcAddress* fornece o conjunto de coordenadas de textura necessárias para executar o exemplo na forma de inteiros sem sinal. Se *srcAddress* estiver fora do intervalo \[ 0... ( \# texels na dimensão-1) \] , **ld2dms** sempre retorna 0 em todos os componentes presentes no formato do recurso, e os padrões (0, 0, 0, 1,0 f/0x00000001) para componentes ausentes.

*sampleIndex* não precisa ser um literal. A contagem de várias amostras não precisa ser especificada no recurso de textura e funciona com exibições de profundidade ou de estêncil.

Um aplicativo que deseja ter um controle mais flexível sobre o comportamento de endereço fora do intervalo deve usar a instrução de **exemplo** , pois ele honra o comportamento de encapsulamento/espelho/fixe/Border definido como um estado de amostra.

*srcAddress. b* (post-swizzle) é ignorado para Texture2Ds. Se o valor estiver fora do intervalo de índices de matriz disponíveis \[ 0... ( tamanho da matriz-1) \] , em seguida, **ld2dms** sempre retorna 0 em todos os componentes presentes no formato do recurso, e os padrões (0, 0, 0, 1,0 f/0x00000001) para componentes ausentes.

Para matrizes Texture2D, *srcAddress. b* (post-swizzle) fornece o índice de matriz. Oherwise ele tem o mesmo comportamento que Texture2D.

*srcAddress. a* (post-swizzle) é sempre ignorada. O compilador HLSL nunca produzirá nada lá.

*srcResource* é um registro de textura (t \# ) que deve ter sido declarado (22.3.11), identificando a qual textura buscar.

A busca de t \# que não tem nada associado retorna 0 para todos os componentes.

### <a name="address-offset"></a>Deslocamento de endereço

O \[ \_ sufixo opcional aoffimmi (u, v, w) \] (deslocamento de endereço por inteiro imediato) indica que as coordenadas de textura para o **ld2dms** devem ser deslocadas por um conjunto de valores de constante de inteiro de espaço de Texel imediato fornecido. Os valores literais são um conjunto de números de complemento de 4 bits 2, com intervalo de números inteiros \[ -8, 7 \] .

Os deslocamentos são adicionados às coordenadas de textura, no espaço Texel.

Deslocamentos de endereço não são aplicados ao longo do eixo de matriz de matrizes Texture1D/2D.

Os componentes *\_ aoffimmi v, w* são ignorados para Texture1Ds.

O componente *\_ aoffimmi w* é ignorado para Texture2Ds.

Como as coordenadas de textura para **ld2dms** são inteiros não assinados, se o deslocamento fizer com que o endereço fique abaixo de zero, ele será encapsulado em um endereço grande e resultará em um acesso fora dos limites, que como **LD** retorna 0 em todos os componentes presentes no formato do recurso e os padrões (0, 0, 0, 1,0 f/0x00000001) para componentes ausentes.

### <a name="sample-number"></a>Número de exemplo

**ld2dms** está disponível para uso em qualquer recurso. o **ld2dms** Opera de forma idêntica a **LD** , exceto em recursos de multsample 2D, usando o operando de *sampleIndex* adicional (baseado em 0) para identificar qual exemplo ler do recurso.

O resultado da especificação de um *sampleIndex* que exceda o número de amostras no recurso é indefinido, mas não pode retornar dados fora do espaço de endereço do contexto do dispositivo.

### <a name="return-type-control"></a>Controle de tipo de retorno

O formato de dados retornado por **ld2dms** para o registro de destino é determinado da mesma maneira que descrito para a instrução de **exemplo** . Ele se baseia no formato associado ao parâmetro *srcResource* (t \# ).

Assim como acontece com a instrução de **exemplo** , os valores retornados para **ld2dms** são 4 vetores com padrões específicos de formato para componentes que não estão presentes no formato. O swizzle em *srcResource* determina como swizzle o resultado de 4 componentes de volta da carga de textura, após o qual. Mask no *dest* determina quais componentes no *dest* são atualizados.

Quando um valor float de 32 bits é lido por **ld2dms** em um registro de 32 bits, os bits são intocados; ou seja, os valores desnormals permanecem desnormalizados. Isso é diferente da instrução de **exemplo** .

### <a name="miscellaneous-details"></a>Detalhes diversos

Como não há nenhuma filtragem associada a essa instrução, conceitos como LOD Bias não se aplicam. Portanto, não há nenhum parâmetro de *s \# de amostra* .

### <a name="restrictions"></a>Restrições

-   *srcResource* deve ser um \# registro t e não um TextureCube, Texture1D ou Texture1DArray. *srcResource* não pode ser um ConstantBuffer, que não pode ser associado a \# registros t.
-   O endereçamento relativo em *srcResource* não é permitido.
-   *srcAddress* e *sampleIndex* devem ser um registro temporário (r \# /x \# ), uma constante (CB \# ) ou de entrada (v \# ).
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
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





