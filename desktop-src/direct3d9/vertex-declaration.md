---
description: Uma declaração de vértice define o layout do buffer de vértice e programa o mecanismo de mosaico.
ms.assetid: 09dae498-3b33-4c33-bc7e-47f2bf784e4c
title: Declaração de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c769aa6fb80de1fd83067ebb9f32b591baa8e883
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105808220"
---
# <a name="vertex-declaration-direct3d-9"></a><span data-ttu-id="75374-103">Declaração de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="75374-103">Vertex Declaration (Direct3D 9)</span></span>

<span data-ttu-id="75374-104">Uma declaração de vértice define o layout do buffer de vértice e programa o mecanismo de mosaico.</span><span class="sxs-lookup"><span data-stu-id="75374-104">A vertex declaration defines the vertex buffer layout and programs the tessellation engine.</span></span> <span data-ttu-id="75374-105">A partir do Direct3D 9, os fluxos de vértice são expressos como uma matriz de estruturas [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) (em vez de usar códigos de formato de vértice flexível (FVF)).</span><span class="sxs-lookup"><span data-stu-id="75374-105">Starting with Direct3D 9, vertex streams are expressed as an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures (instead of using flexible vertex format (FVF) codes).</span></span> <span data-ttu-id="75374-106">Cada elemento da matriz descreve cada tipo de dados por vértice.</span><span class="sxs-lookup"><span data-stu-id="75374-106">Each array element describes each per-vertex data type.</span></span> <span data-ttu-id="75374-107">A conversão de códigos de> FVF no novo formato é abordada nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="75374-107">Converting FVF> codes into the new format is covered in the following topics:</span></span>

-   [<span data-ttu-id="75374-108">Mapeando códigos FVF para uma declaração do Direct3D 9 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="75374-108">Mapping FVF Codes to a Direct3D 9 Declaration (Direct3D 9)</span></span>](mapping-fvf-codes-to-a-directx-9-declaration.md)
-   [<span data-ttu-id="75374-109">Fixos códigos de FVF de função (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="75374-109">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
-   [<span data-ttu-id="75374-110">Mapeamento entre uma declaração de Direct3D e códigos de FVF (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="75374-110">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
-   [<span data-ttu-id="75374-111">Mapeamento entre uma declaração do Direct3D 9 e uma declaração do Direct3D 8 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="75374-111">Mapping between a Direct3D 9 Declaration and a Direct3D 8 Declaration (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-directx-8.md)
-   [<span data-ttu-id="75374-112">Programando um ou mais fluxos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="75374-112">Programming One or More Streams (Direct3D 9)</span></span>](programming-one-or-more-streams.md)

## <a name="related-topics"></a><span data-ttu-id="75374-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75374-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75374-114">Buffers de vértice</span><span class="sxs-lookup"><span data-stu-id="75374-114">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 



