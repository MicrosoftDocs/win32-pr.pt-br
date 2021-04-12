---
title: Explorando um dispositivo
description: Explorando um dispositivo
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media Gerenciador de Dispositivos, explorando dispositivos
- Gerenciador de Dispositivos, explorando dispositivos
- Guia de programação, explorando dispositivos
- aplicativos de área de trabalho, explorando dispositivos
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, explorando dispositivos
- explorando dispositivos
- armazenamentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364039"
---
# <a name="exploring-a-device"></a><span data-ttu-id="b14b5-110">Explorando um dispositivo</span><span class="sxs-lookup"><span data-stu-id="b14b5-110">Exploring a Device</span></span>

<span data-ttu-id="b14b5-111">Explorar um dispositivo é semelhante a explorar uma unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="b14b5-111">Exploring a device is similar to exploring a disk drive.</span></span> <span data-ttu-id="b14b5-112">Todos os objetos em um dispositivo são chamados de *armazenamentos*.</span><span class="sxs-lookup"><span data-stu-id="b14b5-112">All objects on a device are called *storages*.</span></span> <span data-ttu-id="b14b5-113">Um armazenamento pode ser um arquivo, uma pasta ou um objeto abstrato (como uma lista de reprodução) no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b14b5-113">A storage can be a file, folder, or abstract object (such as a playlist) on the device.</span></span> <span data-ttu-id="b14b5-114">Você deve examinar os atributos e metadados de um armazenamento (se houver suporte) para entender o tipo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b14b5-114">You must examine a storage's attributes and metadata (if supported) to understand what kind of storage it is.</span></span> <span data-ttu-id="b14b5-115">Os armazenamentos são organizados hierarquicamente no dispositivo; cada armazenamento tem exatamente um pai e todos os armazenamentos acabaram em um único armazenamento de dispositivo raiz, normalmente denominado " \\ ".</span><span class="sxs-lookup"><span data-stu-id="b14b5-115">Storages are organized hierarchically on the device; every storage has exactly one parent, and all storages ultimately descend from a single root device storage, typically named "\\".</span></span>

<span data-ttu-id="b14b5-116">As etapas a seguir descrevem como explorar um dispositivo:</span><span class="sxs-lookup"><span data-stu-id="b14b5-116">The following steps describe how to explore a device:</span></span>

1.  <span data-ttu-id="b14b5-117">Obtenha a interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) de um dispositivo conforme descrito em [enumerando dispositivos](enumerating-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b14b5-117">Get the [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface of a device as described in [Enumerating Devices](enumerating-devices.md).</span></span>
2.  <span data-ttu-id="b14b5-118">Chame [**IWMDMDevice:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) para recuperar uma interface [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="b14b5-118">Call [**IWMDMDevice::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) to retrieve an [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) interface.</span></span> <span data-ttu-id="b14b5-119">Essa interface é usada para obter todos os objetos filho do armazenamento que retorna essa interface.</span><span class="sxs-lookup"><span data-stu-id="b14b5-119">This interface is used to get all child objects of the storage that returns this interface.</span></span> <span data-ttu-id="b14b5-120">Ao obter essa interface do dispositivo, como estamos aqui, ele manterá apenas um armazenamento: o armazenamento do dispositivo raiz.</span><span class="sxs-lookup"><span data-stu-id="b14b5-120">When getting this interface from the device, as we are here, it will hold only one storage: the root device storage.</span></span>
3.  <span data-ttu-id="b14b5-121">Chame [**IWMDMEnumStorage:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) com uma contagem de 1 para recuperar a interface [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) para o armazenamento do dispositivo raiz.</span><span class="sxs-lookup"><span data-stu-id="b14b5-121">Call [**IWMDMEnumStorage::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) with a count of 1 to retrieve the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface for the root device storage.</span></span> <span data-ttu-id="b14b5-122">(Não é possível solicitar mais de um filho do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="b14b5-122">(You cannot request more than one child from the device.)</span></span>
4.  <span data-ttu-id="b14b5-123">Examine todos os armazenamentos no dispositivo chamando recursivamente [**IWMDMStorage:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) e, em seguida, **IWMDMEnumStorage:: Next** para obter filhos de um armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b14b5-123">Examine all storages on the device by recursively calling [**IWMDMStorage::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) and then **IWMDMEnumStorage::Next** to get children of a storage.</span></span> <span data-ttu-id="b14b5-124">Para ver se um armazenamento tem filhos para evitar as chamadas para **EnumStorage** e **Avançar**, você pode chamar [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para verificar os sinalizadores o \_ atributo de armazenamento WMDM \_ \_ tem \_ arquivos ou o \_ atributo de armazenamento WMDM \_ \_ tem \_ pastas.</span><span class="sxs-lookup"><span data-stu-id="b14b5-124">To see if a storage has children to avoid the calls to **EnumStorage** and **Next**, you can call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to check for the flags WMDM\_STORAGE\_ATTR\_HAS\_FILES or WMDM\_STORAGE\_ATTR\_HAS\_FOLDERS.</span></span> <span data-ttu-id="b14b5-125">Para obter mais informações sobre como obter as propriedades de um armazenamento, consulte [obtendo e definindo metadados e atributos](getting-and-setting-metadata-and-attributes.md) e [obtendo e configurando metadados e atributos no aplicativo](getting-and-setting-metadata-and-attributes-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="b14b5-125">For more information about how to get the properties of a storage, see [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md) and [Getting and Setting Metadata and Attributes in the Application](getting-and-setting-metadata-and-attributes-in-the-application.md).</span></span>

<span data-ttu-id="b14b5-126">O Windows Media Gerenciador de Dispositivos não expõe um conjunto padrão de pastas para manter a mídia de um tipo específico (por exemplo, uma pasta "minhas listas de reprodução" para listas de reprodução).</span><span class="sxs-lookup"><span data-stu-id="b14b5-126">Windows Media Device Manager does not expose a standard set of folders to hold media of a specific type (for example, a "My Playlists" folder for playlists).</span></span> <span data-ttu-id="b14b5-127">Cada dispositivo tem um sistema de arquivos exclusivo, e você terá que decidir um local apropriado para procurar ou enviar um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="b14b5-127">Every device has a unique file system, and you will have to decide on an appropriate place to look for, or to send, a specific file.</span></span>

> [!Note]  
> <span data-ttu-id="b14b5-128">O Windows Explorer pode mostrar as pastas virtuais que não existem de fato no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b14b5-128">Windows Explorer can show virtual folders that do not actually exist on the device.</span></span> <span data-ttu-id="b14b5-129">As pastas virtuais de exemplo são as pastas "mídia" e "dados" exibidas para dispositivos MTP.</span><span class="sxs-lookup"><span data-stu-id="b14b5-129">Example virtual folders are the "Media" and "Data" folders displayed for MTP devices.</span></span> <span data-ttu-id="b14b5-130">Essas pastas são criadas pelo Windows para tornar os downloads mais simples para os usuários finais; Eles não existem de fato no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b14b5-130">These folders are created by Windows to make downloads simpler for end users; they do not actually exist on the device.</span></span> <span data-ttu-id="b14b5-131">Seu aplicativo não deve depender de encontrar esses tipos de pastas gerais.</span><span class="sxs-lookup"><span data-stu-id="b14b5-131">Your application should not depend on finding these types of general folders.</span></span> <span data-ttu-id="b14b5-132">Por outro lado, o Windows Explorer pode não mostrar algumas pastas ou objetos que existem no dispositivo (por exemplo, listas de reprodução).</span><span class="sxs-lookup"><span data-stu-id="b14b5-132">Conversely, Windows Explorer might not show some folders or objects that do exist on the device (for example, playlists).</span></span>

 

<span data-ttu-id="b14b5-133">O código de exemplo C++ a seguir demonstra a exploração recursiva de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b14b5-133">The following C++ example code demonstrates the recursive exploration of a device.</span></span> <span data-ttu-id="b14b5-134">Ele usa duas funções:</span><span class="sxs-lookup"><span data-stu-id="b14b5-134">It uses two functions:</span></span>

-   <span data-ttu-id="b14b5-135">ExploreDevice, uma função inicial que recebe um ponteiro de dispositivo e Obtém um ponteiro para o enumerador raiz para esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b14b5-135">ExploreDevice, a starting function that receives a device pointer and obtains a pointer to the root enumerator for that device.</span></span>
-   <span data-ttu-id="b14b5-136">RecursiveExploreStorage, que é chamado para explorar um dispositivo recursivamente.</span><span class="sxs-lookup"><span data-stu-id="b14b5-136">RecursiveExploreStorage, which is called to explore a device recursively.</span></span>


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="b14b5-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b14b5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b14b5-138">**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**</span><span class="sxs-lookup"><span data-stu-id="b14b5-138">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




