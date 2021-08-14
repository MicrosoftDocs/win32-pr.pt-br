---
title: Etapa
description: Compara dois valores, retornando 0 ou 1 com base em qual valor é maior.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- etapa HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27fe6985a4dfb4e77f1052b421a6c46c617395f46b4484f046b33919a935613f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276506"
---
# <a name="step"></a>Etapa

Compara dois valores, retornando 0 ou 1 com base em qual valor é maior.



| etapa *RET* (*y*, *x*) |
|----------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span id="y"></span><span id="Y"></span>*Iar*<br/> | \[no \] primeiro valor de ponto flutuante a ser comparado.<br/>  |
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] segundo valor de ponto flutuante a ser comparado.<br/> |



 

## <a name="return-value"></a>Valor Retornado

1 se o parâmetro *x* for maior ou igual ao parâmetro *y* ; caso contrário, 0.

## <a name="remarks"></a>Comentários

Essa função usa a seguinte fórmula: (*x*  >=  *y*)? 1:0. A função retorna 0 ou 1 dependendo se o parâmetro *x* é maior que o parâmetro *y* . Para calcular uma interpolação suave entre 0 e 1, use a função intrínseca [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL.

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *x*   | igual a *y* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como *y* de entrada |
| *RET* | igual a *y* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como *y* de entrada |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos | sim                         |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Sim (vs \_ 1 \_ 1 e PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

