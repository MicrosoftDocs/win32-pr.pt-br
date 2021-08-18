---
description: As informações de header ASF são armazenadas nos Objetos de Header ASF de um arquivo de mídia.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Obter informações de objetos de header ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346e57721137fd6064e4d6b9fd21080d96c10e740bb7f7ed45bf3fef4cc92722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974435"
---
# <a name="getting-information-from-asf-header-objects"></a>Obter informações de objetos de header ASF

As informações de header ASF são armazenadas nos Objetos de Header ASF de um arquivo de mídia. Media Foundation fornece o objeto [ContentInfo do ASF](asf-contentinfo-object.md) para trabalhar com o objeto de título. Um objeto ContentInfo populado é necessário para que o aplicativo leia informações de título de um arquivo existente. Isso é feito chamando [**IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader). Se a análise for concluída com êxito, a biblioteca ASF para o arquivo, que é mantida internamente pelo Media Foundation, será preenchida com informações de header de vários Objetos de Header. Algumas dessas propriedades são expostas ao aplicativo, que ele pode recuperar por meio de atributos no descritor de apresentação, descritor de fluxo, perfil e propriedades de metadados.

Para ver a lista completa de atributos, [consulte Media Foundation atributos para objetos de header ASF](media-foundation-attributes-for-asf-header-objects.md).

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>Recuperando informações de header de um descritor de apresentação

Um objeto descritor de apresentação contém a descrição de uma fonte de mídia específica, nesse caso, a fonte de mídia ASF. Se a **chamada ParseHeader** for concluída com êxito, as informações em nível de arquivo do Objeto de Header são armazenadas como atributos no descritor de apresentação. Para criar o descritor de apresentação, chame [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Esse método retorna um ponteiro para um objeto descritor de apresentação populado que contém esses atributos para o arquivo ASF associado ao objeto ContentInfo. Para obter valores para atributos específicos, chame métodos **IMFAttributes::Getxxx** no descritor de apresentação e especifique o atributo **\_ MF PD \_ ASF \_ xxx.**

O código de exemplo a seguir recupera a duração da reprodução de um arquivo ASF, especificado por um objeto ContentInfo.


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



Para obter mais informações sobre descritores de apresentação em geral, consulte [Descritores de apresentação](presentation-descriptors.md).

Para ver o conjunto completo de atributos do descritor de apresentação, consulte [Atributos do descritor de apresentação.](presentation-descriptor-attributes.md)

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>Recuperando informações de header de um descritor de fluxo

Um objeto descritor de fluxo expõe a interface [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) e descreve as características dos fluxos no arquivo. O descritor de apresentação para o conteúdo do ASF contém um ou mais descritores de fluxo que representam os fluxos listados no Objeto de Título. Depois que a chamada para [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) for concluída com êxito, os descritores de fluxo subjacentes serão preenchidos com informações de nível de fluxo dos vários Objetos de Header. Para obter um descritor de fluxo para um fluxo ASF, chame [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) no descritor de apresentação gerado a partir do objeto ContentInfo.

Algumas das propriedades de fluxo são definidas como atributos em descritores de fluxo. Chame **métodos IMFAttributes::Getxxx** em um descritor de fluxo e especifique o atributo **\_ MF SD \_ ASF \_ xxx.**

Para o conjunto completo de atributos do descritor de fluxo, consulte atributos "Descritor de fluxo específico do ASF" listados em [Atributos do Descritor de Fluxo](stream-descriptor-attributes.md).

## <a name="retrieving-header-information-from-the-profile-object"></a>Recuperando informações de header do objeto de perfil

Além dos descritores de fluxo, o objeto de perfil asF também descreve as propriedades do fluxo. Para obter o perfil de um arquivo ASF existente, chame [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). O objeto de perfil ASF retornado por esse método não inclui nenhum dos atributos **\_ MF PD \_ ASF \_ xxx.** Esses atributos estão disponíveis para o aplicativo somente depois que ele chama [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) para gerar o objeto de perfil de um descritor de apresentação. Você pode usar o perfil para obter ponteiros para os objetos de exclusão mútua e priorização de fluxo.

Para obter informações sobre o objeto de perfil, consulte [Perfil ASF](asf-profile.md) .

## <a name="retrieving-metadata-from-header-objects"></a>Recuperando metadados de objetos de header

Um arquivo ASF pode conter várias propriedades de metadados que são definidas durante a codificação do arquivo. Um aplicativo pode enumerar essas propriedades com o objeto ContentInfo. Algumas dessas propriedades, como informações de VBR (taxa de bits variável), estão disponíveis para o aplicativo por meio de atributos no descritor de apresentação, descritores de fluxo e tipos de mídia para o arquivo de mídia. Esses atributos são definidos no objeto ContentInfo durante a inicialização por meio [**da chamada ParseHeader.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto ContentInfo do ASF](asf-contentinfo-object.md)
</dt> </dl>

 

 



