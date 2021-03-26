---
title: acos
description: Retorna o arco cosseno do valor especificado.
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- HLSL de acos
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2cd909c4a4c1300374bba723f1edabb48d51b2e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084848"
---
# <a name="acos"></a>acos

Retorna o arco cosseno do valor especificado.



| acos de *RET* (*x*) |
|-----------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] valor especificado. Cada componente deve ser um valor de ponto flutuante dentro do intervalo de-1 a 1.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O arco cosseno do parâmetro *x* .

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *RET* | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte     |
|------------------------------------------------------------------------------------|---------------|
| [Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos | sim           |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | \_apenas vs 1 \_ 1 |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

