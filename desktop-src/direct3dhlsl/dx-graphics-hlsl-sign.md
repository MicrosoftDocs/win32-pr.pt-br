---
title: sinal
description: Retorna o sinal de x.
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- assinar HLSL
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc177e72e116394ffd6241e0616b84c9066a68a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988704"
---
# <a name="sign"></a>sinal

Retorna o sinal de *x*.



| sinal de *RET* (*x*) |
|-----------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] valor de entrada.<br/> |



 

## <a name="return-value"></a>Valor Retornado

Retornará-1 se *x* for menor que zero; 0 se *x* for igual a zero; e 1 se *x* for maior que zero.

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *RET* | igual ao *x* de entrada                                                                                              | [**int**](/windows/desktop/WinProg/windows-data-types)                                          | mesmas dimensões como entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos | sim                         |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Sim (vs \_ 1 \_ 1 e PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

