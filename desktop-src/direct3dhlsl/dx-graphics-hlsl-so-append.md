---
title: Append (objeto Stream-Output do DirectX HLSL)
description: Acrescente dados geometry-Shader-output a um fluxo existente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97ab88961b22529accb4402fc2bd095ede5275c1
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104293642"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Append (objeto Stream-Output do DirectX HLSL)

Acrescente dados geometry-Shader-output a um fluxo existente.



|                            |
|----------------------------|
| Append ( *StreamDataType*); |



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                             | Descrição                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**<br/> | Uma descrição de entrada de dados. Essa descrição deve corresponder ao parâmetro de modelo de objeto de fluxo chamado [DataType](dx-graphics-hlsl-so-type.md).<br/> |



 

## <a name="return-value"></a>Valor Retornado

Nenhum

## <a name="example"></a>Exemplo

Este trecho de código (do [exemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) mostra um exemplo parcial de como acrescentar primitivos de faixa de triângulo a um objeto Stream-output.


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fluxo-objeto de saída](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





