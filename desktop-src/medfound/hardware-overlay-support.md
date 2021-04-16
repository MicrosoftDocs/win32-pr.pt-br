---
description: Descreve como usar sobreposições de hardware no Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Suporte à sobreposição de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcae33cdf55de59bdcd074829d52b4c1c43ea5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764993"
---
# <a name="hardware-overlay-support"></a><span data-ttu-id="78287-103">Suporte à sobreposição de hardware</span><span class="sxs-lookup"><span data-stu-id="78287-103">Hardware Overlay Support</span></span>

<span data-ttu-id="78287-104">Uma sobreposição de hardware é uma área dedicada de memória de vídeo que pode ser sobreposta na superfície primária.</span><span class="sxs-lookup"><span data-stu-id="78287-104">A hardware overlay is a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="78287-105">Nenhuma cópia é executada quando a sobreposição é exibida.</span><span class="sxs-lookup"><span data-stu-id="78287-105">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="78287-106">A operação de sobreposição é executada no hardware, sem modificar os dados na superfície primária.</span><span class="sxs-lookup"><span data-stu-id="78287-106">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

<span data-ttu-id="78287-107">O uso de sobreposições de hardware para reprodução de vídeo era comum em versões anteriores do Windows, porque as sobreposições são eficientes para o conteúdo de vídeo com uma alta taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="78287-107">The use of hardware overlays for video playback was common in earlier versions of Windows, because overlays are efficient for video content with a high frame rate.</span></span> <span data-ttu-id="78287-108">A partir do Windows 7, o Direct3D 9 oferece suporte a sobreposições de hardware.</span><span class="sxs-lookup"><span data-stu-id="78287-108">Starting in Windows 7, Direct3D 9 supports hardware overlays.</span></span> <span data-ttu-id="78287-109">Esse suporte destina-se principalmente à reprodução de vídeo e difere em alguns aspectos das APIs do DirectDraw anteriores:</span><span class="sxs-lookup"><span data-stu-id="78287-109">This support is intended primarily for video playback, and differs in some respects from earlier DirectDraw APIs:</span></span>

-   <span data-ttu-id="78287-110">A sobreposição não pode ser reduzida, espelhada ou desentrelaçada.</span><span class="sxs-lookup"><span data-stu-id="78287-110">The overlay cannot be shrunk, mirrored, or deinterlaced.</span></span>
-   <span data-ttu-id="78287-111">Não há suporte para chaves de cor de origem e mesclagem alfa.</span><span class="sxs-lookup"><span data-stu-id="78287-111">Source color keys and alpha blending are not supported.</span></span>
-   <span data-ttu-id="78287-112">As sobreposições podem ser ampliadas se o hardware de sobreposição der suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="78287-112">Overlays can be stretched if the overlay hardware supports it.</span></span> <span data-ttu-id="78287-113">Caso contrário, não haverá suporte para o alongamento.</span><span class="sxs-lookup"><span data-stu-id="78287-113">Otherwise, stretching is not supported.</span></span> <span data-ttu-id="78287-114">Na prática, nem todos os drivers gráficos dão suporte ao alongamento.</span><span class="sxs-lookup"><span data-stu-id="78287-114">In practice, not all graphics drivers support stretching.</span></span>
-   <span data-ttu-id="78287-115">Cada dispositivo dá suporte a no máximo uma sobreposição.</span><span class="sxs-lookup"><span data-stu-id="78287-115">Each device supports at most one overlay.</span></span>
-   <span data-ttu-id="78287-116">A sobreposição é executada usando uma chave de cor de destino, mas o tempo de execução do Direct3D seleciona automaticamente a cor e desenha o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="78287-116">Overlay is performed using a destination color key, but the Direct3D runtime automatically selects the color and draws the destination rectangle.</span></span> <span data-ttu-id="78287-117">O Direct3D rastreia automaticamente a posição da janela e atualiza a posição da sobreposição sempre que **PresentEx** é chamado.</span><span class="sxs-lookup"><span data-stu-id="78287-117">Direct3D automatically tracks the position of the window and updates the overlay position whenever the **PresentEx** is called.</span></span>

### <a name="creating-a-hardware-overlay-surface"></a><span data-ttu-id="78287-118">Criando uma superfície de sobreposição de hardware</span><span class="sxs-lookup"><span data-stu-id="78287-118">Creating a Hardware Overlay Surface</span></span>

<span data-ttu-id="78287-119">Para consultar o suporte à sobreposição, chame **IDirect3D9:: GetDeviceCaps**.</span><span class="sxs-lookup"><span data-stu-id="78287-119">To query for overlay support, call **IDirect3D9::GetDeviceCaps**.</span></span> <span data-ttu-id="78287-120">Se o driver oferecer suporte à sobreposição de hardware, o sinalizador de **\_ sobreposição D3DCAPS** será definido no **D3DCAPS9. Arremate** membro.</span><span class="sxs-lookup"><span data-stu-id="78287-120">If the driver supports hardware overlay, the **D3DCAPS\_OVERLAY** flag is set in the **D3DCAPS9.Caps** member.</span></span>

<span data-ttu-id="78287-121">Para descobrir se há suporte para um formato de sobreposição específico para um determinado modo de exibição, chame [**IDirect3D9ExOverlayExtension:: CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span><span class="sxs-lookup"><span data-stu-id="78287-121">To find out whether a specific overlay format is supported for a given display mode, call [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span></span>

<span data-ttu-id="78287-122">Para criar a sobreposição, chame **IDirect3D9Ex:: CreateDeviceEx** e especifique o efeito de permuta de **\_ sobreposição de D3DSWAPEFFECT** .</span><span class="sxs-lookup"><span data-stu-id="78287-122">To create the overlay, call **IDirect3D9Ex::CreateDeviceEx** and specify the **D3DSWAPEFFECT\_OVERLAY** swap effect.</span></span> <span data-ttu-id="78287-123">O buffer de fundo pode usar um formato não RGB se o hardware oferecer suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="78287-123">The back buffer can use a non-RGB format if the hardware supports it.</span></span>

<span data-ttu-id="78287-124">As superfícies de sobreposição têm as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="78287-124">Overlay surfaces have the following limitations:</span></span>

-   <span data-ttu-id="78287-125">O aplicativo não pode criar mais de uma cadeia de troca de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="78287-125">The application cannot create more than one overlay swap chain.</span></span>
-   <span data-ttu-id="78287-126">A sobreposição deve ser usada no modo de janela.</span><span class="sxs-lookup"><span data-stu-id="78287-126">The overlay must be used in windowed mode.</span></span> <span data-ttu-id="78287-127">Ele não pode ser usado no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="78287-127">It cannot be used in fullscreen mode.</span></span>
-   <span data-ttu-id="78287-128">O efeito de troca de sobreposição deve ser usado com a interface **IDirect3DDevice9Ex** .</span><span class="sxs-lookup"><span data-stu-id="78287-128">The overlay swap effect must be used with the **IDirect3DDevice9Ex** interface.</span></span> <span data-ttu-id="78287-129">Não há suporte para **IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="78287-129">It is not supported for **IDirect3DDevice9**.</span></span>
-   <span data-ttu-id="78287-130">A multiamostragem não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="78287-130">Multisampling cannot be used.</span></span>
-   <span data-ttu-id="78287-131">Os sinalizadores **D3DPRESENT \_ DONOTFLIP** e **D3DPRESENT \_ FLIPRESTART** não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="78287-131">The **D3DPRESENT\_DONOTFLIP** and **D3DPRESENT\_FLIPRESTART** flags are not supported.</span></span>
-   <span data-ttu-id="78287-132">As estatísticas de apresentação não estão disponíveis para a superfície de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="78287-132">Presentation statistics are not available for the overlay surface.</span></span>

<span data-ttu-id="78287-133">Se o hardware não der suporte à ampliação, é recomendável criar uma cadeia de permuta tão grande quanto o modo de exibição, para que a janela possa ser redimensionada para qualquer dimensão.</span><span class="sxs-lookup"><span data-stu-id="78287-133">If the hardware does not support stretching, it is recommended to create a swap chain as large as the display mode, so that the window can be resized to any dimensions.</span></span> <span data-ttu-id="78287-134">Recriar a cadeia de permuta não é uma maneira ideal de manipular o redimensionamento da janela, pois pode causar artefatos de renderização graves.</span><span class="sxs-lookup"><span data-stu-id="78287-134">Recreating the swap chain is not an optimal way to handle resizing the window, because it can cause severe rendering artifacts.</span></span> <span data-ttu-id="78287-135">Além disso, devido à maneira como a GPU gerencia a sobreposição de memória, a recriação da cadeia de permuta pode fazer com que um aplicativo fique sem memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78287-135">Also, because of the way the GPU manages the overlay memory, recreating the swap chain can potentially cause an application to run out of video memory.</span></span>

### <a name="new-d3dpresent_parameters-flags"></a><span data-ttu-id="78287-136">Sinalizadores de novos parâmetros de D3DPRESENT \_</span><span class="sxs-lookup"><span data-stu-id="78287-136">New D3DPRESENT\_PARAMETERS Flags</span></span>

<span data-ttu-id="78287-137">Os sinalizadores **de \_ parâmetros D3DPRESENT** a seguir são definidos para a criação de sobreposições.</span><span class="sxs-lookup"><span data-stu-id="78287-137">The following **D3DPRESENT\_PARAMETERS** flags are defined for creating overlays.</span></span>



| <span data-ttu-id="78287-138">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="78287-138">Flag</span></span>                                      | <span data-ttu-id="78287-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="78287-139">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78287-140">**D3DPRESENTFLAG \_ Overlay \_ LIMITEDRGB**</span><span class="sxs-lookup"><span data-stu-id="78287-140">**D3DPRESENTFLAG\_OVERLAY\_LIMITEDRGB**</span></span>   | <span data-ttu-id="78287-141">O intervalo RGB é de 16 a 235.</span><span class="sxs-lookup"><span data-stu-id="78287-141">The RGB range is 16–235.</span></span> <span data-ttu-id="78287-142">O padrão é 0 – 255.</span><span class="sxs-lookup"><span data-stu-id="78287-142">The default is 0–255.</span></span> <br/> <span data-ttu-id="78287-143">Requer o recurso **D3DOVERLAYCAPS \_ LIMITEDRANGERGB** .</span><span class="sxs-lookup"><span data-stu-id="78287-143">Requires the **D3DOVERLAYCAPS\_LIMITEDRANGERGB** capability.</span></span><br/>                                                 |
| <span data-ttu-id="78287-144">**D3DPRESENTFLAG \_ Overlay \_ YCbCr \_ BT709**</span><span class="sxs-lookup"><span data-stu-id="78287-144">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_BT709**</span></span> | <span data-ttu-id="78287-145">As cores YUV usam a definição BT. 709.</span><span class="sxs-lookup"><span data-stu-id="78287-145">YUV colors use the BT.709 definition.</span></span> <span data-ttu-id="78287-146">O padrão é BT. 601.</span><span class="sxs-lookup"><span data-stu-id="78287-146">The default is BT.601.</span></span> <br/> <span data-ttu-id="78287-147">Requer o recurso **D3DOVERLAYCAPS \_ YCbCr \_ BT709** .</span><span class="sxs-lookup"><span data-stu-id="78287-147">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT709** capability.</span></span><br/>                                      |
| <span data-ttu-id="78287-148">**D3DPRESENTFLAG \_ Overlay \_ YCbCr \_ xvYCC**</span><span class="sxs-lookup"><span data-stu-id="78287-148">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_xvYCC**</span></span> | <span data-ttu-id="78287-149">Gere os dados usando o YCbCr estendido (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="78287-149">Output the data by using extended YCbCr (xvYCC).</span></span><br/> <span data-ttu-id="78287-150">Requer o recurso **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** ou **D3DOVERLAYCAPS \_ YCbCr BT709 \_ \_** xvYCC.</span><span class="sxs-lookup"><span data-stu-id="78287-150">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT601\_xvYCC** or **D3DOVERLAYCAPS\_YCbCr\_BT709\_xvYCC** capability.</span></span><br/> |



 

### <a name="using-hardware-overlays"></a><span data-ttu-id="78287-151">Usando sobreposições de hardware</span><span class="sxs-lookup"><span data-stu-id="78287-151">Using Hardware Overlays</span></span>

<span data-ttu-id="78287-152">Para exibir a superfície de sobreposição, o aplicativo chama **IDirect3DDevice9Ex::P resentex**.</span><span class="sxs-lookup"><span data-stu-id="78287-152">To display the overlay surface, the application calls **IDirect3DDevice9Ex::PresentEx**.</span></span> <span data-ttu-id="78287-153">O tempo de execução do Direct3D automaticamente desenha a chave de cor de destino.</span><span class="sxs-lookup"><span data-stu-id="78287-153">The Direct3D runtime automatically draws the destination color key.</span></span>

<span data-ttu-id="78287-154">Os sinalizadores **PresentEx** a seguir são definidos para sobreposições.</span><span class="sxs-lookup"><span data-stu-id="78287-154">The following **PresentEx** flags are defined for overlays.</span></span>



| <span data-ttu-id="78287-155">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="78287-155">Flag</span></span>                              | <span data-ttu-id="78287-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="78287-156">Description</span></span>                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78287-157">**D3DPRESENT \_ UPDATECOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="78287-157">**D3DPRESENT\_UPDATECOLORKEY**</span></span>    | <span data-ttu-id="78287-158">Defina esse sinalizador se a composição de Gerenciador de Janelas da Área de Trabalho (DWM) estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="78287-158">Set this flag if Desktop Window Manager (DWM) composition is disabled.</span></span> <span data-ttu-id="78287-159">Esse sinalizador faz com que o Direct3D redesenhe a chave de cor.</span><span class="sxs-lookup"><span data-stu-id="78287-159">This flag causes Direct3D to redraw the color key.</span></span><br/> <span data-ttu-id="78287-160">Se o DWM estiver habilitado, esse sinalizador não será necessário, pois o Direct3D desenha a chave de cor uma vez na superfície que o DWM usa para o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="78287-160">If DWM is enabled, this flag is not required, because Direct3D draws the color key once on the surface that DWM uses for redirection.</span></span><br/> |
| <span data-ttu-id="78287-161">**D3DPRESENT \_ HIDEOVERLAY**</span><span class="sxs-lookup"><span data-stu-id="78287-161">**D3DPRESENT\_HIDEOVERLAY**</span></span>       | <span data-ttu-id="78287-162">Oculta a sobreposição.</span><span class="sxs-lookup"><span data-stu-id="78287-162">Hides the overlay.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="78287-163">**D3DPRESENT \_ UPDATEOVERLAYONLY**</span><span class="sxs-lookup"><span data-stu-id="78287-163">**D3DPRESENT\_UPDATEOVERLAYONLY**</span></span> | <span data-ttu-id="78287-164">Atualiza a sobreposição sem alterar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="78287-164">Updates the overlay without changing the contents.</span></span><br/> <span data-ttu-id="78287-165">Esse sinalizador será útil se a janela for movida enquanto o vídeo estiver em pausa.</span><span class="sxs-lookup"><span data-stu-id="78287-165">This flag is useful if the window moves while the video is paused.</span></span><br/>                                                                                                                                           |



 

<span data-ttu-id="78287-166">Um aplicativo deve estar preparado para lidar com os seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="78287-166">An application should be prepared to handle the following cases:</span></span>

-   <span data-ttu-id="78287-167">Se outro aplicativo estiver usando a sobreposição, **PresentEx** retornará **D3DERR \_ não disponível**.</span><span class="sxs-lookup"><span data-stu-id="78287-167">If another application is using the overlay, **PresentEx** returns **D3DERR\_NOTAVAILABLE**.</span></span>
-   <span data-ttu-id="78287-168">Se a janela for movida para outro monitor, o aplicativo deverá recriar a cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="78287-168">If the window is moved to another monitor, the application must recreate the swap chain.</span></span> <span data-ttu-id="78287-169">Caso contrário, se o aplicativo chamar **PresentEx** para exibir a sobreposição em um monitor diferente, **PresentEx** retornará **D3DERR \_ INVALIDDEVICE**.</span><span class="sxs-lookup"><span data-stu-id="78287-169">Otherwise, if the application calls **PresentEx** to display the overlay on a different monitor, **PresentEx** returns **D3DERR\_INVALIDDEVICE**.</span></span>
-   <span data-ttu-id="78287-170">Se o modo de exibição for alterado, o Direct3D tentará restaurar a sobreposição.</span><span class="sxs-lookup"><span data-stu-id="78287-170">If the display mode changes, Direct3D attempts to restore the overlay.</span></span> <span data-ttu-id="78287-171">Se o novo modo não oferecer suporte à sobreposição, **PresentEx** retornará **D3DERR \_ UNSUPPORTEDOVERLAY**.</span><span class="sxs-lookup"><span data-stu-id="78287-171">If the new mode does not support the overlay, **PresentEx** returns **D3DERR\_UNSUPPORTEDOVERLAY**.</span></span>

### <a name="example-code"></a><span data-ttu-id="78287-172">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="78287-172">Example Code</span></span>

<span data-ttu-id="78287-173">O exemplo a seguir mostra como criar uma superfície de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="78287-173">The following example shows how to create an overlay surface.</span></span>


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="78287-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78287-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78287-175">APIs de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="78287-175">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 




