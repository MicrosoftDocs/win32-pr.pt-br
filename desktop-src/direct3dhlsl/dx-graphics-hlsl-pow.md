---
title: pow
description: Retorna o valor especificado elevado à potência especificada.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454309"
---
# <a name="pow"></a>pow

Retorna o valor especificado elevado à potência especificada.



| *RET* pow (*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] valor especificado.<br/> |
| <span id="y"></span><span id="Y"></span>*Iar*<br/> | \[na \] potência especificada.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O parâmetro *x* é elevado à potência do parâmetro *y* .

## <a name="remarks"></a>Comentários

A função intrínseca **pow** HLSL calcula *x*<sup>y</sup>.



| X      | Y      | Resultado                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| < 0 | any    | NAN                                                                         |
| > 0 | = = 0   | 1                                                                           |
| = = 0   | > 0 | 0                                                                           |
| = = 0   | < 0 | ini                                                                         |
| > 0 | < 0 | 1/X<sup>-Y</sup>                                                            |
| = = 0   | = = 0   | Depende do processador gráfico específico<br/> 0, ou 1, ou NAN<br/> |



 

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |
| *RET* | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos | sim                 |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Sim ( \_ apenas vs 1 \_ 1) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

