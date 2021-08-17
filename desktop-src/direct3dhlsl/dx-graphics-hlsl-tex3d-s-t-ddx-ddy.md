---
title: tex3D (referência de HLSL) – Selecione o nível mip
description: Amostra uma textura 3D usando um gradiente para selecionar o nível mip. | tex3D (referência HLSL)
ms.assetid: b48a6791-61b7-4a13-9357-923910515164
keywords:
- HLSL do texas3D
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 099d521f803850079235b77aa8f4eb70162882940bcf286a77f02773f355e76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119890"
---
# <a name="tex3d-hlsl-reference---select-the-mip-level"></a>tex3D (referência de HLSL) – Selecione o nível mip

Amostra uma textura 3D usando um gradiente para selecionar o nível mip.



| ret tex3D(s, t, ddx, ddy) |
|---------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                         | Descrição                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[em \] O estado do exemplo.<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[na \] coordenada de textura.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[em \] Taxa de alteração da geometria da superfície na direção x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*Ddy*<br/> | \[em \] Taxa de alteração da geometria da superfície na direção y.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O valor dos dados de textura.

## <a name="type-description"></a>Descrição do tipo



| Nome | Entrada/saída | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ddx  | in     | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ddy  | in     | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
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

 

