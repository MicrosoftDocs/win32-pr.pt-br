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
# <a name="getting-information-from-asf-header-objects"></a>Obtendo informações de objetos de cabeçalho ASF

As informações de cabeçalho ASF são armazenadas nos objetos de cabeçalho ASF de um arquivo de mídia. Media Foundation fornece o [objeto ContentInfo do ASF](asf-contentinfo-object.md) para trabalhar com o objeto header. Um objeto ContentInfo populado é necessário para que o aplicativo Leia as informações de cabeçalho de um arquivo existente. Isso é obtido chamando [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader). Se a análise for concluída com êxito, a biblioteca do ASF para o arquivo, que é mantida internamente pelo Media Foundation, é preenchida com informações de cabeçalho de vários objetos de cabeçalho. Algumas dessas propriedades são expostas ao aplicativo, que pode ser recuperada por meio de atributos no descritor de apresentação, no descritor de fluxo, no perfil e nas propriedades de metadados.

Para obter a lista completa de atributos, consulte [atributos de Media Foundation para objetos de cabeçalho ASF](media-foundation-attributes-for-asf-header-objects.md).

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>Recuperando informações de cabeçalho de um descritor de apresentação

Um objeto de descritor de apresentação contém a descrição de uma origem de mídia específica, nesse caso, a origem de mídia ASF. Se a chamada **ParseHeader** for concluída com êxito, as informações em nível de arquivo do objeto de cabeçalho serão armazenadas como atributos no descritor de apresentação. Para criar o descritor de apresentação, chame [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Esse método retorna um ponteiro para um objeto de descritor de apresentação preenchido que contém esses atributos para o arquivo ASF associado ao objeto ContentInfo. Para obter valores para atributos específicos, chame os métodos **IMFAttributes:: GetXXX** no descritor de apresentação e especifique o atributo **MF \_ PD \_ ASF \_ xxx** .

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



Para obter mais informações sobre descritores de apresentação em geral, consulte [descritores de apresentação](presentation-descriptors.md).

Para obter o conjunto completo de atributos de descritor de apresentação, consulte [atributos do descritor de apresentação](presentation-descriptor-attributes.md).

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>Recuperando informações de cabeçalho de um descritor de fluxo

Um objeto de descritor de fluxo expõe a interface [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) e descreve as características dos fluxos no arquivo. O descritor de apresentação do conteúdo ASF contém um ou mais descritores de fluxo que representam os fluxos listados no objeto de cabeçalho. Depois que a chamada para [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) for concluída com êxito, os descritores de fluxo subjacentes serão preenchidos com informações de nível de fluxo dos vários objetos de cabeçalho. Para obter um descritor de fluxo para um fluxo de ASF, chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) no descritor de apresentação que é gerado do objeto ContentInfo.

Algumas das propriedades de fluxo são definidas como atributos nos descritores de fluxo. Chame os métodos **IMFAttributes:: GetXXX** em um descritor de fluxo e especifique o atributo **MF \_ SD \_ ASF \_ xxx** .

Para obter o conjunto completo de atributos de descritor de fluxo, consulte atributos de "descritor de fluxo específico do ASF" listados em [atributos de descritor de fluxo](stream-descriptor-attributes.md).

## <a name="retrieving-header-information-from-the-profile-object"></a>Recuperando informações de cabeçalho do objeto de perfil

Além dos descritores de fluxo, o objeto de perfil ASF também descreve as propriedades do fluxo. Para obter o perfil de um arquivo ASF existente, chame [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). O objeto de perfil ASF retornado por esse método não inclui nenhum dos atributos **MF \_ PD \_ ASF \_ xxx** . Esses atributos estão disponíveis para o aplicativo somente depois que ele chama [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) para gerar o objeto de perfil a partir de um descritor de apresentação. Você pode usar o perfil para obter ponteiros para os objetos de priorização de fluxo e exclusão mútua.

Para obter informações sobre o objeto de perfil, consulte [ASF Profile](asf-profile.md) .

## <a name="retrieving-metadata-from-header-objects"></a>Recuperando metadados de objetos de cabeçalho

Um arquivo ASF pode conter várias propriedades de metadados que são definidas durante a codificação do arquivo. Um aplicativo pode enumerar essas propriedades com o objeto ContentInfo. Algumas dessas propriedades, como informações de taxa de bits variável (VBR), estão disponíveis para o aplicativo por meio de atributos no descritor de apresentação, os descritores de fluxo e os tipos de mídia para o arquivo de mídia. Esses atributos são definidos no objeto ContentInfo durante a inicialização por meio da chamada [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto ASF ContentInfo](asf-contentinfo-object.md)
</dt> </dl>

 

 



