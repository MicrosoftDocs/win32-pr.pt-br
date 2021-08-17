---
title: max
description: Seleciona o maior x e y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- HLSL máx.
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e81eca4f5cabea57f36aa66b722fedb3e1176c3c189db9cdcfd610e4e26047c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791467"
---
# <a name="max"></a>max

Seleciona o maior x e y.



| RET máx. (x, y) |
|---------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] valor de entrada x.<br/> |
| <span id="y"></span><span id="Y"></span>*Iar*<br/> | \[no \] valor de entrada de y.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O parâmetro *x* ou *y* , o que for o maior valor.


## <a name="remarks"></a>Comentários

Os desnormals são tratados da seguinte maneira:

| src0 src1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | src1          | +inf | -inf |
| F           | src0 | src0 ou src1  | +inf | src0 |
| +inf        | +inf | +inf          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F significa número real finito.


## <a name="type-description"></a>Descrição do tipo

| Nome | Entrada/saída      | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Tamanho                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| a    | in          | igual ao x de entrada                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões como entrada x |
| RET  | tipo de retorno | igual ao x de entrada                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões como entrada x |



 

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

[**Especificação funcional do DirectX**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
