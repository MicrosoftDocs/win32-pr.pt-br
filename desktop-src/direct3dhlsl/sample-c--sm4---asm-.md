---
title: sample_c (sm4-ASM)
description: Executa um filtro de comparação.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988569"
---
# <a name="sample_c-sm4---asm"></a>exemplo \_ c (sm4-ASM)

Executa um filtro de comparação.



| exemplo \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource. r,//deve ser. r swizzle srcSampler, srcReferenceValue//componente único selecionado |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                                       | Descrição                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[no \] endereço dos resultados da operação.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[em \] um conjunto de coordenadas de textura. Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[em \] um registro de textura. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[em \] um registro de amostra. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[em \] um registro com um único componente selecionado, que é usado na comparação.<br/>                            |



 

## <a name="remarks"></a>Comentários

A principal finalidade dessa instrução é fornecer um bloco de construção para a filtragem de profundidade Percentage-Closer. O "c" no **exemplo \_ c** significa comparação.

Os operandos para a **amostra \_ c** são idênticos à instrução de [exemplo](sample--sm4---asm-.md) , exceto pelo fato de que há um operando de origem float32 adicional, *srcReferenceValue*, que deve ser um registro com um único componente selecionado ou um literal escalar.

O parâmetro *srcResource* deve ter um swizzle. r (vermelho). o **exemplo \_ c** funciona exclusivamente no componente vermelho e retorna um único valor. O. r swizzle em *srcResource* indica que o resultado escalar é replicado para todos os componentes.

Quando um buffer de profundidade é definido como uma textura de entrada, o valor de profundidade aparece no componente vermelho.

Se essa instrução for usada com um recurso que não seja um Texture1D/2D/2DArray/Cube/CubeArray, ele produzirá resultados indefinidos.

Quando essa instrução é executada, o hardware de amostragem usa o ComparisonFunction da amostra atual para comparar *srcReferenceValue* com o valor do componente vermelho para o recurso de origem em cada filtro "toque" (Texel) que o filtro de textura configurado atualmente abrange, com base nas coordenadas fornecidas em *srcAddress*.

A comparação ocorre depois que *srcReferenceValue* tem sido quantificado para a precisão do formato de textura, exatamente da mesma forma que z é quantificado para profundidade de buffer de intensidade antes da comparação de profundidade no teste de visibilidade da fusão de saída. Isso inclui um fixe para o intervalo de formato (por exemplo, \[ 0.. 1 \] para um formato UNORM).

O componente vermelho do Texel de origem é comparado com o *srcReferenceValue* quantificado. Para texels que estão fora do recurso, o valor do componente vermelho é determinado pela aplicação dos modos de endereço (e de BorderColor, se estiver no modo de borda) do amostra. A comparação honra todas as regras de comparação de ponto flutuante D3D11, no caso de o formato de textura ser ponto flutuante.

Cada comparação que passa retorna 1,0 f como o valor do componente vermelho para o Texel e cada comparação que falha retorna 0,0 f como o valor vermelho para a textura. Em seguida, a filtragem ocorre exatamente conforme especificado pelos Estados de amostra, operando apenas no componente vermelho e retornando um único resultado de filtro escalar de volta para o sombreador, replicado para todos os componentes de *dest* mascarados.

O uso da **amostra \_ c** é ortogonal a todos os outros controles de filtragem de uso geral. o **exemplo \_ c** funciona diretamente com os outros modos de filtro de uso geral. o **exemplo \_ c** altera o comportamento dos filtros de uso geral, de modo que os valores que estão sendo filtrados se tornem 1,0 f ou 0,0 f devido aos resultados da comparação.

A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.

Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .

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

 

 





