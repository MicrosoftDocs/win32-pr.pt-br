---
description: A partir Windows 7, Microsoft Media Foundation expõe metadados por meio da interface IPropertyStore.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Provedores de metadados do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31960ed41743a86b62b63555236d2876166a14b098f0692f3d6cb22b051e338e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713356"
---
# <a name="shell-metadata-providers"></a>Provedores de metadados do Shell

A partir Windows 7, Microsoft Media Foundation expõe metadados por meio da interface [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Os metadados obtidos usando o processo definido neste tópico só devem ser usados para acesso somente leitura. Não há suporte para a escrita de dados usando esse processo. Você pode criar um objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para fins de escrita usando um CLSID (identificador de classe) obtido de [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).

## <a name="reading-metadata"></a>Lendo metadados

Para ler metadados de uma fonte de mídia, execute as seguintes etapas:

1.  Obter um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia. Você pode usar a interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obter um **ponteiro IMFMediaSource.**
2.  Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) na fonte de mídia para obter um ponteiro para a interface [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) No parâmetro *guidService* de **MFGetService**, especifique o valor **MF \_ PROPERTY HANDLER \_ \_ SERVICE**. Se a origem não for compatível com a interface **IPropertyStore,** **MFGetService** retornará **MF \_ E \_ UNSUPPORTED \_ SERVICE**.
3.  Chame [**métodos IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para enumerar as propriedades de metadados.

O código a seguir mostra estas etapas. Suponha que `DisplayProperty` seja uma função que exibe um valor **PROPVARIANT.**


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



Para ver uma lista de chaves de propriedade de metadados, consulte [Propriedades de metadados para arquivos de mídia](metadata-properties-for-media-files.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Metadados de mídia](media-metadata.md)
</dt> </dl>

 

 
