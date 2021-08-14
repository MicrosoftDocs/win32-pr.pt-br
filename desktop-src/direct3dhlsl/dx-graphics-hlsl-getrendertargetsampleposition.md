---
title: GetRenderTargetSamplePosition
description: Obtém a posição de amostragem (x,y) para um determinado índice de exemplo.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a406fcbd023d0688baf51cabbfea53438f3d58a6fba4d1fc7d1bf8d33077262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514330"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

Obtém a posição de amostragem (x,y) para um determinado índice de exemplo.

float<2> GetRenderTargetSamplePosition( int<1> Index<br/>);



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                       | Descrição                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Índice*<br/> | \[em \] Um índice de exemplo baseado em zero.<br/> |



 

## <a name="return-value"></a>Valor Retornado

A posição (x,y) do exemplo determinado.

## <a name="remarks"></a>Comentários

Use essa função e [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) para descobrir o número e a posição dos locais de amostragem para um destino de renderização.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador superior | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | não        |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





