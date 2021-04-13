---
description: Adicionando um recurso a um objeto
ms.assetid: 81476f50-5ea0-4e02-9e38-2b1dfcc32c4f
title: Adicionando um recurso a um objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869b5cdcf172c4b8f27f7081bfce8e6f05073789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296966"
---
# <a name="adding-a-resource-to-an-object"></a><span data-ttu-id="57185-103">Adicionando um recurso a um objeto</span><span class="sxs-lookup"><span data-stu-id="57185-103">Adding a Resource to an Object</span></span>

<span data-ttu-id="57185-104">Além de transferir objetos para um dispositivo, também é possível adicionar recursos a objetos.</span><span class="sxs-lookup"><span data-stu-id="57185-104">In addition to transferring objects to a device, it's also possible to add resources to objects.</span></span> <span data-ttu-id="57185-105">Por exemplo, um aplicativo pode adicionar uma foto a informações existentes para um determinado contato.</span><span class="sxs-lookup"><span data-stu-id="57185-105">For example, an application could add a photo to existing information for a given contact.</span></span>

<span data-ttu-id="57185-106">Os recursos são adicionados usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="57185-106">Resources are added using the interfaces described in the following table.</span></span>



| <span data-ttu-id="57185-107">Interface</span><span class="sxs-lookup"><span data-stu-id="57185-107">Interface</span></span>                                                              | <span data-ttu-id="57185-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="57185-108">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="57185-109">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="57185-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)     | <span data-ttu-id="57185-110">Fornece acesso aos métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="57185-110">Provides access to the content-specific methods.</span></span>                  |
| [<span data-ttu-id="57185-111">**Interface IPortableDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="57185-111">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) | <span data-ttu-id="57185-112">Usado ao gravar as propriedades e os dados do recurso no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57185-112">Used when writing the resource properties and data to the device.</span></span> |
| [<span data-ttu-id="57185-113">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="57185-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)       | <span data-ttu-id="57185-114">Usado para gravar propriedades que descrevem o recurso.</span><span class="sxs-lookup"><span data-stu-id="57185-114">Used to write properties that describe the resource.</span></span>              |
| <span data-ttu-id="57185-115">Interface IStream</span><span class="sxs-lookup"><span data-stu-id="57185-115">IStream Interface</span></span>                                                      | <span data-ttu-id="57185-116">Usado para simplificar a gravação do recurso no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57185-116">Used to simplify writing the resource to the device.</span></span>              |



 

<span data-ttu-id="57185-117">A função CreateContactPhotoResourceOnDevice no módulo ContentTransfer. cpp do aplicativo de exemplo demonstra como um aplicativo pode adicionar um recurso de foto a um objeto de contato.</span><span class="sxs-lookup"><span data-stu-id="57185-117">The CreateContactPhotoResourceOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application could add a photo resource to a contact object.</span></span> <span data-ttu-id="57185-118">Essa função solicita ao usuário o identificador de objeto do contato no dispositivo, ao qual o recurso de foto será adicionado.</span><span class="sxs-lookup"><span data-stu-id="57185-118">This function prompts the user for the object identifier of the contact on the device, to which the photo resource will be added.</span></span> <span data-ttu-id="57185-119">Em seguida, ele exibe uma caixa de diálogo de FileOpen para que o usuário possa selecionar a imagem a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="57185-119">Then it displays a FileOpen dialog box so that the user can select the image to be added.</span></span> <span data-ttu-id="57185-120">Depois que esses dados são coletados, o aplicativo grava o recurso no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57185-120">Once this data is collected, the application writes the resource to the device.</span></span>

<span data-ttu-id="57185-121">A primeira tarefa realizada pela função CreateContactPhotoResourceOnDevice é solicitar que o usuário insira um identificador de objeto para o contato ao qual a foto será adicionada.</span><span class="sxs-lookup"><span data-stu-id="57185-121">The first task accomplished by the CreateContactPhotoResourceOnDevice function is to prompt the user to enter an object identifier for the contact to which the photo will be added.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
printf("Enter the identifer of the object to which we will add an Audio annotation.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting resource creation\n");
}do
```



<span data-ttu-id="57185-122">A próxima etapa é a recuperação de um objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , que, por sua vez, é usado para obter um objeto [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) .</span><span class="sxs-lookup"><span data-stu-id="57185-122">The next step is the retrieval of an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which in turn is used to obtain an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object.</span></span> <span data-ttu-id="57185-123">(O aplicativo usa esse último objeto para criar e gravar o novo recurso.)</span><span class="sxs-lookup"><span data-stu-id="57185-123">(The application uses this latter object to create and write the new resource.)</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}





if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="57185-124">Depois disso, o exemplo exibe a caixa de diálogo **FileOpen** , que permite ao usuário especificar o nome do arquivo de imagem que contém a foto que deseja adicionar às informações de contato.</span><span class="sxs-lookup"><span data-stu-id="57185-124">After this, the sample displays the **FileOpen** dialog box, which allows the user to specify the name of the image file that contains the photo they want to add to the contact information.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = wszFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(wszFilePath);
    OpenFileNameInfo.lpstrFilter    = L"JPEG (*.JPG)\0*.JPG\0JPEG (*.JPEG)\0*.JPEG\0JPG (*.JPE)\0*.JPE\0JPG (*.JFIF)\0*.JFIF\0\0";;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = L"JPG";

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was cancelled.\n");
        hr = E_ABORT;
    }
}
```



<span data-ttu-id="57185-125">Depois que o exemplo tiver um objeto [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) e o nome do arquivo de imagem, ele fará o seguinte na preparação para realmente transferir dados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57185-125">Once the sample has an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object and the name of the image file, it does the following in preparation for actually transferring data to the device.</span></span>

1.  <span data-ttu-id="57185-126">Ele abre um objeto IStream no arquivo selecionado para operações de leitura.</span><span class="sxs-lookup"><span data-stu-id="57185-126">It opens an IStream object on the selected file for read operations.</span></span>
2.  <span data-ttu-id="57185-127">Ele cria um objeto [**IPortableDeviceValues**](iportabledevicevalues.md) , que conterá informações como o tamanho e o formato da imagem.</span><span class="sxs-lookup"><span data-stu-id="57185-127">It creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, which will contain information such as the image size and format.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(wszFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // CoCreate the IPortableDeviceValues to hold the resource attributes
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pResourceAttributes);
        if (SUCCEEDED(hr))
        {
            // Fill in the necessary information regarding this resource

            // Set the WPD_OBJECT_ID.  This informs the driver which object this request is intended for.
            hr = pResourceAttributes->SetStringValue(WPD_OBJECT_ID, wszSelection);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID when creating a resource, hr = 0x%lx\n",hr);
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetKeyValue(WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY, WPD_RESOURCE_CONTACT_PHOTO);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE by requesting the total size of the
            // data stream.
            if (SUCCEEDED(hr))
            {
                STATSTG statstg = {0};
                hr = pFileStream->Stat(&statstg, STATFLAG_NONAME);
                if (SUCCEEDED(hr))
                {
                    hr = pResourceAttributes->SetUnsignedLargeIntegerValue(WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, statstg.cbSize.QuadPart);
                    if (FAILED(hr))
                    {
                        printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to get file's total size, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF because we are
            // creating a contact photo resource with JPG image data.
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetGuidValue(WPD_RESOURCE_ATTRIBUTE_FORMAT, WPD_OBJECT_FORMAT_JFIF);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF, hr = 0x%lx\n",hr);
                }
            }
        }

    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",wszFilePath, hr);
    }
}
```



<span data-ttu-id="57185-128">Depois de preparar os objetos IStream e [**IPortableDeviceValues**](iportabledevicevalues.md) para a operação de gravação, o exemplo transfere a imagem para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57185-128">After preparing the IStream and [**IPortableDeviceValues**](iportabledevicevalues.md) objects for the write operation, the sample transfers the image to the device.</span></span> <span data-ttu-id="57185-129">O exemplo conclui a transferência em três etapas, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="57185-129">The sample completes the transfer in three steps, as follows:</span></span>

1.  <span data-ttu-id="57185-130">Ele cria o recurso no dispositivo chamando o método [**IPortableDeviceResources:: CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) .</span><span class="sxs-lookup"><span data-stu-id="57185-130">It creates the resource on the device by calling the [**IPortableDeviceResources::CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) method.</span></span>
2.  <span data-ttu-id="57185-131">Ele chama uma função auxiliar StreamCopy para copiar o fluxo de origem para o fluxo de destino.</span><span class="sxs-lookup"><span data-stu-id="57185-131">It calls a StreamCopy helper function to copy the source stream to the destination stream.</span></span>
3.  <span data-ttu-id="57185-132">Ele informa ao driver de dispositivo que a transferência foi concluída chamando o método IPortableDeviceDataStream:: Commit.</span><span class="sxs-lookup"><span data-stu-id="57185-132">It informs the device driver that the transfer is complete by calling the IPortableDeviceDataStream::Commit method.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pResources->CreateResource(pResourceAttributes,    // Properties describing this resource
                                    &pResourceStream,       // Returned resource data stream (to transfer the data to)
                                    &cbOptimalTransferSize, // Returned optimal buffer size to use during transfer
                                    NULL);


    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pResourceStream,        // Destination (The resource to transfer to)
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
        hr = pResourceStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit resource to device, hr = 0x%lx\n",hr);
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="57185-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57185-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57185-134">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="57185-134">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="57185-135">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="57185-135">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="57185-136">**Interface IPortableDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="57185-136">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)
</dt> <dt>

[<span data-ttu-id="57185-137">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="57185-137">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="57185-138">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="57185-138">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



