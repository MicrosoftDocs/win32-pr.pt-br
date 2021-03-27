---
title: Como inicializar o estágio Tessellator
description: Este tópico mostra como inicializar o estágio Tessellator.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988498"
---
# <a name="how-to-initialize-the-tessellator-stage"></a><span data-ttu-id="d23e9-103">Como inicializar o estágio Tessellator</span><span class="sxs-lookup"><span data-stu-id="d23e9-103">How To: Initialize the Tessellator Stage</span></span>

<span data-ttu-id="d23e9-104">Em geral, o mosaico expande o modelo definido pelo usuário e compacto de um patch em geometria que contém uma quantidade de detalhes programável.</span><span class="sxs-lookup"><span data-stu-id="d23e9-104">In general, tessellation expands the compact, user-defined, model of a patch into geometry that contains a programmable amount of detail.</span></span> <span data-ttu-id="d23e9-105">A geometria normalmente é um conjunto de triângulos que representa a geometria de superfície detalhada.</span><span class="sxs-lookup"><span data-stu-id="d23e9-105">The geometry is typically a set of triangles that represents detailed surface geometry.</span></span> <span data-ttu-id="d23e9-106">Este tópico mostra como inicializar o estágio Tessellator.</span><span class="sxs-lookup"><span data-stu-id="d23e9-106">This topic shows how to initialize the tessellator stage.</span></span>

<span data-ttu-id="d23e9-107">O estágio Tessellator é o segundo de três estágios que trabalham em conjunto para incluí ou peça uma superfície.</span><span class="sxs-lookup"><span data-stu-id="d23e9-107">The tessellator stage is the second of three stages that work together to tessellate or tile a surface.</span></span> <span data-ttu-id="d23e9-108">O primeiro estágio é o estágio envoltória-Shader; Ele opera uma vez por patch e configura como o próximo estágio (a função fixa Tessellator) se comporta.</span><span class="sxs-lookup"><span data-stu-id="d23e9-108">The first stage is the hull-shader stage; it operates once per patch and configures how the next stage (the fixed function tessellator) behaves.</span></span> <span data-ttu-id="d23e9-109">Um sombreador envoltória também gera saídas definidas pelo usuário, como pontos de controle de saída e constantes de patch que são enviadas após o Tessellator diretamente para o terceiro estágio, o estágio Domain-Shader.</span><span class="sxs-lookup"><span data-stu-id="d23e9-109">A hull shader also generates user-defined outputs such as output-control points and patch constants that are sent past the tessellator directly to the third stage, the domain-shader stage.</span></span> <span data-ttu-id="d23e9-110">Um sombreador de domínio é invocado uma vez por ponto de Tessellator e avalia as posições da superfície.</span><span class="sxs-lookup"><span data-stu-id="d23e9-110">A domain shader is invoked once per tessellator-stage point and evaluates surface positions.</span></span>

<span data-ttu-id="d23e9-111">O estágio Tessellator é um estágio de função fixo, não há nenhum sombreador a ser gerado e nenhum estado a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d23e9-111">The tessellator stage is a fixed function stage, there is no shader to generate, and no state to set.</span></span> <span data-ttu-id="d23e9-112">Ele recebe todo o seu estado de configuração do estágio envoltória-Shader; Depois que o estágio envoltória-Shader tiver sido inicializado, o estágio Tessellator será inicializado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d23e9-112">It receives all of its setup state from the hull-shader stage; once the hull-shader stage has been initialized, the tessellator stage is automatically initialized.</span></span>

<span data-ttu-id="d23e9-113">**Para inicializar o estágio Tessellator**</span><span class="sxs-lookup"><span data-stu-id="d23e9-113">**To initialize the tessellator stage**</span></span>

-   <span data-ttu-id="d23e9-114">Inicialize o estágio envoltória-Shader usando [**ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="d23e9-114">Initialize the hull-shader stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    <span data-ttu-id="d23e9-115">*ppClassInstances* é um ponteiro para uma matriz de interfaces de sombreador, representado por ponteiros [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) e o número de interfaces, representado por *NumClassInstances*.</span><span class="sxs-lookup"><span data-stu-id="d23e9-115">*ppClassInstances* is a pointer to an array of shader interfaces, represented by [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointers and the number of interfaces, represented by *NumClassInstances*.</span></span> <span data-ttu-id="d23e9-116">Se não for usado, esses parâmetros poderão ser definidos como **NULL** e 0, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d23e9-116">If not used, these parameters can be set to **NULL** and 0 respectively.</span></span>

<span data-ttu-id="d23e9-117">Depois que o estágio envoltória-Shader for inicializado, você também deverá inicializar o estágio Domain-Shader.</span><span class="sxs-lookup"><span data-stu-id="d23e9-117">After the hull-shader stage is initialized, you should also initialize the domain-shader stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d23e9-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d23e9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d23e9-119">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d23e9-119">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="d23e9-120">Visão geral do mosaico</span><span class="sxs-lookup"><span data-stu-id="d23e9-120">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




