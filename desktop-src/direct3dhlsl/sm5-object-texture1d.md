---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- Texture1D HLSL
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 382ac1e436eff4108a2179aeefd4395fbc52c7af304bb719cbadf87a3c1f3d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724867"
---
# <a name="texture1d"></a>Texture1D

Um tipo de textura 1D ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) Além de variáveis de recurso. Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.



| Método                                                                  | Descrição                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | Obtém as dimensões do recurso.                                                              |
| [**Carregar**](texture1d-load.md)                                          | Lê dados de textura.                                                                        |
| [**Operador\[\]**](sm5-object-texture1d-operatorindex.md)              | Obtém uma variável de recurso somente leitura.                                                        |
| [**seqüencia. Operador\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) | Obtém uma variável de recurso somente leitura.                                                        |
| [**Nova**](texture1d-sample.md)                                      | Amostra uma textura.                                                                         |
| [**SampleBias**](texture1d-samplebias.md)                              | Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.                      |
| [**SampleCmp**](texture1d-samplecmp.md)                                | Amostra uma textura, usando um valor de comparação para rejeitar amostras.                             |
| [**SampleCmpLevelZero**](texture1d-samplecmplevelzero.md)              | Amostras de uma textura (somente mipmap nível 0), usando um valor de comparação para rejeitar amostras.       |
| [**SampleGrad**](texture1d-samplegrad.md)                              | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado. |
| [**SampleLevel**](texture1d-samplelevel.md)                            | Amostra uma textura no nível de mipmap especificado.                                           |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




