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
# <a name="creating-an-asf-profile"></a>Criando um perfil ASF

Este tópico descreve como criar um perfil ASF no Microsoft Media Foundation.

-   [Criar um novo perfil](#create-a-new-profile)
-   [Obter o perfil do objeto ContentInfo do ASF](#get-the-profile-from-the-asf-contentinfo-object)
-   [Obter o perfil de um descritor de apresentação](#get-the-profile-from-a-presentation-descriptor)
-   [Tópicos relacionados](#related-topics)

## <a name="create-a-new-profile"></a>Criar um novo perfil

Para criar um perfil ASF vazio, chame a função [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) . Essa função retorna um ponteiro para a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) . O aplicativo pode usar essa interface para adicionar fluxos ao perfil e para configurar cada um dos fluxos. Para obter mais informações, consulte [criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md).

Opcionalmente, o aplicativo pode adicionar objetos de exclusão mútua a dois ou mais fluxos. Consulte [usando a exclusão mútua para fluxos ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>Obter o perfil do objeto ContentInfo do ASF

Um aplicativo pode obter o perfil ASF de um arquivo ASF existente do [objeto ContentInfo do ASF](asf-contentinfo-object.md). O perfil já está configurado e contém configurações para todos os fluxos no arquivo.

Inicialize o objeto ContentInfo analisando o objeto de cabeçalho ASF do arquivo. Isso é feito por meio do método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) . Depois que todos os objetos de cabeçalho são lidos e a biblioteca ASF é populada, o perfil desse arquivo é gerado. O aplicativo pode obter um ponteiro para esse perfil inicializado chamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).

## <a name="get-the-profile-from-a-presentation-descriptor"></a>Obter o perfil de um descritor de apresentação

Você pode obter o objeto de perfil de um arquivo ASF existente do [descritor de apresentação](presentation-descriptors.md) para o arquivo ou do objeto [ContentInfo do ASF](asf-contentinfo-object.md) . Nesse caso, o perfil já está configurado e contém configurações para todos os fluxos no arquivo. Isso pode ser útil se você quiser modificar um perfil ASF existente. Por exemplo, talvez você queira codificar novamente um arquivo de vídeo do Windows Media em uma taxa de bits inferior.

Para obter o perfil do descritor de apresentação, chame [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). Essa função analisa o descritor de apresentação e popula um perfil ASF com informações sobre o arquivo de mídia. A função retorna um ponteiro para a interface IMFASFProfile. Você pode usar essa interface para modificar o perfil.

Para obter o descritor de apresentação, chame um dos seguintes métodos:

-   Na origem de mídia do ASF, chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   No objeto [ASF ContentInfo](asf-contentinfo-object.md) , chame [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Antes de chamar esse método, verifique se o objeto ContentInfo foi inicializado para leitura. Para obter mais informações, consulte "Inicializando o objeto ContentInfo de um arquivo ASF existente" em [lendo o objeto de cabeçalho ASF de um arquivo existente](reading-the-asf-header-object-of-an-existing-file.md). No entanto, se você já tiver um objeto ContentInfo inicializado, poderá obter o perfil diretamente dele. Isso é descrito em "obtendo o perfil do objeto ContentInfo" mais adiante neste tópico.

O exemplo a seguir mostra como criar um perfil de um descritor de apresentação. A função cria uma origem de mídia para o arquivo, obtém o descritor de apresentação da origem da mídia e cria um perfil. Este exemplo pressupõe que *pszFileName* especifica a URL de um arquivo asf.


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



Este exemplo usa [SafeRelease](saferelease.md) para liberar ponteiros de interface.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perfil ASF](asf-profile.md)
</dt> </dl>

 

 



