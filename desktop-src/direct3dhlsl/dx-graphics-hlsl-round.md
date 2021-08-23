---
title: round (Corecrt \_ math.h)
description: Arredoda o valor especificado para o inteiro mais próximo.
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- round HLSL
topic_type:
- apiref
api_name:
- round
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3997e93dbbe7cfda210fea97a2759620f0afb47638d2ec519b9ad56abe3664c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513828"
---
# <a name="round"></a>round

Arredoda o valor especificado para o inteiro mais próximo. Os casos na metade são arredondados para o mais próximo.



| *ret* round(*x*) |
|------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[em \] O valor especificado.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O *parâmetro x,* arredondado para o inteiro mais próximo dentro de um tipo de ponto flutuante.

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

