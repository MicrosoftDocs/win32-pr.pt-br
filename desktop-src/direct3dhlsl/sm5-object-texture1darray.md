---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11573dc84c46149073ca3a7e192ed8541d9cfd4a78494a43f6130a7999534880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508672"
---
# <a name="texture1darray"></a>Texture1DArray

Tipo Texture1DArray ([como ele existe no Modelo de Sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso. Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no Modelo de Sombreador 4.



| Método                                                                       | Descrição                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Obtém as dimensões do recurso.                                                              |
| [**Carregar**](texture1darray-load.md)                                          | Lê dados de textura.                                                                        |
| [**Mips. Operador\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Obtém uma variável de recurso somente leitura.                                                        |
| [**Operador\[\]**](sm5-object-texture1darray-operatorindex.md)              | Obtém uma variável de recurso somente leitura.                                                        |
| [**Amostra**](texture1darray-sample.md)                                      | Amostras de uma textura.                                                                         |
| [**SampleBias**](texture1darray-samplebias.md)                              | Amostra uma textura, depois de aplicar o valor de desvio ao nível de mipmap.                      |
| [**SampleCmp**](texture1darray-samplecmp.md)                                | Amostra uma textura usando um valor de comparação para rejeitar amostras.                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              | Amostra uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.       |
| [**SampleGrad**](texture1darray-samplegrad.md)                              | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado. |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | Amostra uma textura no nível de mipmap especificado.                                           |



 

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

 

 




