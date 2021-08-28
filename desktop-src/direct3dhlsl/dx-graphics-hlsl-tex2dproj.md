---
title: tex2Dproj
description: Amostras de uma textura 2D usando uma divisão projetiva; a coordenada de textura é dividida por t.w antes que a lookup seja realizada.
ms.assetid: c6b79360-3737-4b74-bdf3-6d46323e8e54
keywords:
- HLSL do tex2Dproj
topic_type:
- apiref
api_name:
- tex2Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 928e216f7ae25bd13722a4f432d9d37ca41e0665cc9f1b50158c02386027d4e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789406"
---
# <a name="tex2dproj"></a>tex2Dproj

Amostras de uma textura 2D usando uma divisão projetiva; a coordenada de textura é dividida por t.w antes que a lookup seja realizada.



| ret tex2Dproj(s, t) |
|---------------------|



 

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
| s    | in     | [**Objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
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

 

