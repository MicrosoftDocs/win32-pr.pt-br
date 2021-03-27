---
title: reflexão
description: Retorna um vetor de reflexo usando um incidente Ray e uma superfície normal.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- refletir HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641756"
---
# <a name="reflect"></a>reflexão

Retorna um vetor de reflexo usando um incidente Ray e uma superfície normal.



| *RET* refletir (*i*, *n*) |
|-------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*Encontrei*<br/> | \[em \] um ponto flutuante, vetor de incidente.<br/> |
| <span id="n"></span><span id="N"></span>*p*<br/> | \[em \] um ponto flutuante, vetor normal.<br/>   |



 

## <a name="return-value"></a>Valor Retornado

Um vetor de ponto flutuante, reflexo.

## <a name="remarks"></a>Comentários

Essa função calcula o vetor de reflexo usando a seguinte fórmula: v = i-2 \* n \* ponto (i n).

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*   | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesma dimensão (s) como entrada *i* |
| *RET* | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesma dimensão (s) como entrada *i* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte |
|------------------------------------------------------------------------------------|-----------|
| [Modelo do sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelos de sombreador mais altos | sim       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

