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
# <a name="using-the-system-device-enumerator"></a>Usando o enumerador de dispositivo do sistema

O enumerador de dispositivo do sistema fornece uma maneira uniforme de enumerar, por categoria, os filtros registrados no sistema de um usuário. Além disso, ele diferencia os dispositivos de hardware individuais, mesmo que o mesmo filtro ofereça suporte a eles. Isso é particularmente útil para dispositivos que usam o Windows Driver Model (WDM) e o filtro KSProxy. Por exemplo, o usuário pode ter vários dispositivos de captura de vídeo WDM, todos com suporte no mesmo filtro. O enumerador de dispositivo do sistema os trata como instâncias de dispositivo separadas.

O enumerador de dispositivo do sistema funciona criando um enumerador para uma categoria específica, como captura de áudio ou compactação de vídeo. O enumerador de categoria retorna um moniker exclusivo para cada dispositivo na categoria. O enumerador de categoria inclui automaticamente todos os dispositivos Plug and Play relevantes na categoria. Para obter uma lista de categorias, consulte [Filtrar categorias](filter-categories.md).

Para usar o enumerador de dispositivo do sistema, faça o seguinte:

1.  Crie o enumerador de dispositivo do sistema chamando **CoCreateInstance**. O CLSID (identificador de classe) é CLSID \_ SystemDeviceEnum.
2.  Obtenha um enumerador de categoria chamando [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o CLSID da categoria desejada. Esse método retorna um ponteiro de interface **IEnumMoniker** . Se a categoria estiver vazia (ou não existir), o método retornará S \_ false em vez de um código de erro. Nesse caso, o ponteiro **IEnumMoniker** retornado é **nulo** e a desreferência dele causará uma exceção. Portanto, teste explicitamente para S \_ OK quando você chama **CreateClassEnumerator**, em vez de chamar a macro usualmente **bem-sucedida** .
3.  Use o método **IEnumMoniker:: Next** para enumerar cada moniker. Esse método retorna um ponteiro de interface **IMoniker** . Quando o **próximo** método atinge o final da enumeração, ele também retorna s \_ false; portanto, verifique novamente por s \_ OK.
4.  Para recuperar o nome amigável do dispositivo (por exemplo, para exibir na interface do usuário), chame o método **IMoniker:: BindToStorage** .
5.  Para criar e inicializar o filtro do DirectShow que gerencia o dispositivo, chame **IMoniker:: BindToObject** no moniker. Chame [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o filtro ao grafo.

O diagrama a seguir ilustra esse processo.

![Enumerando dispositivos](images/sysdevenum.png)

O exemplo a seguir mostra como enumerar os compactadores de vídeo instalados no sistema do usuário. Para resumir, o exemplo executa a verificação mínima de erros.


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



**Monikers de dispositivo**

Para monikers de dispositivo, você pode passar o moniker para o método [**IFilterGraph2:: AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) para criar um filtro de captura para o dispositivo. Para obter um exemplo de código, consulte a documentação para esse método.

O método **IMoniker:: GetDisplayName** retorna o nome de exibição do moniker. Embora o nome de exibição seja legível, você normalmente não o exibe para um usuário final. Em vez disso, obtenha o nome amigável do recipiente de propriedades, conforme descrito anteriormente.

O método **IMoniker::P arsedisplayname** ou a função **MkParseDisplayName** pode ser usado para criar um moniker de dispositivo padrão para uma determinada categoria de filtro. Use um nome de exibição com o formulário `@device:*:{category-clsid}` , em que `category-clsid` é a representação da cadeia de caracteres do GUID da categoria. O moniker padrão é o primeiro moniker retornado pelo enumerador de dispositivo para essa categoria.

 

 



