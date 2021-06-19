---
description: Saiba mais sobre como adicionar metadados ao sink de arquivo ASF, que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Adicionando metadados ao sink de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ea86a09ff9e3d2a25bbf8d00d46691fd803365
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409959"
---
# <a name="adding-metadata-to-the-file-sink"></a>Adicionando metadados ao sink de arquivo

O sink de arquivo ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto e o uso geral dos sinks de mídia do ASF, consulte [AsF Media Sinks](asf-media-sinks.md).

Depois [de Criar o sink do arquivo ASF](creating-the-asf-file-sink.md), ele deve ser configurado com informações sobre os fluxos e informações de codificação no arquivo de saída. Esses procedimentos são descritos em [Adicionando informações de fluxo ao sink de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md) e [Definindo propriedades no sink de arquivo](setting-properties-in-the-file-sink.md). Além disso, você também pode adicionar informações de metadados que incluem pares de nome/valor, como "Autor", Título". Este tópico descreve o processo de adição de informações de metadados ao sink de arquivo para que ele apareça no Objeto de [Header ASF final](asf-file-structure.md).

Você pode adicionar informações de metadados ao sink do arquivo ASF antes de criar a topologia de codificação. O objeto ContentInfo do ASF para o sink de arquivo acompanha as propriedades de metadados e é exposto ao aplicativo por meio da interface [**IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) Algumas dessas propriedades, como "IsVBR", que indica se o arquivo contém fluxos de VBR (taxa de bits variável), são definidas automaticamente pelo sink de arquivo por meio da análise das propriedades de codificação de fluxo definidas.

Para ver uma lista completa de propriedades, consulte o tópico "Lista de Atributos" na documentação do SDK de Formato.

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a>Usando a interface IMFMetadata no sink de arquivo ASF

1.  Consulte o objeto de sink do arquivo ASF para obter um ponteiro para sua implementação da interface [**IMFMetadataProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)
2.  Chame [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) para obter um [**ponteiro IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)

    O *parâmetro pPresentationDescriptor* é ignorado e o aplicativo pode passar **NULL.** Se o aplicativo passar zero como o identificador de fluxo no parâmetro *dwStreamIdentifier,* o método recuperará metadados que se aplicarão a todo o arquivo ASF. Caso contrário, somente os metadados do fluxo são recuperados.

3.  Chame [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para recuperar a lista de propriedades de codificação de arquivo definidas no conteúdo da mídia.
4.  Chame [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) para obter os valores da propriedade.

## <a name="example"></a>Exemplo

O código de exemplo a seguir mostra como enumerar os nomes de propriedade e os valores definidos no arquivo ASF.


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

[Sinks de mídia do ASF](asf-media-sinks.md)
</dt> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



