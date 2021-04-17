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
# <a name="direct3d-video-motion-estimation"></a>Estimativa de movimento de vídeo do Direct3D

Este artigo contém diretrizes para a estimativa de vetor de movimento com APIs de vídeo do Direct3D 12. Esse recurso foi introduzido no Windows 10, versão 2004 (10,0; Build 19041). A estimativa de movimento é o processo de determinar os vetores de movimento que descrevem a transformação de uma imagem 2D para outra. A estimativa de movimento é uma parte essencial da codificação de vídeo e pode ser usada em algoritmos de conversão de taxa de quadros. 

Embora a estimativa de movimento possa ser implementada com sombreadores, a finalidade do recurso de estimativa de movimento D3D12 é expor a aceleração de função fixa para a pesquisa de movimento para descarregar essa parte do trabalho de 3D. Geralmente isso vem na forma de expor o avaliador de movimento do codificador de vídeo de GPU. O objetivo da estimativa de movimento D3D12 é o fluxo óptico, mas deve-se observar que os avaliadores de movimento do codificador podem ser otimizados para melhorar a compactação.


## <a name="checking-for-support"></a>Verificando o suporte

Determine o suporte para todos os recursos de vídeo do D3D chamando [ID3D12VideoDevice:: CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) e passando um valor da enumeração [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar o recurso para o qual o suporte está sendo consultado. Para consultar o tamanho de bloco e as resoluções com suporte para um determinado formato, use o valor **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** e forneça uma estrutura de [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) para o *pFeatureSupportData* , conforme mostrado no exemplo abaixo. Na versão atual, somente **DXGI_FORMAT_NV12** tem suporte, portanto, o conteúdo em outros formatos pode precisar ser convertido em cores e downsampled para usar a estimativa de movimento.

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a>O objeto de contexto do avaliador de movimento

O objeto [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) mantém o contexto para operações de estimativa de movimento de vídeo. Crie uma nova instância dessa interface chamando [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).

O tamanho de bloco selecionado, a precisão e o intervalo de tamanho com suporte dependem dos valores com suporte pelo hardware retornado da verificação de recurso de **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** . Você pode selecionar um intervalo de tamanho menor do que o driver dá suporte. Intervalo de tamanho informa tamanhos de alocação internos.

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



## <a name="storage-of-motion-vectors"></a>Armazenamento de vetores de movimento

O [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) armazena vetores de movimento. Essa interface é usada pela estrutura de [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) retornada de [ID3D12VideoEncodeCommandList:: EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion). A textura 2D de saída resolvida é uma textura [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) em que R contém o componente horizontal e G mantém o componente vertical do vetor de movimento. Essa textura é dimensionada para conter um par de componentes por bloco. Chame [ID3D12VideoEncodeCommandList:: ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) para converter a saída de vetor de movimento de **EstimateMotion** de formatos dependentes de hardware em um formato consistente definido pelas APIs de estimativa de movimento de vídeo.

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

 **ID3D12VideoMotionVectorHeap** também é usado para fornecer vetores de dica na estrutura de [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) .



## <a name="estimate-motion-in-a-command-list"></a>Estimar o movimento em uma lista de comandos

Chame o [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) de um [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) para invocar a operação de estimativa de movimento.

O exemplo a seguir executa a pesquisa de movimento e resolve os vetores de movimento para a textura 2D com [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).  Os recursos D3D12 usados como entrada para **EstimateMotion** devem estar no estado [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) e o recurso gravado pelo **ResolveMotionVectorHeap** deve estar no estado [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .

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


## <a name="protected-resources"></a>Recursos protegidos

A estimativa de vetor de movimento do Direct3D 12 dá suporte à leitura e gravação de recursos protegidos por DRM de hardware quando há suporte para o driver. Se os recursos de entrada forem protegidos por DRM de hardware, a saída também será um recurso protegido por DRM de hardware. Os métodos usados para criar o objeto de contexto de estimativa de movimento e o heap de vetor de movimento,  [ID3D12VideoDevice1:: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) e [ID3D12VideoDevice1:: CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), aceitam um [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) que é usado para gerenciar o acesso a recursos protegidos. 

Use [ID3D12VideoMotionEstimator:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) e [ID3D12VideoMotionVectorHeap:: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) para recuperar os objetos **ID3D12ProtectedResourceSession** fornecidos quando os objetos foram criados.



## <a name="related-topics"></a>Tópicos relacionados

* [APIs de vídeo do Direct3D 12](direct3d-12-video-apis.md)
* [Guia de programação Media Foundation](media-foundation-programming-guide.md)
