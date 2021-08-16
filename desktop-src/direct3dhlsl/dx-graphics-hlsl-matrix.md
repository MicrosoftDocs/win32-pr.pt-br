---
title: Tipo de matriz
description: Uma matriz é um tipo de dados especial que contém entre um e dezesseis componentes. Cada componente de uma matriz deve ser do mesmo tipo.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Tipo de matriz HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e6b98309c760a3da4d1e9c488e4aed049aa34f0b449042e8f00a02426cc513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726166"
---
# <a name="matrix-type"></a>Tipo de matriz

Uma matriz é um tipo de dados especial que contém entre um e dezesseis componentes. Cada componente de uma matriz deve ser do mesmo tipo.



|                         |
|-------------------------|
| **Nome do TypeComponents** |



 

## <a name="components"></a>Componentes



| Item                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Um único nome que contém três partes. A primeira parte é um dos tipos [escalares](dx-graphics-hlsl-data-types.md) . A segunda parte é o número de linhas. A terceira parte é o número de colunas. O número de linhas e colunas é um inteiro positivo entre 1 e 4, inclusive.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/>                                         | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a>Exemplos

Estes são alguns exemplos:


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Uma matriz pode ser declarada usando essa sintaxe também:


```
matrix <Type, Number> VariableName
```



O tipo de matriz usa os colchetes angulares para especificar o tipo, o número de linhas e o número de colunas. Este exemplo cria uma matriz de ponto flutuante, com duas linhas e duas colunas. Qualquer um dos tipos de dados escalares pode ser usado.

Veja um exemplo:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





