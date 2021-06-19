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
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="7991a-103">Adicionando metadados ao sink de arquivo</span><span class="sxs-lookup"><span data-stu-id="7991a-103">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="7991a-104">O sink de arquivo ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7991a-104">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="7991a-105">Para obter informações sobre o modelo de objeto e o uso geral dos sinks de mídia do ASF, consulte [AsF Media Sinks](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="7991a-105">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="7991a-106">Depois [de Criar o sink do arquivo ASF](creating-the-asf-file-sink.md), ele deve ser configurado com informações sobre os fluxos e informações de codificação no arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="7991a-106">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="7991a-107">Esses procedimentos são descritos em [Adicionando informações de fluxo ao sink de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md) e [Definindo propriedades no sink de arquivo](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="7991a-107">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="7991a-108">Além disso, você também pode adicionar informações de metadados que incluem pares de nome/valor, como "Autor", Título".</span><span class="sxs-lookup"><span data-stu-id="7991a-108">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="7991a-109">Este tópico descreve o processo de adição de informações de metadados ao sink de arquivo para que ele apareça no Objeto de [Header ASF final](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7991a-109">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="7991a-110">Você pode adicionar informações de metadados ao sink do arquivo ASF antes de criar a topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="7991a-110">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="7991a-111">O objeto ContentInfo do ASF para o sink de arquivo acompanha as propriedades de metadados e é exposto ao aplicativo por meio da interface [**IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)</span><span class="sxs-lookup"><span data-stu-id="7991a-111">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="7991a-112">Algumas dessas propriedades, como "IsVBR", que indica se o arquivo contém fluxos de VBR (taxa de bits variável), são definidas automaticamente pelo sink de arquivo por meio da análise das propriedades de codificação de fluxo definidas.</span><span class="sxs-lookup"><span data-stu-id="7991a-112">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="7991a-113">Para ver uma lista completa de propriedades, consulte o tópico "Lista de Atributos" na documentação do SDK de Formato.</span><span class="sxs-lookup"><span data-stu-id="7991a-113">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="7991a-114">Usando a interface IMFMetadata no sink de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="7991a-114">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="7991a-115">Consulte o objeto de sink do arquivo ASF para obter um ponteiro para sua implementação da interface [**IMFMetadataProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)</span><span class="sxs-lookup"><span data-stu-id="7991a-115">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="7991a-116">Chame [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) para obter um [**ponteiro IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)</span><span class="sxs-lookup"><span data-stu-id="7991a-116">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="7991a-117">O *parâmetro pPresentationDescriptor* é ignorado e o aplicativo pode passar **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7991a-117">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="7991a-118">Se o aplicativo passar zero como o identificador de fluxo no parâmetro *dwStreamIdentifier,* o método recuperará metadados que se aplicarão a todo o arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="7991a-118">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="7991a-119">Caso contrário, somente os metadados do fluxo são recuperados.</span><span class="sxs-lookup"><span data-stu-id="7991a-119">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="7991a-120">Chame [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para recuperar a lista de propriedades de codificação de arquivo definidas no conteúdo da mídia.</span><span class="sxs-lookup"><span data-stu-id="7991a-120">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="7991a-121">Chame [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) para obter os valores da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7991a-121">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="7991a-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7991a-122">Example</span></span>

<span data-ttu-id="7991a-123">O código de exemplo a seguir mostra como enumerar os nomes de propriedade e os valores definidos no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="7991a-123">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7991a-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7991a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7991a-125">Sinks de mídia do ASF</span><span class="sxs-lookup"><span data-stu-id="7991a-125">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="7991a-126">Componentes ASF da camada de pipeline</span><span class="sxs-lookup"><span data-stu-id="7991a-126">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="7991a-127">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7991a-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



