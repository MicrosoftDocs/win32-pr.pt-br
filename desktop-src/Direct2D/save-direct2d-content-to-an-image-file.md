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
# <a name="how-to-save-direct2d-content-to-an-image-file"></a><span data-ttu-id="f0fde-103">Como salvar o conteúdo do Direct2D em um arquivo de imagem</span><span class="sxs-lookup"><span data-stu-id="f0fde-103">How to save Direct2D content to an image file</span></span>

<span data-ttu-id="f0fde-104">Este tópico mostra como usar o [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) para salvar o conteúdo na forma de um [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) em um arquivo de imagem codificado, como JPEG.</span><span class="sxs-lookup"><span data-stu-id="f0fde-104">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span> <span data-ttu-id="f0fde-105">Se você estiver escrevendo um aplicativo da Windows Store, poderá fazer com que o usuário selecione um arquivo de destino usando [**Windows:: Storage::P ickers:: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span><span class="sxs-lookup"><span data-stu-id="f0fde-105">If you are writing a Windows Store app, you can have the user select a destination file using [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f0fde-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="f0fde-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f0fde-107">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="f0fde-107">Technologies</span></span>

-   [<span data-ttu-id="f0fde-108">Direct2D</span><span class="sxs-lookup"><span data-stu-id="f0fde-108">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="f0fde-109">Efeitos de Direct2D</span><span class="sxs-lookup"><span data-stu-id="f0fde-109">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="f0fde-110">**Windows:: armazenamento::P ickers:: FileSavePicker**</span><span class="sxs-lookup"><span data-stu-id="f0fde-110">**Windows::Storage::Pickers::FileSavePicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a><span data-ttu-id="f0fde-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="f0fde-111">Prerequisites</span></span>

-   <span data-ttu-id="f0fde-112">Você precisa de um objeto [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) e de um objeto que contenha conteúdo [Direct2D](./direct2d-portal.md) que implementa [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) como [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) ou [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span><span class="sxs-lookup"><span data-stu-id="f0fde-112">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object and an object containing [Direct2D](./direct2d-portal.md) content that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) such as [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) or [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span></span>

## <a name="instructions"></a><span data-ttu-id="f0fde-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="f0fde-113">Instructions</span></span>

### <a name="step-1-get-a-destination-file-and-stream"></a><span data-ttu-id="f0fde-114">Etapa 1: obter um arquivo de destino e um fluxo</span><span class="sxs-lookup"><span data-stu-id="f0fde-114">Step 1: Get a destination file and stream</span></span>

<span data-ttu-id="f0fde-115">Se você quiser permitir que o usuário selecione um arquivo de destino, poderá usar [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), abrir o arquivo retornado e obter um [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) para usar com o WIC.</span><span class="sxs-lookup"><span data-stu-id="f0fde-115">If you want to allow the user to select a destination file, you can use [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), open the returned file, and obtain an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) to use with WIC.</span></span>

<span data-ttu-id="f0fde-116">Crie um [**Windows:: Storage::P ickers:: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) e defina seus parâmetros para arquivos de imagem.</span><span class="sxs-lookup"><span data-stu-id="f0fde-116">Create a [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) and set its parameters for image files.</span></span> <span data-ttu-id="f0fde-117">Chame o método [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) .</span><span class="sxs-lookup"><span data-stu-id="f0fde-117">Call the [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) method.</span></span>


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



<span data-ttu-id="f0fde-118">Declare um manipulador de conclusão para ser executado depois que a operação assíncrona de seletor de arquivo retornar.</span><span class="sxs-lookup"><span data-stu-id="f0fde-118">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="f0fde-119">Use o método [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) para recuperar o arquivo e obter o objeto de fluxo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f0fde-119">Use the [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) method to retrieve the file and to get the file stream object.</span></span>


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



<span data-ttu-id="f0fde-120">Obtenha um [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) chamando [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) no arquivo e obtendo o resultado da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f0fde-120">Obtain an [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) by calling [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) on the file and getting the result of the async operation.</span></span>


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



<span data-ttu-id="f0fde-121">Por fim, use o método [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) para converter o fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f0fde-121">Finally, use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) method to convert the file stream.</span></span> <span data-ttu-id="f0fde-122">Windows Runtime APIs representam fluxos com [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), enquanto o WIC consome [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="f0fde-122">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while WIC consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> <span data-ttu-id="f0fde-123">Para usar a função [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , você deve incluir **shcore. h** em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="f0fde-123">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include **shcore.h** in your project.</span></span>

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a><span data-ttu-id="f0fde-124">Etapa 2: obter o bitmap do WIC e o codificador de quadros</span><span class="sxs-lookup"><span data-stu-id="f0fde-124">Step 2: Get the WIC bitmap and frame encoder</span></span>

<span data-ttu-id="f0fde-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) fornecem a funcionalidade para salvar dados de imagem em um formato de arquivo codificado.</span><span class="sxs-lookup"><span data-stu-id="f0fde-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) provide the functionality to save imaging data to an encoded file format.</span></span>

<span data-ttu-id="f0fde-126">Crie e inicialize os objetos do codificador.</span><span class="sxs-lookup"><span data-stu-id="f0fde-126">Create and initialize the encoder objects.</span></span>


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



### <a name="step-3-get-an-iwicimageencoder"></a><span data-ttu-id="f0fde-127">Etapa 3: obter um IWICImageEncoder</span><span class="sxs-lookup"><span data-stu-id="f0fde-127">Step 3: Get an IWICImageEncoder</span></span>

<span data-ttu-id="f0fde-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) é uma nova interface no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f0fde-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) is a new interface in Windows 8.</span></span> <span data-ttu-id="f0fde-129">Ele pode ser criado a partir de [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), que estende o **IWICImagingFactory** e também é novo para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f0fde-129">It can be created from [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), which extends **IWICImagingFactory** and is also new for Windows 8.</span></span>


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



<span data-ttu-id="f0fde-130">Chame [**IWICImagingFactory2:: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="f0fde-130">Call [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span> <span data-ttu-id="f0fde-131">O primeiro parâmetro é um [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) e deve ser o dispositivo no qual a imagem que você deseja codificar foi criada – você não pode misturar imagens de domínios de recursos diferentes em um único [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span><span class="sxs-lookup"><span data-stu-id="f0fde-131">The first parameter is an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) and must be the device on which the image you want to encode was created – you cannot mix images from different resource domains within a single [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span></span>


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a><span data-ttu-id="f0fde-132">Etapa 4: gravar o conteúdo do Direct2D usando o IWICImageEncoder</span><span class="sxs-lookup"><span data-stu-id="f0fde-132">Step 4: Write the Direct2D content using IWICImageEncoder</span></span>

<span data-ttu-id="f0fde-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) pode gravar uma imagem [Direct2D](./direct2d-portal.md) em um quadro de imagem, em uma miniatura de quadro ou na miniatura de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f0fde-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) can write a [Direct2D](./direct2d-portal.md) image into an image frame, a frame thumbnail, or the container thumbnail.</span></span> <span data-ttu-id="f0fde-134">Em seguida, você pode usar [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) e [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) para codificar os dados de imagem em um arquivo normalmente.</span><span class="sxs-lookup"><span data-stu-id="f0fde-134">You can then use [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) to encode the imaging data to a file as normal.</span></span>

<span data-ttu-id="f0fde-135">Grave a imagem [Direct2D](./direct2d-portal.md) no quadro.</span><span class="sxs-lookup"><span data-stu-id="f0fde-135">Write the [Direct2D](./direct2d-portal.md) image to the frame.</span></span> <span data-ttu-id="f0fde-136">Neste trecho de código, escrevemos um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que contém conteúdo Direct2D rasterizado.</span><span class="sxs-lookup"><span data-stu-id="f0fde-136">In this snippet we write an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) that contains rasterized Direct2D content.</span></span> <span data-ttu-id="f0fde-137">No entanto, você pode fornecer qualquer interface que implemente [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span><span class="sxs-lookup"><span data-stu-id="f0fde-137">However, you can provide any interface that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span></span>


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
> <span data-ttu-id="f0fde-138">O parâmetro [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) deve ter sido criado no [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) que foi passado em [**IWICImagingFactory2:: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="f0fde-138">The [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) parameter must have been created on the [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) that was passed into [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span>

 

<span data-ttu-id="f0fde-139">Confirme o WIC e os recursos de fluxo para finalizar a operação.</span><span class="sxs-lookup"><span data-stu-id="f0fde-139">Commit the WIC and stream resources to finalize the operation.</span></span>


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
> <span data-ttu-id="f0fde-140">Algumas implementações de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) não implementam o método [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) e retornam **e \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="f0fde-140">Some implementations of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) do not implement the [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) method and return **E\_NOTIMPL**.</span></span>

 

<span data-ttu-id="f0fde-141">Agora você tem um arquivo que contém a imagem [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f0fde-141">Now you have a file containing the [Direct2D](./direct2d-portal.md) image.</span></span>

## <a name="complete-example"></a><span data-ttu-id="f0fde-142">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="f0fde-142">Complete example</span></span>

<span data-ttu-id="f0fde-143">Aqui, o código completo deste exemplo.</span><span class="sxs-lookup"><span data-stu-id="f0fde-143">Here the full code for this example.</span></span>

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



 

 