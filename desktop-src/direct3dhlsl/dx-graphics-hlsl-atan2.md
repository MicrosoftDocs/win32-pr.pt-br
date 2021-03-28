---
title: atan2 (Corecrt \_ Math. h)
description: Retorna o arco tangente de dois valores (x, y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- atan2 HLSL
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172992"
---
# <a name="atan2"></a>atan2

Retorna o arco tangente de dois valores (x, y).



| *RET* ATAN2 (*y*, *x*) |
|-----------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                    |
|--------------------------------------------------------|--------------------------------|
| <span id="y"></span><span id="Y"></span>*Iar*<br/> | \[no \] valor y.<br/> |
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] valor x.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O arco tangente de (y, x).

## <a name="remarks"></a>Comentários

Os sinais dos parâmetros *x* e *y* são usados para determinar o quadrante dos valores de retorno dentro do intervalo de-π a π. A função intrínseca **ATAN2** HLSL é bem definida para cada ponto que não seja a origem, mesmo se *y* for igual a 0 e *x* for igual a 0.

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *RET* | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte |
|------------------------------------------------------------------------------------|-----------|
| [Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos | sim       |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

