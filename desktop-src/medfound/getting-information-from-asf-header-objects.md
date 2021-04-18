---
description: As informações de cabeçalho ASF são armazenadas nos objetos de cabeçalho ASF de um arquivo de mídia.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Obtendo informações de objetos de cabeçalho ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788606"
---
# <a name="getting-information-from-asf-header-objects"></a><span data-ttu-id="410db-103">Obtendo informações de objetos de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="410db-103">Getting Information from ASF Header Objects</span></span>

<span data-ttu-id="410db-104">As informações de cabeçalho ASF são armazenadas nos objetos de cabeçalho ASF de um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="410db-104">ASF header information is stored in the ASF Header Objects of a media file.</span></span> <span data-ttu-id="410db-105">Media Foundation fornece o [objeto ContentInfo do ASF](asf-contentinfo-object.md) para trabalhar com o objeto header.</span><span class="sxs-lookup"><span data-stu-id="410db-105">Media Foundation provides the [ASF ContentInfo Object](asf-contentinfo-object.md) to work with the Header Object.</span></span> <span data-ttu-id="410db-106">Um objeto ContentInfo populado é necessário para que o aplicativo Leia as informações de cabeçalho de um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="410db-106">A populated ContentInfo object is required in order for the application to read header information of an existing file.</span></span> <span data-ttu-id="410db-107">Isso é obtido chamando [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="410db-107">This is achieved by calling [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span> <span data-ttu-id="410db-108">Se a análise for concluída com êxito, a biblioteca do ASF para o arquivo, que é mantida internamente pelo Media Foundation, é preenchida com informações de cabeçalho de vários objetos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="410db-108">If parsing completes successfully, the ASF library for the file, which is maintained internally by Media Foundation, is populated with header information from various Header Objects.</span></span> <span data-ttu-id="410db-109">Algumas dessas propriedades são expostas ao aplicativo, que pode ser recuperada por meio de atributos no descritor de apresentação, no descritor de fluxo, no perfil e nas propriedades de metadados.</span><span class="sxs-lookup"><span data-stu-id="410db-109">Some of these properties are exposed to the application, which it can retrieve through attributes on the presentation descriptor, stream descriptor, the profile, and metadata properties.</span></span>

<span data-ttu-id="410db-110">Para obter a lista completa de atributos, consulte [atributos de Media Foundation para objetos de cabeçalho ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="410db-110">For the complete list of attributes, see [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a><span data-ttu-id="410db-111">Recuperando informações de cabeçalho de um descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="410db-111">Retrieving Header Information from a Presentation Descriptor</span></span>

<span data-ttu-id="410db-112">Um objeto de descritor de apresentação contém a descrição de uma origem de mídia específica, nesse caso, a origem de mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="410db-112">A presentation descriptor object contains the description of a particular media source, in this case the ASF media source.</span></span> <span data-ttu-id="410db-113">Se a chamada **ParseHeader** for concluída com êxito, as informações em nível de arquivo do objeto de cabeçalho serão armazenadas como atributos no descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="410db-113">If the **ParseHeader** call completes successfully, file-level information from the Header Object is stored as attributes on the presentation descriptor.</span></span> <span data-ttu-id="410db-114">Para criar o descritor de apresentação, chame [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="410db-114">To create the presentation descriptor, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="410db-115">Esse método retorna um ponteiro para um objeto de descritor de apresentação preenchido que contém esses atributos para o arquivo ASF associado ao objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="410db-115">This method returns a pointer to a populated presentation descriptor object that contains these attributes for the ASF file associated with the ContentInfo object.</span></span> <span data-ttu-id="410db-116">Para obter valores para atributos específicos, chame os métodos **IMFAttributes:: GetXXX** no descritor de apresentação e especifique o atributo **MF \_ PD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="410db-116">To get values for specific attributes, call **IMFAttributes::Getxxx** methods on the presentation descriptor and specify the **MF\_PD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="410db-117">O código de exemplo a seguir recupera a duração da reprodução de um arquivo ASF, especificado por um objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="410db-117">The following example code retrieves the play duration of an ASF file, specified by a ContentInfo object.</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



<span data-ttu-id="410db-118">Para obter mais informações sobre descritores de apresentação em geral, consulte [descritores de apresentação](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="410db-118">For more information about presentation descriptors in general, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="410db-119">Para obter o conjunto completo de atributos de descritor de apresentação, consulte [atributos do descritor de apresentação](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="410db-119">For the complete set of presentation descriptor attributes, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-a-stream-descriptor"></a><span data-ttu-id="410db-120">Recuperando informações de cabeçalho de um descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="410db-120">Retrieving Header Information from a Stream Descriptor</span></span>

<span data-ttu-id="410db-121">Um objeto de descritor de fluxo expõe a interface [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) e descreve as características dos fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="410db-121">A stream descriptor object exposes the [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface and describes the characteristics of the streams in the file.</span></span> <span data-ttu-id="410db-122">O descritor de apresentação do conteúdo ASF contém um ou mais descritores de fluxo que representam os fluxos listados no objeto de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="410db-122">The presentation descriptor for the ASF content contains one or more stream descriptors that represent the streams listed in the Header Object.</span></span> <span data-ttu-id="410db-123">Depois que a chamada para [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) for concluída com êxito, os descritores de fluxo subjacentes serão preenchidos com informações de nível de fluxo dos vários objetos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="410db-123">After the call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) completes successfully, the underlying stream descriptors are populated with stream-level information from the various Header Objects.</span></span> <span data-ttu-id="410db-124">Para obter um descritor de fluxo para um fluxo de ASF, chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) no descritor de apresentação que é gerado do objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="410db-124">To get a stream descriptor for an ASF stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) on the presentation descriptor that is generated from the ContentInfo object.</span></span>

<span data-ttu-id="410db-125">Algumas das propriedades de fluxo são definidas como atributos nos descritores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="410db-125">Some of the stream properties are set as attributes on stream descriptors.</span></span> <span data-ttu-id="410db-126">Chame os métodos **IMFAttributes:: GetXXX** em um descritor de fluxo e especifique o atributo **MF \_ SD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="410db-126">Call **IMFAttributes::Getxxx** methods on a stream descriptor and specify the **MF\_SD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="410db-127">Para obter o conjunto completo de atributos de descritor de fluxo, consulte atributos de "descritor de fluxo específico do ASF" listados em [atributos de descritor de fluxo](stream-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="410db-127">For the complete set of stream descriptor attributes, see "ASF-Specific Stream Descriptor" attributes listed in [Stream Descriptor Attributes](stream-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-the-profile-object"></a><span data-ttu-id="410db-128">Recuperando informações de cabeçalho do objeto de perfil</span><span class="sxs-lookup"><span data-stu-id="410db-128">Retrieving Header Information from the Profile Object</span></span>

<span data-ttu-id="410db-129">Além dos descritores de fluxo, o objeto de perfil ASF também descreve as propriedades do fluxo.</span><span class="sxs-lookup"><span data-stu-id="410db-129">In addition to stream descriptors, the ASF profile object also describes the stream properties.</span></span> <span data-ttu-id="410db-130">Para obter o perfil de um arquivo ASF existente, chame [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="410db-130">To get the profile of an existing ASF file, call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="410db-131">O objeto de perfil ASF retornado por esse método não inclui nenhum dos atributos **MF \_ PD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="410db-131">The ASF profile object returned by this method does not include any of the **MF\_PD\_ASF\_xxx** attributes.</span></span> <span data-ttu-id="410db-132">Esses atributos estão disponíveis para o aplicativo somente depois que ele chama [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) para gerar o objeto de perfil a partir de um descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="410db-132">These attributes are available to the application only after it calls [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) to generate the profile object from a presentation descriptor.</span></span> <span data-ttu-id="410db-133">Você pode usar o perfil para obter ponteiros para os objetos de priorização de fluxo e exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="410db-133">You can use the profile to get pointers to the mutual exclusion and stream prioritization objects.</span></span>

<span data-ttu-id="410db-134">Para obter informações sobre o objeto de perfil, consulte [ASF Profile](asf-profile.md) .</span><span class="sxs-lookup"><span data-stu-id="410db-134">For information about the profile object, see [ASF Profile](asf-profile.md) .</span></span>

## <a name="retrieving-metadata-from-header-objects"></a><span data-ttu-id="410db-135">Recuperando metadados de objetos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="410db-135">Retrieving Metadata from Header Objects</span></span>

<span data-ttu-id="410db-136">Um arquivo ASF pode conter várias propriedades de metadados que são definidas durante a codificação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="410db-136">An ASF file can contain several metadata properties that are set during file encoding.</span></span> <span data-ttu-id="410db-137">Um aplicativo pode enumerar essas propriedades com o objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="410db-137">An application can enumerate these properties with the ContentInfo object.</span></span> <span data-ttu-id="410db-138">Algumas dessas propriedades, como informações de taxa de bits variável (VBR), estão disponíveis para o aplicativo por meio de atributos no descritor de apresentação, os descritores de fluxo e os tipos de mídia para o arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="410db-138">Some of these properties, such as variable bit rate (VBR) information, are available to the application through attributes on presentation descriptor, stream descriptors, and media types for the media file.</span></span> <span data-ttu-id="410db-139">Esses atributos são definidos no objeto ContentInfo durante a inicialização por meio da chamada [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="410db-139">These attributes are set on the ContentInfo object during initialization through the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="410db-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="410db-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="410db-141">Objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="410db-141">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> </dl>

 

 



