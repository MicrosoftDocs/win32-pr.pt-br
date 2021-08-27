---
title: tan
description: Retorna a tangente do valor especificado.
ms.assetid: ca03b184-9e1a-4152-9292-f8af38aa9423
keywords:
- tan HLSL
topic_type:
- apiref
api_name:
- tan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1abdf0ea751064b6fdfcc73983490f61580a2f4aeb369ab4a096ea8e5d4791fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068126"
---
# <a name="tan"></a>tan

Retorna a tangente do valor especificado.



| *ret* tan(*x*) |
|----------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[em \] O valor especificado, em radianos.<br/> |



 

## <a name="return-value"></a>Valor Retornado

A tangente do *parâmetro x.*

## <a name="type-description"></a>Descrição do tipo



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vetor** ou **matriz** | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
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

 

