---
description: Escolhendo um filtro de compactação
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Escolhendo um filtro de compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088775"
---
# <a name="choosing-a-compression-filter"></a><span data-ttu-id="0da5a-103">Escolhendo um filtro de compactação</span><span class="sxs-lookup"><span data-stu-id="0da5a-103">Choosing a Compression Filter</span></span>

<span data-ttu-id="0da5a-104">Vários tipos de componentes de software podem executar a compactação de vídeo ou áudio, como:</span><span class="sxs-lookup"><span data-stu-id="0da5a-104">Several types of software components can perform video or audio compression, such as:</span></span>

-   <span data-ttu-id="0da5a-105">Filtros do DirectShow nativo</span><span class="sxs-lookup"><span data-stu-id="0da5a-105">Native DirectShow filters</span></span>
-   <span data-ttu-id="0da5a-106">Codecs do VCM (Gerenciador de compactação de vídeo)</span><span class="sxs-lookup"><span data-stu-id="0da5a-106">Video Compression Manager (VCM) codecs</span></span>
-   <span data-ttu-id="0da5a-107">Codecs do Gerenciador de compactação de áudio (ACM)</span><span class="sxs-lookup"><span data-stu-id="0da5a-107">Audio Compression Manager (ACM) codecs</span></span>
-   <span data-ttu-id="0da5a-108">DMOs (objetos de mídia do DirectX)</span><span class="sxs-lookup"><span data-stu-id="0da5a-108">DirectX Media Objects (DMOs)</span></span>

<span data-ttu-id="0da5a-109">No DirectShow, os codecs VCM são encapsulados pelo [filtro de compressor AVI](avi-compressor-filter.md)e os codecs do ACM são encapsulados pelo [filtro de invólucro do ACM](acm-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="0da5a-109">In DirectShow, VCM codecs are wrapped by the [AVI Compressor Filter](avi-compressor-filter.md), and ACM codecs are wrapped by the [ACM Wrapper Filter](acm-wrapper-filter.md).</span></span> <span data-ttu-id="0da5a-110">DMOs são encapsuladas pelo [filtro de invólucro do DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="0da5a-110">DMOs are wrapped by the [DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="0da5a-111">O enumerador de dispositivo do sistema fornece uma maneira consistente de enumerar e criar qualquer um desses tipos de compressor, sem se preocupar com o modelo subjacente.</span><span class="sxs-lookup"><span data-stu-id="0da5a-111">The system device enumerator provides a consistent way to enumerate and create any of these compressor types, without worrying about the underlying model.</span></span>

<span data-ttu-id="0da5a-112">Para obter detalhes sobre o enumerador de dispositivo do sistema, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="0da5a-112">For details about the system device enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="0da5a-113">Resumidamente, todos os filtros do DirectShow são classificados por categoria e cada categoria é identificada por um GUID.</span><span class="sxs-lookup"><span data-stu-id="0da5a-113">Briefly, all DirectShow filters are classified by category, and each category is identified by a GUID.</span></span> <span data-ttu-id="0da5a-114">Para os compactadores de vídeo, o GUID da categoria é CLSID \_ VideoCompressorCategory.</span><span class="sxs-lookup"><span data-stu-id="0da5a-114">For video compressors, the category GUID is CLSID\_VideoCompressorCategory.</span></span> <span data-ttu-id="0da5a-115">Para os compactadores de áudio, é CLSID \_ AudioCompressorCategory.</span><span class="sxs-lookup"><span data-stu-id="0da5a-115">For audio compressors, it is CLSID\_AudioCompressorCategory.</span></span> <span data-ttu-id="0da5a-116">Para enumerar uma determinada categoria, o enumerador de dispositivo do sistema cria um objeto *enumerador* que dá suporte à interface [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="0da5a-116">To enumerate a particular category, the system device enumerator creates an *enumerator* object that supports the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="0da5a-117">O aplicativo usa essa interface para recuperar monikers de dispositivo, onde cada moniker de dispositivo representa uma instância de um filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0da5a-117">The application uses this interface to retrieve device monikers, where each device moniker represents an instance of a DirectShow filter.</span></span> <span data-ttu-id="0da5a-118">Você pode usar o moniker para criar o filtro ou para obter o nome amigável do dispositivo sem criar o filtro.</span><span class="sxs-lookup"><span data-stu-id="0da5a-118">You can use the moniker to create the filter, or to get the device's friendly name without creating the filter.</span></span>

<span data-ttu-id="0da5a-119">Para enumerar os compactadores de vídeo ou áudio disponíveis no sistema do usuário, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0da5a-119">To enumerate the video or audio compressors available on the user's system, do the following:</span></span>

1.  <span data-ttu-id="0da5a-120">Chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o enumerador de dispositivo do sistema, que tem uma ID de classe de CLSID \_ SystemDeviceEnum.</span><span class="sxs-lookup"><span data-stu-id="0da5a-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the system device enumerator, which has a class ID of CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="0da5a-121">Chame [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o GUID da categoria de filtro.</span><span class="sxs-lookup"><span data-stu-id="0da5a-121">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the filter category GUID.</span></span> <span data-ttu-id="0da5a-122">O método retorna um ponteiro de interface **IEnumMoniker** .</span><span class="sxs-lookup"><span data-stu-id="0da5a-122">The method returns an **IEnumMoniker** interface pointer.</span></span>
3.  <span data-ttu-id="0da5a-123">Use o método IEnumMoniker:: Next para enumerar os monikers de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0da5a-123">Use the IEnumMoniker::Next method to enumerate the device monikers.</span></span> <span data-ttu-id="0da5a-124">Esse método retorna uma interface [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , que representa o moniker.</span><span class="sxs-lookup"><span data-stu-id="0da5a-124">This method returns an [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) interface, which represents the moniker.</span></span>

<span data-ttu-id="0da5a-125">Para obter o nome amigável de um moniker, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0da5a-125">To get the friendly name from a moniker, do the following:</span></span>

1.  <span data-ttu-id="0da5a-126">Chame o método **IMoniker:: BindToStorage** .</span><span class="sxs-lookup"><span data-stu-id="0da5a-126">Call the **IMoniker::BindToStorage** method.</span></span> <span data-ttu-id="0da5a-127">Esse método retorna um ponteiro de interface **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="0da5a-127">This method returns an **IPropertyBag** interface pointer.</span></span>
2.  <span data-ttu-id="0da5a-128">Use o método **IPropertyBag:: Read** para ler a propriedade **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="0da5a-128">Use the **IPropertyBag::Read** method to read the **FriendlyName** property.</span></span>

<span data-ttu-id="0da5a-129">Normalmente, um aplicativo exibiria uma lista de compactadores, para que o usuário pudesse escolher um.</span><span class="sxs-lookup"><span data-stu-id="0da5a-129">Typically, an application would display a list of compressors, so that the user could choose one.</span></span> <span data-ttu-id="0da5a-130">Por exemplo, o código a seguir preenche uma caixa de listagem com os nomes dos compactadores de vídeo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0da5a-130">For example, the following code populates a list box with the names of the available video compressors.</span></span>


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



<span data-ttu-id="0da5a-131">Para criar uma instância de filtro a partir do moniker, chame o método **IMoniker:: BindToObject** .</span><span class="sxs-lookup"><span data-stu-id="0da5a-131">To create a filter instance from the moniker, call the **IMoniker::BindToObject** method.</span></span> <span data-ttu-id="0da5a-132">O método retorna um ponteiro [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="0da5a-132">The method returns an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



<span data-ttu-id="0da5a-133">Para codecs VCM, cada moniker representa um codec específico, embora todos os codecs sejam encapsulados pelo mesmo filtro de compactação AVI.</span><span class="sxs-lookup"><span data-stu-id="0da5a-133">For VCM codecs, each moniker represents one particular codec, even though all of the codecs are wrapped by the same AVI Compression filter.</span></span> <span data-ttu-id="0da5a-134">Chamar **BindToObject** cria uma instância desse filtro, inicializada para esse codec.</span><span class="sxs-lookup"><span data-stu-id="0da5a-134">Calling **BindToObject** creates an instance of this filter, initialized for that codec.</span></span> <span data-ttu-id="0da5a-135">Por esse motivo, você não pode chamar **CoCreateInstance** diretamente no filtro de compactação avi.</span><span class="sxs-lookup"><span data-stu-id="0da5a-135">For this reason, you cannot call **CoCreateInstance** directly on the AVI Compression filter.</span></span> <span data-ttu-id="0da5a-136">Você deve passar pelo enumerador de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="0da5a-136">You must go through the system device enumerator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0da5a-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0da5a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0da5a-138">Recompactando um arquivo AVI</span><span class="sxs-lookup"><span data-stu-id="0da5a-138">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 
