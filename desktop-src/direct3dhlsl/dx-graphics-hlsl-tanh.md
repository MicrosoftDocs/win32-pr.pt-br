---
title: tanh
description: Retorna a tangente hiperbólica do valor especificado.
ms.assetid: e2d27aa0-5e03-4f2f-a29c-884711710c8d
keywords:
- Tanh HLSL
topic_type:
- apiref
api_name:
- tanh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a680863cd8aa4c46a74dc4a4d332ce893dc8bbcb2b46589af3ad35acb15e172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725694"
---
# <a name="tanh"></a>tanh

Retorna a tangente hiperbólica do valor especificado.



| Tanh de *RET* (*x*) |
|-----------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] valor especificado, em radianos.<br/> |



 

## <a name="return-value"></a>Valor Retornado

A tangente hiperbólica do parâmetro *x* .

## <a name="type-description"></a>Descrição do tipo



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *RET* | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |



 

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

 

