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
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006656"
---
# <a name="texture1darray"></a>Texture1DArray

Tipo de Texture1DArray ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso. Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.



| Método                                                                       | Descrição                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Obtém as dimensões do recurso.                                                              |
| [**Carregamento**](texture1darray-load.md)                                          | Lê dados de textura.                                                                        |
| [**seqüencia. Operador\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Obtém uma variável de recurso somente leitura.                                                        |
| [**Operador\[\]**](sm5-object-texture1darray-operatorindex.md)              | Obtém uma variável de recurso somente leitura.                                                        |
| [**Nova**](texture1darray-sample.md)                                      | Amostra uma textura.                                                                         |
| [**SampleBias**](texture1darray-samplebias.md)                              | Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.                      |
| [**SampleCmp**](texture1darray-samplecmp.md)                                | Amostra uma textura, usando um valor de comparação para rejeitar amostras.                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              | Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.       |
| [**SampleGrad**](texture1darray-samplegrad.md)                              | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado. |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | Amostra uma textura no nível de mipmap especificado.                                           |



 

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

 

 




