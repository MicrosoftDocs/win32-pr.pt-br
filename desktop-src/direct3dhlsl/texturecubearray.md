---
title: Objeto TextureCubeArray
description: Tipo de TextureCubeArray (como ele existe no modelo de sombreador 4) mais variáveis de recurso. Esse objeto de textura dá suporte a esses métodos, além dos métodos no sombreador modelo 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- Objeto TextureCubeArray HLSL
- Objeto TextureCubeArray HLSL, descrito
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104989124"
---
# <a name="texturecubearray-object"></a>Objeto TextureCubeArray

Tipo de **TextureCubeArray** ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso. Esse objeto de textura dá suporte a esses métodos, além dos métodos no sombreador modelo 4.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **TextureCubeArray** tem esses métodos.



| Método                                                           | Descrição                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gather**](texturecubearray-gather.md)                         | Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                                                |
| [**GatherAlpha**](texturecubearray-gatheralpha.md)               | Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                        |
| [**GatherBlue**](texturecubearray-gatherblue.md)                 | Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                         |
| [**GatherCmp**](texturecubearray-gathercmp.md)                   | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.<br/>                      |
| [**GatherCmpAlpha**](texturecubearray-gathercmpalpha.md)         | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.<br/> |
| [**GatherCmpBlue**](texturecubearray-gathercmpblue.md)           | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.<br/>  |
| [**GatherCmpGreen**](texturecubearray-gathercmpgreen.md)         | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação.<br/> |
| [**GatherCmpRed**](texturecubearray-gathercmpred.md)             | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.<br/>   |
| [**GatherGreen**](texturecubearray-gathergreen.md)               | Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                        |
| [**GatherRed**](texturecubearray-gatherred.md)                   | Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                          |
| [**Nova**](texturecubearray-sample.md)                         | Amostra uma textura.<br/>                                                                                                                                  |
| [**SampleBias**](texturecubearray-samplebias.md)                 | Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecubearray-samplecmp.md)                   | Amostra uma textura, usando um valor de comparação para rejeitar amostras.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecubearray-samplecmplevelzero.md) | Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.<br/>                                                                |
| [**SampleGrad**](texturecubearray-samplegrad.md)                 | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.<br/>                                                          |
| [**SampleLevel**](texturecubearray-samplelevel.md)               | Amostra uma textura no nível de mipmap especificado.<br/>                                                                                                    |



 

## <a name="remarks"></a>Comentários

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

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

 

 





