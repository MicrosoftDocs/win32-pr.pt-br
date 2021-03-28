---
title: faceforward
description: Inverte a superfície – normal (se necessário) para enfrentar uma direção oposta à i; Retorna o resultado em n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- faceforward HLSL
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084635"
---
# <a name="faceforward"></a>faceforward

Inverte a superfície – normal (se necessário) para enfrentar uma direção oposta à i; Retorna o resultado em n.



| *RET* faceforward (*n*, *i*, *ng*) |
|-----------------------------------|



 

Essa função usa a seguinte fórmula:-*n*  sinal (ponto (*i*, *ng*)).

## <a name="parameters"></a>Parâmetros



| Item                                                      | Descrição                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*p*<br/>    | \[na \] superfície de ponto flutuante resultante-vetor normal.<br/>                                           |
| <span id="i"></span><span id="I"></span>*Encontrei*<br/>    | \[em \] um ponto flutuante, o vetor de incidente que aponta da posição de exibição para a posição de sombreamento.<br/> |
| <span id="ng"></span><span id="NG"></span>*ção*<br/> | \[em \] uma superfície de ponto flutuante-vetor normal.<br/>                                                       |



 

## <a name="return-value"></a>Valor Retornado

Um vetor de ponto flutuante, de superfície normal, que está voltado para a direção da exibição.

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *i*   | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesma dimensão (s) como entrada *n* |
| *ção*  | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *n*   |
| *RET* | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *n*   |



 

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

 

