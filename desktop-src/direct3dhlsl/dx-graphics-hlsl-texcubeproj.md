---
title: texCUBEproj
description: Amostras de uma textura de cubo usando uma divisão projetiva; a coordenada de textura é dividida por t.w antes que a lookup seja realizada.
ms.assetid: 86bdd1c3-0a8d-4d09-b70d-1ebcee32c866
keywords:
- HLSL de texCUBEproj
topic_type:
- apiref
api_name:
- texCUBEproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aacc393080d06d8f6f72e4a55cc17f2d276f47174cbbb9e9b2fe495e27e7a749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725464"
---
# <a name="texcubeproj"></a>texCUBEproj

Amostras de uma textura de cubo usando uma divisão projetiva; a coordenada de textura é dividida por t.w antes que a lookup seja realizada.



| ret texCUBEproj(s, t) |
|-----------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[em \] O estado do exemplo.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[na \] coordenada de textura.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O valor dos dados de textura.

## <a name="type-description"></a>Descrição do tipo



| Nome | Entrada/saída | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [samplerCUBE](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | out    | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte               |
|-----------------------------------------------------------|-------------------------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim (somente sombreador de pixel) |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sim (somente sombreador de pixel) |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sim (somente sombreador de pixel) |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não                      |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

