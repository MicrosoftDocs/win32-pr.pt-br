---
title: tex2Dgrad
description: Amostra uma textura 2D usando um gradiente para selecionar o nível MIP. | tex2Dgrad
ms.assetid: a9ab7972-3480-4b37-aa10-c5cf811bdd0e
keywords:
- tex2Dgrad HLSL
topic_type:
- apiref
api_name:
- tex2Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74b20f1cf1f6f5d3b2873f4546dd57ef73b23dbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968292"
---
# <a name="tex2dgrad"></a>tex2Dgrad

Amostra uma textura 2D usando um gradiente para selecionar o nível MIP.



| RET tex2Dgrad (s, t, campo DDX, ddy) |
|-------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                         | Descrição                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*&*<br/>       | \[no \] estado de amostra.<br/>                                         |
| <span id="t"></span><span id="T"></span>*t*<br/>       | \[nas \] coordenadas de textura.<br/>                                   |
| <span id="ddx"></span><span id="DDX"></span>*campo DDX*<br/> | \[em \] taxa de alteração da geometria da superfície na direção x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[em \] taxa de alteração da geometria da superfície na direção y.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O valor dos dados de textura.

## <a name="type-description"></a>Descrição do tipo



| Name | Entrada/saída | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| campo DDX  | in     | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| ddy  | in     | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| RET  | out    | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte                |
|-----------------------------------------------------------|--------------------------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sim (somente sombreador de pixel)  |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Sim (somente sombreador de pixel) |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Sim (somente sombreador de pixel) |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não                       |



 

1.  A reordenação de código significativa é feita para mover computações de gradiente fora do controle de fluxo.
2.  Se o limite de D3DPSHADERCAPS2 \_ 0 for definido com D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, o compilador mapeará essa função para texldd.

## <a name="remarks"></a>Comentários

Quando o controle de fluxo está presente em um sombreador, o resultado de um cálculo de gradiente solicitado dentro de um determinado caminho de ramificação é ambíguo quando os pixels adjacentes podem descer os caminhos de controle de fluxo separados. Portanto, é considerado ilegal usar qualquer operação de sombreador de pixel que solicite a ocorrência de um cálculo de gradiente em um local que esteja dentro de uma construção de controle de fluxo que pode variar em pixels para um determinado primitivo ser rasterizado. Se um dos lados de uma instrução **If** com o atributo Branch usar uma função de gradiente, um erro de compilador poderá ser gerado. Consulte a [instrução if (DirectX HLSL)](dx-graphics-hlsl-if.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

