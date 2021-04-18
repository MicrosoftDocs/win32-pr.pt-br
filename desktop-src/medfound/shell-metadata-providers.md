---
description: A partir do Windows 7, Microsoft Media Foundation expõe os metadados por meio da interface IPropertyStore.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Provedores de metadados do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788685"
---
# <a name="shell-metadata-providers"></a>Provedores de metadados do Shell

A partir do Windows 7, Microsoft Media Foundation expõe os metadados por meio da interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Os metadados obtidos usando o processo definido neste tópico devem ser usados somente para acesso somente leitura. Não há suporte para a gravação de dados usando esse processo. Você pode criar um objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para fins de escrita usando um identificador de classe (CLSID) obtido do [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).

## <a name="reading-metadata"></a>Lendo metadados

Para ler metadados de uma fonte de mídia, execute as seguintes etapas:

1.  Obtenha um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da origem da mídia. Você pode usar a interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obter um ponteiro **IMFMediaSource** .
2.  Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) na origem de mídia para obter um ponteiro para a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . No parâmetro *guidService* de **MFGetService**, especifique o valor do **\_ serviço de \_ manipulador \_ de propriedades MF**. Se a origem não oferecer suporte à interface **IPropertyStore** , **MFGetService** retornará **o \_ serviço MF E \_ sem \_ suporte**.
3.  Chame os métodos [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para enumerar as propriedades de metadados.

O código a seguir mostra essas etapas. Suponha que `DisplayProperty` seja uma função que exibe um valor de **PROPVARIANT** .


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



Para obter uma lista de chaves de propriedade de metadados, consulte [Propriedades de metadados para arquivos de mídia](metadata-properties-for-media-files.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Metadados de mídia](media-metadata.md)
</dt> </dl>

 

 
