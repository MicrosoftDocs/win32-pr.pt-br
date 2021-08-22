---
title: ld2dms (sm4.1 – asm)
description: Lê exemplos individuais de texturas de várias amostras bidimensionais.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17d00b3d6cdc3640f0b8d5266bd6dc8fd6dafefaf10cf47b500011cfe952d4ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043784"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (sm4.1 – asm)

Lê exemplos individuais de texturas de várias amostras bidimensionais.



| ld2dms \[ \_ aoffimmi(u,v) \] dest \[ .mask \] , srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] , sampleIndex (operand escalar) |
|------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[em \] O endereço do resultado da operação. <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] As coordenadas de textura necessárias para executar o exemplo.<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em Um registro de textura (t ) que deve ter sido declarado identificando de \] qual textura ou buffer \# buscar<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[em \] Idendifififies the samples to read from *srcResource*.<br/>                                                       |



 

## <a name="remarks"></a>Comentários

Essa instrução é uma alternativa simplificada à [instrução de](sample--sm4---asm-.md) exemplo. Ele busca dados da Textura especificada sem nenhuma filtragem (por exemplo, amostragem de ponto) usando o inteiro *srcAddress* e *sampleIndex fornecidos.*

*srcAddress* fornece o conjunto de coordenadas de textura necessárias para executar a amostra na forma de inteiros sem sinal. Se *srcAddress* estiver fora do intervalo \[ 0...( \# texels na dimensão -1) , ld2dms sempre retorna 0 em todos os componentes presentes no formato do recurso e padrões \] (0,0,0,1.0f/0x00000001) para componentes ausentes. 

*sampleIndex* não precisa ser um literal. A contagem de vários exemplos não precisa ser especificada no recurso de textura e funciona com exibições de profundidade ou estêncil.

Um aplicativo que deseja um controle mais flexível sobre o  comportamento de endereço fora do intervalo deve usar a instrução de exemplo em vez disso, pois ele aborda o comportamento de wrap/mirror/fix/border definido como estado de amostra.

*srcAddress.b* (pós-swizzle) é ignorado para Texture2Ds. Se o valor estiver fora do intervalo de índices de matriz disponíveis \[ 0...( array size-1) , em seguida, ld2dms sempre retorna 0 em todos os componentes presentes no formato do recurso e padrões \] (0,0,0,1.0f/0x00000001) para componentes ausentes. 

Para matrizes Texture2D, *srcAddress.b* (pós-swizzle) fornece o índice da matriz. Por outro lado, ele tem o mesmo comportamento que Texture2D.

*srcAddress.a* (pós-swizzle) é sempre ignorado. O compilador HLSL nunca vai fazer nada lá.

*srcResource é* um registro de textura (t ) que deve ter sido declarado \# (22.3.11), identificando de qual Textura buscar.

Buscar de t que \# não tem nada vinculado a ele retorna 0 para todos os componentes.

### <a name="address-offset"></a>Deslocamento de endereço

O sufixo \[ \_ opcional aoffimmi(u,v,w) (deslocamento de endereço por inteiro imediato) indica que as coordenadas de textura para \] os **ld2dms** devem ser deslocadas por um conjunto de valores constantes de inteiros de espaço de texel imediato fornecidos. Os valores literais são um conjunto de números de complemento de 4 bits 2, com intervalo de \[ inteiros -8,7 \] .

Os deslocamentos são adicionados às coordenadas de textura, no espaço texel.

Deslocamentos de endereço não são aplicados ao longo do eixo de matriz de Matrizes Texture1D/2D.

Os *\_ componentes aoffimmi v,w* são ignorados para Texture1Ds.

O *\_ componente aoffimmi w* é ignorado para Texture2Ds.

Como as coordenadas de textura para **ld2dms** são inteiros sem sinal, se o deslocamento faz com que o endereço vá abaixo de zero, ele será vinculado a um endereço grande e resultará em um acesso fora dos limites, que, como **ld,** retorna 0 em todos os componentes presentes no formato do recurso e os padrões (0,0,0,1,0f/0x00000001) para componentes ausentes.

### <a name="sample-number"></a>Número de exemplo

**ld2dms** está disponível para uso em qualquer recurso. **ld2dms** opera de forma idêntica a **ld,** exceto em recursos de multsample 2D, usando o operando *sampleIndex* adicional (baseado em 0) para identificar qual amostra ler do recurso.

O resultado da especificação de *um sampleIndex* que excede o número de amostras no recurso é indefinido, mas não pode retornar dados fora do espaço de endereço do contexto do dispositivo.

### <a name="return-type-control"></a>Controle de tipo de retorno

O formato de dados retornado **por ld2dms** para o registro de destino é determinado da mesma maneira que descrito para a instrução **de** exemplo. Ele se baseia no formato vinculado ao parâmetro *srcResource* (t \# ).

Assim como na **instrução** de exemplo, os valores retornados para **ld2dms** são quatro vetores com padrões específicos de formato para componentes que não estão presentes no formato. O swizzle em *srcResource* determina como fazer swizzle do resultado de quatro componentes que volta da carga de textura, após o qual .mask no *dest* determina quais componentes no *dest* são atualizados.

Quando um valor float de 32 bits é lido por **ld2dms** em um registro de 32 bits, os bits são intocados; ou seja, os valores denormais permanecem desnormais. Isso é diferente da **instrução de** exemplo.

### <a name="miscellaneous-details"></a>Detalhes diversos

Como não há nenhuma filtragem associada a essa instrução, conceitos como desvio de LOD não se aplicam. Portanto, não há nenhum *parâmetro de amostra. \#*

### <a name="restrictions"></a>Restrições

-   *srcResource* deve ser um t register e não \# um TextureCube, Texture1D ou Texture1DArray. *srcResource não* pode ser um ConstantBuffer, que não pode ser vinculado a \# registros t.
-   O *endereçamento relativo em srcResource* não é permitido.
-   *srcAddress* e *sampleIndex* devem ser um registro temp (r \# /x \# ), constante (cb \# ) ou entrada \# (v).
-   *dest* deve ser um registro temporário (r \# /x \# ) ou de saída (o \* \# ).

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

 

 





