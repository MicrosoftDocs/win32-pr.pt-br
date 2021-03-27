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
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916801"
---
# <a name="texture1d"></a>Texture1D

Um tipo de textura 1D ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) Além de variáveis de recurso. Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.



| Método                                                                  | Descrição                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | Obtém as dimensões do recurso.                                                              |
| [**Carregamento**](texture1d-load.md)                                          | Lê dados de textura.                                                                        |
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



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




