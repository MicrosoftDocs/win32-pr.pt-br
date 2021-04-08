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
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="5cfc9-104">Adicionando metadados ao coletor de arquivos</span><span class="sxs-lookup"><span data-stu-id="5cfc9-104">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="5cfc9-105">O coletor de arquivos ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="5cfc9-106">Para obter informações sobre o modelo de objeto do coletor de mídia ASF e o uso geral, consulte [coletores de mídia ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="5cfc9-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="5cfc9-107">Depois de [criar o coletor de arquivos ASF](creating-the-asf-file-sink.md), ele deve ser configurado com informações sobre os fluxos e as informações de codificação no arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-107">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="5cfc9-108">Esses procedimentos são descritos em [adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md) e [definindo as propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="5cfc9-108">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="5cfc9-109">Além disso, você também pode adicionar informações de metadados, incluindo pares de nome/valor, como "autor", título ".</span><span class="sxs-lookup"><span data-stu-id="5cfc9-109">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="5cfc9-110">Este tópico descreve o processo de adicionar informações de metadados ao coletor de arquivos para que ele apareça no [objeto de cabeçalho ASF](asf-file-structure.md)final.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-110">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="5cfc9-111">Você pode adicionar informações de metadados ao coletor de arquivo ASF antes de compilar a topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-111">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="5cfc9-112">O objeto ContentInfo do ASF para o coletor de arquivos controla as propriedades de metadados e são expostos ao aplicativo por meio da interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="5cfc9-112">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="5cfc9-113">Algumas dessas propriedades, como "IsVBR", que indica se o arquivo contém fluxos de taxa de bits variável (VBR), são definidas automaticamente pelo coletor de arquivos analisando as propriedades de codificação de fluxo que estão definidas.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-113">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="5cfc9-114">Para obter uma lista completa das propriedades, consulte o tópico "lista de atributos" no formato documentação do SDK.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-114">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="5cfc9-115">Usando a interface IMFMetadata no coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="5cfc9-115">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="5cfc9-116">Consulte o objeto de coletor de arquivo ASF para obter um ponteiro para sua implementação da interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="5cfc9-116">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="5cfc9-117">Chame [**IMFMetadataProvider:: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) para obter um ponteiro [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="5cfc9-117">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="5cfc9-118">O parâmetro *pPresentationDescriptor* é ignorado e o aplicativo pode passar **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-118">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="5cfc9-119">Se o aplicativo passar zero como o identificador de fluxo no parâmetro *dwStreamIdentifier* , o método recuperará os metadados que se aplicam ao arquivo ASF inteiro.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-119">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="5cfc9-120">Caso contrário, somente os metadados do fluxo serão recuperados.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-120">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="5cfc9-121">Chame [**IMFMetadata:: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para recuperar a lista de propriedades de codificação de arquivo definida no conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-121">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="5cfc9-122">Chame [**IMFMetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) para obter os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="5cfc9-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5cfc9-123">Example</span></span>

<span data-ttu-id="5cfc9-124">O código de exemplo a seguir mostra como enumerar os nomes de propriedade e os valores que são definidos no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-124">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5cfc9-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5cfc9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cfc9-126">Coletores de mídia ASF</span><span class="sxs-lookup"><span data-stu-id="5cfc9-126">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="5cfc9-127">Componentes ASF da camada de pipeline</span><span class="sxs-lookup"><span data-stu-id="5cfc9-127">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="5cfc9-128">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5cfc9-128">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



