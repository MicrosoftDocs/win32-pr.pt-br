---
title: modf (Corecrt \_ math.h)
description: Divide o valor x em partes fracionadas e inteiras, cada uma das quais tem o mesmo sinal que x.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- modf HLSL
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c09af44cb95f35854d4366c05d238423fcecaff7c9a10c3c55fadf6b51dd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513807"
---
# <a name="modf"></a>modf

Divide o valor x em partes fracionadas e inteiras, cada uma das quais tem o mesmo sinal que x.



| ret modf(x, out ip) |
|---------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                      | Descrição                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>    | \[no \] valor de entrada x.<br/>           |
| <span id="ip"></span><span id="IP"></span>*Ip*<br/> | \[out \] A parte inteira de *x*.<br/> |



 

## <a name="return-value"></a>Valor Retornado

A parte fracionada com assinatura de x.

## <a name="type-description"></a>Descrição do tipo



| Nome | Entrada/saída | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Tamanho                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in     | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vetor** ou **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| ip   | out    | mesmo que a entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões que a entrada x |
| Ret  | out    | mesmo que a entrada x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões que a entrada x |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                       | Com suporte           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador superior | sim                 |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sim (somente \_ versus \_ 1 1) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

