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
ms.openlocfilehash: 253d581ef5ea2eddac55c63245039f1ccda6c0e73032468d1598fb919e850a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950376"
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



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
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

 

