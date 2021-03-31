---
title: Como salvar o conteúdo do Direct2D em um arquivo de imagem
description: Este tópico mostra como usar o IWICImageEncoder para salvar o conteúdo na forma de um ID2D1Image em um arquivo de imagem codificado, como JPEG.
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19146d838474046fd634cb5524ddf2367fd1d6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823814"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a>Como salvar o conteúdo do Direct2D em um arquivo de imagem

Este tópico mostra como usar o [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) para salvar o conteúdo na forma de um [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) em um arquivo de imagem codificado, como JPEG. Se você estiver escrevendo um aplicativo da Windows Store, poderá fazer com que o usuário selecione um arquivo de destino usando [**Windows:: Storage::P ickers:: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Direct2D](./direct2d-portal.md)
-   [Efeitos de Direct2D](effects-overview.md)
-   [**Windows:: armazenamento::P ickers:: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a>Pré-requisitos

-   Você precisa de um objeto [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e de um objeto que contenha conteúdo [Direct2D](./direct2d-portal.md) que implementa [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) como [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) ou [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).

## <a name="instructions"></a>Instruções

### <a name="step-1-get-a-destination-file-and-stream"></a>Etapa 1: obter um arquivo de destino e um fluxo

Se você quiser permitir que o usuário selecione um arquivo de destino, poderá usar [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), abrir o arquivo retornado e obter um [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) para usar com o WIC.

Crie um [**Windows:: Storage::P ickers:: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) e defina seus parâmetros para arquivos de imagem. Chame o método [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) .


```C++
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    savePicker->DefaultFileExtension = ".jpg";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
```



Declare um manipulador de conclusão para ser executado depois que a operação assíncrona de seletor de arquivo retornar. Use o método [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) para recuperar o arquivo e obter o objeto de fluxo de arquivo.


```C++
    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }
```



Obtenha um [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) chamando [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) no arquivo e obtendo o resultado da operação assíncrona.


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



Por fim, use o método [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) para converter o fluxo de arquivos. Windows Runtime APIs representam fluxos com [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), enquanto o WIC consome [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> Para usar a função [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , você deve incluir **shcore. h** em seu projeto.

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a>Etapa 2: obter o bitmap do WIC e o codificador de quadros

[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) fornecem a funcionalidade para salvar dados de imagem em um formato de arquivo codificado.

Crie e inicialize os objetos do codificador.


```C++
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );
```



### <a name="step-3-get-an-iwicimageencoder"></a>Etapa 3: obter um IWICImageEncoder

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) é uma nova interface no Windows 8. Ele pode ser criado a partir de [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), que estende o **IWICImagingFactory** e também é novo para o Windows 8.


```C++
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );
```



Chame [**IWICImagingFactory2:: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder). O primeiro parâmetro é um [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) e deve ser o dispositivo no qual a imagem que você deseja codificar foi criada – você não pode misturar imagens de domínios de recursos diferentes em um único [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a>Etapa 4: gravar o conteúdo do Direct2D usando o IWICImageEncoder

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) pode gravar uma imagem [Direct2D](./direct2d-portal.md) em um quadro de imagem, em uma miniatura de quadro ou na miniatura de contêiner. Em seguida, você pode usar [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) para codificar os dados de imagem em um arquivo normalmente.

Grave a imagem [Direct2D](./direct2d-portal.md) no quadro. Neste trecho de código, escrevemos um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que contém conteúdo Direct2D rasterizado. No entanto, você pode fornecer qualquer interface que implemente [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).


```C++
    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );
```



> [!Note]  
> O parâmetro [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) deve ter sido criado no [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) que foi passado em [**IWICImagingFactory2:: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).

 

Confirme o WIC e os recursos de fluxo para finalizar a operação.


```C++
    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
```



> [!Note]  
> Algumas implementações de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) não implementam o método [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) e retornam **e \_ NOTIMPL**.

 

Agora você tem um arquivo que contém a imagem [Direct2D](./direct2d-portal.md) .

## <a name="complete-example"></a>Exemplo completo

Aqui, o código completo deste exemplo.

```cpp
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );

void SaveAsImageFile::SaveBitmapToFile()
{
    // Prepare a file picker for customers to input image file name.
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto pngExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    auto bmpExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    bmpExtensions->Append(".bmp");
    savePicker->FileTypeChoices->Insert("BMP file", bmpExtensions);
    savePicker->DefaultFileExtension = ".png";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            m_imageFileName = file->Name;
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".bmp")
            {
                wicFormat = GUID_ContainerFormatBmp;
            }
            else if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }

            // Retrieve a stream from the file.
            task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
            createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
                // Convert the RandomAccessStream to an IStream.
                ComPtr<IStream> stream;
                DX::ThrowIfFailed(
                    CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
                    );

                SaveBitmapToStream(m_d2dTargetBitmap, m_wicFactory, m_d2dContext, wicFormat, stream.Get());
            });
        }
    });
}

// Save render target bitmap to a stream using WIC.
void SaveAsImageFile::SaveBitmapToStream(
    _In_ ComPtr<ID2D1Bitmap1> d2dBitmap,
    _In_ ComPtr<IWICImagingFactory2> wicFactory2,
    _In_ ComPtr<ID2D1DeviceContext> d2dContext,
    _In_ REFGUID wicFormat,
    _In_ IStream* stream
    )
{
    // Create and initialize WIC Bitmap Encoder.
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    // Create and initialize WIC Frame Encoder.
    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );

    // Retrieve D2D Device.
    ComPtr<ID2D1Device> d2dDevice;
    d2dContext->GetDevice(&d2dDevice);

    // Create IWICImageEncoder.
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );

    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
}

```



 

 