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
ms.openlocfilehash: aab6e5c0a500a9f34cbd4e418a35e96687650f3df863e1fe77576c66ade718e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023396"
---
# <a name="texture2darray"></a>Texture2DArray

Tipo Texture2DArray ([como ele existe no Modelo de Sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso. Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no Modelo de Sombreador 4.



| Método                                                                      | Descrição                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reunir**](texture2darray-gather.md)                                      | Retorna os quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                                                |
| [**GatherRed**](texture2darray-gatherred.md)                                | Retorna os componentes vermelhos dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                          |
| [**GatherGreen**](texture2darray-gathergreen.md)                            | Retorna os componentes verdes dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                        |
| [**GatherBlue**](texture2darray-gatherblue.md)                              | Retorna os componentes azuis dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                         |
| [**GatherAlpha**](texture2darray-gatheralpha.md)                            | Retorna os componentes alfa dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                        |
| [**GatherCmp**](texture2darray-gathercmp.md)                                | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna sua comparação com um valor de comparação.                      |
| [**GatherCmpRed**](texture2darray-gathercmpred.md)                          | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente vermelho em relação a um valor de comparação.   |
| [**GatherCmpGreen**](texture2darray-gathercmpgreen.md)                      | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente verde em relação a um valor de comparação. |
| [**GatherCmpBlue**](texture2darray-gathercmpblue.md)                        | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente azul em relação a um valor de comparação.  |
| [**GatherCmpAlpha**](texture2darray-gathercmpalpha.md)                      | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente alfa em relação a um valor de comparação. |
| [**GetDimensions**](sm5-object-texture2darray-getdimensions.md)             | Obtém as dimensões do recurso.                                                                                                                       |
| [**Carregar**](texture2darray-load.md)                                          | Lê dados de textura.                                                                                                                                 |
| [**Mips. Operador\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) | Obtém uma variável de recurso somente leitura.                                                                                                                 |
| [**Operador\[\]**](sm5-object-texture2darray-operatorindex.md)              | Obtém uma variável de recurso somente leitura.                                                                                                                 |
| [**Amostra**](texture2darray-sample.md)                                      | Amostras de uma textura.                                                                                                                                  |
| [**SampleBias**](texture2darray-samplebias.md)                              | Amostra uma textura, depois de aplicar o valor de desvio ao nível de mipmap.                                                                               |
| [**SampleCmp**](texture2darray-samplecmp.md)                                | Amostra uma textura usando um valor de comparação para rejeitar amostras.                                                                                      |
| [**SampleCmpLevelZero**](texture2darray-samplecmplevelzero.md)              | Amostra uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.                                                                |
| [**SampleGrad**](texture2darray-samplegrad.md)                              | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.                                                          |
| [**SampleLevel**](texture2darray-samplelevel.md)                            | Amostra uma textura no nível de mipmap especificado.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esse objeto tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Esse objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Modelo de Sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




