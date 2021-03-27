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
# <a name="signatures"></a><span data-ttu-id="dedab-103">Assinaturas</span><span class="sxs-lookup"><span data-stu-id="dedab-103">Signatures</span></span>

<span data-ttu-id="dedab-104">Uma assinatura de sombreador é uma lista dos parâmetros que são de entrada ou de saída de uma função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dedab-104">A shader signature is a list of the parameters that are either input to or output from a shader function.</span></span> <span data-ttu-id="dedab-105">No Direct3D 10, os estágios adjacentes compartilham efetivamente uma matriz de registro, em que o sombreador de saída (ou estágio de pipeline) grava dados em locais específicos na matriz de registro e o sombreador de entrada deve ler dos mesmos locais.</span><span class="sxs-lookup"><span data-stu-id="dedab-105">In Direct3D 10, adjacent stages effectively share a register array, where the output shader (or pipeline stage) writes data to specific locations in the register array and the input shader must read from the same locations.</span></span> <span data-ttu-id="dedab-106">A API usa assinaturas de sombreador para associar saídas de sombreador com entradas sem a sobrecarga de resolução semântica.</span><span class="sxs-lookup"><span data-stu-id="dedab-106">The API uses shader signatures to bind shader outputs with inputs without the overhead of semantic resolution.</span></span>

<span data-ttu-id="dedab-107">No Direct3D 10, as assinaturas de entrada são geradas de uma declaração de entrada de sombreador e a assinatura de saída é gerada a partir de uma declaração de saída de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dedab-107">In Direct3D 10, input signatures are generated from a shader-input declaration and the output signature is generated from a shader-output declaration.</span></span> <span data-ttu-id="dedab-108">Uma assinatura de entrada é considerada compatível com uma assinatura de saída quando a assinatura de saída é um subconjunto estrito (tipo de argumento e correspondência de ordem) da assinatura de entrada.</span><span class="sxs-lookup"><span data-stu-id="dedab-108">An input signature is said to be compatible with an output signature when the output signature is a strict subset (argument type and order match) of the input signature.</span></span> <span data-ttu-id="dedab-109">A maneira mais direta de conseguir isso é vincular entradas e saídas de sombreador correspondentes pelo mesmo tipo de estrutura.</span><span class="sxs-lookup"><span data-stu-id="dedab-109">The most straightforward way to achieve this is to link corresponding shader inputs and outputs by the same structure type.</span></span>

<span data-ttu-id="dedab-110">Aqui está um exemplo de assinaturas compatíveis.</span><span class="sxs-lookup"><span data-stu-id="dedab-110">Here is an example of compatible signatures.</span></span>


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



<span data-ttu-id="dedab-111">Aqui está um exemplo de assinaturas incompatíveis; a ordem dos parâmetros na assinatura de entrada não corresponde à ordem na assinatura de saída.</span><span class="sxs-lookup"><span data-stu-id="dedab-111">Here is an example of incompatible signatures; the order of parameters in the input signature does not match the order in the output signature.</span></span>


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



<span data-ttu-id="dedab-112">PSInWorks é um subconjunto compatível de VSOut (as duas primeiras entradas correspondem ao tipo e à ordem com as duas primeiras entradas no VSOut).</span><span class="sxs-lookup"><span data-stu-id="dedab-112">PSInWorks is a compatible subset of VSOut (the first two entries match both type and order with the first two entries in VSOut).</span></span> <span data-ttu-id="dedab-113">No entanto, PSInFails é incompatível porque a ordenação não corresponde a VSOut.</span><span class="sxs-lookup"><span data-stu-id="dedab-113">However, PSInFails is incompatible because the ordering does not match with VSOut.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dedab-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dedab-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dedab-115">Funções</span><span class="sxs-lookup"><span data-stu-id="dedab-115">Functions</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




