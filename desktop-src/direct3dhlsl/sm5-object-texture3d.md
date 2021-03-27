---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006426"
---
# <a name="texture3d"></a>Texture3D

Tipo de Texture3D ([como ele existe no modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) mais variáveis de recurso. Esse objeto de textura dá suporte aos métodos a seguir, além dos métodos no sombreador modelo 4.



| Método                                                                  | Descrição                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | Obtém as dimensões do recurso.                                                              |
| [**Carregamento**](texture3d-load.md)                                          | Lê dados de textura.                                                                        |
| [**seqüencia. Operador\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | Obtém uma variável de recurso somente leitura.                                                        |
| [**Operador\[\]**](sm5-object-texture3d-operatorindex.md)              | Obtém uma variável de recurso somente leitura.                                                        |
| [**Nova**](texture3d-sample.md)                                      | Amostra uma textura.                                                                         |
| [**SampleBias**](texture3d-samplebias.md)                              | Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap.                      |
| [**SampleGrad**](texture3d-samplegrad.md)                              | Amostra uma textura usando um gradiente para influenciar a maneira como o local de exemplo é calculado. |
| [**SampleLevel**](texture3d-samplelevel.md)                            | Amostra uma textura no nível de mipmap especificado.                                           |



 

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

 

 




