---
title: lerp
description: Executa uma interpolação linear.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- Lerp HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6981ef4134bbce17cbc7fa1e17de4d55de198572716ac39cbdd44b5e552e7f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791632"
---
# <a name="lerp"></a>lerp

Executa uma interpolação linear.



| *RET* Lerp (*x*, *y*, *s*) |
|---------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] primeiro valor de ponto flutuante.<br/>                                                     |
| <span id="y"></span><span id="Y"></span>*Iar*<br/> | \[no \] segundo valor de ponto flutuante.<br/>                                                    |
| <span id="s"></span><span id="S"></span>*&*<br/> | \[em \] um valor que interpola linearmente entre o parâmetro *x* e o parâmetro *y* .<br/> |



 

## <a name="return-value"></a>Valor Retornado

O resultado da interpolação linear.

## <a name="type-description"></a>Descrição do tipo



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |
| *s*   | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |
| *RET* | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |



 

## <a name="remarks"></a>Comentários

A interpolação linear baseia-se na fórmula a seguir: x \* (1-s) + y \* s que pode ser escrito de forma equivalente como x + s (y-x).

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos | sim                         |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Sim (vs \_ 1 \_ 1 e PS \_ 1 \_ 1) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

