---
title: mul
description: Multiplica x e y usando matriz Math. A dimensão interna x-Columns e as linhas y devem ser iguais.
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- Mul HLSL
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2e9fe545cb16f8ac1fef1935b9d7e97075521b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006326"
---
# <a name="mul"></a>mul

Multiplica x e y usando matriz Math. A dimensão interna x-Columns e as linhas y devem ser iguais.



| RET Mul (x, y) |
|---------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] valor de entrada x. Se x for um vetor, ele será tratado como um vetor de linha.<br/>    |
| <span id="y"></span><span id="Y"></span>*Iar*<br/> | \[no \] valor de entrada de y. Se y for um vetor, ele será tratado como um vetor de coluna.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O resultado de x vezes y. O resultado tem a dimensão x-linhas x y-colunas.

## <a name="type-description"></a>Descrição do tipo

Há 9 versões sobrecarregadas dessa função; as versões sobrecarregadas lidam com casos diferentes para os tipos e tamanhos dos argumentos de entrada.



| Versão | Nome | Finalidade | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md) | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | a    | in      | escalar                                                        | igual ao x de entrada                                                | 1                                                                        |
|         | RET  | out     | escalar                                                        | igual ao x de entrada                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | a    | in      | vector                                                        | float, int                                                     | any                                                                      |
|         | RET  | out     | vector                                                        | float, int                                                     | mesmas dimensões como y de entrada                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | a    | in      | matriz                                                        | float, int                                                     | any                                                                      |
|         | RET  | out     | matriz                                                        | igual a y de entrada                                                | mesmas dimensões como y de entrada                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | RET  | out     | vector                                                        | float, int                                                     | mesmas dimensões como entrada x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | vector                                                        | float, int                                                     | mesmas dimensões como entrada x                                             |
|         | RET  | out     | escalar                                                        | float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | matriz                                                        | float, int                                                     | linhas = as mesmas dimensões como x de entrada, colunas = qualquer                       |
|         | RET  | out     | vector                                                        | float, int                                                     | mesmas dimensões como colunas y de entrada                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | RET  | out     | matriz                                                        | float, int                                                     | mesmas dimensões como entrada x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | vector                                                        | float, int                                                     | número de colunas na entrada x                                             |
|         | RET  | out     | vector                                                        | float, int                                                     | número de linhas no x de entrada                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | matriz                                                        | float, int                                                     | Rows = número de colunas na entrada x                                      |
|         | RET  | out     | matriz                                                        | float, int                                                     | linhas = número de linhas na entrada x, colunas = número de colunas na entrada y |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte |
|------------------------------------------------------------------------------------|-----------|
| [Modelo do sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelos de sombreador mais altos | sim       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





