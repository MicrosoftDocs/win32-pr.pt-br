---
description: O modelo de sombreador de vértice 3,0 dá suporte à pesquisa de textura no sombreador de vértice usando a instrução texldl-vs de carregamento de textura.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Texturas de vértice no vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646064"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a><span data-ttu-id="eaba3-103">Texturas de vértice no vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eaba3-103">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>

<span data-ttu-id="eaba3-104">O modelo de sombreador de vértice 3,0 dá suporte à pesquisa de textura no sombreador de vértice usando a instrução [texldl-vs](../direct3dhlsl/texldl---vs.md) de carregamento de textura.</span><span class="sxs-lookup"><span data-stu-id="eaba3-104">The vertex shader 3.0 model supports texture lookup in the vertex shader using the [texldl - vs](../direct3dhlsl/texldl---vs.md) texture load statement.</span></span> <span data-ttu-id="eaba3-105">O mecanismo de vértice contém quatro estágios de amostra de textura, chamados [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 e D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="eaba3-105">The vertex engine contains four texture sampler stages, named [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2, and D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="eaba3-106">Eles são diferentes dos exemplos de amostra e textura de mapa de deslocamento no mecanismo de pixel.</span><span class="sxs-lookup"><span data-stu-id="eaba3-106">These are distinct from the displacement map sampler and texture samplers in the pixel engine.</span></span>

<span data-ttu-id="eaba3-107">Para exemplos de texturas definidas nesses quatro estágios, você pode usar o mecanismo de vértice e programar os estágios com o método [**CheckDeviceFormat**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="eaba3-107">To sample textures set at those four stages, you can use the vertex engine and program the stages with the [**CheckDeviceFormat**](/windows/desktop/api) method.</span></span> <span data-ttu-id="eaba3-108">Defina texturas nesses estágios usando [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), com o índice de estágio [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) por meio de D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="eaba3-108">Set textures at those stages using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), with the stage index [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) through D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="eaba3-109">Um novo registro foi introduzido no sombreador de vértice, o registro de amostra (como no PS \_ 2 \_ 0), que representa a amostra de textura de vértice.</span><span class="sxs-lookup"><span data-stu-id="eaba3-109">A new register has been introduced in the vertex shader, the sampler register (like in ps\_2\_0), which represents the vertex texture sampler.</span></span> <span data-ttu-id="eaba3-110">Esse registro precisa ser definido no sombreador antes de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="eaba3-110">This register needs to be defined in the shader before using it.</span></span>

<span data-ttu-id="eaba3-111">Um aplicativo pode consultar se há suporte para um formato como uma textura de vértice chamando [**CheckDeviceFormat**](/windows/desktop/api) com [D3DUSAGE de \_ consulta \_ VERTEXTEXTURE](d3dusage-query.md).</span><span class="sxs-lookup"><span data-stu-id="eaba3-111">An application can query if a format is supported as a vertex texture by calling [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE](d3dusage-query.md).</span></span>

> [!Note]  
> <span data-ttu-id="eaba3-112">Esse é um sinalizador de consulta para que não seja aceito em nenhuma função Createxxx.</span><span class="sxs-lookup"><span data-stu-id="eaba3-112">This is a query flag so it is not accepted in any Createxxx function.</span></span> <span data-ttu-id="eaba3-113">Uma textura de vértice criada no pool padrão pode ser definida como uma textura de pixel e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="eaba3-113">A vertex texture created in the default pool can be set as a pixel texture and vice versa.</span></span> <span data-ttu-id="eaba3-114">No entanto, para usar o processamento de vértice de software, a textura de vértice deve ser criada no pool transitório (não importa se é um dispositivo de modo misto ou um dispositivo de processamento de vértice de software).</span><span class="sxs-lookup"><span data-stu-id="eaba3-114">However, to use the software vertex processing, the vertex texture must be created in the scratch pool (no matter if it is a mixed-mode device or a software vertex processing device).</span></span>

 

<span data-ttu-id="eaba3-115">A funcionalidade é idêntica às texturas de pixel, exceto para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="eaba3-115">The functionality is identical to the pixel textures, except for the following:</span></span>

-   <span data-ttu-id="eaba3-116">Não há suporte para a filtragem de textura anisotropic, portanto, D3DSAMP \_ MAXANISOTROPY é ignorado e D3DTEXF \_ anisotropic não pode ser definido para a ampliação ou reduzir para esses estágios.</span><span class="sxs-lookup"><span data-stu-id="eaba3-116">Anisotropic texture filtering is not supported, hence D3DSAMP\_MAXANISOTROPY is ignored and D3DTEXF\_ANISOTROPIC cannot be set for magnify, or minify for these stages.</span></span>
-   <span data-ttu-id="eaba3-117">A taxa de informações de alteração não está disponível, portanto, o aplicativo precisa calcular o nível de detalhes e fornecer essas informações como um parâmetro para [texldl-vs](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="eaba3-117">Rate of change information is not available, hence the application has to compute the level of detail and provide that information as a parameter to [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="eaba3-118">As restrições incluem:</span><span class="sxs-lookup"><span data-stu-id="eaba3-118">Restrictions include:</span></span>

-   <span data-ttu-id="eaba3-119">Como em sombreadores de pixel, se as texturas de Multielemento tiverem suporte, D3DSAMP \_ ELEMENTINDEX será usado para descobrir a qual elemento criar amostra.</span><span class="sxs-lookup"><span data-stu-id="eaba3-119">As in pixel shaders, if multielement textures are supported, D3DSAMP\_ELEMENTINDEX is used to figure out which element to sample from.</span></span>
-   <span data-ttu-id="eaba3-120">O estado D3DSAMP \_ DMAPOFFSET é ignorado para esses estágios.</span><span class="sxs-lookup"><span data-stu-id="eaba3-120">The state D3DSAMP\_DMAPOFFSET is ignored for these stages.</span></span>
-   <span data-ttu-id="eaba3-121">Use [**CheckDeviceFormat**](/windows/desktop/api) com [D3DUSAGE \_ Query \_ VERTEXTEXTURE "](d3dusage-query.md) para consultar uma textura para ver se ela pode ser usada como uma textura de vértice.</span><span class="sxs-lookup"><span data-stu-id="eaba3-121">Use [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE"](d3dusage-query.md) to query a texture to see if it can be used as a vertex texture.</span></span>
-   <span data-ttu-id="eaba3-122">VertexTextureFilterCaps indica que tipo de filtros são permitidos nos exemplos de textura de vértice.</span><span class="sxs-lookup"><span data-stu-id="eaba3-122">VertexTextureFilterCaps indicates what kind of filters are allowed at the vertex texture samplers.</span></span> <span data-ttu-id="eaba3-123">[D3DPTFILTERCAPS \_ MINFANISOTROPIC](d3dptfiltercaps.md) e D3DPTFILTERCAPS \_ MAGFANISOTROPIC não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="eaba3-123">[D3DPTFILTERCAPS\_MINFANISOTROPIC](d3dptfiltercaps.md) and D3DPTFILTERCAPS\_MAGFANISOTROPIC are disallowed.</span></span>

## <a name="sampling-stage-registers"></a><span data-ttu-id="eaba3-124">Registros de estágio de amostragem</span><span class="sxs-lookup"><span data-stu-id="eaba3-124">Sampling Stage Registers</span></span>

<span data-ttu-id="eaba3-125">Um registro de estágio de amostragem identifica uma unidade de amostragem que pode ser usada em instruções de carregamento de textura.</span><span class="sxs-lookup"><span data-stu-id="eaba3-125">A sampling stage register identifies a sampling unit that can be used in texture load statements.</span></span> <span data-ttu-id="eaba3-126">Uma unidade de amostragem corresponde ao estágio de amostragem de textura, encapsulando o estado específico de amostragem fornecido em [**Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="eaba3-126">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span>

<span data-ttu-id="eaba3-127">Cada amostra identifica exclusivamente uma superfície de textura única que é definida como a amostra correspondente usando [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="eaba3-127">Each sampler uniquely identifies a single texture surface that is set to the corresponding sampler using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="eaba3-128">No entanto, a mesma superfície de textura pode ser definida em vários exemplos.</span><span class="sxs-lookup"><span data-stu-id="eaba3-128">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="eaba3-129">No momento do desenho, uma textura não pode ser definida simultaneamente como um destino de renderização e uma textura em um estágio.</span><span class="sxs-lookup"><span data-stu-id="eaba3-129">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="eaba3-130">Como o vs \_ 3 \_ 0 dá suporte a quatro amostragens, até quatro superfícies de textura podem ser lidas em uma única passagem de sombreador.</span><span class="sxs-lookup"><span data-stu-id="eaba3-130">Because vs\_3\_0 supports four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="eaba3-131">Um registro de amostra pode aparecer apenas como um argumento na instrução de carga de textura: [texldl-vs](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="eaba3-131">A sampler register might appear only as an argument in the texture load statement: [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="eaba3-132">No vs \_ 3 \_ 0, se você usar uma amostra, ela deverá ser declarada no início do programa do sombreador, usando o [ \_ SampleType de DCL (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) (como no PS \_ 2 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="eaba3-132">In vs\_3\_0, if you use a sampler, it must be declared at the beginning of the shader program, using the [dcl\_samplerType (sm3 - vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (as in ps\_2\_0).</span></span>

## <a name="software-processing"></a><span data-ttu-id="eaba3-133">Processamento de software</span><span class="sxs-lookup"><span data-stu-id="eaba3-133">Software Processing</span></span>

<span data-ttu-id="eaba3-134">Esse recurso terá suporte no processamento de vértice de software.</span><span class="sxs-lookup"><span data-stu-id="eaba3-134">This feature will be supported in software vertex processing.</span></span> <span data-ttu-id="eaba3-135">Os tipos de filtro específicos com suporte podem ser verificados chamando [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) e verificando VertexTextureFilterCaps.</span><span class="sxs-lookup"><span data-stu-id="eaba3-135">The specific filter types supported can be checked by calling [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) and checking VertexTextureFilterCaps.</span></span> <span data-ttu-id="eaba3-136">Todos os formatos de textura publicados terão suporte como texturas de vértice no processamento de vértice de software.</span><span class="sxs-lookup"><span data-stu-id="eaba3-136">All published texture formats will be supported as vertex textures in software vertex processing.</span></span>

<span data-ttu-id="eaba3-137">Os aplicativos podem verificar se há suporte para um formato de textura específico no modo de processamento de vértice de software chamando [**CheckDeviceFormat**](/windows/desktop/api) e fornecendo (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) como uso.</span><span class="sxs-lookup"><span data-stu-id="eaba3-137">Applications can check if a particular texture format is supported in the software vertex processing mode by calling [**CheckDeviceFormat**](/windows/desktop/api) and providing (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md)) as usage.</span></span> <span data-ttu-id="eaba3-138">Todos os formatos têm suporte para o processamento de vértice de software.</span><span class="sxs-lookup"><span data-stu-id="eaba3-138">All formats are supported for software vertex processing.</span></span> <span data-ttu-id="eaba3-139">O pool transitório é necessário para o processamento de vértice de software.</span><span class="sxs-lookup"><span data-stu-id="eaba3-139">The scratch pool is required for software vertex processing.</span></span>

## <a name="api-changes"></a><span data-ttu-id="eaba3-140">Alterações de API</span><span class="sxs-lookup"><span data-stu-id="eaba3-140">API Changes</span></span>


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a><span data-ttu-id="eaba3-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eaba3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaba3-142">Pipeline de vértice</span><span class="sxs-lookup"><span data-stu-id="eaba3-142">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
