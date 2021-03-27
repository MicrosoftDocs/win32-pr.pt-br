---
title: Como criar um sombreador envoltória
description: Este tópico mostra como criar um sombreador envoltória.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635129"
---
# <a name="how-to-create-a-hull-shader"></a><span data-ttu-id="223b5-103">Como: criar um sombreador envoltória</span><span class="sxs-lookup"><span data-stu-id="223b5-103">How To: Create a Hull Shader</span></span>

<span data-ttu-id="223b5-104">Um sombreador envoltória é o primeiro de três estágios que trabalham juntos para implementar o [mosaico](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="223b5-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="223b5-105">As saídas do envoltória-Shader direcionam o estágio Tessellator, bem como o estágio Domain-Shader.</span><span class="sxs-lookup"><span data-stu-id="223b5-105">The hull-shader outputs drive the tessellator stage, as well as the domain-shader stage.</span></span> <span data-ttu-id="223b5-106">Este tópico mostra como criar um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="223b5-106">This topic shows how to create a hull shader.</span></span>

<span data-ttu-id="223b5-107">Um sombreador envoltória transforma um conjunto de pontos de controle de entrada (de um sombreador de vértice) em um conjunto de pontos de controle de saída.</span><span class="sxs-lookup"><span data-stu-id="223b5-107">A hull shader transforms a set of input control points (from a vertex shader) into a set of output control points.</span></span> <span data-ttu-id="223b5-108">O número de pontos de entrada e saída pode variar no conteúdo e no número, dependendo da transformação (uma transformação típica seria uma transformação base).</span><span class="sxs-lookup"><span data-stu-id="223b5-108">The number of input and output points can vary in contents and number depending on the transform (a typical transformation would be a basis transformation).</span></span>

<span data-ttu-id="223b5-109">Um sombreador envoltória também gera informações constantes de patch, como fatores de mosaico, para um sombreador de domínio e o Tessellator.</span><span class="sxs-lookup"><span data-stu-id="223b5-109">A hull shader also outputs patch constant information, such as tessellation factors, for a domain shader and the tessellator.</span></span> <span data-ttu-id="223b5-110">O estágio Tessellator de função fixa usa os fatores de mosaico, bem como outro Estado declarado em um sombreador envoltória para determinar o quanto a incluí.</span><span class="sxs-lookup"><span data-stu-id="223b5-110">The fixed-function tessellator stage uses the tessellation factors as well as other state declared in a hull shader to determine how much to tessellate.</span></span>

<span data-ttu-id="223b5-111">**Para criar um sombreador envoltória**</span><span class="sxs-lookup"><span data-stu-id="223b5-111">**To create a hull shader**</span></span>

1.  <span data-ttu-id="223b5-112">Criar um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="223b5-112">Design a hull shader.</span></span> <span data-ttu-id="223b5-113">Consulte [como: criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="223b5-113">See [How To: Design a Hull Shader](direct3d-11-advanced-stages-hull-shader-design.md).</span></span>
2.  <span data-ttu-id="223b5-114">Compilar o código do sombreador</span><span class="sxs-lookup"><span data-stu-id="223b5-114">Compile the shader code</span></span>
3.  <span data-ttu-id="223b5-115">Crie um objeto envoltória-Shader usando [**ID3D11Device:: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span><span class="sxs-lookup"><span data-stu-id="223b5-115">Create a hull-shader object using [**ID3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span></span>
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  <span data-ttu-id="223b5-116">Inicialize o estágio do pipeline usando [**ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="223b5-116">Initialize the pipeline stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="223b5-117">Um sombreador de domínio deve ser associado ao pipeline se um sombreador envoltória estiver associado.</span><span class="sxs-lookup"><span data-stu-id="223b5-117">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="223b5-118">Em particular, não é válido transmitir diretamente pontos de controle do sombreador envoltória com o sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="223b5-118">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="223b5-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="223b5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="223b5-120">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="223b5-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="223b5-121">Visão geral do mosaico</span><span class="sxs-lookup"><span data-stu-id="223b5-121">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




