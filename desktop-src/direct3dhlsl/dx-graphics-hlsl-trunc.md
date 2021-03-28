---
title: trunc (Corecrt \_ Math. h)
description: Trunca um valor de ponto flutuante para o componente de número inteiro.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- truncar HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989319"
---
# <a name="trunc"></a>trunc

Trunca um valor de ponto flutuante para o componente de número inteiro.



| RET TRUNC (*x*) |
|----------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[na \] entrada especificada.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O valor de entrada truncado para um componente de número inteiro.

## <a name="remarks"></a>Comentários

Essa função Trunca um valor de ponto flutuante para o componente de número inteiro. Dado um valor de ponto flutuante de 1,6, a função TRUNC retornaria 1,0, onde como a função [**Round (DirectX HLSL)**](dx-graphics-hlsl-round.md) retornaria 2,0.

## <a name="type-description"></a>Descrição do tipo



| Name | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                          |
| RET  | Mesmo tipo que o x de entrada                                                                                           | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | Mesmas dimensões como entrada x |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte |
|------------------------------------------------------------------------------------|-----------|
| [Modelo do sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelos de sombreador mais altos | sim       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

