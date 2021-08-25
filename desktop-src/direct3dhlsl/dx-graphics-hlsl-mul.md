---
title: mul
description: Multiplica x e y usando matemática de matriz. As colunas x e y da dimensão interna devem ser iguais.
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- mul HLSL
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6362c734cbbf30defa8fed75f28c6f39397d75977488d9efc170d2647a9b3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950356"
---
# <a name="mul"></a>mul

Multiplica x e y usando matemática de matriz. As colunas x e y da dimensão interna devem ser iguais.



| ret mul(x, y) |
|---------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[no \] valor de entrada x. Se x for um vetor, ele será tratado como um vetor de linha.<br/>    |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[no \] valor de entrada y. Se y for um vetor, ele será tratado como um vetor de coluna.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O resultado de x vezes y. O resultado tem a dimensão x-rows x y-columns.

## <a name="type-description"></a>Descrição do tipo

Há 9 versões sobrecarregadas dessa função; as versões sobrecarregadas lidam com os diferentes casos para os tipos e tamanhos dos argumentos de entrada.



| Versão | Nome | Finalidade | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md) | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | a    | in      | escalar                                                        | mesmo que a entrada x                                                | 1                                                                        |
|         | Ret  | out     | escalar                                                        | mesmo que a entrada x                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | a    | in      | vector                                                        | float, int                                                     | any                                                                      |
|         | Ret  | out     | vector                                                        | float, int                                                     | mesmas dimensões que a entrada y                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | a    | in      | matriz                                                        | float, int                                                     | any                                                                      |
|         | Ret  | out     | matriz                                                        | mesmo que a entrada y                                                | mesmas dimensões que a entrada y                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | Ret  | out     | vector                                                        | float, int                                                     | mesmas dimensões que a entrada x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | vector                                                        | float, int                                                     | mesmas dimensões que a entrada x                                             |
|         | Ret  | out     | escalar                                                        | float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vector                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | matriz                                                        | float, int                                                     | rows = same dimension(s) as input x, columns = any                       |
|         | Ret  | out     | vector                                                        | float, int                                                     | mesmas dimensões que as colunas y de entrada                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | escalar                                                        | float, int                                                     | 1                                                                        |
|         | Ret  | out     | matriz                                                        | float, int                                                     | mesmas dimensões que a entrada x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | vector                                                        | float, int                                                     | número de colunas na entrada x                                             |
|         | Ret  | out     | vector                                                        | float, int                                                     | número de linhas na entrada x                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matriz                                                        | float, int                                                     | any                                                                      |
|         | a    | in      | matriz                                                        | float, int                                                     | rows = número de colunas na entrada x                                      |
|         | Ret  | out     | matriz                                                        | float, int                                                     | rows = número de linhas na entrada x, colunas = número de colunas na entrada y |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                       | Com suporte |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelos de sombreador superior | sim       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





