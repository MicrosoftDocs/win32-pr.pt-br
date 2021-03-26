---
title: Round (Corecrt \_ Math. h)
description: Arredonda o valor especificado para o número inteiro mais próximo.
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- arredondar HLSL
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
ms.openlocfilehash: f00bf845dfe16a92729b523fba62f6fd6dcde2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930636"
---
# <a name="round"></a>round

Arredonda o valor especificado para o número inteiro mais próximo. Os casos intermediários são arredondados para o mais próximo mesmo.



| *ida e* volta (*x*) |
|------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[no \] valor especificado.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O parâmetro *x* , arredondado para o número inteiro mais próximo dentro de um tipo de ponto flutuante.

## <a name="type-description"></a>Descrição do tipo



| Name  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz** | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *RET* | igual ao *x* de entrada                                                                                              | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões como entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos | sim                 |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Sim ( \_ apenas vs 1 \_ 1) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

