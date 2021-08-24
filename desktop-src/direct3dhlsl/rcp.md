---
title: rcp
description: Calcula um recíproco rápido, aproximado por componente.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- rcp HLSL
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb66fd2edf543dfb8beaf23dd2105925d15d169ee1b134019fb54da8fdf889e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672216"
---
# <a name="rcp"></a>rcp

Calcula um recíproco rápido, aproximado por componente.



| *ret* rcp(*x*) |
|----------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

\[em \] O valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

O recíproco do *parâmetro x.*

## <a name="type-description"></a>Descrição do tipo



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                      | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vetor** ou **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types) ou [ **double**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *Ret* | mesmo que a entrada *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types) ou [ **double**](/windows/desktop/WinProg/windows-data-types) | mesmas dimensões que a entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 