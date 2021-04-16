---
description: .
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Criando um processador de vídeo de DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee524681cad43a8e140421e8e6eff30d44cabcc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764980"
---
# <a name="creating-a-dxva-hd-video-processor"></a><span data-ttu-id="ae9aa-103">Criando um processador de vídeo de DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ae9aa-103">Creating a DXVA-HD Video Processor</span></span>

<span data-ttu-id="ae9aa-104">A alta definição da aceleração de vídeo do Microsoft DirectX (DXVA-HD) usa duas interfaces primárias:</span><span class="sxs-lookup"><span data-stu-id="ae9aa-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) uses two primary interfaces:</span></span>

-   <span data-ttu-id="ae9aa-105">[**IDXVAHD \_ Dispositivo**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span><span class="sxs-lookup"><span data-stu-id="ae9aa-105">[**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span></span> <span data-ttu-id="ae9aa-106">Representa o dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-106">Represents the DXVA-HD device.</span></span> <span data-ttu-id="ae9aa-107">Use essa interface para consultar os recursos do dispositivo e criar o processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-107">Use this interface to query the device capabilities and create the video processor.</span></span>
-   <span data-ttu-id="ae9aa-108">[**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span><span class="sxs-lookup"><span data-stu-id="ae9aa-108">[**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span></span> <span data-ttu-id="ae9aa-109">Representa um conjunto de recursos de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-109">Represents a set of video processing capabilities.</span></span> <span data-ttu-id="ae9aa-110">Use esta interface para executar o blit de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-110">Use this interface to perform the video processing blit.</span></span>

<span data-ttu-id="ae9aa-111">No código a seguir, as seguintes variáveis globais são presumidas:</span><span class="sxs-lookup"><span data-stu-id="ae9aa-111">In the code that follows, the following global variables are assumed:</span></span>


```C++
IDirect3D9Ex            *g_pD3D = NULL;     
IDirect3DDevice9Ex      *g_pD3DDevice = NULL;   // Direct3D device.
IDXVAHD_Device          *g_pDXVAHD = NULL;      // DXVA-HD device.
IDXVAHD_VideoProcessor  *g_pDXVAVP = NULL;      // DXVA-HD video processor.
IDirect3DSurface9       *g_pSurface = NULL;     // Video surface.
        
const D3DFORMAT     RENDER_TARGET_FORMAT = D3DFMT_X8R8G8B8;
const D3DFORMAT     VIDEO_FORMAT         = D3DFMT_X8R8G8B8; 
const UINT          VIDEO_FPS            = 60;
const UINT          VIDEO_WIDTH          = 640;
const UINT          VIDEO_HEIGHT         = 480;
```



<span data-ttu-id="ae9aa-112">Para criar um processador de vídeo DXVA-HD:</span><span class="sxs-lookup"><span data-stu-id="ae9aa-112">To create a DXVA-HD video processor:</span></span>

1.  <span data-ttu-id="ae9aa-113">Preencha uma estrutura [**\_ \_ desc de conteúdo do DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) com uma descrição do conteúdo do vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-113">Fill in a [**DXVAHD\_CONTENT\_DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) structure with a description of the video content.</span></span> <span data-ttu-id="ae9aa-114">O driver usa essas informações como uma dica para otimizar os recursos do processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-114">The driver uses this information as a hint to optimize the capabilities of the video processor.</span></span> <span data-ttu-id="ae9aa-115">A estrutura não contém uma descrição completa do formato.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-115">The structure does not contain a complete format description.</span></span>
    ```C++
        DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

        DXVAHD_CONTENT_DESC desc;

        desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
        desc.InputFrameRate = fps;
        desc.InputWidth = VIDEO_WIDTH;
        desc.InputHeight = VIDEO_HEIGHT;
        desc.OutputFrameRate = fps;
        desc.OutputWidth = VIDEO_WIDTH;
        desc.OutputHeight = VIDEO_HEIGHT;
    ```

    

2.  <span data-ttu-id="ae9aa-116">Chame [**DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) para criar o dispositivo DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-116">Call [**DXVAHD\_CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) to create the DXVA-HD device.</span></span> <span data-ttu-id="ae9aa-117">Essa função retorna um ponteiro para a interface do [**\_ dispositivo IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) .</span><span class="sxs-lookup"><span data-stu-id="ae9aa-117">This function returns a pointer to the [**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) interface.</span></span>
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  <span data-ttu-id="ae9aa-118">Chame [**o \_ dispositivo IDXVAHD:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span><span class="sxs-lookup"><span data-stu-id="ae9aa-118">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span></span> <span data-ttu-id="ae9aa-119">Esse método preenche uma estrutura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) com os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-119">This method fills in a [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure with the device capabilities.</span></span> <span data-ttu-id="ae9aa-120">Se você precisar de recursos de processamento de vídeo específicos, como Luma de criação de imagem ou filtragem de imagens, verifique a disponibilidade usando essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-120">If you require specific video processing features, such as luma keying or image filtering, check their availability by using this structure.</span></span>
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  <span data-ttu-id="ae9aa-121">Verifique se o dispositivo DXVA-HD dá suporte aos formatos de vídeo de entrada que você precisa.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-121">Check whether the DXVA-HD device supports the input video formats that you require.</span></span> <span data-ttu-id="ae9aa-122">O tópico [verificando os formatos de DXVA-HD com suporte](checking-supported-dxva-hd-formats.md) descreve essa etapa mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-122">The topic [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
5.  <span data-ttu-id="ae9aa-123">Verifique se o dispositivo DXVA-HD dá suporte ao formato de saída que você precisa.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-123">Check whether the DXVA-HD device supports the output format that you require.</span></span> <span data-ttu-id="ae9aa-124">A seção [verificando os formatos de DXVA-HD com suporte](checking-supported-dxva-hd-formats.md) descreve essa etapa mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-124">The section [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
6.  <span data-ttu-id="ae9aa-125">Aloque uma matriz de estruturas [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) .</span><span class="sxs-lookup"><span data-stu-id="ae9aa-125">Allocate an array of [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structures.</span></span> <span data-ttu-id="ae9aa-126">O número de elementos da matriz que devem ser alocados é fornecido pelo membro **VideoProcessorCount** da estrutura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) , obtida na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-126">The number of array elements that must be allocated is given by the **VideoProcessorCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure, obtained in step 3.</span></span>
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  <span data-ttu-id="ae9aa-127">Cada estrutura [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) representa um processador de vídeo distinto.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-127">Each [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure represents a distinct video processor.</span></span> <span data-ttu-id="ae9aa-128">Você pode executar um loop nessa matriz para descobrir os recursos de cada processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-128">You can loop through this array to discover the capabilities of each video processor.</span></span> <span data-ttu-id="ae9aa-129">A estrutura inclui informações sobre os recursos de desentrelaçamento, telecineon e conversão de taxa de quadros do processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-129">The structure includes information about the deinterlacing, telecine, and frame-rate conversion capabilities of the video processor.</span></span>
8.  <span data-ttu-id="ae9aa-130">Selecione um processador de vídeo para criar.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-130">Select a video processor to create.</span></span> <span data-ttu-id="ae9aa-131">O membro **VPGuid** da estrutura [**\_ VPCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contém um GUID que identifica exclusivamente o processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-131">The **VPGuid** member of the [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure contains a GUID that uniquely identifies the video processor.</span></span> <span data-ttu-id="ae9aa-132">Passe este GUID para o método [**IDXVAHD \_ Device:: CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="ae9aa-132">Pass this GUID to the [**IDXVAHD\_Device::CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) method.</span></span> <span data-ttu-id="ae9aa-133">O método retorna um ponteiro [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="ae9aa-133">The method returns an [**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) pointer.</span></span>
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  <span data-ttu-id="ae9aa-134">Opcionalmente, chame [**IDXVAHD \_ Device:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) para criar uma matriz de superfícies de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae9aa-134">Optionally, call [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) to create an array of input video surfaces.</span></span>

<span data-ttu-id="ae9aa-135">O exemplo de código a seguir mostra a sequência completa de etapas:</span><span class="sxs-lookup"><span data-stu-id="ae9aa-135">The following code example shows the complete sequence of steps:</span></span>


```C++
// Initializes the DXVA-HD video processor.

// NOTE: The following example makes some simplifying assumptions:
//
// 1. There is a single input stream.
// 2. The input frame rate matches the output frame rate.
// 3. No advanced DXVA-HD features are needed, such as luma keying or IVTC.
// 4. The application uses a single input video surface.

HRESULT InitializeDXVAHD()
{
    if (g_pD3DDevice == NULL)
    {
        return E_FAIL;
    }

    HRESULT hr = S_OK;

    IDXVAHD_Device          *pDXVAHD = NULL;
    IDXVAHD_VideoProcessor  *pDXVAVP = NULL;
    IDirect3DSurface9       *pSurf = NULL;

    DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

    DXVAHD_CONTENT_DESC desc;

    desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
    desc.InputFrameRate = fps;
    desc.InputWidth = VIDEO_WIDTH;
    desc.InputHeight = VIDEO_HEIGHT;
    desc.OutputFrameRate = fps;
    desc.OutputWidth = VIDEO_WIDTH;
    desc.OutputHeight = VIDEO_HEIGHT;

#ifdef USE_SOFTWARE_PLUGIN    
    HMODULE hSWPlugin = LoadLibrary(L"C:\\dxvahdsw.dll");

    PDXVAHDSW_Plugin pSWPlugin = (PDXVAHDSW_Plugin)GetProcAddress(hSWPlugin, "DXVAHDSW_Plugin");

    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc,DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        pSWPlugin, &pDXVAHD);
#else
    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        NULL, &pDXVAHD);
#endif
    if (FAILED(hr))
    {
        goto done;
    }

    DXVAHD_VPDEVCAPS caps;

    hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    if (FAILED(hr))
    {
        goto done;
    }

    // Check whether the device supports the input and output formats.

    hr = CheckInputFormatSupport(pDXVAHD, caps, VIDEO_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CheckOutputFormatSupport(pDXVAHD, caps, RENDER_TARGET_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the VP device.
    hr = CreateVPDevice(pDXVAHD, caps, &pDXVAVP);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );

    if (FAILED(hr))
    {
        goto done;
    }


    g_pDXVAHD = pDXVAHD;
    g_pDXVAHD->AddRef();

    g_pDXVAVP = pDXVAVP;
    g_pDXVAVP->AddRef();

    g_pSurface = pSurf;
    g_pSurface->AddRef();

done:
    SafeRelease(&pDXVAHD);
    SafeRelease(&pDXVAVP);
    SafeRelease(&pSurf);
    return hr;
}
```



<span data-ttu-id="ae9aa-136">A função CreateVPDevice mostrada neste exemplo cria o processador de vídeo (etapas 5 a 7):</span><span class="sxs-lookup"><span data-stu-id="ae9aa-136">The CreateVPDevice function show in this example creates the video processor (steps 5–7):</span></span>


```C++
// Creates a DXVA-HD video processor.

HRESULT CreateVPDevice(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    IDXVAHD_VideoProcessor  **ppDXVAVP
    )
{
    // Create the array of video processor caps. 
    
    DXVAHD_VPCAPS *pVPCaps = 
        new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

    if (pVPCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
        caps.VideoProcessorCount, pVPCaps);

    // At this point, an application could loop through the array and examine
    // the capabilities. For purposes of this example, however, we simply
    // create the first video processor in the list.

    if (SUCCEEDED(hr))
    {
        // The VPGuid member contains the GUID that identifies the video 
        // processor.

        hr = pDXVAHD->CreateVideoProcessor(&pVPCaps[0].VPGuid, ppDXVAVP);
    }

    delete [] pVPCaps;
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ae9aa-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae9aa-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae9aa-138">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ae9aa-138">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



