---
title: smoothstep
description: Retorna uma interpolação de Hermite suave entre 0 e 1, se x estiver no intervalo de \ min, máx.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- smoothstep HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967180"
---
# <a name="smoothstep"></a>smoothstep

Retorna uma interpolação de Hermite suave entre 0 e 1, se *x* estiver no intervalo \[ *mín*., *máx* \] .



| *RET* smoothstep (*mín*., *máx*. *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                         | Descrição                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*min*<br/> | \[no \] intervalo mínimo do parâmetro *x* .<br/> |
| <span id="max"></span><span id="MAX"></span>*maximizar*<br/> | \[no \] intervalo máximo do parâmetro *x* .<br/> |
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/>       | \[no \] valor especificado a ser interpolado.<br/> |



 

## <a name="return-value"></a>Valor Retornado

Retornará 0 se *x* for menor que *mín*; 1 se *x* for maior que *Max*; caso contrário, um valor entre 0 e 1 se *x* está no intervalo \[ *mín*., *máx* \] .

## <a name="remarks"></a>Comentários

Use a função intrínseca **smoothstep** HLSL para criar uma transição suave entre dois valores. Por exemplo, você pode usar essa função para misturar duas cores suavemente.

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *min* | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |
| *max* | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |
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

 

