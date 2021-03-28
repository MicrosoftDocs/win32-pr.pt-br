---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- Texture2D HLSL
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0c9b73d66f1c5a38b077b241df8e5859b706e2f
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104968266"
---
# <a name="texture2d"></a>Texture2D

Tipo de Texture2D ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso. Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.



| Método                                                                 | Descrição                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Gather**](texture2d-gather.md)                                      | Retorna os quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                                                |
| [**GatherRed**](texture2d-gatherred.md)                                | Retorna os componentes vermelhos dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                          |
| [**GatherGreen**](texture2d-gathergreen.md)                            | Retorna os componentes verdes dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                        |
| [**GatherBlue**](texture2d-gatherblue.md)                              | Retorna os componentes azuis dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                         |
| [**GatherAlpha**](texture2d-gatheralpha.md)                            | Retorna os componentes alfa dos quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear.                                        |
| [**GatherCmp**](texture2d-gathercmp.md)                                | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna a comparação contra um valor de comparação.                      |
| [**GatherCmpRed**](texture2d-gathercmpred.md)                          | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente vermelho em relação a um valor de comparação.   |
| [**GatherCmpGreen**](texture2d-gathercmpgreen.md)                      | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente verde em relação a um valor de comparação. |
| [**GatherCmpBlue**](texture2d-gathercmpblue.md)                        | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente azul em relação a um valor de comparação.  |
| [**GatherCmpAlpha**](texture2d-gathercmpalpha.md)                      | Para quatro valores Texel que seriam usados em uma operação de filtragem de bi-linear, o retorna uma comparação de seu componente alfa em relação a um valor de comparação. |
| [**GetDimensions**](sm5-object-texture2d-getdimensions.md)             | Obtém as dimensões do recurso.                                                                                                                       |
| [**Carregamento**](texture2d-load.md)                                          | Lê dados de textura.                                                                                                                                 |
| [**seqüencia. Operador\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) | Obtém uma variável de recurso somente leitura.                                                                                                                 |
| [**Operador\[\]**](sm5-object-texture2d-operatorindex.md)              | Obtém uma variável de recurso somente leitura.                                                                                                                 |
| [**Nova**](texture-sample-overload.md)                               | Amostra uma textura.                                                                                                                                  |
| [**SampleBias**](texture2d-samplebias.md)                              | Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.                                                                               |
| [**SampleCmp**](texture2d-samplecmp.md)                                | Amostra uma textura, usando um valor de comparação para rejeitar amostras.                                                                                      |
| [**SampleCmpLevelZero**](texture2d-samplecmplevelzero.md)              | Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.                                                                |
| [**SampleGrad**](texture2d-samplegrad.md)                              | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.                                                          |
| [**SampleLevel**](texture2d-samplelevel.md)                            | Amostra uma textura no nível de mipmap especificado.                                                                                                    |



 

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

 

 




