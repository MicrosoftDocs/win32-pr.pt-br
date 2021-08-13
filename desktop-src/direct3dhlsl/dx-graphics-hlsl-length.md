---
title: comprimento
description: Retorna o comprimento do vetor de ponto flutuante especificado.
ms.assetid: eb06c87c-d536-448e-becb-762783cc2a77
keywords:
- comprimento HLSL
topic_type:
- apiref
api_name:
- length
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d6c361a7ad16216d686ab71747354a9b1ba3184d88759ed1e994c152c7b3636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791722"
---
# <a name="length"></a>comprimento

Retorna o comprimento do vetor de ponto flutuante especificado.



| *ret* length(*x*) |
|-------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | O vetor de ponto flutuante especificado.<br/> |



 

## <a name="return-value"></a>Valor Retornado

Um escalar de ponto flutuante que representa o comprimento do *parâmetro x.*

## <a name="type-description"></a>Descrição do tipo



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**Vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | any  |
| *Ret* | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

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

 

