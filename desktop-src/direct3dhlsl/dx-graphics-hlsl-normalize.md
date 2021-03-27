---
title: normaliza
description: Normaliza o vetor de ponto flutuante especificado de acordo com x/Length (x).
ms.assetid: 7fd6f8ff-f3ff-4d14-b3fc-b44fdddf6c75
keywords:
- normalizar HLSL
topic_type:
- apiref
api_name:
- normalize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f48c78f80f5f92f950795018f05a46c7883d9736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917646"
---
# <a name="normalize"></a>normaliza

Normaliza o vetor de ponto flutuante especificado de acordo com x/Length (x).



| Normalize. de *RET* (*x*) |
|----------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                            |
|--------------------------------------------------------|--------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] vetor de ponto flutuante especificado.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O parâmetro *x* normalizado. Se o comprimento do parâmetro *x* for 0, o resultado será indefinido.

## <a name="remarks"></a>Comentários

A função intrínseca **Normalize** HLSL usa a seguinte fórmula: *x*  /  [**comprimento**](dx-graphics-hlsl-length.md)(*x*).

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *RET* | igual ao *x* de entrada                                                                   | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |



 

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

 

