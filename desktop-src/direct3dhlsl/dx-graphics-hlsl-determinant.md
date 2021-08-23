---
title: Determinante
description: Retorna o determinante da matriz quadrada e de ponto flutuante especificada.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- HLSL determinante
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b17982560d70cf00cfb13832de9605b910f169d1461692f4c6a97274709e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120300"
---
# <a name="determinant"></a>Determinante

Retorna o determinante da matriz quadrada e de ponto flutuante especificada.



| *ret* determinant(*m*) |
|------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="m"></span><span id="M"></span>*M*<br/> | \[em \] O valor especificado.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O valor escalar de ponto flutuante que representa o determinante do *parâmetro m.*

## <a name="type-description"></a>Descrição do tipo



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| *m*   | [**Matriz**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | any (número de linhas = número de colunas) |
| *Ret* | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                                        |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                       | Com suporte             |
|------------------------------------------------------------------------------------|-----------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador superior | sim                   |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 e ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

