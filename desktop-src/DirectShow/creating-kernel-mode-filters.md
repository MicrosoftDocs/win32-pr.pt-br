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
# <a name="creating-kernel-mode-filters"></a>Criando filtros de Kernel-Mode

Determinados filtros no modo kernel não podem ser criados por meio de **CoCreateInstance** e, portanto, não têm CLSIDs. Esses filtros incluem o [conversor de t/Sink-to-Sink](tee-sink-to-sink-converter.md), o filtro de [decodificador de CC](cc-decoder-filter.md) e o filtro de [codec de WST](wst-codec-filter.md) . Para criar um desses filtros, use o objeto [enumerador de dispositivo do sistema](system-device-enumerator.md) e pesquise pelo nome do filtro.

1.  Crie o enumerador de dispositivo do sistema.
2.  Chame o método [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o CLSID da categoria de filtro para esse filtro. Esse método cria um enumerador para a categoria de filtro. (Um *enumerador* é simplesmente um objeto que retorna uma lista de outros objetos, usando uma interface com definida.) O enumerador retorna ponteiros **IMoniker** , que representam os filtros nessa categoria.
3.  Para cada moniker, chame **IMoniker:: BindToStorage** para obter uma interface **IPropertyBag** .
4.  Chame **IPropertyBag:: Read** para obter o nome do filtro.
5.  Se o nome corresponder, chame **IMoniker:: BindToObject** para criar o filtro.

O código a seguir mostra uma função que executa estas etapas:


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



O exemplo de código a seguir usa essa função para criar o filtro de decodificador de CC e adicioná-lo ao grafo de filtro:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



