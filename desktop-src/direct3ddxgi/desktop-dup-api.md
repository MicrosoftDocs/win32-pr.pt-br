---
description: Windows 8 desabilita os drivers de espelho do XDDM (modelo de Driver de vídeo) padrão Windows 2000 e oferece a API de duplicação de desktop em vez disso.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: API de duplicação da Área de Trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c1960d064d7fd1e34748dcc2efb3c86459b498df91b52c1384ef8698a37c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518456"
---
# <a name="desktop-duplication-api"></a>API de duplicação da Área de Trabalho

Windows 8 desabilita os drivers de espelho do XDDM (modelo de Driver de vídeo) padrão Windows 2000 e oferece a API de duplicação de desktop em vez disso. A API de duplicação de desktop fornece acesso remoto a uma imagem de área de trabalho para cenários de colaboração. Os aplicativos podem usar a API de duplicação de área de trabalho para acessar atualizações quadro a quadro para a área de trabalho. Como os aplicativos recebem atualizações para a imagem da área de trabalho em uma superfície DXGI, os aplicativos podem usar todo o poder da GPU para processar as atualizações da imagem.

-   [Atualizando os dados da imagem da área de trabalho](#updating-the-desktop-image-data)
-   [Girando a imagem da área de trabalho](#rotating-the-desktop-image)
-   [Atualizando o ponteiro da área de trabalho](#updating-the-desktop-pointer)
-   [Tópicos relacionados](#related-topics)

## <a name="updating-the-desktop-image-data"></a>Atualizando os dados da imagem da área de trabalho

DXGI fornece uma superfície que contém uma imagem de área de trabalho atual por meio do novo método [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) . O formato da imagem da área de trabalho é sempre o [**\_ formato dxgi \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) não importa qual é o modo de exibição atual. Junto com essa superfície, esses métodos [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) retornam os tipos indicados de informações que ajudam a determinar quais pixels dentro da superfície você precisa processar:

-   [**IDXGIOutputDuplication:: GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) retorna regiões sujas, que são retângulos não sobrepostos que indicam as áreas da imagem da área de trabalho que o sistema operacional atualizou desde que você processou a imagem da área de trabalho anterior.
-   [**IDXGIOutputDuplication:: GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) retorna regiões de movimentação, que são retângulos de pixels na imagem da área de trabalho que o sistema operacional moveu para outro local dentro da mesma imagem. Cada região de movimentação consiste em um retângulo de destino e um ponto de origem. O ponto de origem especifica o local de onde o sistema operacional copiou a região e o retângulo de destino especifica para onde o sistema operacional moveu essa região. As regiões de movimentação sempre são regiões não ampliadas para que a origem seja sempre do mesmo tamanho que o destino.

Suponha que a imagem da área de trabalho foi transmitida por uma conexão lenta ao seu aplicativo cliente remoto. A quantidade de dados enviados pela conexão é reduzida com o recebimento de apenas dados sobre como seu aplicativo cliente deve mover regiões de pixels em vez de dados de pixel reais. Para processar as movimentações, seu aplicativo cliente deve ter armazenado a última imagem completa.

Enquanto o sistema operacional acumula atualizações de imagem de área de trabalho não processadas, pode ficar sem espaço para armazenar com precisão as regiões de atualização. Nessa situação, o sistema operacional começa a acumular as atualizações, unindo-as com regiões de atualização existentes para abranger todas as novas atualizações. Como resultado, o sistema operacional abrange pixels que ainda não foram atualizados nesse quadro. Mas essa situação não produz problemas visuais em seu aplicativo cliente porque você recebe toda a imagem da área de trabalho e não apenas os pixels atualizados.

Para reconstruir a imagem da área de trabalho correta, o aplicativo cliente deve primeiro processar todas as regiões de movimentação e processar todas as regiões sujas. Uma dessas listas de regiões sujas e de movimentação pode estar completamente vazia. O código de exemplo do [exemplo de duplicação de área de trabalho](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) mostra como processar as regiões suja e mover em um único quadro:


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



## <a name="rotating-the-desktop-image"></a>Girando a imagem da área de trabalho

Você deve adicionar um código explícito ao seu aplicativo cliente de duplicação de área de trabalho para dar suporte a modos girados. Em um modo girado, a superfície que você recebe de [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) está sempre na orientação não girada e a imagem da área de trabalho é girada dentro da superfície. Por exemplo, se a área de trabalho estiver definida como 768x1024 às 90 graus de rotação, **AcquireNextFrame** retornará uma superfície de 1024x768 com a imagem da área de trabalho girada dentro dela. Aqui estão alguns exemplos de rotação.



| Modo de exibição definido no painel de controle de vídeo | Modo de exibição retornado por GDI ou DXGI | Superfície retornada de [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| paisagem de 1024x768                          | rotação de 1024x768 0 graus           | 1024x768 com \[ nova linha\] ![área de trabalho remota não girada](images/dxgi-outdupl-0-rotate.png)<br/>            |
| 1024x768 retrato                           | 768x1024 90 graus de rotação          | 1024x768 com \[ nova linha\] ![girado em 90 graus área de trabalho remota](images/dxgi-outdupl-90-rotate.png)<br/>   |
| paisagem de 1024x768 (invertido)                | rotação de nível de 1024x768 180         | 1024x768 com \[ nova linha\] ![girado em 180 graus área de trabalho remota](images/dxgi-outdupl-180-rotate.png)<br/> |
| 1024x768 retrato (invertido)                 | 768x1024 270 graus de rotação         | 1024x768 com \[ nova linha\] ![girado em 270 graus área de trabalho remota](images/dxgi-outdupl-270-rotate.png)<br/> |



 

O código em seu aplicativo cliente de duplicação de área de trabalho deve girar a imagem da área de trabalho apropriadamente antes de exibir a imagem da área de trabalho.

> [!Note]  
> Em cenários de vários monitores, você pode girar a imagem da área de trabalho para cada monitor de forma independente.

 

## <a name="updating-the-desktop-pointer"></a>Atualizando o ponteiro da área de trabalho

Você precisa usar a API de duplicação de área de trabalho para determinar se o aplicativo cliente deve desenhar a forma do ponteiro do mouse na imagem da área de trabalho. Ou o ponteiro do mouse já está desenhado na imagem da área de trabalho que [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) fornece ou o ponteiro do mouse é separado da imagem da área de trabalho. Se o ponteiro do mouse for desenhado na imagem da área de trabalho, os dados de posição do ponteiro relatados por **AcquireNextFrame** (no membro **PointerPosition** das informações de  quadro de OUTDUPL de dxgi que o parâmetro pFrameInfo apontam) indicarão que um ponteiro separado não está visível. [**\_ \_ \_**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) Se o adaptador gráfico sobrepor o ponteiro do mouse sobre a imagem da área de trabalho, **AcquireNextFrame** relatará que um ponteiro separado está visível. Portanto, seu aplicativo cliente deve desenhar a forma do ponteiro do mouse na imagem da área de trabalho para representar com precisão o que o usuário atual verá em seu monitor.

Para desenhar o ponteiro do mouse do desktop, use o membro **PointerPosition** de [**informações de quadro de dxgi \_ OUTDUPL \_ \_**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) do parâmetro *pFrameInfo* de [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) para determinar onde localizar o canto superior esquerdo do ponteiro do mouse na imagem da área de trabalho. Ao desenhar o primeiro quadro, você deve usar o método [**IDXGIOutputDuplication:: GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) para obter informações sobre a forma do ponteiro do mouse. Cada chamada para **AcquireNextFrame** para obter o próximo quadro também fornece a posição atual do ponteiro para esse quadro. Por outro lado, você precisará usar **GetFramePointerShape** novamente somente se a forma for alterada. Portanto, mantenha uma cópia da última imagem do ponteiro e use-a para desenhar na área de trabalho, a menos que a forma do ponteiro do mouse seja alterada.

> [!Note]  
> Junto com a imagem de forma do ponteiro, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) fornece o tamanho do local de ponto de acesso. O ponto de acesso é fornecido apenas para fins informativos. O local de onde desenhar a imagem do ponteiro é independente do ponto de HotSpot.

 

Este exemplo de código do [exemplo de duplicação de área de trabalho](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) mostra como obter a forma do ponteiro do mouse:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimoramentos de DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
