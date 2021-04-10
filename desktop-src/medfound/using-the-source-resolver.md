---
description: Usando o resolvedor de origem
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Usando o resolvedor de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165284"
---
# <a name="using-the-source-resolver"></a>Usando o resolvedor de origem

O resolvedor de origem utiliza um fluxo de bytes ou uma URL e cria a origem de mídia adequada para esse conteúdo. Para criar o resolvedor de origem, chame [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver). Essa função retorna um ponteiro de interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .

O resolvedor de origem tem métodos síncronos e assíncronos. Se você estiver usando o resolvedor de origem do seu thread de aplicativo principal, os métodos assíncronos tornarão sua interface do usuário mais responsiva. Os métodos síncronos podem ser bloqueados por um período de tempo perceptível, especialmente se o resolvedor de origem precisar abrir um recurso de rede.

Os métodos síncronos são:

-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

Os métodos assíncronos são:

-   [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

Para os métodos assíncronos, cada método tem um método **end...** correspondente para concluir a solicitação assíncrona e um método **Cancel...** para cancelar uma solicitação pendente. Para obter mais informações sobre métodos assíncronos no Media Foundation, consulte [métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md).

O exemplo de código a seguir cria uma fonte de mídia de uma URL. Este exemplo usa o método síncrono.


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolvedor de origem](source-resolver.md)
</dt> </dl>

 

 



