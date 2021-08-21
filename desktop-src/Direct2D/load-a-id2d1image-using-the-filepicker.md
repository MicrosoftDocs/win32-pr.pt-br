---
title: como carregar uma imagem em efeitos de Direct2D usando o fileescolhidor
description: mostra como usar o Windows Armazenamento seletores FileOpenPicker para carregar uma imagem em efeitos de Direct2D.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- FilePicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bb23faf2b9d50f12219f3b99c07ec835558addc55e67d4843dee049946a60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160527"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a>como carregar uma imagem em efeitos de Direct2D usando o fileescolhidor

mostra como usar o [**Windows:: Armazenamento::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) para carregar uma imagem em [efeitos de Direct2D](effects-overview.md). se você quiser permitir que o usuário selecione um arquivo de imagem do armazenamento em um aplicativo da Windows Store, recomendamos que você use o [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Direct2D](./direct2d-portal.md)
-   [efeitos de Direct2D](effects-overview.md)
-   [**Windows:: Armazenamento::P ickers:: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a>Pré-requisitos

-   Você precisa de um objeto [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para criar efeitos.
-   Você precisa de um objeto [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) para criar objetos WIC.

## <a name="instructions"></a>Instruções

### <a name="step-1-open-the-file-picker"></a>Etapa 1: abrir o seletor de arquivos

Crie um objeto [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) e defina *ViewMode*, *SuggestedStartLocation* e *FileTypeFilter* para selecionar imagens. Chame o método [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) .


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



Após a conclusão do [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) , você obtém um fluxo de arquivo da interface [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) que ele retorna.

### <a name="step-2-get-a-file-stream"></a>Etapa 2: obter um fluxo de arquivos

Declare um manipulador de conclusão para ser executado depois que a operação assíncrona de seletor de arquivo retornar. Use o método [**GetResults**](/previous-versions//br205815(v=vs.85)) para recuperar o arquivo e obter o objeto de fluxo de arquivo.


```C++
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file) // If file == nullptr, the user did not select a file.
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
```



Na próxima etapa, você converte o objeto [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) em um [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que pode passar para o [WIC](/windows/desktop/wic/-wic-api).

### <a name="step-3-convert-the-file-stream"></a>Etapa 3: converter o fluxo de arquivos

Use a função [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) para converter o fluxo de arquivos. Windows As APIs de tempo de execução representam fluxos com [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), enquanto o [WIC](/windows/desktop/wic/-wic-api) consome [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).


```C++
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
        reinterpret_cast<IUnknown*>(fileStream),
        IID_PPV_ARGS(&istream)
        )
    );
```



> [!Note]  
> Para usar a função [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , você deve incluir *shcore. h* em seu projeto.

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a>Etapa 4: criar um decodificador de WIC e obter o quadro

Crie um objeto [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) usando o método [**IWICImagingFactory:: CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .


```C++
    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );
```



Obtenha o primeiro quadro da imagem do decodificador usando o método [**IWICBitmapDecoder:: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a>Etapa 5: criar um conversor de WIC e inicializar

Converta a imagem no formato de cor BGRA usando o [WIC](/windows/desktop/wic/-wic-api). [IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) retornará o formato de pixel nativo da imagem, como os JPEGs são armazenados no GUID \_ WICPixelFormat24bppBGR. no entanto, como uma otimização de desempenho com Direct2D recomendamos que você converta em WICPixelFormat32bppPBGRA.

1.  Crie um objeto [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) usando o método [**IWICImagingFactory:: CreateFormat**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  Inicialize o conversor de formato para usar o WICPixelFormat32bppPBGRA e passar o quadro de bitmap.

    ```C++
       DX::ThrowIfFailed(
            converter->Initialize(
                frame.Get(),
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                nullptr,
                0.0f,
                WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
                )
            );
    ```

    

A interface [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) é derivada da interface [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) , para que você possa passar o conversor para o efeito de [origem de bitmap](bitmap-source.md) .

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a>Etapa 6: criar efeito e passar um IWICBitmapSource

Use o [**método createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) para criar um objeto [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) de [origem de bitmap](bitmap-source.md) usando o contexto do [**dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](getting-started-with-direct2d.md) .

Use o método [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) para definir a *propriedade \_ \_ origem do \_ \_ bitmap do \_ WIC de prop do d2d1 BITMAPSOURCE* para o conversor de [**formato**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)do [WIC](/windows/desktop/wic/-wic-api) .

> [!Note]  
> o efeito de [origem de bitmap](bitmap-source.md) não assume uma entrada do método [**setinput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) , como muitos [Direct2D efeitos](effects-overview.md). Em vez disso, o objeto [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) é especificado como uma propriedade.

 


```C++
    ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
```



Agora que você tem o efeito de [origem do bitmap](bitmap-source.md) , você pode usá-lo como entrada para qualquer [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) e criar um grafo de efeito.

## <a name="complete-example"></a>Exemplo completo

Este é o código completo deste exemplo.


```C++
ComPtr<ID2D1Effect> bitmapSourceEffect;

void OpenFilePicker()
{
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
    
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file)
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
}

void OpenFile(Windows::Storage::Streams::IRandomAccessStream^ fileStream)
{
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
            reinterpret_cast<IUnknown*>(fileStream),
            IID_PPV_ARGS(&istream)
            )
        );

    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );

    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );

    ComPtr<IWICFormatConverter> converter;
    DX::ThrowIfFailed(
        m_wicFactory->CreateFormatConverter(&converter)
        );

    DX::ThrowIfFailed(
        converter->Initialize(
            frame.Get(),
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            nullptr,
            0.0f,
            WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
            )
        );

       ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
}
```



 

 