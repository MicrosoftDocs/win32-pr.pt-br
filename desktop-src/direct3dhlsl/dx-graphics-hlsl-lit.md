---
title: aceso
description: Retorna um vetor de coeficiente de iluminação.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- HLSL aceso
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823777"
---
# <a name="lit"></a>aceso

Retorna um vetor de coeficiente de iluminação.



| *RET* aceso (*n \_ ponto \_ l*, *n \_ ponto \_ h*, *m*) |
|------------------------------------------|



 

Essa função retorna um vetor de coeficiente de iluminação (ambiente, difuso, especular, 1) em que:

-   ambiente = 1
-   difuso = n · l < 0? 0: n · debug
-   especular = n · l < 0 \| \| n · h < 0? 0: (n · h) ^ m

Onde o vetor n é o vetor normal, l é a direção para acender e h é a metade do vetor.

## <a name="parameters"></a>Parâmetros



| Item                                                                       | Descrição                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ ponto \_ l*<br/> | \[no \] produto de ponto da superfície normalizada normal e do vetor claro.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ ponto \_ h*<br/> | \[no \] produto de ponto do vetor de metade do ângulo e na superfície normal.<br/>       |
| <span id="m"></span><span id="M"></span>*d*<br/>                     | \[em \] um expoente especular.<br/>                                                   |



 

## <a name="return-value"></a>Valor Retornado

O vetor de coeficiente de iluminação.

## <a name="type-description"></a>Descrição do tipo



| Name        | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ ponto \_ l* | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ ponto \_ h* | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *RET*       | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

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

 

