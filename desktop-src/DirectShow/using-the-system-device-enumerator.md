---
description: Usando o enumerador de dispositivo do sistema
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Usando o enumerador de dispositivo do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7192a1ea85d807dd388b79eef455edf59c83d3c22ab3a4a330799b3491253bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083526"
---
# <a name="using-the-system-device-enumerator"></a>Usando o enumerador de dispositivo do sistema

O Enumerador de Dispositivo do Sistema fornece uma maneira uniforme de enumerar, por categoria, os filtros registrados no sistema de um usuário. Além disso, ele diferencia entre dispositivos de hardware individuais, mesmo que o mesmo filtro seja compatível com eles. Isso é particularmente útil para dispositivos que usam o WDM (modelo Windows driver) e o filtro KSProxy. Por exemplo, o usuário pode ter vários dispositivos de captura de vídeo WDM, todos com suporte pelo mesmo filtro. O Enumerador de Dispositivo do Sistema os trata como instâncias de dispositivo separadas.

O Enumerador de Dispositivo do Sistema funciona criando um enumerador para uma categoria específica, como captura de áudio ou compactação de vídeo. O enumerador de categoria retorna um moniker exclusivo para cada dispositivo na categoria. O enumerador de categoria inclui automaticamente todos os Plug and Play relevantes na categoria. Para ver uma lista de categorias, consulte [Categorias de filtro.](filter-categories.md)

Para usar o Enumerador de Dispositivo do Sistema, faça o seguinte:

1.  Crie o enumerador de dispositivo do sistema chamando **CoCreateInstance**. O CLSID (identificador de classe) é CLSID \_ SystemDeviceEnum.
2.  Obtenha um enumerador de categoria chamando [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) com o CLSID da categoria desejada. Esse método retorna um ponteiro de interface **IEnumMoniker.** Se a categoria estiver vazia (ou não existir), o método retornará S \_ FALSE em vez de um código de erro. Em caso afirmatório, o ponteiro **IEnumMoniker** retornado é **NULL** e dereferenciá-lo causará uma exceção. Portanto, teste explicitamente para S OK quando você chamar \_ **CreateClassEnumerator**, em vez de chamar a macro **SUCCEEDED** normal.
3.  Use o **método IEnumMoniker::Next** para enumerar cada moniker. Esse método retorna um ponteiro de interface **IMoniker.** Quando o **método Next** atingir o final da enumeração, ele também retornará S \_ FALSE, portanto, verifique novamente se há S \_ OK.
4.  Para recuperar o nome amigável do dispositivo (por exemplo, para exibição na interface do usuário), chame o **método IMoniker::BindToStorage.**
5.  Para criar e inicializar o filtro DirectShow que gerencia o dispositivo, chame **IMoniker::BindToObject** no moniker. Chame [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o filtro ao grafo.

O diagrama a seguir ilustra esse processo.

![enumerando dispositivos](images/sysdevenum.png)

O exemplo a seguir mostra como enumerar os videoclipes instalados no sistema do usuário. Para brevidade, o exemplo executa a verificação mínima de erros.


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

Para monikers de dispositivo, você pode passar o moniker para o método [**IFilterGraph2::AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) para criar um filtro de captura para o dispositivo. Para ver o código de exemplo, consulte a documentação desse método.

O **método IMoniker::GetDisplayName** retorna o nome de exibição do moniker. Embora o nome de exibição seja acessível, você normalmente não o exibiria para um usuário final. Em vez disso, obter o nome amigável do pacote de propriedades, conforme descrito anteriormente.

O **método IMoniker::P arseDisplayName** ou a **função MkParseDisplayName** pode ser usado para criar um moniker de dispositivo padrão para uma determinada categoria de filtro. Use um nome de exibição com o formulário , em que é a `@device:*:{category-clsid}` representação de cadeia de `category-clsid` caracteres do GUID da categoria. O moniker padrão é o primeiro moniker retornado pelo enumerador de dispositivo para essa categoria.

 

 



