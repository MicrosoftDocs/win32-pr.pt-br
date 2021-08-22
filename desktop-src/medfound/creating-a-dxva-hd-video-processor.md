---
description: Criando um processador de vídeo de DXVA-HD
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Criando um processador de vídeo de DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945153dfd3e14f1d2caae9b0a84f201745ea24722781bf998930477054138c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974815"
---
# <a name="creating-a-dxva-hd-video-processor"></a>Criando um processador de vídeo de DXVA-HD

A alta definição da aceleração de vídeo do Microsoft DirectX (DXVA-HD) usa duas interfaces primárias:

-   [**IDXVAHD \_ Dispositivo**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device). Representa o dispositivo DXVA-HD. Use essa interface para consultar os recursos do dispositivo e criar o processador de vídeo.
-   [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor). Representa um conjunto de recursos de processamento de vídeo. Use esta interface para executar o blit de processamento de vídeo.

No código a seguir, as seguintes variáveis globais são presumidas:


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



Para criar um processador de vídeo DXVA-HD:

1.  Preencha uma estrutura [**\_ \_ desc de conteúdo do DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) com uma descrição do conteúdo do vídeo. O driver usa essas informações como uma dica para otimizar os recursos do processador de vídeo. A estrutura não contém uma descrição completa do formato.
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

    

2.  Chame [**DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) para criar o dispositivo DXVA-HD. Essa função retorna um ponteiro para a interface do [**\_ dispositivo IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) .
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  Chame [**o \_ dispositivo IDXVAHD:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps). Esse método preenche uma estrutura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) com os recursos do dispositivo. Se você precisar de recursos de processamento de vídeo específicos, como Luma de criação de imagem ou filtragem de imagens, verifique a disponibilidade usando essa estrutura.
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  Verifique se o dispositivo DXVA-HD dá suporte aos formatos de vídeo de entrada que você precisa. O tópico [verificando os formatos de DXVA-HD com suporte](checking-supported-dxva-hd-formats.md) descreve essa etapa mais detalhadamente.
5.  Verifique se o dispositivo DXVA-HD dá suporte ao formato de saída que você precisa. A seção [verificando os formatos de DXVA-HD com suporte](checking-supported-dxva-hd-formats.md) descreve essa etapa mais detalhadamente.
6.  Aloque uma matriz de estruturas [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) . O número de elementos da matriz que devem ser alocados é fornecido pelo membro **VideoProcessorCount** da estrutura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) , obtida na etapa 3.
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  Cada estrutura [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) representa um processador de vídeo distinto. Você pode executar um loop nessa matriz para descobrir os recursos de cada processador de vídeo. A estrutura inclui informações sobre os recursos de desentrelaçamento, telecineon e conversão de taxa de quadros do processador de vídeo.
8.  Selecione um processador de vídeo para criar. O membro **VPGuid** da estrutura [**\_ VPCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contém um GUID que identifica exclusivamente o processador de vídeo. Passe este GUID para o método [**IDXVAHD \_ Device:: CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) . O método retorna um ponteiro [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) .
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  Opcionalmente, chame [**IDXVAHD \_ Device:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) para criar uma matriz de superfícies de vídeo de entrada.

O exemplo de código a seguir mostra a sequência completa de etapas:


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



A função CreateVPDevice mostrada neste exemplo cria o processador de vídeo (etapas 5 a 7):


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



