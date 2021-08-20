---
title: tex1Dlod
description: Amostras de uma textura 1D com mipmaps. O LOD mipmap é especificado em t.w.
ms.assetid: f1700ee6-2f79-4b8b-ad34-30561f319356
keywords:
- tex1Dlod HLSL
topic_type:
- apiref
api_name:
- tex1Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e339e7e9383715a125075fcef619ab0d9846c63c809a08781e2e154e93127022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090551"
---
# <a name="tex1dlod"></a>tex1Dlod

Amostras de uma textura 1D com mipmaps. O LOD mipmap é especificado em t.w.



| RET tex1Dlod (s, t) |
|--------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*&*<br/> | \[no \] estado de amostra.<br/>      |
| <span id="t"></span><span id="T"></span>*t*<br/> | \[na \] coordenada de textura.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O valor dos dados de textura.

## <a name="type-description"></a>Descrição do tipo



| Nome | Entrada/saída | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler1D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| RET  | out    | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte               |
|-----------------------------------------------------------|-------------------------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sim (somente sombreador de pixel) |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Sim (somente sombreador de pixel) |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não                      |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não                      |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

