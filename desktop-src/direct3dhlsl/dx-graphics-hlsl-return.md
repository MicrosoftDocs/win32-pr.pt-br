---
title: Instrução Return
description: Uma instrução de retorno sinaliza o fim de uma função.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- return Statement HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876c69f3ecfcf1ee1c8391ccc503b2316056b37a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119581"
---
# <a name="return-statement"></a>Instrução Return

Uma instrução de retorno sinaliza o fim de uma função.

valor \[ de retorno \] ;



 

A instrução return mais simples retorna o controle da função para o programa de chamada; ele não retorna nenhum valor.


```
void main()
{
    return ;
}
```



No entanto, uma instrução de retorno pode retornar um ou mais valores. Este exemplo retorna um valor literal:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



Este exemplo retorna o resultado escalar de uma expressão.


```
return  light.enabled = true ;
```



Este exemplo retorna um vetor de quatro componentes que é construído de uma variável local e um literal.


```
return  float4(color.rgb, 1) ;
```



Este exemplo retorna um vetor de quatro componentes que é construído a partir do resultado retornado de uma função intrínseca, junto com valores literais.


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



Este exemplo retorna uma estrutura que contém um ou mais membros.


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




