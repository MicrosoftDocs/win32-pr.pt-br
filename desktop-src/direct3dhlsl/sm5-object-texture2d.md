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
ms.openlocfilehash: ad13843dd74ab7cc188c3ab37d76df978f2a5fbd4bc6c292cfddfdf7c5841b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789372"
---
# <a name="texture2d"></a>Texture2D

Tipo Texture2D ([como ele existe no Modelo de Sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso. Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no Modelo de Sombreador 4.



| Método                                                                 | Descrição                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reunir**](texture2d-gather.md)                                      | Retorna os quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                                                |
| [**GatherRed**](texture2d-gatherred.md)                                | Retorna os componentes vermelhos dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                          |
| [**GatherGreen**](texture2d-gathergreen.md)                            | Retorna os componentes verdes dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                        |
| [**GatherBlue**](texture2d-gatherblue.md)                              | Retorna os componentes azuis dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                         |
| [**GatherAlpha**](texture2d-gatheralpha.md)                            | Retorna os componentes alfa dos quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.                                        |
| [**GatherCmp**](texture2d-gathercmp.md)                                | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna sua comparação com um valor de comparação.                      |
| [**GatherCmpRed**](texture2d-gathercmpred.md)                          | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente vermelho em relação a um valor de comparação.   |
| [**GatherCmpGreen**](texture2d-gathercmpgreen.md)                      | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente verde em relação a um valor de comparação. |
| [**GatherCmpBlue**](texture2d-gathercmpblue.md)                        | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente azul em relação a um valor de comparação.  |
| [**GatherCmpAlpha**](texture2d-gathercmpalpha.md)                      | Para quatro valores de texel que seriam usados em uma operação de filtragem bi-linear, retorna uma comparação de seu componente alfa em relação a um valor de comparação. |
| [**GetDimensions**](sm5-object-texture2d-getdimensions.md)             | Obtém as dimensões do recurso.                                                                                                                       |
| [**Carregar**](texture2d-load.md)                                          | Lê dados de textura.                                                                                                                                 |
| [**Mips. Operador\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) | Obtém uma variável de recurso somente leitura.                                                                                                                 |
| [**Operador\[\]**](sm5-object-texture2d-operatorindex.md)              | Obtém uma variável de recurso somente leitura.                                                                                                                 |
| [**Amostra**](texture-sample-overload.md)                               | Amostras de uma textura.                                                                                                                                  |
| [**SampleBias**](texture2d-samplebias.md)                              | Amostra uma textura, depois de aplicar o valor de desvio ao nível de mipmap.                                                                               |
| [**SampleCmp**](texture2d-samplecmp.md)                                | Amostra uma textura usando um valor de comparação para rejeitar amostras.                                                                                      |
| [**SampleCmpLevelZero**](texture2d-samplecmplevelzero.md)              | Amostra uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.                                                                |
| [**SampleGrad**](texture2d-samplegrad.md)                              | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado.                                                          |
| [**SampleLevel**](texture2d-samplelevel.md)                            | Amostra uma textura no nível de mipmap especificado.                                                                                                    |



 

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

 

 




