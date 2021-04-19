---
title: refract
description: Retorna um vetor de refração usando uma entrada Ray, uma superfície normal e um índice refracionário.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- refract HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988705"
---
# <a name="refract"></a>refract

Retorna um vetor de refração usando uma entrada Ray, uma superfície normal e um índice refracionário.



| *RET* refract (*i*, *n*,?) |
|----------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*Encontrei*<br/> | \[em \] um ponto flutuante, vetor de direção de raio.<br/>    |
| <span id="n"></span><span id="N"></span>*p*<br/> | \[em \] um ponto flutuante, vetor normal de superfície.<br/>   |
| *?*<br/>                                         | \[em \] um ponto flutuante, refração do índice escalar.<br/> |



 

## <a name="return-value"></a>Valor Retornado

Um vetor de ponto flutuante, refração. Se o ângulo entre a inserção de Ray i e a superfície normal n for muito grande para um determinado índice de refração?, o valor de retorno será (0, 0, 0).

## <a name="type-description"></a>Descrição do tipo



| Name              | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*               | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*               | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesma dimensão (s) como entrada *i* |
| ?                 | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |
| vetor de refração | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | mesma dimensão (s) como entrada *i* |



 

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

 

