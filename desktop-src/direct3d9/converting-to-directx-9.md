---
description: Os recursos a seguir foram alterados no Microsoft Direct3D 9. Se você estiver usando esses recursos, consulte as alterações listadas abaixo para ajudá-lo a portar seu aplicativo para o Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Convertendo para Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811723"
---
# <a name="converting-to-direct3d-9"></a><span data-ttu-id="19b39-104">Convertendo para Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="19b39-104">Converting to Direct3D 9</span></span>

<span data-ttu-id="19b39-105">Os recursos a seguir foram alterados no Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="19b39-105">The following features were changed in Microsoft Direct3D 9.</span></span> <span data-ttu-id="19b39-106">Se você estiver usando esses recursos, consulte as alterações listadas abaixo para ajudá-lo a portar seu aplicativo para o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="19b39-106">If you are using these features, see the changes listed below to help you port your application to Direct3D 9.</span></span>

-   [<span data-ttu-id="19b39-107">BaseVertexIndex alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-107">BaseVertexIndex Changes</span></span>](#basevertexindex-changes)
-   [<span data-ttu-id="19b39-108">CreateImageSurface alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-108">CreateImageSurface Changes</span></span>](#createimagesurface-changes)
-   [<span data-ttu-id="19b39-109">D3DENUM \_ nenhuma \_ alteração no nível do WHQL \_</span><span class="sxs-lookup"><span data-stu-id="19b39-109">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>](/windows)
-   [<span data-ttu-id="19b39-110">Criar alterações de recurso</span><span class="sxs-lookup"><span data-stu-id="19b39-110">Create Resource Changes</span></span>](#create-resource-changes)
-   [<span data-ttu-id="19b39-111">EnumAdapterModes alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-111">EnumAdapterModes Changes</span></span>](#enumadaptermodes-changes)
-   [<span data-ttu-id="19b39-112">Alterações de Get/setstreamname \_</span><span class="sxs-lookup"><span data-stu-id="19b39-112">Get/SetStreamSource\_Changes</span></span>](#getsetstreamsource-changes)
-   [<span data-ttu-id="19b39-113">Alterações de qualidade de multiamostrar</span><span class="sxs-lookup"><span data-stu-id="19b39-113">Multisampling Quality Changes</span></span>](#multisampling-quality-changes)
-   [<span data-ttu-id="19b39-114">ResourceManagerDiscardBytes alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-114">ResourceManagerDiscardBytes Changes</span></span>](#resourcemanagerdiscardbytes-changes)
-   [<span data-ttu-id="19b39-115">SetSoftwareVertexProcessing alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-115">SetSoftwareVertexProcessing Changes</span></span>](#setsoftwarevertexprocessing-changes)
-   [<span data-ttu-id="19b39-116">Alterações de amostra de textura</span><span class="sxs-lookup"><span data-stu-id="19b39-116">Texture Sampler Changes</span></span>](#texture-sampler-changes)
-   [<span data-ttu-id="19b39-117">Alterações de declaração de vértice</span><span class="sxs-lookup"><span data-stu-id="19b39-117">Vertex Declaration Changes</span></span>](#vertex-declaration-changes)
-   [<span data-ttu-id="19b39-118">Intervalos \_ e \_ alterações SwapEffectss \_</span><span class="sxs-lookup"><span data-stu-id="19b39-118">Intervals,\_and\_SwapEffects\_Changes</span></span>](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a><span data-ttu-id="19b39-119">BaseVertexIndex alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-119">BaseVertexIndex Changes</span></span>

<span data-ttu-id="19b39-120">No DirectX 8. x, IDirect3DDevice8:: SetIndices exigia um ponteiro para o buffer de índice e um BaseVertexIndex para a posição inicial no buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="19b39-120">In DirectX 8.x, IDirect3DDevice8::SetIndices required a pointer to the index buffer and a BaseVertexIndex for the starting position in the vertex buffer.</span></span> <span data-ttu-id="19b39-121">Um aplicativo que armazena em lote objetos diferentes no buffer de vértice tinha que alternar o buffer de índice (ou fazer uma chamada para IDirect3DDevice8:: setindexes) antes de chamar IDirect3DDevice8::D rawIndexedPrimitive.</span><span class="sxs-lookup"><span data-stu-id="19b39-121">An application batching different objects into the vertex buffer had to switch the index buffer (or make a call to IDirect3DDevice8::SetIndices) before calling IDirect3DDevice8::DrawIndexedPrimitive.</span></span>

<span data-ttu-id="19b39-122">No Direct3D 9, a posição inicial no buffer de vértice, *BaseVertexIndex*, foi movida para IDirect3DDevice9::D rawindexedprimitive e seu tipo de dados foi alterado de um DWORD para um int.</span><span class="sxs-lookup"><span data-stu-id="19b39-122">In Direct3D 9, the starting position in the vertex buffer, *BaseVertexIndex*, has been moved to IDirect3DDevice9::DrawIndexedPrimitive, and its data type changed from a DWORD to an INT.</span></span>


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a><span data-ttu-id="19b39-123">CreateImageSurface alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-123">CreateImageSurface Changes</span></span>

<span data-ttu-id="19b39-124">IDirect3DDevice8:: CreateImageSurface foi renomeado [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span><span class="sxs-lookup"><span data-stu-id="19b39-124">IDirect3DDevice8::CreateImageSurface was renamed [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface).</span></span> <span data-ttu-id="19b39-125">Um parâmetro adicional que usa um tipo D3DPOOL foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="19b39-125">An additional parameter that takes a D3DPOOL type was added.</span></span> <span data-ttu-id="19b39-126">D3DPOOL \_ Scratch retornará uma superfície que tem características idênticas a uma superfície criada por IDirect3DDevice8:: CreateImageSurface.</span><span class="sxs-lookup"><span data-stu-id="19b39-126">D3DPOOL\_SCRATCH will return a surface that has identical characteristics to a surface created by IDirect3DDevice8::CreateImageSurface.</span></span> <span data-ttu-id="19b39-127">D3DPOOL \_ padrão é o pool apropriado para uso com [**StretchRect**](/windows/desktop/api) e [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span><span class="sxs-lookup"><span data-stu-id="19b39-127">D3DPOOL\_DEFAULT is the appropriate pool for use with [**StretchRect**](/windows/desktop/api) and [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).</span></span>

## <a name="d3denum_no_whql_level-changes"></a><span data-ttu-id="19b39-128">D3DENUM \_ nenhuma \_ alteração no nível do WHQL \_</span><span class="sxs-lookup"><span data-stu-id="19b39-128">D3DENUM\_NO\_WHQL\_LEVEL Changes</span></span>

<span data-ttu-id="19b39-129">Agora, os aplicativos precisam solicitar explicitamente o Microsoft Windows Hardware Quality Labs (WHQL), pois a resposta demora relativamente tempo (alguns segundos).</span><span class="sxs-lookup"><span data-stu-id="19b39-129">Applications now have to explicitly ask for the Microsoft Windows Hardware Quality Labs (WHQL) because the response takes relatively long (a few seconds).</span></span> <span data-ttu-id="19b39-130">D3DENUM \_ nenhum \_ \_ nível de WHQL foi removido e o \_ nível de WHQL D3DENUM foi \_ adicionado.</span><span class="sxs-lookup"><span data-stu-id="19b39-130">D3DENUM\_NO\_WHQL\_LEVEL has been removed and D3DENUM\_WHQL\_LEVEL has been added.</span></span>

## <a name="create-resource-changes"></a><span data-ttu-id="19b39-131">Criar alterações de recurso</span><span class="sxs-lookup"><span data-stu-id="19b39-131">Create Resource Changes</span></span>

<span data-ttu-id="19b39-132">Um identificador foi adicionado a vários métodos e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="19b39-132">A handle has been added to several methods and should be set to **NULL**.</span></span> <span data-ttu-id="19b39-133">Os métodos afetados incluem:</span><span class="sxs-lookup"><span data-stu-id="19b39-133">The methods affected include:</span></span>

-   [<span data-ttu-id="19b39-134">**CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="19b39-134">**CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="19b39-135">**CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="19b39-135">**CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [<span data-ttu-id="19b39-136">**CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="19b39-136">**CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="19b39-137">**CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="19b39-137">**CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [<span data-ttu-id="19b39-138">**CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="19b39-138">**CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [<span data-ttu-id="19b39-139">**CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="19b39-139">**CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [<span data-ttu-id="19b39-140">**CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="19b39-140">**CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [<span data-ttu-id="19b39-141">**CreateOffscreenPlainSurface**</span><span class="sxs-lookup"><span data-stu-id="19b39-141">**CreateOffscreenPlainSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a><span data-ttu-id="19b39-142">EnumAdapterModes alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-142">EnumAdapterModes Changes</span></span>

<span data-ttu-id="19b39-143">O [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) agora usa um D3DFORMAT.</span><span class="sxs-lookup"><span data-stu-id="19b39-143">The [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) now takes a D3DFORMAT.</span></span>


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



<span data-ttu-id="19b39-144">O formato oferece suporte a um conjunto crescente de modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="19b39-144">The format supports an expanding set of display modes.</span></span> <span data-ttu-id="19b39-145">Para proteger aplicativos da enumeração de formatos que não foram inventados quando o aplicativo foi enviado, o aplicativo deve informar ao Direct3D o formato dos modos de exibição que devem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="19b39-145">To protect applications from enumerating formats that were not invented when the application shipped, the application must tell Direct3D the format for the display modes that should be enumerated.</span></span> <span data-ttu-id="19b39-146">A matriz resultante de modos de exibição será diferente apenas por largura, altura e taxa de atualização.</span><span class="sxs-lookup"><span data-stu-id="19b39-146">The resulting array of display modes will differ only by width, height, and refresh rate.</span></span>

<span data-ttu-id="19b39-147">O aplicativo especifica um formato de pixel e a enumeração é restrita a esses modos de exibição que correspondem exatamente ao formato.</span><span class="sxs-lookup"><span data-stu-id="19b39-147">The application specifies a pixel format and the enumeration is restricted to those display modes that exactly match the format.</span></span> <span data-ttu-id="19b39-148">Veja a seguir uma lista dos formatos permitidos:</span><span class="sxs-lookup"><span data-stu-id="19b39-148">The following is a list of the allowed formats:</span></span>

-   <span data-ttu-id="19b39-149">D3DFMT \_ A1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="19b39-149">D3DFMT\_A1R5G5B5</span></span>
-   <span data-ttu-id="19b39-150">D3DFMT \_ A2B10G10R10</span><span class="sxs-lookup"><span data-stu-id="19b39-150">D3DFMT\_A2B10G10R10</span></span>
-   <span data-ttu-id="19b39-151">D3DFMT \_ A8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="19b39-151">D3DFMT\_A8R8G8B8</span></span>
-   <span data-ttu-id="19b39-152">D3DFMT \_ R5G6B5</span><span class="sxs-lookup"><span data-stu-id="19b39-152">D3DFMT\_R5G6B5</span></span>
-   <span data-ttu-id="19b39-153">D3DFMT \_ X1R5G5B5</span><span class="sxs-lookup"><span data-stu-id="19b39-153">D3DFMT\_X1R5G5B5</span></span>
-   <span data-ttu-id="19b39-154">D3DFMT \_ X8R8G8B8</span><span class="sxs-lookup"><span data-stu-id="19b39-154">D3DFMT\_X8R8G8B8</span></span>

<span data-ttu-id="19b39-155">A enumeração é equivalente a versões alfa e não alfa do mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="19b39-155">Enumeration is equivalent for alpha and nonalpha versions of the same format.</span></span> <span data-ttu-id="19b39-156">O formato retornado sempre será preenchido com o mesmo formato fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="19b39-156">The returned Format will always be filled with the same format supplied by the application.</span></span>

<span data-ttu-id="19b39-157">Esse método trata 565 e 555 como equivalente e retorna a versão correta no formato.</span><span class="sxs-lookup"><span data-stu-id="19b39-157">This method treats 565 and 555 as equivalent, and returns the correct version in the Format.</span></span> <span data-ttu-id="19b39-158">A diferença entra em cena somente quando o aplicativo bloqueia o buffer de fundo, e há um sinalizador explícito que o aplicativo deve definir para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="19b39-158">The difference comes into play only when the application locks the back buffer, and there is an explicit flag that the application must set in order to accomplish this.</span></span>

## <a name="getsetstreamsource-changes"></a><span data-ttu-id="19b39-159">Alterações de Get/setstreamname</span><span class="sxs-lookup"><span data-stu-id="19b39-159">Get/SetStreamSource Changes</span></span>

<span data-ttu-id="19b39-160">Um parâmetro foi adicionado aos métodos [**Getstreamname**](/windows/desktop/api) e [**setstreamexception**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) .</span><span class="sxs-lookup"><span data-stu-id="19b39-160">One parameter has been added to the [**GetStreamSource**](/windows/desktop/api) and [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) methods.</span></span> <span data-ttu-id="19b39-161">O deslocamento é o número de bytes entre o início do fluxo e o início dos dados do vértice.</span><span class="sxs-lookup"><span data-stu-id="19b39-161">The offset is the number of bytes between the beginning of the stream and the beginning of the vertex data.</span></span> <span data-ttu-id="19b39-162">É medido em bytes.</span><span class="sxs-lookup"><span data-stu-id="19b39-162">It is measured in bytes.</span></span> <span data-ttu-id="19b39-163">Isso permite que o pipeline ofereça suporte a deslocamentos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="19b39-163">This enables the pipeline to support stream offsets.</span></span> <span data-ttu-id="19b39-164">Para descobrir se o dispositivo dá suporte a deslocamentos de fluxo, consulte D3DDEVCAPS2 \_ STREAMOFFSET.</span><span class="sxs-lookup"><span data-stu-id="19b39-164">To find out if the device supports stream offsets, see D3DDEVCAPS2\_STREAMOFFSET.</span></span>


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a><span data-ttu-id="19b39-165">Alterações de qualidade de multiamostrar</span><span class="sxs-lookup"><span data-stu-id="19b39-165">Multisampling Quality Changes</span></span>

<span data-ttu-id="19b39-166">Anteriormente, havia apenas a enumeração de \_ tipo D3DMULTISAMPLE.</span><span class="sxs-lookup"><span data-stu-id="19b39-166">Previously, there was only the D3DMULTISAMPLE\_TYPE enumeration.</span></span> <span data-ttu-id="19b39-167">O Direct3D 9 mantém essa enumeração e adiciona a ideia de um nível de qualidade para cada elemento da enumeração.</span><span class="sxs-lookup"><span data-stu-id="19b39-167">Direct3D 9 retains this enumeration and adds the idea of a quality level for each element of the enumeration.</span></span> <span data-ttu-id="19b39-168">O nível de qualidade indica uma compensação entre a qualidade visual e o desempenho indicando o número de amostras mascaradas (no sentido de D3DRS \_ MULTISAMPLEMASK).</span><span class="sxs-lookup"><span data-stu-id="19b39-168">The quality level indicates a trade-off between visual quality and performance by indicating the number of maskable samples (in the sense of D3DRS\_MULTISAMPLEMASK).</span></span>

<span data-ttu-id="19b39-169">Um aplicativo deve escolher quantas amostras mascaradas são necessárias e, em seguida, consultar pQualityLevels.</span><span class="sxs-lookup"><span data-stu-id="19b39-169">An application should choose how many maskable samples it requires, and then consult pQualityLevels.</span></span> <span data-ttu-id="19b39-170">Se for diferente de zero, esse valor indicará o número de níveis de qualidade que o aplicativo pode passar para as várias funções de criação por meio de MultiSampleQuality.</span><span class="sxs-lookup"><span data-stu-id="19b39-170">If nonzero, this value indicates the number of quality levels the application can pass to the various creation functions through MultiSampleQuality.</span></span> <span data-ttu-id="19b39-171">Como os drivers expõem todos os seus esquemas de multiamostrar como níveis de qualidade em D3DMULTISAMPLE não \_ mascarable, você pode enumerar todos os esquemas de multiamostragens disponíveis por meio desse tipo, caso seu aplicativo não precise mascarar amostras.</span><span class="sxs-lookup"><span data-stu-id="19b39-171">Because drivers expose all their multisample schemes as quality levels at D3DMULTISAMPLE\_NONMASKABLE, you can enumerate all available multisampling schemes through this one type if your application does not need to mask samples.</span></span>

<span data-ttu-id="19b39-172">O \_ bit D3DPRASTERCAPS STRETCHBLTMULTISAMPLE Caps foi desativado.</span><span class="sxs-lookup"><span data-stu-id="19b39-172">The D3DPRASTERCAPS\_STRETCHBLTMULTISAMPLE caps bit has been retired.</span></span> <span data-ttu-id="19b39-173">Esse bit costumava significar que o método de multiamostragem não oferecia suporte a máscaras de gravação e não pôde ser alternado e desativado entre [**BeginScene**](/windows/desktop/api) e [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span><span class="sxs-lookup"><span data-stu-id="19b39-173">This bit used to mean that the multisampling method did not support write masks, and could not be toggled on and off between [**BeginScene**](/windows/desktop/api) and [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene).</span></span> <span data-ttu-id="19b39-174">Esses métodos que não podem ser mascarados agora são expostos por meio de D3DMULTISAMPLE sem \_ máscara.</span><span class="sxs-lookup"><span data-stu-id="19b39-174">Such nonmaskable methods are now exposed through D3DMULTISAMPLE\_NONMASKABLE.</span></span>


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



<span data-ttu-id="19b39-175">Há um máximo diferente para cada número de amostras mascaradas.</span><span class="sxs-lookup"><span data-stu-id="19b39-175">There is a different maximum for each number of maskable samples.</span></span> <span data-ttu-id="19b39-176">Por exemplo, exemplos de D3DMULTISAMPLE \_ 4 \_ podem ter três níveis de qualidade, enquanto os exemplos de D3DMULTISAMPLE \_ 2 \_ podem ter apenas um.</span><span class="sxs-lookup"><span data-stu-id="19b39-176">For example, D3DMULTISAMPLE\_4\_SAMPLES might have three levels of quality, while D3DMULTISAMPLE\_2\_SAMPLES might have only one.</span></span> <span data-ttu-id="19b39-177">Há no máximo oito níveis de qualidade para cada número de amostras mascaradas (o driver não tem permissão para expressar mais).</span><span class="sxs-lookup"><span data-stu-id="19b39-177">There are at most eight levels of quality for each number of maskable samples (the driver is not allowed to express more).</span></span> <span data-ttu-id="19b39-178">A qualidade varia de zero a ( \* pQualityLevels-1).</span><span class="sxs-lookup"><span data-stu-id="19b39-178">The quality ranges from zero to (\*pQualityLevels - 1).</span></span>

## <a name="resourcemanagerdiscardbytes-changes"></a><span data-ttu-id="19b39-179">ResourceManagerDiscardBytes alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-179">ResourceManagerDiscardBytes Changes</span></span>

<span data-ttu-id="19b39-180">ResourceManagerDiscardBytes foi substituído por IDirect3DDevice9:: EvictManagedResources.</span><span class="sxs-lookup"><span data-stu-id="19b39-180">ResourceManagerDiscardBytes has been replaced by IDirect3DDevice9::EvictManagedResources.</span></span> <span data-ttu-id="19b39-181">Ele pode remover todos os recursos, tanto os recursos do Direct3D quanto do driver.</span><span class="sxs-lookup"><span data-stu-id="19b39-181">It can evict all resources, both Direct3D and driver resources.</span></span>

<span data-ttu-id="19b39-182">O Gerenciador de recursos agora é consultado quando um recurso (seja gerenciado ou não gerenciado) falha na criação porque não há memória de vídeo suficiente.</span><span class="sxs-lookup"><span data-stu-id="19b39-182">The resource manager is now consulted when a resource (whether managed or nonmanaged) fails creation because there is insufficient video memory.</span></span> <span data-ttu-id="19b39-183">O gerente será solicitado automaticamente a liberar recursos suficientes para que a criação tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="19b39-183">The manager will automatically be asked to free enough resources for the creation to succeed.</span></span> <span data-ttu-id="19b39-184">No DirectX 8,0, esse não era um processo automatizado.</span><span class="sxs-lookup"><span data-stu-id="19b39-184">In DirectX 8.0, this was not an automated process.</span></span>

## <a name="setsoftwarevertexprocessing-changes"></a><span data-ttu-id="19b39-185">SetSoftwareVertexProcessing alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-185">SetSoftwareVertexProcessing Changes</span></span>

<span data-ttu-id="19b39-186">Um aplicativo pode criar um dispositivo de modo misto para usar o processamento de vértice de software e hardware.</span><span class="sxs-lookup"><span data-stu-id="19b39-186">An application can create a mixed-mode device to use software and hardware vertex processing.</span></span>

<span data-ttu-id="19b39-187">Para alternar entre os dois modos de processamento de vértice no DirectX 8. x, chame IDirect3DDevice8:: setrenderingstate.</span><span class="sxs-lookup"><span data-stu-id="19b39-187">To switch between the two vertex processing modes in DirectX 8.x, call IDirect3DDevice8::SetRenderState.</span></span> <span data-ttu-id="19b39-188">Isso foi substituído por [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) para facilitar os problemas causados por blocos de estado.</span><span class="sxs-lookup"><span data-stu-id="19b39-188">This has been replaced with [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) to ease problems caused by state blocks.</span></span> <span data-ttu-id="19b39-189">Esse novo método não é gravado por blocos de estado.</span><span class="sxs-lookup"><span data-stu-id="19b39-189">This new method is not recorded by state blocks.</span></span>

## <a name="texture-sampler-changes"></a><span data-ttu-id="19b39-190">Alterações de amostra de textura</span><span class="sxs-lookup"><span data-stu-id="19b39-190">Texture Sampler Changes</span></span>

<span data-ttu-id="19b39-191">O Direct3D 9 dá suporte a até 16 superfícies de textura em uma passagem usando o modelo de sombreador de pixel 2 \_ 0; no entanto, o número de coordenadas de textura permanece limitado a oito.</span><span class="sxs-lookup"><span data-stu-id="19b39-191">Direct3D 9 supports up to sixteen texture surfaces in one pass using the pixel shader 2\_0 model; however, the number of texture coordinates remains limited to eight.</span></span> <span data-ttu-id="19b39-192">O estado do estágio de textura está associado a superfícies, conjuntos de coordenadas, processamento de vértice e processamento de pixel.</span><span class="sxs-lookup"><span data-stu-id="19b39-192">Texture stage state is associated with surfaces, coordinate sets, vertex processing, and pixel processing.</span></span> <span data-ttu-id="19b39-193">Para gerenciar essas diferenças em tempo de compilação, o [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) foi dividido em dois métodos:</span><span class="sxs-lookup"><span data-stu-id="19b39-193">To manage these differences at compile time, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) has been broken into two methods:</span></span>

-   <span data-ttu-id="19b39-194">IDirect3DDevice9:: SetTextureStageState ainda será usado para o estado de coordenada de textura, como modos de encapsulamento e geração de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="19b39-194">IDirect3DDevice9::SetTextureStageState will still be used for texture coordinate state, such as wrap modes and texture coordinate generation.</span></span>
-   <span data-ttu-id="19b39-195">[**Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) foi adicionado e agora será usado para filtragem, disposição em blocos, fixação MSS, MIPLOD e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="19b39-195">[**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) has been added and will now be used for filtering, tiling, clamping, MIPLOD, and so forth.</span></span> <span data-ttu-id="19b39-196">Isso funcionará para até dezesseis amostras.</span><span class="sxs-lookup"><span data-stu-id="19b39-196">This will work for up to sixteen samplers.</span></span>

### <a name="settexturestagestate-changes"></a><span data-ttu-id="19b39-197">SetTextureStageState alterações</span><span class="sxs-lookup"><span data-stu-id="19b39-197">SetTextureStageState Changes</span></span>

<span data-ttu-id="19b39-198">IDirect3DDevice9:: SetTextureStageState agora define os seguintes Estados:</span><span class="sxs-lookup"><span data-stu-id="19b39-198">IDirect3DDevice9::SetTextureStageState now sets the following states:</span></span>

-   <span data-ttu-id="19b39-199">Estado de processamento de vértice da função fixa.</span><span class="sxs-lookup"><span data-stu-id="19b39-199">Fixed function vertex processing state.</span></span> <span data-ttu-id="19b39-200">Esse estado controla a manipulação de coordenadas de textura D3DTSS \_ TEXTURETRANSFORMFLAGS e D3DTSS \_ TEXCOORDINDEX.</span><span class="sxs-lookup"><span data-stu-id="19b39-200">This state controls the manipulation of texture coordinates D3DTSS\_TEXTURETRANSFORMFLAGS and D3DTSS\_TEXCOORDINDEX.</span></span> <span data-ttu-id="19b39-201">Até oito de cada um pode ser definido (porque oito coordenadas de textura são sempre suportadas).</span><span class="sxs-lookup"><span data-stu-id="19b39-201">Up to eight of each can be set (because eight texture coordinates are always supported).</span></span> <span data-ttu-id="19b39-202">D3DTSS \_ TEXCOORDINDEX é um estado de processamento de vértice de função fixo.</span><span class="sxs-lookup"><span data-stu-id="19b39-202">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="19b39-203">Se um sombreador de vértice programável for usado, esse Estado será ignorado.</span><span class="sxs-lookup"><span data-stu-id="19b39-203">If a programmable vertex shader is used, this state is ignored.</span></span>
-   <span data-ttu-id="19b39-204">Estado do sombreador do pixel da função fixa (o TextureStageState herdado).</span><span class="sxs-lookup"><span data-stu-id="19b39-204">Fixed function pixel shader state (the legacy TextureStageState).</span></span>

    -   <span data-ttu-id="19b39-205">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="19b39-205">D3DTSS\_ALPHAARG0</span></span>
    -   <span data-ttu-id="19b39-206">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="19b39-206">D3DTSS\_ALPHAARG1</span></span>
    -   <span data-ttu-id="19b39-207">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="19b39-207">D3DTSS\_ALPHAARG2</span></span>
    -   <span data-ttu-id="19b39-208">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="19b39-208">D3DTSS\_ALPHAOP</span></span>
    -   <span data-ttu-id="19b39-209">D3DTSS \_ BUMPENVLOFFSET</span><span class="sxs-lookup"><span data-stu-id="19b39-209">D3DTSS\_BUMPENVLOFFSET</span></span>
    -   <span data-ttu-id="19b39-210">D3DTSS \_ BUMPENVLSCALE</span><span class="sxs-lookup"><span data-stu-id="19b39-210">D3DTSS\_BUMPENVLSCALE</span></span>
    -   <span data-ttu-id="19b39-211">D3DTSS \_ BUMPENVMAT00</span><span class="sxs-lookup"><span data-stu-id="19b39-211">D3DTSS\_BUMPENVMAT00</span></span>
    -   <span data-ttu-id="19b39-212">D3DTSS \_ BUMPENVMAT01</span><span class="sxs-lookup"><span data-stu-id="19b39-212">D3DTSS\_BUMPENVMAT01</span></span>
    -   <span data-ttu-id="19b39-213">D3DTSS \_ BUMPENVMAT10</span><span class="sxs-lookup"><span data-stu-id="19b39-213">D3DTSS\_BUMPENVMAT10</span></span>
    -   <span data-ttu-id="19b39-214">D3DTSS \_ BUMPENVMAT11</span><span class="sxs-lookup"><span data-stu-id="19b39-214">D3DTSS\_BUMPENVMAT11</span></span>
    -   <span data-ttu-id="19b39-215">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="19b39-215">D3DTSS\_COLORARG0</span></span>
    -   <span data-ttu-id="19b39-216">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="19b39-216">D3DTSS\_COLORARG1</span></span>
    -   <span data-ttu-id="19b39-217">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="19b39-217">D3DTSS\_COLORARG2</span></span>
    -   <span data-ttu-id="19b39-218">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="19b39-218">D3DTSS\_COLOROP</span></span>
    -   <span data-ttu-id="19b39-219">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="19b39-219">D3DTSS\_RESULTARG</span></span>

    <span data-ttu-id="19b39-220">O número de Estados de sombreador de pixel de função fixa que pode ser definido é menor ou igual ao número representado por MaxTextureBlendStages.</span><span class="sxs-lookup"><span data-stu-id="19b39-220">The number of fixed function pixel shader states that can be set is less than or equal to the number represented by MaxTextureBlendStages.</span></span>

<span data-ttu-id="19b39-221">O número de amostragens de textura disponíveis para o aplicativo é determinado pela versão do sombreador de pixel, conforme indicado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="19b39-221">The number of texture samplers available to the application is determined by the pixel shader version, as indicated in the following table.</span></span>



| <span data-ttu-id="19b39-222">Nome</span><span class="sxs-lookup"><span data-stu-id="19b39-222">Name</span></span>                    | <span data-ttu-id="19b39-223">Número</span><span class="sxs-lookup"><span data-stu-id="19b39-223">Number</span></span>                                                         |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="19b39-224">PS \_ 1 \_ 1 para PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="19b39-224">ps\_1\_1 to ps\_1\_3</span></span>    | <span data-ttu-id="19b39-225">4 amostragens de textura</span><span class="sxs-lookup"><span data-stu-id="19b39-225">4 texture samplers</span></span>                                             |
| <span data-ttu-id="19b39-226">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="19b39-226">ps\_1\_4</span></span>                | <span data-ttu-id="19b39-227">6 amostras de textura</span><span class="sxs-lookup"><span data-stu-id="19b39-227">6 texture samplers</span></span>                                             |
| <span data-ttu-id="19b39-228">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="19b39-228">ps\_2\_0</span></span>                | <span data-ttu-id="19b39-229">16 classificadores de textura</span><span class="sxs-lookup"><span data-stu-id="19b39-229">16 texture samplers</span></span>                                            |
| <span data-ttu-id="19b39-230">pipeline de função fixa</span><span class="sxs-lookup"><span data-stu-id="19b39-230">fixed function pipeline</span></span> | <span data-ttu-id="19b39-231">Exemplos de textura de MaxTextureBlendStages/MaxSimultaneousTextures</span><span class="sxs-lookup"><span data-stu-id="19b39-231">MaxTextureBlendStages/MaxSimultaneousTextures texture samplers</span></span> |



 

<span data-ttu-id="19b39-232">Os dispositivos que dão suporte ao mapeamento de deslocamento no Direct3D 9 oferecerão suporte a uma amostra adicional (D3DDMAPSAMPLER), que amostra os mapas de deslocamento na unidade Tessellator.</span><span class="sxs-lookup"><span data-stu-id="19b39-232">Devices that support displacement mapping in Direct3D 9 will support an additional sampler (D3DDMAPSAMPLER), which samples the displacement maps in the tessellator unit.</span></span>

### <a name="setsamplerstate-changes"></a><span data-ttu-id="19b39-233">Alterações de setsamplestate</span><span class="sxs-lookup"><span data-stu-id="19b39-233">SetSamplerState Changes</span></span>

<span data-ttu-id="19b39-234">IDirect3DDevice9:: setamostrastate define o estado de amostra (incluindo o usado na unidade Tessellator para mapas de deslocamento de exemplo).</span><span class="sxs-lookup"><span data-stu-id="19b39-234">IDirect3DDevice9::SetSamplerState sets the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="19b39-235">Elas foram renomeadas com um prefixo D3DSAMP \_ para habilitar a detecção de erros em tempo de compilação ao portar do DirectX 8. x.</span><span class="sxs-lookup"><span data-stu-id="19b39-235">These have been renamed with a D3DSAMP\_ prefix to enable compile-time error detection when porting from DirectX 8.x.</span></span> <span data-ttu-id="19b39-236">Os Estados incluem:</span><span class="sxs-lookup"><span data-stu-id="19b39-236">The states include:</span></span>

-   <span data-ttu-id="19b39-237">Endereço de D3DSAMP \_</span><span class="sxs-lookup"><span data-stu-id="19b39-237">D3DSAMP\_ADDRESSU</span></span>
-   <span data-ttu-id="19b39-238">D3DSAMP \_ ADDRESSV</span><span class="sxs-lookup"><span data-stu-id="19b39-238">D3DSAMP\_ADDRESSV</span></span>
-   <span data-ttu-id="19b39-239">D3DSAMP \_ ADDRESSW</span><span class="sxs-lookup"><span data-stu-id="19b39-239">D3DSAMP\_ADDRESSW</span></span>
-   <span data-ttu-id="19b39-240">\_BORDERCOLOR D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="19b39-240">D3DSAMP\_BORDERCOLOR</span></span>
-   <span data-ttu-id="19b39-241">D3DSAMP \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="19b39-241">D3DSAMP\_MAGFILTER</span></span>
-   <span data-ttu-id="19b39-242">D3DSAMP \_ MAXANISOTROPY</span><span class="sxs-lookup"><span data-stu-id="19b39-242">D3DSAMP\_MAXANISOTROPY</span></span>
-   <span data-ttu-id="19b39-243">D3DSAMP \_ MAXMIPLEVEL</span><span class="sxs-lookup"><span data-stu-id="19b39-243">D3DSAMP\_MAXMIPLEVEL</span></span>
-   <span data-ttu-id="19b39-244">D3DSAMP \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="19b39-244">D3DSAMP\_MINFILTER</span></span>
-   <span data-ttu-id="19b39-245">D3DSAMP \_ MIPFILTER</span><span class="sxs-lookup"><span data-stu-id="19b39-245">D3DSAMP\_MIPFILTER</span></span>
-   <span data-ttu-id="19b39-246">D3DSAMP \_ MIPMAPLODBIAS</span><span class="sxs-lookup"><span data-stu-id="19b39-246">D3DSAMP\_MIPMAPLODBIAS</span></span>

## <a name="vertex-declaration-changes"></a><span data-ttu-id="19b39-247">Alterações de declaração de vértice</span><span class="sxs-lookup"><span data-stu-id="19b39-247">Vertex Declaration Changes</span></span>

<span data-ttu-id="19b39-248">As declarações de vértice agora são dissociadas da criação do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="19b39-248">Vertex declarations are now decoupled from vertex shader creation.</span></span> <span data-ttu-id="19b39-249">As declarações de vértice agora usam uma interface de Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="19b39-249">Vertex declarations now use a Component Object Model (COM) interface.</span></span>

<span data-ttu-id="19b39-250">Para o DirectX 8. x, as declarações de vértice são vinculadas a sombreadores de vértice.</span><span class="sxs-lookup"><span data-stu-id="19b39-250">For DirectX 8.x, vertex declarations are tied to vertex shaders.</span></span>

-   <span data-ttu-id="19b39-251">Para o pipeline de função fixa, chame [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) com o código de FVF (formato de vértice flexível) do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="19b39-251">For the fixed function pipeline, call [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) with the flexible vertex format (FVF) code of the vertex buffer.</span></span>
-   <span data-ttu-id="19b39-252">Para sombreadores de vértice, chame IDirect3DDevice9:: SetVertexShader com um identificador para um sombreador de vértice criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="19b39-252">For vertex shaders, call IDirect3DDevice9::SetVertexShader with a handle to a previously create vertex shader.</span></span> <span data-ttu-id="19b39-253">O sombreador inclui uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="19b39-253">The shader includes a vertex declaration.</span></span>

<span data-ttu-id="19b39-254">Para o Direct3D 9, as declarações de vértice são dissociadas de sombreadores de vértice e podem ser usadas com o pipeline de função fixa ou com sombreadores.</span><span class="sxs-lookup"><span data-stu-id="19b39-254">For Direct3D 9, vertex declarations are decoupled from vertex shaders and they can be used with either the fixed function pipeline or with shaders.</span></span>

-   <span data-ttu-id="19b39-255">Para o pipeline de função fixa, não é necessário chamar IDirect3DDevice9:: SetVertexShader.</span><span class="sxs-lookup"><span data-stu-id="19b39-255">For the fixed function pipeline, there is no need to call IDirect3DDevice9::SetVertexShader.</span></span> <span data-ttu-id="19b39-256">Se, no entanto, você quiser alternar para o pipeline de função fixa e tiver usado anteriormente um sombreador de vértice, chame IDirect3DDevice9:: SetVertexShader (**NULL**).</span><span class="sxs-lookup"><span data-stu-id="19b39-256">If, however, you want to switch to the fixed function pipeline and have previously used a vertex shader, call IDirect3DDevice9::SetVertexShader(**NULL**).</span></span> <span data-ttu-id="19b39-257">Quando isso for feito, você ainda precisará chamar [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) para declarar o código FVF.</span><span class="sxs-lookup"><span data-stu-id="19b39-257">When this is done, you will still need to call [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) to declare the FVF code.</span></span>
-   <span data-ttu-id="19b39-258">Ao usar sombreadores de vértice, chame IDirect3DDevice9:: SetVertexShader com o objeto de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="19b39-258">When using vertex shaders, call IDirect3DDevice9::SetVertexShader with the vertex shader object.</span></span> <span data-ttu-id="19b39-259">Além disso, chame IDirect3DDevice9:: SetFVF para configurar uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="19b39-259">Additionally, call IDirect3DDevice9::SetFVF to set up a vertex declaration.</span></span> <span data-ttu-id="19b39-260">Isso usa as informações implícitas no FVF.</span><span class="sxs-lookup"><span data-stu-id="19b39-260">This uses the information implicit in the FVF.</span></span> <span data-ttu-id="19b39-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) pode ser chamado em vez de IDirect3DDevice9:: SetFVF porque oferece suporte a declarações de vértice que não podem ser expressas com um FVF.</span><span class="sxs-lookup"><span data-stu-id="19b39-261">[**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) can be called in place of IDirect3DDevice9::SetFVF because it supports vertex declarations that cannot be expressed with an FVF.</span></span>

## <a name="intervals-and-swapeffects-changes"></a><span data-ttu-id="19b39-262">Intervalos e alterações SwapEffectss</span><span class="sxs-lookup"><span data-stu-id="19b39-262">Intervals, and SwapEffects Changes</span></span>

<span data-ttu-id="19b39-263">Várias alterações foram feitas para dar ao usuário mais controle sobre a taxa de atualização do monitor, a taxa de apresentação e o buffer de frente e para o desenho de buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="19b39-263">Several changes were made to give the user more control over monitor refresh rate, presentation rate, and front-buffer versus back-buffer drawing.</span></span> <span data-ttu-id="19b39-264">Elas são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="19b39-264">They are as follows:</span></span>

-   <span data-ttu-id="19b39-265">Um efeito de permuta foi removido, D3DSWAPEFFECT \_ cópia \_ vsync e uma taxa de apresentação, taxa de D3DPRESENT \_ \_ ilimitada.</span><span class="sxs-lookup"><span data-stu-id="19b39-265">Removed one swap effect, D3DSWAPEFFECT\_COPY\_VSYNC, and one presentation rate, D3DPRESENT\_RATE\_UNLIMITED.</span></span>
-   <span data-ttu-id="19b39-266">Parâmetros D3DPRESENT renomeados \_ . Tela inteira \_ PresentationInterval para PresentationIntervals.</span><span class="sxs-lookup"><span data-stu-id="19b39-266">Renamed D3DPRESENT\_PARAMETERS.FullScreen\_PresentationInterval to PresentationIntervals.</span></span>
-   <span data-ttu-id="19b39-267">Intervalo D3DPRESENT \_ adicionado \_ imediatamente, o que significa que a apresentação não está sincronizada com a sincronização vertical. Como no DirectX 8. x, o \_ padrão de intervalo D3DPRESENT \_ é definido como zero e é equivalente a D3DPRESENT \_ intervalo \_ um.</span><span class="sxs-lookup"><span data-stu-id="19b39-267">Added D3DPRESENT\_INTERVAL\_IMMEDIATE, which means that the presentation is not synchronized with the vertical sync. As in DirectX 8.x, D3DPRESENT\_INTERVAL\_DEFAULT is defined as zero and is equivalent to D3DPRESENT\_INTERVAL\_ONE.</span></span> <span data-ttu-id="19b39-268">\_ \_ O padrão de intervalo D3DPRESENT é uma conveniência para inicializar \_ parâmetros de D3DPRESENT para zero.</span><span class="sxs-lookup"><span data-stu-id="19b39-268">D3DPRESENT\_INTERVAL\_DEFAULT is a convenience for initializing D3DPRESENT\_PARAMETERS to zero.</span></span>

<span data-ttu-id="19b39-269">Para obter uma explicação detalhada dos modos e dos intervalos com suporte, consulte D3DPRESENT.</span><span class="sxs-lookup"><span data-stu-id="19b39-269">For a detailed explanation of the modes and the intervals that are supported, see D3DPRESENT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19b39-270">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19b39-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b39-271">Gráficos do Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="19b39-271">Direct3D 9 Graphics</span></span>](dx9-graphics.md)
</dt> </dl>

 

 
