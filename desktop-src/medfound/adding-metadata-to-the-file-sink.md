---
description: O coletor de arquivos ASF é uma implementação de IMFMediaSink fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto de coletor de mídia ASF e uso geral, consulte coletores de mídia ASF.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Adicionando metadados ao coletor de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bb63a10d935b52e6d048dbc5dcd07370dd2ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010537"
---
# <a name="adding-metadata-to-the-file-sink"></a>Adicionando metadados ao coletor de arquivos

O coletor de arquivos ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto do coletor de mídia ASF e o uso geral, consulte [coletores de mídia ASF](asf-media-sinks.md).

Depois de [criar o coletor de arquivos ASF](creating-the-asf-file-sink.md), ele deve ser configurado com informações sobre os fluxos e as informações de codificação no arquivo de saída. Esses procedimentos são descritos em [adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md) e [definindo as propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md). Além disso, você também pode adicionar informações de metadados, incluindo pares de nome/valor, como "autor", título ". Este tópico descreve o processo de adicionar informações de metadados ao coletor de arquivos para que ele apareça no [objeto de cabeçalho ASF](asf-file-structure.md)final.

Você pode adicionar informações de metadados ao coletor de arquivo ASF antes de compilar a topologia de codificação. O objeto ContentInfo do ASF para o coletor de arquivos controla as propriedades de metadados e são expostos ao aplicativo por meio da interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) . Algumas dessas propriedades, como "IsVBR", que indica se o arquivo contém fluxos de taxa de bits variável (VBR), são definidas automaticamente pelo coletor de arquivos analisando as propriedades de codificação de fluxo que estão definidas.

Para obter uma lista completa das propriedades, consulte o tópico "lista de atributos" no formato documentação do SDK.

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a>Usando a interface IMFMetadata no coletor de arquivo ASF

1.  Consulte o objeto de coletor de arquivo ASF para obter um ponteiro para sua implementação da interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .
2.  Chame [**IMFMetadataProvider:: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) para obter um ponteiro [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .

    O parâmetro *pPresentationDescriptor* é ignorado e o aplicativo pode passar **nulo**. Se o aplicativo passar zero como o identificador de fluxo no parâmetro *dwStreamIdentifier* , o método recuperará os metadados que se aplicam ao arquivo ASF inteiro. Caso contrário, somente os metadados do fluxo serão recuperados.

3.  Chame [**IMFMetadata:: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para recuperar a lista de propriedades de codificação de arquivo definida no conteúdo de mídia.
4.  Chame [**IMFMetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) para obter os valores de propriedade.

## <a name="example"></a>Exemplo

O código de exemplo a seguir mostra como enumerar os nomes de propriedade e os valores que são definidos no arquivo ASF.


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coletores de mídia ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



