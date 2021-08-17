---
title: GetRenderTargetSampleCount
description: Obtém o número de amostras de um destino de renderização.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- GetRenderTargetSampleCount HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54414d7af326c1a069585f9d5deaa3e728d421a65490c5b9f5322b98e06f531e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120130"
---
# <a name="getrendertargetsamplecount"></a>GetRenderTargetSampleCount

Obtém o número de amostras de um destino de renderização.



| *Uint* GetRenderTargetSampleCount() |
|-------------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                 | Descrição |
|--------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>None<br/> |             |



 

## <a name="return-value"></a>Valor Retornado

O número de amostras.

## <a name="remarks"></a>Comentários

Use essa função e [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) para descobrir o número e a posição dos locais de amostragem para um destino de renderização.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | não        |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





