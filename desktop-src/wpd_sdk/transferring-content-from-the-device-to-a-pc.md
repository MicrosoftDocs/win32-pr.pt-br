---
description: Transferindo o conteúdo do dispositivo para um PC
ms.assetid: 76069097-a513-42f7-bdcc-a65714e95f0a
title: Transferindo o conteúdo do dispositivo para um PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de06861ba74b4b7883c8d96e25cebe3fbb64e21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170992"
---
# <a name="transferring-content-from-the-device-to-a-pc"></a><span data-ttu-id="63f0b-103">Transferindo o conteúdo do dispositivo para um PC</span><span class="sxs-lookup"><span data-stu-id="63f0b-103">Transferring Content from the Device to a PC</span></span>

<span data-ttu-id="63f0b-104">Uma operação comum realizada por um aplicativo WPD é a transferência de conteúdo de um dispositivo conectado para o PC.</span><span class="sxs-lookup"><span data-stu-id="63f0b-104">One common operation accomplished by a WPD application is the transfer of content from a connected device to the PC.</span></span>

<span data-ttu-id="63f0b-105">Transferências de conteúdo são realizadas usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="63f0b-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="63f0b-106">Interface</span><span class="sxs-lookup"><span data-stu-id="63f0b-106">Interface</span></span>                                                                | <span data-ttu-id="63f0b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="63f0b-107">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="63f0b-108">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="63f0b-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="63f0b-109">Fornece acesso à interface **IPortableDeviceProperties** .</span><span class="sxs-lookup"><span data-stu-id="63f0b-109">Provides access to the **IPortableDeviceProperties** interface.</span></span> |
| [<span data-ttu-id="63f0b-110">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="63f0b-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="63f0b-111">Fornece acesso a métodos específicos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="63f0b-111">Provides access to property-specific methods.</span></span>                   |
| [<span data-ttu-id="63f0b-112">**Interface IPortableDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="63f0b-112">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)   | <span data-ttu-id="63f0b-113">Usado para armazenar as chaves de propriedade para o perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="63f0b-113">Used to store the property keys for the given profile.</span></span>          |
| <span data-ttu-id="63f0b-114">Interface IStream</span><span class="sxs-lookup"><span data-stu-id="63f0b-114">IStream Interface</span></span>                                                        | <span data-ttu-id="63f0b-115">Usado para ler e gravar os dados.</span><span class="sxs-lookup"><span data-stu-id="63f0b-115">Used to read and write the data.</span></span>                                |



 

<span data-ttu-id="63f0b-116">A `TransferContentFromDevice` função no módulo ContentTransfer. cpp do aplicativo de exemplo demonstra como um aplicativo pode transferir informações de contato de um dispositivo conectado para um PC.</span><span class="sxs-lookup"><span data-stu-id="63f0b-116">The `TransferContentFromDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a connected device to a PC.</span></span>

<span data-ttu-id="63f0b-117">A primeira tarefa realizada pela `TransferContentFromDevice` função é solicitar que o usuário insira um identificador de objeto para o objeto pai no dispositivo (sob o qual o conteúdo será transferido).</span><span class="sxs-lookup"><span data-stu-id="63f0b-117">The first task accomplished by the `TransferContentFromDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                            hr                   = S_OK;
WCHAR                              szSelection[81]      = {0};
CComPtr<IPortableDeviceContent>    pContent;
CComPtr<IPortableDeviceResources>  pResources;
CComPtr<IPortableDeviceProperties> pProperties;
CComPtr<IStream>                   pObjectDataStream;
CComPtr<IStream>                   pFinalFileStream;
DWORD                              cbOptimalTransferSize = 0;
CAtlStringW                        strOriginalFileName;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Prompt user to enter an object identifier on the device to transfer.
printf("Enter the identifer of the object you wish to transfer.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="63f0b-118">A próxima etapa é a recuperação de um objeto **IPortableDeviceContent** que o exemplo usa para acessar os métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="63f0b-118">The next step is the retrieval of an **IPortableDeviceContent** object that the sample uses to access the content-specific methods.</span></span>


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



<span data-ttu-id="63f0b-119">A próxima etapa é a recuperação de um objeto **IPortableDeviceResources** que o exemplo usa para acessar os métodos específicos do recurso.</span><span class="sxs-lookup"><span data-stu-id="63f0b-119">The next step is the retrieval of an **IPortableDeviceResources** object that the sample uses to access the resource-specific methods.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="63f0b-120">A próxima etapa é a recuperação de um objeto IStream que o exemplo usa para ler os dados que ele está transferindo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63f0b-120">The next step is the retrieval of an IStream object that the sample uses to read the data it is transferring from the device.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pResources->GetStream(szSelection,             // Identifier of the object we want to transfer
                               WPD_RESOURCE_DEFAULT,    // We are transferring the default resource (which is the entire object's data)
                               STGM_READ,               // Opening a stream in READ mode, because we are reading data from the device.
                               &cbOptimalTransferSize,  // Driver supplied optimal transfer size
                               &pObjectDataStream);
    if (FAILED(hr))
    {
        printf("! Failed to get IStream (representing object data on the device) from IPortableDeviceResources, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="63f0b-121">A próxima etapa é a recuperação do nome de arquivo do objeto no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63f0b-121">The next step is the retrieval of the object's file name on the device.</span></span> <span data-ttu-id="63f0b-122">Essa cadeia de caracteres é usada para criar o nome de arquivo correspondente no computador.</span><span class="sxs-lookup"><span data-stu-id="63f0b-122">This string is used to create the corresponding file name on the PC.</span></span> <span data-ttu-id="63f0b-123">Se o objeto não tiver um nome de arquivo no dispositivo, o identificador do objeto será convertido em uma cadeia de caracteres e usado para criar o nome do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="63f0b-123">If the object does not have a file name on the device, the object's identifier is converted to a string and used to create the destination file name.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (SUCCEEDED(hr))
    {
        hr = GetStringValue(pProperties,
                            szSelection,
                            WPD_OBJECT_ORIGINAL_FILE_NAME,
                            strOriginalFileName);
        if (FAILED(hr))
        {
            printf("! Failed to read WPD_OBJECT_ORIGINAL_FILE_NAME on object '%ws', hr = 0x%lx\n", szSelection, hr);
            strOriginalFileName.Format(L"%ws.data", szSelection);
            printf("* Creating a filename '%ws' as a default.\n", (PWSTR)strOriginalFileName.GetString());
            // Set the HRESULT to S_OK, so we can continue with our newly generated
            // temporary file name.
            hr = S_OK;
        }
    }
    else
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="63f0b-124">Depois disso, o exemplo cria um objeto de destino IStream.</span><span class="sxs-lookup"><span data-stu-id="63f0b-124">After this, the sample creates a destination IStream object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = SHCreateStreamOnFile(strOriginalFileName, STGM_CREATE|STGM_WRITE, &pFinalFileStream);
    if (FAILED(hr))
    {
        printf("! Failed to create a temporary file named (%ws) to transfer object (%ws), hr = 0x%lx\n",(PWSTR)strOriginalFileName.GetString(), szSelection, hr);
    }
}
```



<span data-ttu-id="63f0b-125">Por fim, o objeto IStream de origem é copiado para o destino no PC.</span><span class="sxs-lookup"><span data-stu-id="63f0b-125">Finally, the source IStream object is copied to the destination on the PC.</span></span>


```C++
if (SUCCEEDED(hr))
{
    DWORD cbTotalBytesWritten = 0;

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    hr = StreamCopy(pFinalFileStream,       // Destination (The Final File to transfer to)
                    pObjectDataStream,      // Source (The Object's data to transfer from)
                    cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                    &cbTotalBytesWritten);  // The total number of bytes transferred from device to the finished file
    if (FAILED(hr))
    {
        printf("! Failed to transfer object from device, hr = 0x%lx\n",hr);
    }
    else
    {
        printf("* Transferred object '%ws' to '%ws'.\n", szSelection, (PWSTR)strOriginalFileName.GetString());
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="63f0b-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63f0b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63f0b-127">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="63f0b-127">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="63f0b-128">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="63f0b-128">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="63f0b-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="63f0b-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="63f0b-130">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="63f0b-130">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



