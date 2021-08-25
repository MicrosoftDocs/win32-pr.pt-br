---
title: sincos
description: Retorna o seno e o cosseno de x.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- sincos HLSL
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff2854ea4c8b956298a65107136a963c5591b91de32d108b3179772bd0043a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673476"
---
# <a name="sincos"></a>sincos

Retorna o seno e o cosseno de x.



| sincos(*x*, out *s*, out *c*) |
|-------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[em \] O valor especificado, em radianos.<br/> |
| <span id="s"></span><span id="S"></span>*s*<br/> | \[out \] Retorna o seno de x.<br/>          |
| <span id="c"></span><span id="C"></span>*C*<br/> | \[out \] Retorna o cosseno de x.<br/>        |



 

## <a name="return-value"></a>Valor Retornado

Nenhum.

## <a name="type-description"></a>Descrição do tipo



| Nome | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*  | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vetor** ou **matriz** | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *s*  | mesmo que a entrada *x*                                                                                              | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões que a entrada *x* |
| c    | mesmo que a entrada *x*                                                                                              | [**Flutuar**](/windows/desktop/WinProg/windows-data-types)                        | mesmas dimensões que a entrada *x* |



 

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

 

