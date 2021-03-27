---
title: D3DCOLORtoUBYTE4
description: Converte um ponto flutuante, um vetor de 4D definido por um D3DCOLOR para um UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499139"
---
# <a name="d3dcolortoubyte4"></a>D3DCOLORtoUBYTE4

Converte um ponto flutuante, um vetor de 4D definido por um D3DCOLOR para um UBYTE4.



| *RET* D3DCOLORtoUBYTE4 (*x*) |
|-----------------------------|



 

Essa função swizzles e dimensiona os componentes do parâmetro *x* . Use essa função para compensar a falta de suporte a UBYTE4 em alguns hardwares.

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] Vector4 de ponto flutuante a ser convertido.<br/> |



 

## <a name="return-value"></a>Valor Retornado

A representação UBYTE4 do parâmetro *x* .

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| *RET* | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**valores**](/windows/desktop/WinProg/windows-data-types)                      | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte |
|------------------------------------------------------------------------------------|-----------|
| [Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos | sim       |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

