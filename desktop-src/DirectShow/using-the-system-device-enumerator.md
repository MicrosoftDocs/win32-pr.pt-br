---
description: Usando o enumerador de dispositivo do sistema
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Usando o enumerador de dispositivo do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567626"
---
# <a name="using-the-system-device-enumerator"></a><span data-ttu-id="1948d-103">Usando o enumerador de dispositivo do sistema</span><span class="sxs-lookup"><span data-stu-id="1948d-103">Using the System Device Enumerator</span></span>

<span data-ttu-id="1948d-104">O enumerador de dispositivo do sistema fornece uma maneira uniforme de enumerar, por categoria, os filtros registrados no sistema de um usuário.</span><span class="sxs-lookup"><span data-stu-id="1948d-104">The System Device Enumerator provides a uniform way to enumerate, by category, the filters registered on a user's system.</span></span> <span data-ttu-id="1948d-105">Além disso, ele diferencia os dispositivos de hardware individuais, mesmo que o mesmo filtro ofereça suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="1948d-105">Moreover, it differentiates between individual hardware devices, even if the same filter supports them.</span></span> <span data-ttu-id="1948d-106">Isso é particularmente útil para dispositivos que usam o Windows Driver Model (WDM) e o filtro KSProxy.</span><span class="sxs-lookup"><span data-stu-id="1948d-106">This is particularly useful for devices that use the Windows Driver Model (WDM) and the KSProxy filter.</span></span> <span data-ttu-id="1948d-107">Por exemplo, o usuário pode ter vários dispositivos de captura de vídeo WDM, todos com suporte no mesmo filtro.</span><span class="sxs-lookup"><span data-stu-id="1948d-107">For example, the user might have several WDM video capture devices, all supported by the same filter.</span></span> <span data-ttu-id="1948d-108">O enumerador de dispositivo do sistema os trata como instâncias de dispositivo separadas.</span><span class="sxs-lookup"><span data-stu-id="1948d-108">The System Device Enumerator treats them as separate device instances.</span></span>

<span data-ttu-id="1948d-109">O enumerador de dispositivo do sistema funciona criando um enumerador para uma categoria específica, como captura de áudio ou compactação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1948d-109">The System Device Enumerator works by creating an enumerator for a specific category, such as audio capture or video compression.</span></span> <span data-ttu-id="1948d-110">O enumerador de categoria retorna um moniker exclusivo para cada dispositivo na categoria.</span><span class="sxs-lookup"><span data-stu-id="1948d-110">The category enumerator returns a unique moniker for each device in the category.</span></span> <span data-ttu-id="1948d-111">O enumerador de categoria inclui automaticamente todos os dispositivos Plug and Play relevantes na categoria.</span><span class="sxs-lookup"><span data-stu-id="1948d-111">The category enumerator automatically includes any relevant Plug and Play devices in the category.</span></span> <span data-ttu-id="1948d-112">Para obter uma lista de categorias, consulte [Filtrar categorias](filter-categories.md).</span><span class="sxs-lookup"><span data-stu-id="1948d-112">For a list of categories, see [Filter Categories](filter-categories.md).</span></span>

<span data-ttu-id="1948d-113">Para usar o enumerador de dispositivo do sistema, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1948d-113">To use the System Device Enumerator, do the following:</span></span>

1.  <span data-ttu-id="1948d-114">Crie o enumerador de dispositivo do sistema chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="1948d-114">Create the system device enumerator by calling **CoCreateInstance**.</span></span> <span data-ttu-id="1948d-115">O CLSID (identificador de classe) é CLSID \_ SystemDeviceEnum.</span><span class="sxs-lookup"><span data-stu-id="1948d-115">The class identifier (CLSID) is CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="1948d-116">Obtenha um enumerador de categoria chamando [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o CLSID da categoria desejada.</span><span class="sxs-lookup"><span data-stu-id="1948d-116">Obtain a category enumerator by calling [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the CLSID of the desired category.</span></span> <span data-ttu-id="1948d-117">Esse método retorna um ponteiro de interface **IEnumMoniker** .</span><span class="sxs-lookup"><span data-stu-id="1948d-117">This method returns an **IEnumMoniker** interface pointer.</span></span> <span data-ttu-id="1948d-118">Se a categoria estiver vazia (ou não existir), o método retornará S \_ false em vez de um código de erro.</span><span class="sxs-lookup"><span data-stu-id="1948d-118">If the category is empty (or does not exist), the method returns S\_FALSE rather than an error code.</span></span> <span data-ttu-id="1948d-119">Nesse caso, o ponteiro **IEnumMoniker** retornado é **nulo** e a desreferência dele causará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="1948d-119">If so, the returned **IEnumMoniker** pointer is **NULL** and dereferencing it will cause an exception.</span></span> <span data-ttu-id="1948d-120">Portanto, teste explicitamente para S \_ OK quando você chama **CreateClassEnumerator**, em vez de chamar a macro usualmente **bem-sucedida** .</span><span class="sxs-lookup"><span data-stu-id="1948d-120">Therefore, explicitly test for S\_OK when you call **CreateClassEnumerator**, instead of calling the usual **SUCCEEDED** macro.</span></span>
3.  <span data-ttu-id="1948d-121">Use o método **IEnumMoniker:: Next** para enumerar cada moniker.</span><span class="sxs-lookup"><span data-stu-id="1948d-121">Use the **IEnumMoniker::Next** method to enumerate each moniker.</span></span> <span data-ttu-id="1948d-122">Esse método retorna um ponteiro de interface **IMoniker** .</span><span class="sxs-lookup"><span data-stu-id="1948d-122">This method returns an **IMoniker** interface pointer.</span></span> <span data-ttu-id="1948d-123">Quando o **próximo** método atinge o final da enumeração, ele também retorna s \_ false; portanto, verifique novamente por s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1948d-123">When the **Next** method reaches the end of the enumeration, it also returns S\_FALSE, so again check for S\_OK.</span></span>
4.  <span data-ttu-id="1948d-124">Para recuperar o nome amigável do dispositivo (por exemplo, para exibir na interface do usuário), chame o método **IMoniker:: BindToStorage** .</span><span class="sxs-lookup"><span data-stu-id="1948d-124">To retrieve the friendly name of the device (for example, to display in the user interface), call the **IMoniker::BindToStorage** method.</span></span>
5.  <span data-ttu-id="1948d-125">Para criar e inicializar o filtro do DirectShow que gerencia o dispositivo, chame **IMoniker:: BindToObject** no moniker.</span><span class="sxs-lookup"><span data-stu-id="1948d-125">To create and initialize the DirectShow filter that manages the device, call **IMoniker::BindToObject** on the moniker.</span></span> <span data-ttu-id="1948d-126">Chame [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o filtro ao grafo.</span><span class="sxs-lookup"><span data-stu-id="1948d-126">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span>

<span data-ttu-id="1948d-127">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="1948d-127">The following diagram illustrates this process.</span></span>

![Enumerando dispositivos](images/sysdevenum.png)

<span data-ttu-id="1948d-129">O exemplo a seguir mostra como enumerar os compactadores de vídeo instalados no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="1948d-129">The following example shows how to enumerate the video compressors installed on the user's system.</span></span> <span data-ttu-id="1948d-130">Para resumir, o exemplo executa a verificação mínima de erros.</span><span class="sxs-lookup"><span data-stu-id="1948d-130">For brevity, the example performs minimal error checking.</span></span>


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



<span data-ttu-id="1948d-131">**Monikers de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="1948d-131">**Device Monikers**</span></span>

<span data-ttu-id="1948d-132">Para monikers de dispositivo, você pode passar o moniker para o método [**IFilterGraph2:: AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) para criar um filtro de captura para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1948d-132">For device monikers, you can pass the moniker to the [**IFilterGraph2::AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) method to create a capture filter for the device.</span></span> <span data-ttu-id="1948d-133">Para obter um exemplo de código, consulte a documentação para esse método.</span><span class="sxs-lookup"><span data-stu-id="1948d-133">For example code, see the documentation for that method.</span></span>

<span data-ttu-id="1948d-134">O método **IMoniker:: GetDisplayName** retorna o nome de exibição do moniker.</span><span class="sxs-lookup"><span data-stu-id="1948d-134">The **IMoniker::GetDisplayName** method returns the display name of the moniker.</span></span> <span data-ttu-id="1948d-135">Embora o nome de exibição seja legível, você normalmente não o exibe para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="1948d-135">Although the display name is readable, you would not typically display it to an end-user.</span></span> <span data-ttu-id="1948d-136">Em vez disso, obtenha o nome amigável do recipiente de propriedades, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1948d-136">Get the friendly name from the property bag instead, as described previously.</span></span>

<span data-ttu-id="1948d-137">O método **IMoniker::P arsedisplayname** ou a função **MkParseDisplayName** pode ser usado para criar um moniker de dispositivo padrão para uma determinada categoria de filtro.</span><span class="sxs-lookup"><span data-stu-id="1948d-137">The **IMoniker::ParseDisplayName** method or the **MkParseDisplayName** function can be used to create a default device moniker for a given filter category.</span></span> <span data-ttu-id="1948d-138">Use um nome de exibição com o formulário `@device:*:{category-clsid}` , em que `category-clsid` é a representação da cadeia de caracteres do GUID da categoria.</span><span class="sxs-lookup"><span data-stu-id="1948d-138">Use a display name with the form `@device:*:{category-clsid}`, where `category-clsid` is the string representation of the category GUID.</span></span> <span data-ttu-id="1948d-139">O moniker padrão é o primeiro moniker retornado pelo enumerador de dispositivo para essa categoria.</span><span class="sxs-lookup"><span data-stu-id="1948d-139">The default moniker is the first moniker returned by the device enumerator for that category.</span></span>

 

 



