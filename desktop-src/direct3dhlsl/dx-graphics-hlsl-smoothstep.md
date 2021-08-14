---
title: smoothstep
description: Retorna uma interpolação de Hermite suave entre 0 e 1, se x estiver no intervalo \ min, max\ .
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
ms.openlocfilehash: 5416dab57fc77f7b664518afcb0f4623875fd2a660f7d1aff82ab42f2c297b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513785"
---
# <a name="smoothstep"></a>smoothstep

Retorna uma interpolação de Hermite suave entre 0 e 1, se *x* estiver no intervalo \[ *mínimo*, *máx.* \]



| *ret* smoothstep(*min*, *max*, *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                         | Descrição                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*Min*<br/> | \[em \] O intervalo mínimo do parâmetro *x.*<br/> |
| <span id="max"></span><span id="MAX"></span>*Max*<br/> | \[em \] O intervalo máximo do parâmetro *x.*<br/> |
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[em \] O valor especificado a ser interpolado.<br/> |



 

## <a name="return-value"></a>Valor Retornado

Retornará 0 se *x* for menor que *mín.* 1 se *x* for maior que *o máximo*; caso contrário, um valor entre 0 e 1 *se x* estiver no intervalo \[ *min*, *máx.* \]

## <a name="remarks"></a>Comentários

Use a **função intrínseca** HLSL smoothstep para criar uma transição suave entre dois valores. Por exemplo, você pode usar essa função para combinar duas cores sem problemas.

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vetor** ou **matriz** | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *min* | mesmo que a entrada *x*                                                                                              | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões que a entrada *x* |
| *max* | mesmo que a entrada *x*                                                                                              | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões que a entrada *x* |
| *Ret* | mesmo que a entrada *x*                                                                                              | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões que a entrada *x* |



 

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

 

