---
title: Como criar um sombreador de domínio
description: Este tópico mostra como criar um sombreador de domínio.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005043"
---
# <a name="how-to-create-a-domain-shader"></a><span data-ttu-id="3978f-103">Como: criar um sombreador de domínio</span><span class="sxs-lookup"><span data-stu-id="3978f-103">How To: Create a Domain Shader</span></span>

<span data-ttu-id="3978f-104">Um sombreador de domínio é o terceiro de três estágios que trabalham em conjunto para implementar o [mosaico](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="3978f-104">A domain shader is the third of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="3978f-105">As entradas para o estágio de sombreador de domínio vêm de um sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="3978f-105">The inputs for the domain-shader stage come from a hull shader.</span></span> <span data-ttu-id="3978f-106">Este tópico mostra como criar um sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="3978f-106">This topic shows how to create a domain shader.</span></span>

<span data-ttu-id="3978f-107">Um sombreador de domínio transforma a geometria da superfície (criada pelo estágio de Tessellator da função fixa) usando pontos de controle de saída do sombreador envoltória, patch de saída do sombreador envoltória-dados constantes e um único conjunto de coordenadas Tessellator UV.</span><span class="sxs-lookup"><span data-stu-id="3978f-107">A domain shader transforms surface geometry (created by the fixed-function tessellator stage) using hull shader output-control points, hull shader output patch-constant data, and a single set of tessellator uv coordinates.</span></span>

<span data-ttu-id="3978f-108">**Para criar um sombreador de domínio**</span><span class="sxs-lookup"><span data-stu-id="3978f-108">**To create a domain shader**</span></span>

1.  <span data-ttu-id="3978f-109">Criar um sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="3978f-109">Design a domain shader.</span></span> <span data-ttu-id="3978f-110">Consulte [como: criar um sombreador de domínio](direct3d-11-advanced-stages-domain-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="3978f-110">See [How To: Design a Domain Shader](direct3d-11-advanced-stages-domain-shader-design.md).</span></span>
2.  <span data-ttu-id="3978f-111">Compile o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="3978f-111">Compile the shader code.</span></span>
3.  <span data-ttu-id="3978f-112">Crie um objeto de sombreador de domínio usando [**ID3D11Device:: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span><span class="sxs-lookup"><span data-stu-id="3978f-112">Create a domain-shader object using [**ID3D11Device::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span></span>
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  <span data-ttu-id="3978f-113">Inicialize o estágio do pipeline usando [**ID3D11DeviceContext::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span><span class="sxs-lookup"><span data-stu-id="3978f-113">Initialize the pipeline stage using [**ID3D11DeviceContext::DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span></span>
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="3978f-114">Um sombreador de domínio deve ser associado ao pipeline se um sombreador envoltória estiver associado.</span><span class="sxs-lookup"><span data-stu-id="3978f-114">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="3978f-115">Em particular, não é válido transmitir diretamente pontos de controle do sombreador envoltória com o sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="3978f-115">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3978f-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3978f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3978f-117">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3978f-117">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="3978f-118">Visão geral do mosaico</span><span class="sxs-lookup"><span data-stu-id="3978f-118">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




