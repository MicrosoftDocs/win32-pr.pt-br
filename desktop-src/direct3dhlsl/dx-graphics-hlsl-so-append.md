---
title: Anexar (objeto de Stream-Output DirectX HLSL)
description: Anexar dados geometry-shader-output a um fluxo existente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 956d4b2e37c4430e20fc4b75b2847c096c7832369d036f5224d8c36d86b7c66c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068166"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Anexar (objeto de Stream-Output DirectX HLSL)

Anexar dados geometry-shader-output a um fluxo existente.

Append( *StreamDataType*);



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                             | Descrição                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**<br/> | Uma descrição de entrada de dados. Essa descrição deve corresponder ao parâmetro de modelo stream-object chamado [DataType](dx-graphics-hlsl-so-type.md).<br/> |



 

## <a name="return-value"></a>Valor Retornado

Nenhum

## <a name="example"></a>Exemplo

Este snippet de código (da amostra [CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) mostra um exemplo parcial de primitivos de faixa de triângulos pendentes para um objeto de saída de fluxo.


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



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto Stream-Output](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





