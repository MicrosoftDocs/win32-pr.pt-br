---
title: atan2 (Corecrt \_ math.h)
description: Retorna o tangente de dois valores (x,y).
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
ms.openlocfilehash: 2932f82cf6d9e8b2071446b63f84e60727aff2da2213461d3c1194b2811fe1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854966"
---
# <a name="atan2"></a>atan2

Retorna o tangente de dois valores (x,y).



| *ret* atan2(*y*, *x*) |
|-----------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                    |
|--------------------------------------------------------|--------------------------------|
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[no \] valor y.<br/> |
| <span id="x"></span><span id="X"></span>*X*<br/> | \[no \] valor x.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O tangente de (y,x).

## <a name="remarks"></a>Comentários

Os sinais dos parâmetros *x* e *y* são usados para determinar o quadrante dos valores de retorno dentro do intervalo de -π a π. A função intrínseca **atan2** HLSL é bem definida para cada ponto diferente da origem, mesmo que *y* seja igual a 0 e *x* não seja igual a 0.

## <a name="type-description"></a>Descrição do tipo



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | mesmo que a entrada *x*                                                                                              | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões que a entrada *x* |
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vetor** ou **matriz** | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | mesmo que a entrada *x*                                                                                              | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões que a entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                       | Com suporte |
|------------------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador superior | sim       |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

