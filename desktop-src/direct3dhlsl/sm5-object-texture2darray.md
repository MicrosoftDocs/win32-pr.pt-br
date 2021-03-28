---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- Texture2DArray HLSL
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104968262"
---
# <a name="texture2darray"></a>Texture2DArray

Tipo de Texture2DArray ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso. Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.



| Método                                                                      | Descrição                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gather**](texture2darray-gather.md)                                      | Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                                                |
| [**GatherRed**](texture2darray-gatherred.md)                                | Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                          |
| [**GatherGreen**](texture2darray-gathergreen.md)                            | Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                        |
| [**GatherBlue**](texture2darray-gatherblue.md)                              | Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                         |
| [**GatherAlpha**](texture2darray-gatheralpha.md)                            | Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                        |
| [**GatherCmp**](texture2darray-gathercmp.md)                                | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.                      |
| [**GatherCmpRed**](texture2darray-gathercmpred.md)                          | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.   |
| [**GatherCmpGreen**](texture2darray-gathercmpgreen.md)                      | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação. |
| [**GatherCmpBlue**](texture2darray-gathercmpblue.md)                        | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.  |
| [**GatherCmpAlpha**](texture2darray-gathercmpalpha.md)                      | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação. |
| [**GetDimensions**](sm5-object-texture2darray-getdimensions.md)             | Obtém as dimensões do recurso.                                                                                                                       |
| [**Carregamento**](texture2darray-load.md)                                          | Lê dados de textura.                                                                                                                                 |
| [**seqüencia. Operador\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) | Obtém uma variável de recurso somente leitura.                                                                                                                 |
| [**Operador\[\]**](sm5-object-texture2darray-operatorindex.md)              | Obtém uma variável de recurso somente leitura.                                                                                                                 |
| [**Nova**](texture2darray-sample.md)                                      | Amostra uma textura.                                                                                                                                  |
| [**SampleBias**](texture2darray-samplebias.md)                              | Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.                                                                               |
| [**SampleCmp**](texture2darray-samplecmp.md)                                | Amostra uma textura, usando um valor de comparação para rejeitar amostras.                                                                                      |
| [**SampleCmpLevelZero**](texture2darray-samplecmplevelzero.md)              | Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.                                                                |
| [**SampleGrad**](texture2darray-samplegrad.md)                              | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.                                                          |
| [**SampleLevel**](texture2darray-samplelevel.md)                            | Amostra uma textura no nível de mipmap especificado.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




