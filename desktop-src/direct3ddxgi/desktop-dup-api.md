---
description: O Windows 8 desabilita os drivers de espelho padrão do Windows 2000 Display Driver Model (XDDM) e oferece a API de duplicação de desktop em vez disso.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: API de duplicação da Área de Trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad27f545318254404beb6372344d8dd0cdfdf604
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456464"
---
# <a name="desktop-duplication-api"></a><span data-ttu-id="04fa0-103">API de duplicação da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="04fa0-103">Desktop Duplication API</span></span>

<span data-ttu-id="04fa0-104">O Windows 8 desabilita os drivers de espelho padrão do Windows 2000 Display Driver Model (XDDM) e oferece a API de duplicação de desktop em vez disso.</span><span class="sxs-lookup"><span data-stu-id="04fa0-104">Windows 8 disables standard Windows 2000 Display Driver Model (XDDM) mirror drivers and offers the desktop duplication API instead.</span></span> <span data-ttu-id="04fa0-105">A API de duplicação de desktop fornece acesso remoto a uma imagem de área de trabalho para cenários de colaboração.</span><span class="sxs-lookup"><span data-stu-id="04fa0-105">The desktop duplication API provides remote access to a desktop image for collaboration scenarios.</span></span> <span data-ttu-id="04fa0-106">Os aplicativos podem usar a API de duplicação de área de trabalho para acessar atualizações quadro a quadro para a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="04fa0-106">Apps can use the desktop duplication API to access frame-by-frame updates to the desktop.</span></span> <span data-ttu-id="04fa0-107">Como os aplicativos recebem atualizações para a imagem da área de trabalho em uma superfície DXGI, os aplicativos podem usar todo o poder da GPU para processar as atualizações da imagem.</span><span class="sxs-lookup"><span data-stu-id="04fa0-107">Because apps receive updates to the desktop image in a DXGI surface, the apps can use the full power of the GPU to process the image updates.</span></span>

-   [<span data-ttu-id="04fa0-108">Atualizando os dados da imagem da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="04fa0-108">Updating the desktop image data</span></span>](#updating-the-desktop-image-data)
-   [<span data-ttu-id="04fa0-109">Girando a imagem da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="04fa0-109">Rotating the desktop image</span></span>](#rotating-the-desktop-image)
-   [<span data-ttu-id="04fa0-110">Atualizando o ponteiro da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="04fa0-110">Updating the desktop pointer</span></span>](#updating-the-desktop-pointer)
-   [<span data-ttu-id="04fa0-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04fa0-111">Related topics</span></span>](#related-topics)

## <a name="updating-the-desktop-image-data"></a><span data-ttu-id="04fa0-112">Atualizando os dados da imagem da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="04fa0-112">Updating the desktop image data</span></span>

<span data-ttu-id="04fa0-113">DXGI fornece uma superfície que contém uma imagem de área de trabalho atual por meio do novo método [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) .</span><span class="sxs-lookup"><span data-stu-id="04fa0-113">DXGI provides a surface that contains a current desktop image through the new [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) method.</span></span> <span data-ttu-id="04fa0-114">O formato da imagem da área de trabalho é sempre o [**\_ formato dxgi \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) não importa qual é o modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="04fa0-114">The format of the desktop image is always [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) no matter what the current display mode is.</span></span> <span data-ttu-id="04fa0-115">Junto com essa superfície, esses métodos [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) retornam os tipos indicados de informações que ajudam a determinar quais pixels dentro da superfície você precisa processar:</span><span class="sxs-lookup"><span data-stu-id="04fa0-115">Along with this surface, these [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) methods return the indicated types of info that help you determine which pixels within the surface you need to process:</span></span>

-   <span data-ttu-id="04fa0-116">[**IDXGIOutputDuplication:: GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) retorna regiões sujas, que são retângulos não sobrepostos que indicam as áreas da imagem da área de trabalho que o sistema operacional atualizou desde que você processou a imagem da área de trabalho anterior.</span><span class="sxs-lookup"><span data-stu-id="04fa0-116">[**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) returns dirty regions, which are non-overlapping rectangles that indicate the areas of the desktop image that the operating system updated since you processed the previous desktop image.</span></span>
-   <span data-ttu-id="04fa0-117">[**IDXGIOutputDuplication:: GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) retorna regiões de movimentação, que são retângulos de pixels na imagem da área de trabalho que o sistema operacional moveu para outro local dentro da mesma imagem.</span><span class="sxs-lookup"><span data-stu-id="04fa0-117">[**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) returns move regions, which are rectangles of pixels in the desktop image that the operating system moved to another location within the same image.</span></span> <span data-ttu-id="04fa0-118">Cada região de movimentação consiste em um retângulo de destino e um ponto de origem.</span><span class="sxs-lookup"><span data-stu-id="04fa0-118">Each move region consists of a destination rectangle and a source point.</span></span> <span data-ttu-id="04fa0-119">O ponto de origem especifica o local de onde o sistema operacional copiou a região e o retângulo de destino especifica para onde o sistema operacional moveu essa região.</span><span class="sxs-lookup"><span data-stu-id="04fa0-119">The source point specifies the location from where the operating system copied the region and the destination rectangle specifies to where the operating system moved that region.</span></span> <span data-ttu-id="04fa0-120">As regiões de movimentação sempre são regiões não ampliadas para que a origem seja sempre do mesmo tamanho que o destino.</span><span class="sxs-lookup"><span data-stu-id="04fa0-120">Move regions are always non-stretched regions so the source is always the same size as the destination.</span></span>

<span data-ttu-id="04fa0-121">Suponha que a imagem da área de trabalho foi transmitida por uma conexão lenta ao seu aplicativo cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="04fa0-121">Suppose the desktop image was transmitted over a slow connection to your remote client app.</span></span> <span data-ttu-id="04fa0-122">A quantidade de dados enviados pela conexão é reduzida com o recebimento de apenas dados sobre como seu aplicativo cliente deve mover regiões de pixels em vez de dados de pixel reais.</span><span class="sxs-lookup"><span data-stu-id="04fa0-122">The amount of data that is sent over the connection is reduced by receiving only data about how your client app must move regions of pixels rather than actual pixel data.</span></span> <span data-ttu-id="04fa0-123">Para processar as movimentações, seu aplicativo cliente deve ter armazenado a última imagem completa.</span><span class="sxs-lookup"><span data-stu-id="04fa0-123">To process the moves, your client app must have stored the complete last image.</span></span>

<span data-ttu-id="04fa0-124">Enquanto o sistema operacional acumula atualizações de imagem de área de trabalho não processadas, pode ficar sem espaço para armazenar com precisão as regiões de atualização.</span><span class="sxs-lookup"><span data-stu-id="04fa0-124">While the operating system accumulates unprocessed desktop image updates, it might run out of space to accurately store the update regions.</span></span> <span data-ttu-id="04fa0-125">Nessa situação, o sistema operacional começa a acumular as atualizações, unindo-as com regiões de atualização existentes para abranger todas as novas atualizações.</span><span class="sxs-lookup"><span data-stu-id="04fa0-125">In this situation, the operating system starts to accumulate the updates by coalescing them with existing update regions to cover all new updates.</span></span> <span data-ttu-id="04fa0-126">Como resultado, o sistema operacional abrange pixels que ainda não foram atualizados nesse quadro.</span><span class="sxs-lookup"><span data-stu-id="04fa0-126">As a result, the operating system covers pixels that it has not actually updated in that frame yet.</span></span> <span data-ttu-id="04fa0-127">Mas essa situação não produz problemas visuais em seu aplicativo cliente porque você recebe toda a imagem da área de trabalho e não apenas os pixels atualizados.</span><span class="sxs-lookup"><span data-stu-id="04fa0-127">But this situation doesn’t produce visual issues on your client app because you receive the entire desktop image and not just the updated pixels.</span></span>

<span data-ttu-id="04fa0-128">Para reconstruir a imagem da área de trabalho correta, o aplicativo cliente deve primeiro processar todas as regiões de movimentação e processar todas as regiões sujas.</span><span class="sxs-lookup"><span data-stu-id="04fa0-128">To reconstruct the correct desktop image, your client app must first process all the move regions and then process all the dirty regions.</span></span> <span data-ttu-id="04fa0-129">Uma dessas listas de regiões sujas e de movimentação pode estar completamente vazia.</span><span class="sxs-lookup"><span data-stu-id="04fa0-129">Either of these lists of dirty and move regions can be completely empty.</span></span> <span data-ttu-id="04fa0-130">O código de exemplo do [exemplo de duplicação de área de trabalho](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) mostra como processar as regiões suja e mover em um único quadro:</span><span class="sxs-lookup"><span data-stu-id="04fa0-130">The example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to process both the dirty and move regions in a single frame:</span></span>


```C++
//
// Get next frame and write it into Data
//
HRESULT DUPLICATIONMANAGER::GetFrame(_Out_ FRAME_DATA* Data)
{
    HRESULT hr = S_OK;

    IDXGIResource* DesktopResource = NULL;
    DXGI_OUTDUPL_FRAME_INFO FrameInfo;

    //Get new frame
    hr = DeskDupl->AcquireNextFrame(500, &FrameInfo, &DesktopResource);
    if (FAILED(hr))
    {
        if ((hr != DXGI_ERROR_ACCESS_LOST) && (hr != DXGI_ERROR_WAIT_TIMEOUT))
        {
            DisplayErr(L"Failed to acquire next frame in DUPLICATIONMANAGER", L"Error", hr);
        }
        return hr;
    }

    // If still holding old frame, destroy it
    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    // QI for IDXGIResource
    hr = DesktopResource->QueryInterface(__uuidof(ID3D11Texture2D), reinterpret_cast<void **>(&AcquiredDesktopImage));
    DesktopResource->Release();
    DesktopResource = NULL;
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to QI for ID3D11Texture2D from acquired IDXGIResource in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    // Get metadata
    if (FrameInfo.TotalMetadataBufferSize)
    {
        // Old buffer too small
        if (FrameInfo.TotalMetadataBufferSize > MetaDataSize)
        {
            if (MetaDataBuffer)
            {
                delete [] MetaDataBuffer;
                MetaDataBuffer = NULL;
            }
            MetaDataBuffer = new (std::nothrow) BYTE[FrameInfo.TotalMetadataBufferSize];
            if (!MetaDataBuffer)
            {
                DisplayErr(L"Failed to allocate memory for metadata in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
                MetaDataSize = 0;
                Data->MoveCount = 0;
                Data->DirtyCount = 0;
                return E_OUTOFMEMORY;
            }
            MetaDataSize = FrameInfo.TotalMetadataBufferSize;
        }

        UINT BufSize = FrameInfo.TotalMetadataBufferSize;

        // Get move rectangles
        hr = DeskDupl->GetFrameMoveRects(BufSize, reinterpret_cast<DXGI_OUTDUPL_MOVE_RECT*>(MetaDataBuffer), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame move rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->MoveCount = BufSize / sizeof(DXGI_OUTDUPL_MOVE_RECT);

        BYTE* DirtyRects = MetaDataBuffer + BufSize;
        BufSize = FrameInfo.TotalMetadataBufferSize - BufSize;

        // Get dirty rectangles
        hr = DeskDupl->GetFrameDirtyRects(BufSize, reinterpret_cast<RECT*>(DirtyRects), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame dirty rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->DirtyCount = BufSize / sizeof(RECT);

        Data->MetaData = MetaDataBuffer;
    }

    Data->Frame = AcquiredDesktopImage;
    Data->FrameInfo = FrameInfo;

    return hr;
}

//
// Release frame
//
HRESULT DUPLICATIONMANAGER::DoneWithFrame()
{
    HRESULT hr = S_OK;

    hr = DeskDupl->ReleaseFrame();
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to release frame in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    return hr;
}
```



## <a name="rotating-the-desktop-image"></a><span data-ttu-id="04fa0-131">Girando a imagem da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="04fa0-131">Rotating the desktop image</span></span>

<span data-ttu-id="04fa0-132">Você deve adicionar um código explícito ao seu aplicativo cliente de duplicação de área de trabalho para dar suporte a modos girados.</span><span class="sxs-lookup"><span data-stu-id="04fa0-132">You must add explicit code to your desktop duplication client app to support rotated modes.</span></span> <span data-ttu-id="04fa0-133">Em um modo girado, a superfície que você recebe de [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) está sempre na orientação não girada e a imagem da área de trabalho é girada dentro da superfície.</span><span class="sxs-lookup"><span data-stu-id="04fa0-133">In a rotated mode, the surface that you receive from [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) is always in the un-rotated orientation, and the desktop image is rotated within the surface.</span></span> <span data-ttu-id="04fa0-134">Por exemplo, se a área de trabalho estiver definida como 768x1024 às 90 graus de rotação, **AcquireNextFrame** retornará uma superfície de 1024x768 com a imagem da área de trabalho girada dentro dela.</span><span class="sxs-lookup"><span data-stu-id="04fa0-134">For example, if the desktop is set to 768x1024 at 90 degrees rotation, **AcquireNextFrame** returns a 1024x768 surface with the desktop image rotated within it.</span></span> <span data-ttu-id="04fa0-135">Aqui estão alguns exemplos de rotação.</span><span class="sxs-lookup"><span data-stu-id="04fa0-135">Here are some rotation examples.</span></span>



| <span data-ttu-id="04fa0-136">Modo de exibição definido no painel de controle de vídeo</span><span class="sxs-lookup"><span data-stu-id="04fa0-136">Display mode set from display control panel</span></span> | <span data-ttu-id="04fa0-137">Modo de exibição retornado por GDI ou DXGI</span><span class="sxs-lookup"><span data-stu-id="04fa0-137">Display mode returned by GDI or DXGI</span></span> | <span data-ttu-id="04fa0-138">Superfície retornada de [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span><span class="sxs-lookup"><span data-stu-id="04fa0-138">Surface returned from [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span></span>                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04fa0-139">paisagem de 1024x768</span><span class="sxs-lookup"><span data-stu-id="04fa0-139">1024x768 landscape</span></span>                          | <span data-ttu-id="04fa0-140">rotação de 1024x768 0 graus</span><span class="sxs-lookup"><span data-stu-id="04fa0-140">1024x768 0 degree rotation</span></span>           | <span data-ttu-id="04fa0-141">1024x768 com \[ nova linha\]</span><span class="sxs-lookup"><span data-stu-id="04fa0-141">1024x768\[newline\]</span></span> ![área de trabalho remota não girada](images/dxgi-outdupl-0-rotate.png)<br/>            |
| <span data-ttu-id="04fa0-143">1024x768 retrato</span><span class="sxs-lookup"><span data-stu-id="04fa0-143">1024x768 portrait</span></span>                           | <span data-ttu-id="04fa0-144">768x1024 90 graus de rotação</span><span class="sxs-lookup"><span data-stu-id="04fa0-144">768x1024 90 degree rotation</span></span>          | <span data-ttu-id="04fa0-145">1024x768 com \[ nova linha\]</span><span class="sxs-lookup"><span data-stu-id="04fa0-145">1024x768\[newline\]</span></span> ![girado em 90 graus área de trabalho remota](images/dxgi-outdupl-90-rotate.png)<br/>   |
| <span data-ttu-id="04fa0-147">paisagem de 1024x768 (invertido)</span><span class="sxs-lookup"><span data-stu-id="04fa0-147">1024x768 landscape (flipped)</span></span>                | <span data-ttu-id="04fa0-148">rotação de nível de 1024x768 180</span><span class="sxs-lookup"><span data-stu-id="04fa0-148">1024x768 180 degree rotation</span></span>         | <span data-ttu-id="04fa0-149">1024x768 com \[ nova linha\]</span><span class="sxs-lookup"><span data-stu-id="04fa0-149">1024x768\[newline\]</span></span> ![girado em 180 graus área de trabalho remota](images/dxgi-outdupl-180-rotate.png)<br/> |
| <span data-ttu-id="04fa0-151">1024x768 retrato (invertido)</span><span class="sxs-lookup"><span data-stu-id="04fa0-151">1024x768 portrait (flipped)</span></span>                 | <span data-ttu-id="04fa0-152">768x1024 270 graus de rotação</span><span class="sxs-lookup"><span data-stu-id="04fa0-152">768x1024 270 degree rotation</span></span>         | <span data-ttu-id="04fa0-153">1024x768 com \[ nova linha\]</span><span class="sxs-lookup"><span data-stu-id="04fa0-153">1024x768\[newline\]</span></span> ![girado em 270 graus área de trabalho remota](images/dxgi-outdupl-270-rotate.png)<br/> |



 

<span data-ttu-id="04fa0-155">O código em seu aplicativo cliente de duplicação de área de trabalho deve girar a imagem da área de trabalho apropriadamente antes de exibir a imagem da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="04fa0-155">The code in your desktop duplication client app must rotate the desktop image appropriately before you display the desktop image.</span></span>

> [!Note]  
> <span data-ttu-id="04fa0-156">Em cenários de vários monitores, você pode girar a imagem da área de trabalho para cada monitor de forma independente.</span><span class="sxs-lookup"><span data-stu-id="04fa0-156">In multi-monitor scenarios, you can rotate the desktop image for each monitor independently.</span></span>

 

## <a name="updating-the-desktop-pointer"></a><span data-ttu-id="04fa0-157">Atualizando o ponteiro da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="04fa0-157">Updating the desktop pointer</span></span>

<span data-ttu-id="04fa0-158">Você precisa usar a API de duplicação de área de trabalho para determinar se o aplicativo cliente deve desenhar a forma do ponteiro do mouse na imagem da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="04fa0-158">You need to use the desktop duplication API to determine if your client app must draw the mouse pointer shape onto the desktop image.</span></span> <span data-ttu-id="04fa0-159">Ou o ponteiro do mouse já está desenhado na imagem da área de trabalho que [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) fornece ou o ponteiro do mouse é separado da imagem da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="04fa0-159">Either the mouse pointer is already drawn onto the desktop image that [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) provides or the mouse pointer is separate from the desktop image.</span></span> <span data-ttu-id="04fa0-160">Se o ponteiro do mouse for desenhado na imagem da área de trabalho, os dados de posição do ponteiro relatados por **AcquireNextFrame** (no membro **PointerPosition** das informações de  quadro de OUTDUPL de dxgi que o parâmetro pFrameInfo apontam) indicarão que um ponteiro separado não está visível. [**\_ \_ \_**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info)</span><span class="sxs-lookup"><span data-stu-id="04fa0-160">If the mouse pointer is drawn onto the desktop image, the pointer position data that is reported by **AcquireNextFrame** (in the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) that the *pFrameInfo* parameter points to) indicates that a separate pointer isn’t visible.</span></span> <span data-ttu-id="04fa0-161">Se o adaptador gráfico sobrepor o ponteiro do mouse sobre a imagem da área de trabalho, **AcquireNextFrame** relatará que um ponteiro separado está visível.</span><span class="sxs-lookup"><span data-stu-id="04fa0-161">If the graphics adapter overlays the mouse pointer on top of the desktop image, **AcquireNextFrame** reports that a separate pointer is visible.</span></span> <span data-ttu-id="04fa0-162">Portanto, seu aplicativo cliente deve desenhar a forma do ponteiro do mouse na imagem da área de trabalho para representar com precisão o que o usuário atual verá em seu monitor.</span><span class="sxs-lookup"><span data-stu-id="04fa0-162">So, your client app must draw the mouse pointer shape onto the desktop image to accurately represent what the current user will see on their monitor.</span></span>

<span data-ttu-id="04fa0-163">Para desenhar o ponteiro do mouse do desktop, use o membro **PointerPosition** de [**informações de quadro de dxgi \_ OUTDUPL \_ \_**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) do parâmetro *pFrameInfo* de [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) para determinar onde localizar o canto superior esquerdo do ponteiro do mouse na imagem da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="04fa0-163">To draw the desktop’s mouse pointer, use the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) from the *pFrameInfo* parameter of [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) to determine where to locate the top left hand corner of the mouse pointer on the desktop image.</span></span> <span data-ttu-id="04fa0-164">Ao desenhar o primeiro quadro, você deve usar o método [**IDXGIOutputDuplication:: GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) para obter informações sobre a forma do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="04fa0-164">When you draw the first frame, you must use the [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) method to obtain info about the shape of the mouse pointer.</span></span> <span data-ttu-id="04fa0-165">Cada chamada para **AcquireNextFrame** para obter o próximo quadro também fornece a posição atual do ponteiro para esse quadro.</span><span class="sxs-lookup"><span data-stu-id="04fa0-165">Each call to **AcquireNextFrame** to get the next frame also provides the current pointer position for that frame.</span></span> <span data-ttu-id="04fa0-166">Por outro lado, você precisará usar **GetFramePointerShape** novamente somente se a forma for alterada.</span><span class="sxs-lookup"><span data-stu-id="04fa0-166">On the other hand, you need to use **GetFramePointerShape** again only if the shape changes.</span></span> <span data-ttu-id="04fa0-167">Portanto, mantenha uma cópia da última imagem do ponteiro e use-a para desenhar na área de trabalho, a menos que a forma do ponteiro do mouse seja alterada.</span><span class="sxs-lookup"><span data-stu-id="04fa0-167">So, keep a copy of the last pointer image and use it to draw on the desktop unless the shape of the mouse pointer changes.</span></span>

> [!Note]  
> <span data-ttu-id="04fa0-168">Junto com a imagem de forma do ponteiro, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) fornece o tamanho do local de ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="04fa0-168">Together with the pointer shape image, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) provides the size of the hot spot location.</span></span> <span data-ttu-id="04fa0-169">O ponto de acesso é fornecido apenas para fins informativos.</span><span class="sxs-lookup"><span data-stu-id="04fa0-169">The hot spot is given for informational purposes only.</span></span> <span data-ttu-id="04fa0-170">O local de onde desenhar a imagem do ponteiro é independente do ponto de HotSpot.</span><span class="sxs-lookup"><span data-stu-id="04fa0-170">The location of where to draw the pointer image is independent to the hotspot.</span></span>

 

<span data-ttu-id="04fa0-171">Este exemplo de código do [exemplo de duplicação de área de trabalho](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) mostra como obter a forma do ponteiro do mouse:</span><span class="sxs-lookup"><span data-stu-id="04fa0-171">This example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to get the mouse pointer shape:</span></span>


```C++
//
// Retrieves mouse info and write it into PtrInfo
//
HRESULT DUPLICATIONMANAGER::GetMouse(_Out_ PTR_INFO* PtrInfo, _In_ DXGI_OUTDUPL_FRAME_INFO* FrameInfo, INT OffsetX, INT OffsetY)
{
    HRESULT hr = S_OK;

    // A non-zero mouse update timestamp indicates that there is a mouse position update and optionally a shape change
    if (FrameInfo->LastMouseUpdateTime.QuadPart == 0)
    {
        return hr;
    }

    bool UpdatePosition = true;

    // Make sure we don't update pointer position wrongly
    // If pointer is invisible, make sure we did not get an update from another output that the last time that said pointer
    // was visible, if so, don't set it to invisible or update.
    if (!FrameInfo->PointerPosition.Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber))
    {
        UpdatePosition = false;
    }

    // If two outputs both say they have a visible, only update if new update has newer timestamp
    if (FrameInfo->PointerPosition.Visible && PtrInfo->Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber) && (PtrInfo->LastTimeStamp.QuadPart > FrameInfo->LastMouseUpdateTime.QuadPart))
    {
        UpdatePosition = false;
    }

    // Update position
    if (UpdatePosition)
    {
        PtrInfo->Position.x = FrameInfo->PointerPosition.Position.x + OutputDesc.DesktopCoordinates.left - OffsetX;
        PtrInfo->Position.y = FrameInfo->PointerPosition.Position.y + OutputDesc.DesktopCoordinates.top - OffsetY;
        PtrInfo->WhoUpdatedPositionLast = OutputNumber;
        PtrInfo->LastTimeStamp = FrameInfo->LastMouseUpdateTime;
        PtrInfo->Visible = FrameInfo->PointerPosition.Visible != 0;
    }

    // No new shape
    if (FrameInfo->PointerShapeBufferSize == 0)
    {
        return hr;
    }

    // Old buffer too small
    if (FrameInfo->PointerShapeBufferSize > PtrInfo->BufferSize)
    {
        if (PtrInfo->PtrShapeBuffer)
        {
            delete [] PtrInfo->PtrShapeBuffer;
            PtrInfo->PtrShapeBuffer = NULL;
        }
        PtrInfo->PtrShapeBuffer = new (std::nothrow) BYTE[FrameInfo->PointerShapeBufferSize];
        if (!PtrInfo->PtrShapeBuffer)
        {
            DisplayErr(L"Failed to allocate memory for pointer shape in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
            PtrInfo->BufferSize = 0;
            return E_OUTOFMEMORY;
        }

        // Update buffer size
        PtrInfo->BufferSize = FrameInfo->PointerShapeBufferSize;
    }

    UINT BufferSizeRequired;
    // Get shape
    hr = DeskDupl->GetFramePointerShape(FrameInfo->PointerShapeBufferSize, reinterpret_cast<VOID*>(PtrInfo->PtrShapeBuffer), &BufferSizeRequired, &(PtrInfo->ShapeInfo));
    if (FAILED(hr))
    {
        if (hr != DXGI_ERROR_ACCESS_LOST)
        {
            DisplayErr(L"Failed to get frame pointer shape in DUPLICATIONMANAGER", L"Error", hr);
        }
        delete [] PtrInfo->PtrShapeBuffer;
        PtrInfo->PtrShapeBuffer = NULL;
        PtrInfo->BufferSize = 0;
        return hr;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="04fa0-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04fa0-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04fa0-173">Aprimoramentos de DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="04fa0-173">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
