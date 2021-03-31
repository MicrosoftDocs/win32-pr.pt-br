---
title: Lendo arquivos do dispositivo
description: Lendo arquivos do dispositivo
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Media Gerenciador de Dispositivos, lendo arquivos de dispositivos
- Gerenciador de Dispositivos, lendo arquivos de dispositivos
- Guia de programação, lendo arquivos de dispositivos
- aplicativos de área de trabalho, lendo arquivos de dispositivos
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, lendo arquivos de dispositivos
- lendo arquivos de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b80cf820e889b29e612206f90b07e1cb02c4c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159455"
---
# <a name="reading-files-from-the-device"></a><span data-ttu-id="ca7a9-109">Lendo arquivos do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ca7a9-109">Reading Files from the Device</span></span>

<span data-ttu-id="ca7a9-110">Quando encontrar um arquivo que deseja copiar do dispositivo, você pode copiar o arquivo do dispositivo para o computador em uma única chamada ou usar um retorno de chamada para que os bytes de arquivo sejam lidos diretamente para seu aplicativo, o que pode processar ou armazenar os dados conforme eles se ajustam.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-110">When you have found a file you would like to copy from the device, you can then copy the file from the device to the computer in a single call, or use a callback to have the file bytes read directly to your application, which can then process or store the data as it sees fits.</span></span>

<span data-ttu-id="ca7a9-111">As etapas a seguir mostram a maneira básica de copiar um arquivo de um dispositivo em uma única chamada:</span><span class="sxs-lookup"><span data-stu-id="ca7a9-111">The following steps show the basic way to copy a file from a device in a single call:</span></span>

1.  <span data-ttu-id="ca7a9-112">Obtenha um identificador para o arquivo no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-112">Get a handle to the file on the device.</span></span> <span data-ttu-id="ca7a9-113">Você pode obter o identificador usando uma pesquisa de arquivo recursiva ou, se souber a ID persistente do armazenamento, chamando [**IWMDMDevice3:: FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span><span class="sxs-lookup"><span data-stu-id="ca7a9-113">You might obtain the handle by using a recursive file search or, if you know the persistent ID of the storage, by calling [**IWMDMDevice3::FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span></span> <span data-ttu-id="ca7a9-114">Em ambos os casos, você precisa da interface [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-114">In either case, you need the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface of the object.</span></span>
2.  <span data-ttu-id="ca7a9-115">Determine se o armazenamento é um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-115">Determine whether the storage is a file or a folder.</span></span> <span data-ttu-id="ca7a9-116">Somente os arquivos podem ser copiados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-116">Only files can be copied from the device.</span></span> <span data-ttu-id="ca7a9-117">Chame [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para obter atributos de armazenamento, o que informará se o armazenamento é um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-117">Call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to get storage attributes, which will tell you whether the storage is a file or a folder.</span></span>
3.  <span data-ttu-id="ca7a9-118">Consulte **IWMDMStorage** para [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)e chame [**IWMDMStorageControl:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) para ler o arquivo do dispositivo e salvá-lo em um local especificado.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-118">Query **IWMDMStorage** for [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol), and call [**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) to read the file from the device and save it to a specified location.</span></span>

<span data-ttu-id="ca7a9-119">Se, em vez disso, você quiser ler o bloco de arquivo por bloco do dispositivo, deverá implementar a interface de retorno de chamada [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) .</span><span class="sxs-lookup"><span data-stu-id="ca7a9-119">If, instead, you want to read the file block by block from the device, you must implement the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) callback interface.</span></span> <span data-ttu-id="ca7a9-120">Passe essa interface para a chamada **IWMDMStorageControl:: Read** e o Windows Media Gerenciador de dispositivos enviará partes de dados de arquivo sequencialmente para seu retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-120">Pass this interface into the **IWMDMStorageControl::Read** call, and Windows Media Device Manager will send chunks of file data sequentially to your callback.</span></span> <span data-ttu-id="ca7a9-121">As etapas a seguir mostram como ler um bloco de arquivos do dispositivo por bloco:</span><span class="sxs-lookup"><span data-stu-id="ca7a9-121">The following steps show how to read a device file block by block:</span></span>

1.  <span data-ttu-id="ca7a9-122">Obtenha a interface **IWMDMStorage** para o armazenamento e determine se ele é um arquivo, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-122">Get the **IWMDMStorage** interface for the storage and determine whether it is a file, as described previously.</span></span>
2.  <span data-ttu-id="ca7a9-123">Prepare quaisquer identificadores de arquivo ou outros identificadores necessários para manter os dados recebidos.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-123">Prepare any file handles or other handles you need to hold the received data.</span></span>
3.  <span data-ttu-id="ca7a9-124">Consulta para a interface **IWMDMStorageControl** do armazenamento</span><span class="sxs-lookup"><span data-stu-id="ca7a9-124">Query for the storage's **IWMDMStorageControl** interface</span></span>
4.  <span data-ttu-id="ca7a9-125">Chame **IWMDMStorageControl:: Read** para iniciar a operação de leitura, passando a interface **IWMDMOperation** que você implementou.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-125">Call **IWMDMStorageControl::Read** to begin the read operation, passing in the **IWMDMOperation** interface you have implemented.</span></span>
5.  <span data-ttu-id="ca7a9-126">O Windows Media Gerenciador de Dispositivos enviará o bloco de dados por bloco para seu dispositivo, conforme descrito em [manipulando transferências de arquivo manualmente](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="ca7a9-126">Windows Media Device Manager will send the data block by block to your device as described in [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>

<span data-ttu-id="ca7a9-127">A seguinte função de exemplo C++ lê um objeto de armazenamento de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-127">The following C++ example function reads a storage object from a device.</span></span> <span data-ttu-id="ca7a9-128">A função aceita um ponteiro de interface **IWMDMOperation** opcional; Se for enviado, a função criará um arquivo explicitamente e manipulará a gravação dos dados no arquivo em sua implementação de **IWMDMOperation:: TransferObjectData**; caso contrário, ele lerá o arquivo e salvará no destino especificado por *pwszDestName*.</span><span class="sxs-lookup"><span data-stu-id="ca7a9-128">The function accepts an optional **IWMDMOperation** interface pointer; if submitted, the function will create a file explicitly and handle writing the data to file on its implementation of **IWMDMOperation::TransferObjectData**; if not, it will read the file and save to the destination specified by *pwszDestName*.</span></span>


```C++
HANDLE m_File = NULL;

HRESULT myFileRead(IWMDMStorage pStorage, LPWSTR pwszDestName, IWMDMOperation* pOperation)
{
    HRESULT hr = S_OK;
    if ((pStorage == NULL) || (pwszDestName == NULL)) 
    {
        return E_INVALIDPARAM;
    }

    // Check that the storage is readable.
    DWORD attributes = 0;
    UINT flags = 0;
    hr = pStorage->GetAttributes(&attributes, NULL); 
    if (FAILED(hr))
    {
        return hr;
    }

    // Check that content is readable.
    if ((attributes & WMDM_FILE_ATTR_CANREAD) == 0)
    {
        return E_FAIL;
    }
    // Check that it is not abstract (such as an abstract playlist).
    else if (attributes & WMDM_STORAGE_ATTR_VIRTUAL)
    {
        return E_FAIL;
    }

    // Set some flag values for the read operation.
    flags |= WMDM_MODE_BLOCK;
    if (attributes & WMDM_FILE_ATTR_FOLDER)
    {
        flags |= WMDM_CONTENT_FOLDER;
    }
    if (attributes & WMDM_FILE_ATTR_FILE)
    {
        flags |= WMDM_CONTENT_FILE;
    }

    // Get the IWMDMStorageControl interface.
    CComQIPtr<IWMDMStorageControl> pStgControl(pStorage);
    
    // Extra steps if we want to read the file ourselves using IWMDMOperation3.
    if (pOperation != NULL)
    {
        // Create a new file and get the handle. m_File is a global variable
        // that we will use in IWMDMOperation::TransferObjectData.
        // This can also be done when IWMDMOperation::BeginRead is called.
        m_File = CreateFile(
            pwszDestName,   // Destination file name.
            GENERIC_WRITE,  // Write and append writes
            NULL,           // File can't be shared while using, and must be closed.
            NULL,           // Handle can't be inherited.
            CREATE_ALWAYS,  // Overwrite existing files.
            FILE_ATTRIBUTE_NORMAL, // No special attributes.
            NULL            // No template file supplied.
           );
        if (m_File == INVALID_HANDLE_VALUE) return E_FAIL;
        // Modify the Read() method flag. WMDM_CONTENT_FILE and WMDM_CONTENT_FOLDER 
        // are not valid flags when pOperation != NULL.
        flags |= WMDM_CONTENT_OPERATIONINTERFACE;
    }

    // Read the file.
    hr = pStgControl->Read(
             flags,        // Synchronous call specified.
             pwszDestName, // Ignored if pOperation is not NULL.
             NULL,         // No progress callback sent.
             pOperation);  // IWMDMOperation interface, if provided.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ca7a9-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca7a9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca7a9-130">**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**</span><span class="sxs-lookup"><span data-stu-id="ca7a9-130">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




