---
title: Assinaturas
description: Uma assinatura de sombreador é uma lista dos parâmetros que são de entrada ou de saída de uma função de sombreador.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988527"
---
# <a name="signatures"></a>Assinaturas

Uma assinatura de sombreador é uma lista dos parâmetros que são de entrada ou de saída de uma função de sombreador. No Direct3D 10, os estágios adjacentes compartilham efetivamente uma matriz de registro, em que o sombreador de saída (ou estágio de pipeline) grava dados em locais específicos na matriz de registro e o sombreador de entrada deve ler dos mesmos locais. A API usa assinaturas de sombreador para associar saídas de sombreador com entradas sem a sobrecarga de resolução semântica.

No Direct3D 10, as assinaturas de entrada são geradas de uma declaração de entrada de sombreador e a assinatura de saída é gerada a partir de uma declaração de saída de sombreador. Uma assinatura de entrada é considerada compatível com uma assinatura de saída quando a assinatura de saída é um subconjunto estrito (tipo de argumento e correspondência de ordem) da assinatura de entrada. A maneira mais direta de conseguir isso é vincular entradas e saídas de sombreador correspondentes pelo mesmo tipo de estrutura.

Aqui está um exemplo de assinaturas compatíveis.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



Aqui está um exemplo de assinaturas incompatíveis; a ordem dos parâmetros na assinatura de entrada não corresponde à ordem na assinatura de saída.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



PSInWorks é um subconjunto compatível de VSOut (as duas primeiras entradas correspondem ao tipo e à ordem com as duas primeiras entradas no VSOut). No entanto, PSInFails é incompatível porque a ordenação não corresponde a VSOut.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




