---
title: asfloat
description: Interpreta o padrão de bit de x como um número de ponto flutuante.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- asfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988696"
---
# <a name="asfloat"></a>asfloat

Interpreta o padrão de bit de *x* como um número de ponto flutuante.



| RET asfloat (*x*) |
|------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] valor de entrada.<br/> |



 

## <a name="return-value"></a>Valor Retornado

A entrada interpretada como um número de ponto flutuante.

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *RET* | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                                                                                | mesmas dimensões como entrada *x* |



 

## <a name="function-overloads"></a>Sobrecargas de função

<dl> ' float <x> asfloat ( <x> valor float); `  
` float <x> asfloat ( <x> valor int); `  
` float <x> asfloat ( <x> valor UINT); '
</dl>

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | não        |



 

## <a name="remarks"></a>Comentários

Os compiladores mais antigos são permitidos incorretamente `asfloat(bool)` , mas observe que não há suporte para entradas bool.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

