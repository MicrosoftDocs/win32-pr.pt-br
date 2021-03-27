---
title: fixe
description: Coloca o valor especificado para o intervalo mínimo e máximo especificado.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- Fixe HLSL
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641660"
---
# <a name="clamp"></a>fixe

Coloca o valor especificado para o intervalo mínimo e máximo especificado.



| *RET* fixe (*x*, *mín*., *máx*.) |
|--------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                         | Descrição                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/>       | \[em \] um valor para fixe.<br/>            |
| <span id="min"></span><span id="MIN"></span>*min*<br/> | \[no \] intervalo mínimo especificado.<br/> |
| <span id="max"></span><span id="MAX"></span>*maximizar*<br/> | \[no \] intervalo máximo especificado.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O valor de clamped para o parâmetro *x* .

## <a name="remarks"></a>Comentários

Para os valores de-INF ou INF, fixe se comportará conforme o esperado. No entanto, para valores de NaN, os resultados são indefinidos.

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *min* | igual ao *x* de entrada                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões como entrada *x* |
| *max* | igual ao *x* de entrada                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões como entrada *x* |
| *RET* | igual ao *x* de entrada                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões como entrada *x* |



 

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

 

