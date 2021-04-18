---
description: Transferindo um arquivo de imagem ou música para o dispositivo
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: Transferindo um arquivo de imagem ou música para o dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3308212825f6c67ea79a40873fc466164d62f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791412"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a><span data-ttu-id="61c62-103">Transferindo um arquivo de imagem ou música para o dispositivo</span><span class="sxs-lookup"><span data-stu-id="61c62-103">Transferring an Image or Music File to the Device</span></span>

<span data-ttu-id="61c62-104">Uma das operações mais comuns realizadas por um aplicativo é a transferência de conteúdo para um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="61c62-104">One of the most common operations accomplished by an application is the transfer of content to a connected device.</span></span>

<span data-ttu-id="61c62-105">Transferências de conteúdo são realizadas usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="61c62-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="61c62-106">Interface</span><span class="sxs-lookup"><span data-stu-id="61c62-106">Interface</span></span>                                                                | <span data-ttu-id="61c62-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="61c62-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="61c62-108">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="61c62-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="61c62-109">Fornece acesso aos métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="61c62-109">Provides access to the content-specific methods.</span></span>               |
| [<span data-ttu-id="61c62-110">**Interface IPortableDeviceDataStream**</span><span class="sxs-lookup"><span data-stu-id="61c62-110">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | <span data-ttu-id="61c62-111">Usado ao gravar o conteúdo no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61c62-111">Used when writing the content to the device.</span></span>                   |
| [<span data-ttu-id="61c62-112">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="61c62-112">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="61c62-113">Usado para recuperar propriedades que descrevem o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="61c62-113">Used to retrieve properties that describe the content.</span></span>         |
| <span data-ttu-id="61c62-114">Interface IStream</span><span class="sxs-lookup"><span data-stu-id="61c62-114">IStream Interface</span></span>                                                        | <span data-ttu-id="61c62-115">Usado para simplificar a leitura do conteúdo e a gravação no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61c62-115">Used to simplify reading of content and writing to the device.</span></span> |



 

<span data-ttu-id="61c62-116">A `TransferContentToDevice` função no módulo ContentTransfer. cpp do aplicativo de exemplo demonstra como um aplicativo pode transferir conteúdo de um PC para um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="61c62-116">The `TransferContentToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer content from a PC to a connected device.</span></span> <span data-ttu-id="61c62-117">Neste exemplo específico, o conteúdo transferido pode ser um arquivo que contém uma imagem, música ou informações de contato.</span><span class="sxs-lookup"><span data-stu-id="61c62-117">In this particular sample, the transferred content can be a file containing an image, music, or contact information.</span></span>

<span data-ttu-id="61c62-118">A primeira tarefa realizada pela `TransferContentToDevice` função é solicitar que o usuário insira um identificador de objeto, que identifica o objeto a ser transferido.</span><span class="sxs-lookup"><span data-stu-id="61c62-118">The first task accomplished by the `TransferContentToDevice` function is to prompt the user to enter an object identifier, which identifies the object to be transferred.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
WCHAR                               szFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IPortableDeviceDataStream>  pFinalObjectDataStream;
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IStream>                    pTempStream;  // Temporary IStream which we use to QI for IPortableDeviceDataStream

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the file will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="61c62-119">A segunda tarefa realizada pela `TransferContentToDevice` função é criar um objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) chamando o método [**IPortableDevice:: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="61c62-119">The second task accomplished by the `TransferContentToDevice` function is to create an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="61c62-120">A próxima tarefa realizada pela `TransferContentToDevice` função é a criação de uma caixa de diálogo do **FileOpen** com a qual o usuário pode especificar o local e o nome do arquivo a ser transferido.</span><span class="sxs-lookup"><span data-stu-id="61c62-120">The next task accomplished by the `TransferContentToDevice` function is the creation of a **FileOpen** dialog with which the user can specify the location and name of the file to be transferred.</span></span>


```C++
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = szFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(szFilePath);
    OpenFileNameInfo.lpstrFilter    = pszFileTypeFilter;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = pszDefaultFileExtension;

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was canceled.\n");
        hr = E_ABORT;
    }
}
```



<span data-ttu-id="61c62-121">A `TransferContentToDevice` função passa uma cadeia de caracteres de filtro ( `wszFileTypeFilter` ) para o método GetOpenFileName, que determina o tipo de arquivos que o usuário pode escolher.</span><span class="sxs-lookup"><span data-stu-id="61c62-121">The `TransferContentToDevice` function passes a filter string (`wszFileTypeFilter`) to the GetOpenFileName method, which determines the type of files that the user can choose.</span></span> <span data-ttu-id="61c62-122">Consulte a `DoMenu` função no módulo WpdApiSample. cpp para obter exemplos dos três filtros diferentes permitidos pelo exemplo.</span><span class="sxs-lookup"><span data-stu-id="61c62-122">Refer to the `DoMenu` function in the WpdApiSample.cpp module for examples of the three different filters allowed by the sample.</span></span>

<span data-ttu-id="61c62-123">Depois que o usuário identifica um arquivo específico para transferência para o dispositivo, a `TransferContentToDevice` função abre esse arquivo como um objeto IStream e recupera as propriedades necessárias para concluir a transferência.</span><span class="sxs-lookup"><span data-stu-id="61c62-123">After the user identifies a particular file for transfer to the device, the `TransferContentToDevice` function opens that file as an IStream object and retrieves properties that are required to complete the transfer.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(szFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // Get the required properties needed to properly describe the data being
        // transferred to the device.
        hr = GetRequiredPropertiesForContentType(guidContentType,           // Content type of the data
                                                 szSelection,              // Parent to transfer the data under
                                                 szFilePath,               // Full file path to the data file
                                                 pFileStream,               // Open IStream that contains the data
                                                 &pFinalObjectProperties);  // Returned properties describing the data
        if (FAILED(hr))
        {
            printf("! Failed to get required properties needed to transfer a file to the device, hr = 0x%lx\n", hr);
        }
    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",szFilePath, hr);
    }
}
```



<span data-ttu-id="61c62-124">As propriedades obrigatórias são recuperadas chamando `GetRequiredPropertiesForContentType` -se a função auxiliar, que opera no objeto IStream.</span><span class="sxs-lookup"><span data-stu-id="61c62-124">The required properties are retrieved by calling the`GetRequiredPropertiesForContentType` helper-function, which operates on the IStream object.</span></span> <span data-ttu-id="61c62-125">A `GetRequiredPropertiesForContentType` função auxiliar cria um objeto [**IPortableDeviceValues**](iportabledevicevalues.md) , recupera as propriedades na lista a seguir e as adiciona a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="61c62-125">The `GetRequiredPropertiesForContentType` helper-function creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, retrieves the properties in the following list, and adds them to this object.</span></span>

-   <span data-ttu-id="61c62-126">Identificador de objeto pai</span><span class="sxs-lookup"><span data-stu-id="61c62-126">Parent-object identifier</span></span>
-   <span data-ttu-id="61c62-127">Tamanho do fluxo em bytes</span><span class="sxs-lookup"><span data-stu-id="61c62-127">Stream size in bytes</span></span>
-   <span data-ttu-id="61c62-128">Nome do arquivo de conteúdo</span><span class="sxs-lookup"><span data-stu-id="61c62-128">Content file name</span></span>
-   <span data-ttu-id="61c62-129">Nome do conteúdo (o nome do arquivo sem a extensão)</span><span class="sxs-lookup"><span data-stu-id="61c62-129">Content name (the file name without the extension)</span></span>
-   <span data-ttu-id="61c62-130">Tipo de conteúdo (imagem, áudio ou contato)</span><span class="sxs-lookup"><span data-stu-id="61c62-130">Content type (image, audio, or contact)</span></span>
-   <span data-ttu-id="61c62-131">Formato de conteúdo (JFIF, WMA ou vCard2)</span><span class="sxs-lookup"><span data-stu-id="61c62-131">Content format (JFIF, WMA, or vCard2)</span></span>

<span data-ttu-id="61c62-132">O aplicativo de exemplo usa as propriedades recuperadas para criar o novo conteúdo no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61c62-132">The sample application uses the retrieved properties to create the new content on the device.</span></span> <span data-ttu-id="61c62-133">Isso é feito em três fases:</span><span class="sxs-lookup"><span data-stu-id="61c62-133">This is done in three phases:</span></span>

1.  <span data-ttu-id="61c62-134">O aplicativo chama o método [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) para criar um novo objeto IStream no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61c62-134">The application calls [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) method to create a new IStream object on the device.</span></span>
2.  <span data-ttu-id="61c62-135">O aplicativo usa esse objeto para obter um objeto [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) do driver WPD.</span><span class="sxs-lookup"><span data-stu-id="61c62-135">The application uses this object to obtain an [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) object from the WPD driver.</span></span>
3.  <span data-ttu-id="61c62-136">O aplicativo usa o novo objeto **IPortableDeviceDataStream** para gravar o conteúdo no dispositivo (por meio da função auxiliar StreamCopy).</span><span class="sxs-lookup"><span data-stu-id="61c62-136">The application uses the new **IPortableDeviceDataStream** object to write the content to the device (via the StreamCopy helper function).</span></span> <span data-ttu-id="61c62-137">A função auxiliar grava os dados do arquivo de origem no fluxo retornado por [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="61c62-137">The helper function writes the data from the source file to the stream returned by [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span>
4.  <span data-ttu-id="61c62-138">O aplicativo conclui a operação chamando o método Commit no fluxo de destino.</span><span class="sxs-lookup"><span data-stu-id="61c62-138">The application completes the operation by calling the Commit method on the destination stream.</span></span>


```C++
// 4) Transfer for the content to the device
if (SUCCEEDED(hr))
{
    hr = pContent->CreateObjectWithPropertiesAndData(pFinalObjectProperties,    // Properties describing the object data
                                                     &pTempStream,              // Returned object data stream (to transfer the data to)
                                                     &cbOptimalTransferSize,    // Returned optimal buffer size to use during transfer
                                                     NULL);

    // Once we have a the IStream returned from CreateObjectWithPropertiesAndData,
    // QI for IPortableDeviceDataStream so we can use the additional methods
    // to get more information about the object (i.e. The newly created object
    // identifier on the device)
    if (SUCCEEDED(hr))
    {
        hr = pTempStream->QueryInterface(IID_PPV_ARGS(&pFinalObjectDataStream));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface for IPortableDeviceDataStream, hr = 0x%lx\n",hr);
        }
    }

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pFinalObjectDataStream, // Destination (The Object to transfer to)
                        pFileStream,            // Source (The File data to transfer from)
                        cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                        &cbTotalBytesWritten);  // The total number of bytes transferred from file to the device
        if (FAILED(hr))
        {
            printf("! Failed to transfer object to device, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to get IStream (representing destination object data on the device) from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // After transferring content to the device, the client is responsible for letting the
    // driver know that the transfer is complete by calling the Commit() method
    // on the IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        hr = pFinalObjectDataStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit object to device, hr = 0x%lx\n",hr);
        }
    }

    // Some clients may want to know the object identifier of the newly created
    // object.  This is done by calling GetObjectID() method on the
    // IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        PWSTR pszNewlyCreatedObject = NULL;
        hr = pFinalObjectDataStream->GetObjectID(&pszNewlyCreatedObject);
        if (SUCCEEDED(hr))
        {
            printf("The file '%ws' was transferred to the device.\nThe newly created object's ID is '%ws'\n",szFilePath ,pszNewlyCreatedObject);
        }

        if (FAILED(hr))
        {
            printf("! Failed to get the newly transferred object's identifier from the device, hr = 0x%lx\n",hr);
        }

        // Free the object identifier string returned from the GetObjectID() method.
        CoTaskMemFree(pszNewlyCreatedObject);
        pszNewlyCreatedObject = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="61c62-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61c62-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61c62-140">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="61c62-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="61c62-141">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="61c62-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="61c62-142">**Interface IPortableDeviceDataStream**</span><span class="sxs-lookup"><span data-stu-id="61c62-142">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[<span data-ttu-id="61c62-143">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="61c62-143">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="61c62-144">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="61c62-144">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



