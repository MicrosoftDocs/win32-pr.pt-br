---
description: Criando filtros de Kernel-Mode
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Criando filtros de Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c915a08312e33f0e35245325fd8bce7e55e486c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087904"
---
# <a name="creating-kernel-mode-filters"></a><span data-ttu-id="a5b65-103">Criando filtros de Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="a5b65-103">Creating Kernel-Mode Filters</span></span>

<span data-ttu-id="a5b65-104">Determinados filtros no modo kernel não podem ser criados por meio de **CoCreateInstance** e, portanto, não têm CLSIDs.</span><span class="sxs-lookup"><span data-stu-id="a5b65-104">Certain kernel-mode filters cannot be created through **CoCreateInstance**, and thus do not have CLSIDs.</span></span> <span data-ttu-id="a5b65-105">Esses filtros incluem o [conversor de t/Sink-to-Sink](tee-sink-to-sink-converter.md), o filtro de [decodificador de CC](cc-decoder-filter.md) e o filtro de [codec de WST](wst-codec-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b65-105">These filters include the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md), the [CC Decoder](cc-decoder-filter.md) filter, and the [WST Codec](wst-codec-filter.md) filter.</span></span> <span data-ttu-id="a5b65-106">Para criar um desses filtros, use o objeto [enumerador de dispositivo do sistema](system-device-enumerator.md) e pesquise pelo nome do filtro.</span><span class="sxs-lookup"><span data-stu-id="a5b65-106">To create one of these filters, use the [System Device Enumerator](system-device-enumerator.md) object and search by the filter's name.</span></span>

1.  <span data-ttu-id="a5b65-107">Crie o enumerador de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="a5b65-107">Create the System Device Enumerator.</span></span>
2.  <span data-ttu-id="a5b65-108">Chame o método [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o CLSID da categoria de filtro para esse filtro.</span><span class="sxs-lookup"><span data-stu-id="a5b65-108">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method with the CLSID of the filter category for that filter.</span></span> <span data-ttu-id="a5b65-109">Esse método cria um enumerador para a categoria de filtro.</span><span class="sxs-lookup"><span data-stu-id="a5b65-109">This method creates an enumerator for the filter category.</span></span> <span data-ttu-id="a5b65-110">(Um *enumerador* é simplesmente um objeto que retorna uma lista de outros objetos, usando uma interface com definida.) O enumerador retorna ponteiros **IMoniker** , que representam os filtros nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="a5b65-110">(An *enumerator* is simply an object that returns a list of other objects, using a defined COM interface.) The enumerator returns **IMoniker** pointers, which represent the filters in that category.</span></span>
3.  <span data-ttu-id="a5b65-111">Para cada moniker, chame **IMoniker:: BindToStorage** para obter uma interface **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="a5b65-111">For each moniker, call **IMoniker::BindToStorage** to get an **IPropertyBag** interface.</span></span>
4.  <span data-ttu-id="a5b65-112">Chame **IPropertyBag:: Read** para obter o nome do filtro.</span><span class="sxs-lookup"><span data-stu-id="a5b65-112">Call **IPropertyBag::Read** to get the name of the filter.</span></span>
5.  <span data-ttu-id="a5b65-113">Se o nome corresponder, chame **IMoniker:: BindToObject** para criar o filtro.</span><span class="sxs-lookup"><span data-stu-id="a5b65-113">If the name matches, call **IMoniker::BindToObject** to create the filter.</span></span>

<span data-ttu-id="a5b65-114">O código a seguir mostra uma função que executa estas etapas:</span><span class="sxs-lookup"><span data-stu-id="a5b65-114">The following code shows a function that performs these steps:</span></span>


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



<span data-ttu-id="a5b65-115">O exemplo de código a seguir usa essa função para criar o filtro de decodificador de CC e adicioná-lo ao grafo de filtro:</span><span class="sxs-lookup"><span data-stu-id="a5b65-115">The following code example uses this function to create the CC Decoder filter and add it to the filter graph:</span></span>


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="a5b65-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5b65-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5b65-117">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="a5b65-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="a5b65-118">Usando o enumerador de dispositivo do sistema</span><span class="sxs-lookup"><span data-stu-id="a5b65-118">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



