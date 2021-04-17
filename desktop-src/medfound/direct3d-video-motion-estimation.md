---
description: Este artigo contém diretrizes para a estimativa de vetor de movimento com APIs de vídeo do Direct3D 12.
ms.assetid: ''
title: Estimativa de movimento de vídeo do Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 7fdb6146e1bb77c673eb89d944bcf42a8babce49
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105812139"
---
# <a name="direct3d-video-motion-estimation"></a><span data-ttu-id="41499-103">Estimativa de movimento de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="41499-103">Direct3D video motion estimation</span></span>

<span data-ttu-id="41499-104">Este artigo contém diretrizes para a estimativa de vetor de movimento com APIs de vídeo do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="41499-104">This article contains guidance for motion vector estimation with Direct3D 12 video APIs.</span></span> <span data-ttu-id="41499-105">Esse recurso foi introduzido no Windows 10, versão 2004 (10,0; Build 19041).</span><span class="sxs-lookup"><span data-stu-id="41499-105">This feature was introduced in Windows 10, version 2004 (10.0; Build 19041).</span></span> <span data-ttu-id="41499-106">A estimativa de movimento é o processo de determinar os vetores de movimento que descrevem a transformação de uma imagem 2D para outra.</span><span class="sxs-lookup"><span data-stu-id="41499-106">Motion estimation is the process of determining motion vectors that describe the transformation from one 2D image to another.</span></span> <span data-ttu-id="41499-107">A estimativa de movimento é uma parte essencial da codificação de vídeo e pode ser usada em algoritmos de conversão de taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="41499-107">Motion estimation is an essential part of video encoding and can be used in frame rate conversion algorithms.</span></span> 

<span data-ttu-id="41499-108">Embora a estimativa de movimento possa ser implementada com sombreadores, a finalidade do recurso de estimativa de movimento D3D12 é expor a aceleração de função fixa para a pesquisa de movimento para descarregar essa parte do trabalho de 3D.</span><span class="sxs-lookup"><span data-stu-id="41499-108">While motion estimation can be implemented with shaders, the purpose of the D3D12 Motion Estimation feature is to expose fixed function acceleration for motion searching to offload this part of the work from 3D.</span></span> <span data-ttu-id="41499-109">Geralmente isso vem na forma de expor o avaliador de movimento do codificador de vídeo de GPU.</span><span class="sxs-lookup"><span data-stu-id="41499-109">Often this comes in the form of exposing the GPU video encoder motion estimator.</span></span> <span data-ttu-id="41499-110">O objetivo da estimativa de movimento D3D12 é o fluxo óptico, mas deve-se observar que os avaliadores de movimento do codificador podem ser otimizados para melhorar a compactação.</span><span class="sxs-lookup"><span data-stu-id="41499-110">The goal of D3D12 Motion estimation is optical flow, but it should be noted that encoder motion estimators may be optimized for improving compression.</span></span>


## <a name="checking-for-support"></a><span data-ttu-id="41499-111">Verificando o suporte</span><span class="sxs-lookup"><span data-stu-id="41499-111">Checking for Support</span></span>

<span data-ttu-id="41499-112">Determine o suporte para todos os recursos de vídeo do D3D chamando [ID3D12VideoDevice:: CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) e passando um valor da enumeração [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar o recurso para o qual o suporte está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="41499-112">Determine support for all D3D video features by calling [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) and passing in a value from the [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify the feature for which support is being queried.</span></span> <span data-ttu-id="41499-113">Para consultar o tamanho de bloco e as resoluções com suporte para um determinado formato, use o valor **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** e forneça uma estrutura de [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) para o *pFeatureSupportData* , conforme mostrado no exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="41499-113">To query the supported block size and resolutions for a given format, use the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** value and supply a [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) structure for the *pFeatureSupportData* as shown in the example below.</span></span> <span data-ttu-id="41499-114">Na versão atual, somente **DXGI_FORMAT_NV12** tem suporte, portanto, o conteúdo em outros formatos pode precisar ser convertido em cores e downsampled para usar a estimativa de movimento.</span><span class="sxs-lookup"><span data-stu-id="41499-114">In the current release, only **DXGI_FORMAT_NV12** is supported, so content in other formats may need to be color converted and downsampled to use motion estimation.</span></span>

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a><span data-ttu-id="41499-115">O objeto de contexto do avaliador de movimento</span><span class="sxs-lookup"><span data-stu-id="41499-115">The motion estimator context object</span></span>

<span data-ttu-id="41499-116">O objeto [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) mantém o contexto para operações de estimativa de movimento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41499-116">The [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) object maintains context for video motion estimation operations.</span></span> <span data-ttu-id="41499-117">Crie uma nova instância dessa interface chamando [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span><span class="sxs-lookup"><span data-stu-id="41499-117">Create a new instance of this interface by calling [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span></span>

<span data-ttu-id="41499-118">O tamanho de bloco selecionado, a precisão e o intervalo de tamanho com suporte dependem dos valores com suporte pelo hardware retornado da verificação de recurso de **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** .</span><span class="sxs-lookup"><span data-stu-id="41499-118">The selected block size, precision, and supported size range would depend on values supported by hardware returned from the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** feature check.</span></span> <span data-ttu-id="41499-119">Você pode selecionar um intervalo de tamanho menor do que o driver dá suporte.</span><span class="sxs-lookup"><span data-stu-id="41499-119">You can select a smaller size range than the driver supports.</span></span> <span data-ttu-id="41499-120">Intervalo de tamanho informa tamanhos de alocação internos.</span><span class="sxs-lookup"><span data-stu-id="41499-120">Size range informs internal allocation sizes.</span></span>

```c++
D3D12_VIDEO_MOTION_ESTIMATOR_DESC motionEstimatorDesc = { 
    0, //NodeIndex
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionEstimator> spVideoMotionEstimator;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionEstimator(
    &motionEstimatorDesc, 
    nullptr,
    IID_PPV_ARGS(&spVideoMotionEstimator)));
```



## <a name="storage-of-motion-vectors"></a><span data-ttu-id="41499-121">Armazenamento de vetores de movimento</span><span class="sxs-lookup"><span data-stu-id="41499-121">Storage of motion vectors</span></span>

<span data-ttu-id="41499-122">O [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) armazena vetores de movimento.</span><span class="sxs-lookup"><span data-stu-id="41499-122">The [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) stores motion vectors.</span></span> <span data-ttu-id="41499-123">Essa interface é usada pela estrutura de [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) retornada de [ID3D12VideoEncodeCommandList:: EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span><span class="sxs-lookup"><span data-stu-id="41499-123">This interface is used by the [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) structure returned from [ID3D12VideoEncodeCommandList::EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span></span> <span data-ttu-id="41499-124">A textura 2D de saída resolvida é uma textura [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) em que R contém o componente horizontal e G mantém o componente vertical do vetor de movimento.</span><span class="sxs-lookup"><span data-stu-id="41499-124">The resolved output 2D texture is a [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) texture where R holds the horizontal component and G holds the vertical component of the motion vector.</span></span> <span data-ttu-id="41499-125">Essa textura é dimensionada para conter um par de componentes por bloco.</span><span class="sxs-lookup"><span data-stu-id="41499-125">This texture is sized to hold one pair of components per block.</span></span> <span data-ttu-id="41499-126">Chame [ID3D12VideoEncodeCommandList:: ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) para converter a saída de vetor de movimento de **EstimateMotion** de formatos dependentes de hardware em um formato consistente definido pelas APIs de estimativa de movimento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41499-126">Call [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) to translates the motion vector output of **EstimateMotion** from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.</span></span>

```c++
D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC MotionVectorHeapDesc = { 
    0, // NodeIndex 
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionVectorHeap> spVideoMotionVectorHeap;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionVectorHeap(
    &MotionVectorHeapDesc, 
    nullptr, 
    IID_PPV_ARGS(&spVideoMotionVectorHeap)));
```

```cpp
    CD3DX12_RESOURCE_DESC::Tex2D(
        DXGI_FORMAT_R16G16_SINT, 
        Align(1920, 16) / 16, // This example uses a 16x16 block size. Pixel width and height
        Align(1080, 16) / 16, // are adjusted to store the vectors for those blocks.
        1, // ArraySize
        1  // MipLevels
        );

    ATL::CComPtr< ID3D12Resource > spResolvedMotionVectors;
    VERIFY_SUCCEEDED(pDevice->CreateCommittedResource(
        &Properties,
        D3D12_HEAP_FLAG_NONE,
        &resolvedMotionVectorDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        IID_PPV_ARGS(&spResolvedMotionVectors)));
```

 <span data-ttu-id="41499-127">**ID3D12VideoMotionVectorHeap** também é usado para fornecer vetores de dica na estrutura de [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) .</span><span class="sxs-lookup"><span data-stu-id="41499-127">**ID3D12VideoMotionVectorHeap** is also used to supply hint vectors in the [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) structure.</span></span>



## <a name="estimate-motion-in-a-command-list"></a><span data-ttu-id="41499-128">Estimar o movimento em uma lista de comandos</span><span class="sxs-lookup"><span data-stu-id="41499-128">Estimate motion in a command list</span></span>

<span data-ttu-id="41499-129">Chame o [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) de um [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) para invocar a operação de estimativa de movimento.</span><span class="sxs-lookup"><span data-stu-id="41499-129">Call the [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) from a [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) to invoke the motion estimation operation.</span></span>

<span data-ttu-id="41499-130">O exemplo a seguir executa a pesquisa de movimento e resolve os vetores de movimento para a textura 2D com [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="41499-130">The example below executes the motion search and resolves the motion vectors to the 2D texture with [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>  <span data-ttu-id="41499-131">Os recursos D3D12 usados como entrada para **EstimateMotion** devem estar no estado [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) e o recurso gravado pelo **ResolveMotionVectorHeap** deve estar no estado [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="41499-131">D3D12 Resources used as input to **EstimateMotion** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state and the resource written to by **ResolveMotionVectorHeap** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state.</span></span>

```cpp
const D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT outputArgs = {spVideoMotionVectorHeap};

const D3D12_VIDEO_MOTION_ESTIMATOR_INPUT inputArgs = {
    spCurrentResource,
    0,
    spReferenceResource,
    0,
    nullptr // pHintMotionVectorHeap
    };

spCommandList->EstimateMotion(spVideoMotionEstimator, &outputArgs, &inputArgs);

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT outputArgs = { 
    spResolvedMotionVectors,
    {}};

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT inputArgs = {
    spVideoMotionVectorHeap,
    1920,
    1080
    };

spCommandList->ResolveMotionVectorHeap(&outputArgs, &inputArgs);
        
VERIFY(spCommandList->Close());

// Execute Commandlist.
ID3D12CommandList *ppCommandLists[1] = { spCommandList.p };
spCommandQueue->ExecuteCommandLists(1, ppCommandLists);
```


## <a name="protected-resources"></a><span data-ttu-id="41499-132">Recursos protegidos</span><span class="sxs-lookup"><span data-stu-id="41499-132">Protected resources</span></span>

<span data-ttu-id="41499-133">A estimativa de vetor de movimento do Direct3D 12 dá suporte à leitura e gravação de recursos protegidos por DRM de hardware quando há suporte para o driver.</span><span class="sxs-lookup"><span data-stu-id="41499-133">Direct3D 12 motion vector estimation supports reading from and writing to hardware DRM protected resources when supported by the driver.</span></span> <span data-ttu-id="41499-134">Se os recursos de entrada forem protegidos por DRM de hardware, a saída também será um recurso protegido por DRM de hardware. Os métodos usados para criar o objeto de contexto de estimativa de movimento e o heap de vetor de movimento,  [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) e [ID3D12VideoDevice1:: CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), aceitam um [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) que é usado para gerenciar o acesso a recursos protegidos.</span><span class="sxs-lookup"><span data-stu-id="41499-134">If the input resources are hardware DRM protected, the output is also a hardware DRM protected resource.The methods used to create the motion estimation context object and the motion vector heap,  [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) and [ID3D12VideoDevice1::CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), both accept a [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) that is used to manage access to protected resources.</span></span> 

<span data-ttu-id="41499-135">Use [ID3D12VideoMotionEstimator:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) e [ID3D12VideoMotionVectorHeap:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) para recuperar os objetos **ID3D12ProtectedResourceSession** fornecidos quando os objetos foram criados.</span><span class="sxs-lookup"><span data-stu-id="41499-135">Use [ID3D12VideoMotionEstimator::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) and [ID3D12VideoMotionVectorHeap::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) to retrieve the **ID3D12ProtectedResourceSession** objects provided when the objects were created.</span></span>



## <a name="related-topics"></a><span data-ttu-id="41499-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41499-136">Related topics</span></span>

* [<span data-ttu-id="41499-137">APIs de vídeo do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="41499-137">Direct3D 12 Video APIs</span></span>](direct3d-12-video-apis.md)
* [<span data-ttu-id="41499-138">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41499-138">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
