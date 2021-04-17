---
description: Descritores de apresentação
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Descritores de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759582"
---
# <a name="presentation-descriptors"></a>Descritores de apresentação

Uma *apresentação* é um conjunto de fluxos de mídia relacionados que compartilham um tempo de apresentação comum. Por exemplo, uma apresentação pode consistir em fluxos de áudio e vídeo de um filme. Um *descritor de apresentação* é um objeto que contém a descrição de uma apresentação específica. Os descritores de apresentação são usados para configurar as fontes de mídia e alguns coletores de mídia.

Cada descritor de apresentação contém uma lista de um ou mais *descripdores de fluxo*. Elas descrevem os fluxos na apresentação. Os fluxos podem ser selecionados ou desmarcados. Somente os fluxos selecionados produzem dados. Os fluxos desmarcados não estão ativos e não produzem nenhum dado. Cada descritor de fluxo tem um *manipulador de tipo de mídia*, que é usado para alterar o tipo de mídia do fluxo ou obter o tipo de mídia atual do fluxo. (Para obter mais informações sobre tipos de mídia, consulte [tipos de mídia](media-types.md).)

A tabela a seguir mostra as interfaces primárias que cada um desses objetos expõe.



| Objeto                  | Interface                                                      |
|-------------------------|----------------------------------------------------------------|
| Descritor de apresentação | [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| Descritor de fluxo       | [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| Manipulador de tipo de mídia      | [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a>Apresentações de origem de mídia

Cada fonte de mídia fornece um descritor de apresentação que descreve a configuração padrão para a origem. Na configuração padrão, pelo menos um fluxo é selecionado e cada fluxo selecionado tem um tipo de mídia. Para obter o descritor de apresentação, chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). O método retorna um ponteiro [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

Você pode modificar o descritor de apresentação da origem para selecionar um conjunto diferente de fluxos. Não modifique o descritor de apresentação a menos que a origem da mídia seja interrompida. As alterações são aplicadas quando você chama [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) para iniciar a origem.

Para obter o número de fluxos, chame [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount). Para obter o descritor de fluxo para um fluxo, chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) e passe o índice do fluxo. Os fluxos são indexados de zero. O método **GetStreamDescriptorByIndex** retorna um ponteiro [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) . Ele também retorna um sinalizador booliano que indica se o fluxo está selecionado. Se o fluxo for selecionado, a origem da mídia produzirá dados para esse fluxo. Caso contrário, a origem não produzirá nenhum dado para esse fluxo. Para selecionar um fluxo, chame [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) com o índice do fluxo. Para anular a seleção de um fluxo, chame [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).

O código a seguir mostra como obter o descritor de apresentação de uma origem de mídia e enumerar os fluxos.


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a>Manipuladores de tipo de mídia

Para alterar o tipo de mídia do fluxo ou obter o tipo de mídia atual do fluxo, use o manipulador de tipo de mídia do descritor de fluxo. Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) para obter o manipulador de tipo de mídia. Esse método retorna um ponteiro [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

Se você simplesmente deseja saber que tipo de dados está no fluxo, como áudio ou vídeo, chame [**IMFMediaTypeHandler:: Getmajortype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Esse método retorna o GUID para o tipo de mídia principal. Por exemplo, um aplicativo de reprodução normalmente conecta um fluxo de áudio ao processador de áudio e um fluxo de vídeo ao processador de vídeo. Se você usar a sessão de mídia ou o carregador de topologia para criar uma topologia, o GUID de tipo principal poderá ser a única informação de formato de que você precisa.

Se seu aplicativo precisar de informações mais detalhadas sobre o formato atual, chame [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Esse método retorna um ponteiro para a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) do tipo de mídia. Use esta interface para obter os detalhes do formato.

O manipulador de tipo de mídia também contém uma lista de tipos de mídia com suporte para o fluxo. Para obter o tamanho da lista, chame [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount). Para obter um tipo de mídia da lista, chame [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) com o índice do tipo de mídia. Os tipos de mídia são retornados na ordem aproximada de preferência. Por exemplo, para formatos de áudio, taxas de exemplo mais altas são preferenciais em relação às taxas de amostra mais baixas. No entanto, não há nenhuma regra definitiva que governa a ordenação, portanto, você deve tratá-la simplesmente como uma diretriz.

A lista de tipos com suporte pode não conter todos os tipos de mídia possíveis aos quais o fluxo dá suporte. Para testar se um tipo de mídia específico tem suporte, chame [**IMFMediaTypeHandler:: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported). Para definir o tipo de mídia, chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Se o método tiver sucesso, o fluxo conterá dados que estejam de acordo com o formato especificado. O método **SetCurrentMediaType** não altera a lista de tipos preferenciais.

O código a seguir mostra como obter o manipulador de tipo de mídia, enumerar os tipos de mídia preferenciais e definir o tipo de mídia. Este exemplo pressupõe que o aplicativo tem algum algoritmo, não mostrado aqui, para selecionar o tipo de mídia. As especificações dependerão muito do seu aplicativo.


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



