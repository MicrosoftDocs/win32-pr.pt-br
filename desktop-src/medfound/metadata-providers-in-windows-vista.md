---
description: No Windows Vista, Microsoft Media Foundation expõe metadados por meio da interface IMFMetadata.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Provedores de metadados no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759583"
---
# <a name="metadata-providers-in-windows-vista"></a>Provedores de metadados no Windows Vista

No Windows Vista, Microsoft Media Foundation expõe metadados por meio da interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .

## <a name="reading-metadata"></a>Lendo metadados

Para ler metadados de uma fonte de mídia, execute as seguintes etapas:

1.  Obtenha um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da origem da mídia. Você pode usar a interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obter um ponteiro **IMFMediaSource** .
2.  Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obter o descritor de apresentação da fonte de mídia.
3.  Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) na origem de mídia para obter um ponteiro para a interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) . No parâmetro *guidService* de **MFGetService**, especifique o valor **serviço do \_ \_ provedor de \_ metadados MF**. Se a origem não oferecer suporte à interface **IMFMetadataProvider** , **MFGetService** retornará **o \_ serviço MF E \_ sem \_ suporte**.
4.  Chame [**IMFMetadataProvider:: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) e transmita um ponteiro para o descritor de apresentação. Esse método retorna um ponteiro para a interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .
    -   Para obter metadados de nível de fluxo, primeiro chame [**IMFStreamDescriptor:: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) para obter o identificador de fluxo. Em seguida, passe o identificador de fluxo no parâmetro *dwStreamIdentifier* de [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).
    -   Para obter metadados no nível da apresentação, defina *dwStreamIdentifier* como zero.
5.  \[\]Chamada opcional [**IMFMetadata:: GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) para obter uma lista dos idiomas nos quais os metadados estão disponíveis. Os idiomas são identificados usando marcas de idioma compatíveis com o RFC 1766.
6.  \[\]Chamada opcional [**IMFMetadata:: setlanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) para selecionar o idioma.
7.  \[\]Chamada opcional [**IMFMetadata:: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para obter uma lista dos nomes de todas as propriedades de metadados para este fluxo ou apresentação.
8.  Chame [**IMFMetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) para obter um valor de propriedade de metadados específico, passando o nome da propriedade.

O código a seguir mostra as etapas 2 a 4:


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



O código a seguir mostra as etapas 7 a 8. Suponha que `DisplayProperty` seja uma função que exibe um valor de **PROPVARIANT** .


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Metadados de mídia](media-metadata.md)
</dt> <dt>

[Provedores de metadados do Shell](shell-metadata-providers.md)
</dt> </dl>

 

 



