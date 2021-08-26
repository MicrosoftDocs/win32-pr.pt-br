---
title: asfloat
description: Interpreta o padrão de bit de x como um número de ponto flutuante.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- asfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 901b64099547060305bab6db43cbe75b3fdb8d9c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886262"
---
# <a name="asfloat"></a>asfloat

Interpreta o padrão de bit *de x como* um número de ponto flutuante.



| ret asfloat(*x*) |
|------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[em \] O valor de entrada.<br/> |



 

## <a name="return-value"></a>Valor Retornado

A entrada interpretada como um número de ponto flutuante.

## <a name="type-description"></a>Descrição do tipo



| Nome  | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Tamanho                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vetor** ou **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *Ret* | mesmo que a entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                                                                                | mesmas dimensões que a entrada *x* |



 

## <a name="function-overloads"></a>Sobrecargas de função

<dl> `float&lt;x&gt; asfloat(float&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(int&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(uint&lt;x&gt; value);`  
</dl>

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador superior | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | não        |



 

## <a name="remarks"></a>Comentários

Compiladores mais antigos permitiam incorretamente , mas observe que não há suporte `asfloat(bool)` para entradas bool.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

