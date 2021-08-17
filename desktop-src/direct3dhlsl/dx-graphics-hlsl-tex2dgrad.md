---
title: tex2Dgrad
description: Amostra uma textura 2D usando um gradiente para selecionar o nível mip. | tex2Dgrad
ms.assetid: a9ab7972-3480-4b37-aa10-c5cf811bdd0e
keywords:
- HLSL do tex2Dgrad
topic_type:
- apiref
api_name:
- tex2Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 358690291cbb8cffbf6d60ef034b42d075902b923a3899824845e42bad999a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119910"
---
# <a name="tex2dgrad"></a>tex2Dgrad

Amostra uma textura 2D usando um gradiente para selecionar o nível mip.



| ret tex2Dgrad(s, t, ddx, ddy) |
|-------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                         | Descrição                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[em \] O estado do exemplo.<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[em \] As coordenadas de textura.<br/>                                   |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[em \] Taxa de alteração da geometria da superfície na direção x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*Ddy*<br/> | \[em \] Taxa de alteração da geometria da superfície na direção y.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O valor dos dados de textura.

## <a name="type-description"></a>Descrição do tipo



| Nome | Entrada/saída | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| Ddx  | in     | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| Ddy  | in     | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| Ret  | out    | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte                |
|-----------------------------------------------------------|--------------------------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim (somente sombreador de pixel)  |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sim (somente sombreador de pixel) |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sim (somente sombreador de pixel) |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não                       |



 

1.  A reordenação significativa de código é feita para mover cálculos de gradiente para fora do controle de fluxo.
2.  Se o limite D3DPSHADERCAPS2 0 for definido com \_ D3DD3DPSHADERCAPS2 \_ 0 GRADIENTINSTRUCTIONS, o compilador mapeia essa função para \_ o texldd.

## <a name="remarks"></a>Comentários

Quando o controle de fluxo está presente em um sombreador, o resultado de um cálculo de gradiente solicitado dentro de um determinado caminho de ramificação é ambíguo quando pixels adjacentes podem cair em caminhos separados de controle de fluxo. Portanto, é considerado ilegal usar qualquer operação de sombreador de pixel que solicita que um cálculo de gradiente ocorra em um local que está dentro de um constructo de controle de fluxo que pode variar entre pixels para um determinado primitivo que está sendo rasterizado. Se um dos lados de uma **instrução if** com o atributo branch usar uma função de gradiente, um erro do compilador poderá ser gerado. Veja [se instrução (DirectX HLSL)](dx-graphics-hlsl-if.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

