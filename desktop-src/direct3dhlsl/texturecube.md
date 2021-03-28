---
title: Objeto TextureCube
description: Tipo de TextureCube (como ele existe no modelo de sombreador 4) mais variáveis de recurso. Esse objeto de textura dá suporte a esses métodos, além dos métodos no sombreador modelo 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- Objeto TextureCube HLSL
- Objeto TextureCube HLSL, descrito
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104091865"
---
# <a name="texturecube-object"></a>Objeto TextureCube

Tipo de **TextureCube** ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso. Esse objeto de textura dá suporte a esses métodos, além dos métodos no sombreador modelo 4.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **TextureCube** tem esses métodos.



| Método                                                      | Descrição                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gather**](texturecube-gather.md)                         | Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                                                |
| [**GatherAlpha**](texturecube-gatheralpha.md)               | Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                        |
| [**GatherBlue**](texturecube-gatherblue.md)                 | Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                         |
| [**GatherCmp**](texturecube-gathercmp.md)                   | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.<br/>                      |
| [**GatherCmpAlpha**](texturecube-gathercmpalpha.md)         | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação.<br/> |
| [**GatherCmpBlue**](texturecube-gathercmpblue.md)           | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.<br/>  |
| [**GatherCmpGreen**](texturecube-gathercmpgreen.md)         | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação.<br/> |
| [**GatherCmpRed**](texturecube-gathercmpred.md)             | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.<br/>   |
| [**GatherGreen**](texturecube-gathergreen.md)               | Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                        |
| [**GatherRed**](texturecube-gatherred.md)                   | Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.<br/>                                          |
| [**Nova**](texturecube-sample.md)                         | Amostra uma textura.<br/>                                                                                                                                  |
| [**SampleBias**](texturecube-samplebias.md)                 | Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.<br/>                                                                               |
| [**SampleCmp**](texturecube-samplecmp.md)                   | Amostra uma textura, usando um valor de comparação para rejeitar amostras.<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecube-samplecmplevelzero.md) | Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.<br/>                                                                |
| [**SampleGrad**](texturecube-samplegrad.md)                 | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.<br/>                                                          |
| [**SampleLevel**](texturecube-samplelevel.md)               | Amostra uma textura no nível de mipmap especificado.<br/>                                                                                                    |



 

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

 

 





