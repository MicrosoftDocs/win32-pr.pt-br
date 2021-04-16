---
description: Este tópico descreve como criar um perfil ASF no Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Criando um perfil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757911"
---
# <a name="creating-an-asf-profile"></a><span data-ttu-id="9175b-103">Criando um perfil ASF</span><span class="sxs-lookup"><span data-stu-id="9175b-103">Creating an ASF Profile</span></span>

<span data-ttu-id="9175b-104">Este tópico descreve como criar um perfil ASF no Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9175b-104">This topic describes how to create as ASF profile in Microsoft Media Foundation.</span></span>

-   [<span data-ttu-id="9175b-105">Criar um novo perfil</span><span class="sxs-lookup"><span data-stu-id="9175b-105">Create a New Profile</span></span>](#create-a-new-profile)
-   [<span data-ttu-id="9175b-106">Obter o perfil do objeto ContentInfo do ASF</span><span class="sxs-lookup"><span data-stu-id="9175b-106">Get the Profile from the ASF ContentInfo Object</span></span>](#get-the-profile-from-the-asf-contentinfo-object)
-   [<span data-ttu-id="9175b-107">Obter o perfil de um descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="9175b-107">Get the Profile from a Presentation Descriptor</span></span>](#get-the-profile-from-a-presentation-descriptor)
-   [<span data-ttu-id="9175b-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9175b-108">Related topics</span></span>](#related-topics)

## <a name="create-a-new-profile"></a><span data-ttu-id="9175b-109">Criar um novo perfil</span><span class="sxs-lookup"><span data-stu-id="9175b-109">Create a New Profile</span></span>

<span data-ttu-id="9175b-110">Para criar um perfil ASF vazio, chame a função [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="9175b-110">To create an empty ASF profile, call the [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) function.</span></span> <span data-ttu-id="9175b-111">Essa função retorna um ponteiro para a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="9175b-111">This function returns a pointer to the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="9175b-112">O aplicativo pode usar essa interface para adicionar fluxos ao perfil e para configurar cada um dos fluxos.</span><span class="sxs-lookup"><span data-stu-id="9175b-112">The application can use this interface to add streams to the profile, and to configure each of the streams.</span></span> <span data-ttu-id="9175b-113">Para obter mais informações, consulte [criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="9175b-113">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>

<span data-ttu-id="9175b-114">Opcionalmente, o aplicativo pode adicionar objetos de exclusão mútua a dois ou mais fluxos.</span><span class="sxs-lookup"><span data-stu-id="9175b-114">Optionally, the application can add mutual-exclusion objects to two or more streams.</span></span> <span data-ttu-id="9175b-115">Consulte [usando a exclusão mútua para fluxos ASF](using-mutual-exclusion-for-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="9175b-115">See [Using Mutual Exclusion for ASF Streams](using-mutual-exclusion-for-asf-streams.md).</span></span>

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a><span data-ttu-id="9175b-116">Obter o perfil do objeto ContentInfo do ASF</span><span class="sxs-lookup"><span data-stu-id="9175b-116">Get the Profile from the ASF ContentInfo Object</span></span>

<span data-ttu-id="9175b-117">Um aplicativo pode obter o perfil ASF de um arquivo ASF existente do [objeto ContentInfo do ASF](asf-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="9175b-117">An application can get the ASF profile of an existing ASF file from the [ASF ContentInfo Object](asf-contentinfo-object.md).</span></span> <span data-ttu-id="9175b-118">O perfil já está configurado e contém configurações para todos os fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="9175b-118">The profile is already configured and contains settings for the all of the streams in the file.</span></span>

<span data-ttu-id="9175b-119">Inicialize o objeto ContentInfo analisando o objeto de cabeçalho ASF do arquivo.</span><span class="sxs-lookup"><span data-stu-id="9175b-119">Initialize the ContentInfo object by parsing the ASF Header Object of the file.</span></span> <span data-ttu-id="9175b-120">Isso é feito por meio do método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="9175b-120">This is done through the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="9175b-121">Depois que todos os objetos de cabeçalho são lidos e a biblioteca ASF é populada, o perfil desse arquivo é gerado.</span><span class="sxs-lookup"><span data-stu-id="9175b-121">After all the Header Objects are read and the ASF library is populated, the profile for this file is generated.</span></span> <span data-ttu-id="9175b-122">O aplicativo pode obter um ponteiro para esse perfil inicializado chamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="9175b-122">The application can get a pointer to this initialized profile by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>

## <a name="get-the-profile-from-a-presentation-descriptor"></a><span data-ttu-id="9175b-123">Obter o perfil de um descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="9175b-123">Get the Profile from a Presentation Descriptor</span></span>

<span data-ttu-id="9175b-124">Você pode obter o objeto de perfil de um arquivo ASF existente do [descritor de apresentação](presentation-descriptors.md) para o arquivo ou do objeto [ContentInfo do ASF](asf-contentinfo-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9175b-124">You can get the profile object of an existing ASF file from the [presentation descriptor](presentation-descriptors.md) for the file, or from the [ASF ContentInfo](asf-contentinfo-object.md) object.</span></span> <span data-ttu-id="9175b-125">Nesse caso, o perfil já está configurado e contém configurações para todos os fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="9175b-125">In this case, the profile is already configured and contains settings for all of the streams in the file.</span></span> <span data-ttu-id="9175b-126">Isso pode ser útil se você quiser modificar um perfil ASF existente.</span><span class="sxs-lookup"><span data-stu-id="9175b-126">This can be useful if you want to modify an existing ASF profile.</span></span> <span data-ttu-id="9175b-127">Por exemplo, talvez você queira codificar novamente um arquivo de vídeo do Windows Media em uma taxa de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="9175b-127">For example, you might wish to re-encode a Windows Media Video file at a lower bit rate.</span></span>

<span data-ttu-id="9175b-128">Para obter o perfil do descritor de apresentação, chame [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="9175b-128">To get the profile from the presentation descriptor, call [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor).</span></span> <span data-ttu-id="9175b-129">Essa função analisa o descritor de apresentação e popula um perfil ASF com informações sobre o arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9175b-129">This function parses the presentation descriptor, and populates an ASF profile with information about the media file.</span></span> <span data-ttu-id="9175b-130">A função retorna um ponteiro para a interface IMFASFProfile.</span><span class="sxs-lookup"><span data-stu-id="9175b-130">The function returns a pointer to the IMFASFProfile interface.</span></span> <span data-ttu-id="9175b-131">Você pode usar essa interface para modificar o perfil.</span><span class="sxs-lookup"><span data-stu-id="9175b-131">You can then use this interface to modify the profile.</span></span>

<span data-ttu-id="9175b-132">Para obter o descritor de apresentação, chame um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="9175b-132">To get the presentation descriptor, call one of the following methods:</span></span>

-   <span data-ttu-id="9175b-133">Na origem de mídia do ASF, chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="9175b-133">From the ASF media source, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="9175b-134">No objeto [ASF ContentInfo](asf-contentinfo-object.md) , chame [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="9175b-134">From the [ASF ContentInfo](asf-contentinfo-object.md) object, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="9175b-135">Antes de chamar esse método, verifique se o objeto ContentInfo foi inicializado para leitura.</span><span class="sxs-lookup"><span data-stu-id="9175b-135">Prior to calling this method, make sure that the ContentInfo object is initialized for reading.</span></span> <span data-ttu-id="9175b-136">Para obter mais informações, consulte "Inicializando o objeto ContentInfo de um arquivo ASF existente" em [lendo o objeto de cabeçalho ASF de um arquivo existente](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="9175b-136">For more information, see "Initializing the ContentInfo Object from an Existing ASF File" in [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span> <span data-ttu-id="9175b-137">No entanto, se você já tiver um objeto ContentInfo inicializado, poderá obter o perfil diretamente dele.</span><span class="sxs-lookup"><span data-stu-id="9175b-137">However, if you already have an initialized ContentInfo object, you can get the profile directly from it.</span></span> <span data-ttu-id="9175b-138">Isso é descrito em "obtendo o perfil do objeto ContentInfo" mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="9175b-138">This is described in "Getting the Profile from the ContentInfo Object " later in this topic.</span></span>

<span data-ttu-id="9175b-139">O exemplo a seguir mostra como criar um perfil de um descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="9175b-139">The following example shows how to create a profile from a presentation descriptor.</span></span> <span data-ttu-id="9175b-140">A função cria uma origem de mídia para o arquivo, obtém o descritor de apresentação da origem da mídia e cria um perfil.</span><span class="sxs-lookup"><span data-stu-id="9175b-140">The function creates a media source for the file, gets the presentation descriptor from the media source, and creates a profile.</span></span> <span data-ttu-id="9175b-141">Este exemplo pressupõe que *pszFileName* especifica a URL de um arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="9175b-141">This example assumes that *pszFileName* specifies the URL of an ASF file.</span></span>


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



<span data-ttu-id="9175b-142">Este exemplo usa [SafeRelease](saferelease.md) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="9175b-142">This example uses [SafeRelease](saferelease.md) to release interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9175b-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9175b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9175b-144">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="9175b-144">ASF Profile</span></span>](asf-profile.md)
</dt> </dl>

 

 



