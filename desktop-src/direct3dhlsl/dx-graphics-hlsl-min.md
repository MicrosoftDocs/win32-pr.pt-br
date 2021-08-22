---
title: min
description: Seleciona o menor de x e y.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- min HLSL
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ba9474383af448c36c6bb1130470aa6706fd8bd06c2d21bef66eb1c4bbcda0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513817"
---
# <a name="min"></a>min

Seleciona o menor de x e y.



| ret min(x, y) |
|---------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[no \] valor de entrada x.<br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[no \] valor de entrada y.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O *parâmetro x* ou *y,* o que for o menor valor.


## <a name="remarks"></a>Comentários

Os desnormais são tratados da seguinte forma:

| src0 src1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | -inf          | -inf | -inf |
| F           | -inf | src0 ou src1  | src0 | src0 |
| +inf        | -inf | src1          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F significa número finito real.


## <a name="type-description"></a>Descrição do tipo

| Nome | Entrada/saída      | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Tamanho                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vetor** ou **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| a    | in          | mesmo que a entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões que a entrada x |
| Ret  | tipo de retorno | mesmo que a entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões que a entrada x |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                       | Com suporte                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador superior | sim                         |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sim (vs \_ 1 \_ 1 e ps \_ 1 \_ 4) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**Especificação funcional do DirectX**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)