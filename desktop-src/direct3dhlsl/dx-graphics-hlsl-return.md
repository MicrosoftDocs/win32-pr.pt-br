---
title: Instrução Return
description: Uma instrução return sinaliza o final de uma função.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- Instrução de retorno HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 525abf6d815d2073ee39a6bc6a5a81120cf652ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104967061"
---
# <a name="return-statement"></a>Instrução Return

Uma instrução return sinaliza o final de uma função.



|                   |
|-------------------|
| valor de retorno \[ \] ; |



 

A instrução de retorno mais simples retorna o controle da função para o programa de chamada; Ele não retorna nenhum valor.


```
void main()
{
    return ;
}
```



No entanto, uma instrução return pode retornar um ou mais valores. Este exemplo retorna um valor literal:


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



Este exemplo retorna um vetor de quatro componentes que é construído a partir de uma variável local e um literal.


```
return  float4(color.rgb, 1) ;
```



Este exemplo retorna um vetor de quatro componentes que é construído a partir do resultado retornado por uma função intrínseca, junto com valores literais.


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

 

 




