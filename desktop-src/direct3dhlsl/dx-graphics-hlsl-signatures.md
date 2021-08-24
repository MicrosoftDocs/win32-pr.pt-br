---
title: Assinaturas
description: Uma assinatura de sombreador é uma lista dos parâmetros que são entrada ou saída de uma função de sombreador.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5631dbe473b2e3eea0abb525e58621faf9c5137dd5dc3d743bde53b0ae258f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789576"
---
# <a name="signatures"></a>Assinaturas

Uma assinatura de sombreador é uma lista dos parâmetros que são entrada ou saída de uma função de sombreador. No Direct3D 10, os estágios adjacentes compartilham efetivamente uma matriz de registro, em que o sombreador de saída (ou estágio de pipeline) grava dados em locais específicos na matriz de registro e o sombreador de entrada deve ler dos mesmos locais. A API usa assinaturas de sombreador para vincular saídas de sombreador com entradas sem a sobrecarga de resolução semântica.

No Direct3D 10, as assinaturas de entrada são geradas de uma declaração de entrada do sombreador e a assinatura de saída é gerada de uma declaração de saída do sombreador. É dito que uma assinatura de entrada é compatível com uma assinatura de saída quando a assinatura de saída é um subconjunto estrito (tipo de argumento e combinação de ordem) da assinatura de entrada. A maneira mais simples de fazer isso é vincular entradas e saídas de sombreador correspondentes pelo mesmo tipo de estrutura.

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



Aqui está um exemplo de assinaturas incompatíveis; A ordem dos parâmetros na assinatura de entrada não corresponderá à ordem na assinatura de saída.


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



PSInWorks é um subconjunto compatível do VSOut (as duas primeiras entradas são compatíveis com o tipo e a ordem com as duas primeiras entradas no VSOut). No entanto, PSInFails é incompatível porque a ordenação não é compatível com VSOut.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




