---
title: cruzadas
description: Retorna o produto cruzado de dois vetores 3D de ponto flutuante.
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- HLSL cruzado
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988708"
---
# <a name="cross"></a>cruzadas

Retorna o produto cruzado de dois vetores 3D de ponto flutuante.



| cruzada de *RET* (*x*, *y*) |
|-----------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] primeiro ponto flutuante, vetor 3D.<br/>  |
| <span id="y"></span><span id="Y"></span>*Iar*<br/> | \[no \] segundo ponto flutuante, vetor 3D.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O produto cruzado do parâmetro *x* e o parâmetro *y* .

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *y*   | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *RET* | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 3    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte             |
|------------------------------------------------------------------------------------|-----------------------|
| [Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos | sim                   |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 e PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

