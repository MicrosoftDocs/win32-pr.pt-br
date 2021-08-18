---
title: Iluminado
description: Retorna um vetor de coeficiente de iluminação.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- HLSL com luz
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d3f941fe3aad52f352f5a36d3642141b31e08ef00c25dd8687c8fc7a8ed2de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791612"
---
# <a name="lit"></a>Iluminado

Retorna um vetor de coeficiente de iluminação.



| *ret* lit(*n \_ dot \_ l*, *n dot \_ \_ h*, *m*) |
|------------------------------------------|



 

Essa função retorna um vetor de coeficiente de iluminação (ambiente, difuso, especular, 1) em que:

-   ambiente = 1
-   difuso = n · l < 0 ? 0: n · L
-   specular = n · l < 0 \| \| n · h < 0 ? 0: (n · h) ^ m

Quando o vetor n é o vetor normal, l é a direção para a luz e h é o meio vetor.

## <a name="parameters"></a>Parâmetros



| Item                                                                       | Descrição                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ dot \_ l*<br/> | \[em \] O produto de ponto da superfície normalizada e o vetor de luz.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ dot \_ h*<br/> | \[em \] O produto de ponto do vetor de meio ângulo e da superfície normal.<br/>       |
| <span id="m"></span><span id="M"></span>*M*<br/>                     | \[em \] Um expoente especular.<br/>                                                   |



 

## <a name="return-value"></a>Valor Retornado

O vetor do coeficiente de iluminação.

## <a name="type-description"></a>Descrição do tipo



| Nome        | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ dot \_ l* | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ dot \_ h* | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *Ret*       | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                       | Com suporte           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador superior | sim                 |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sim (somente \_ versus \_ 1 1) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

