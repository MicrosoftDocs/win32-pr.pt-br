---
description: Este tópico é a etapa 2 do tutorial como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 'Etapa 2: criar o objeto CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788684"
---
# <a name="step-2-create-the-cplayer-object"></a>Etapa 2: criar o objeto CPlayer

Este tópico é a etapa 2 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md). O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.

Para criar uma instância da `CPlayer` classe, o aplicativo chama o método estático `CPlayer::CreateInstance` . Esse método usa os seguintes parâmetros:

-   *hVideo* especifica a janela para exibir o vídeo.
-   *hEvent* especifica uma janela para receber eventos. É válido passar o mesmo identificador para ambos os identificadores de janela.
-   *ppPlayer* recebe um ponteiro para uma nova `CPlayer` instância.

O código a seguir mostra o `CreateInstance` método:


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



O código a seguir mostra o `CPlayer` Construtor:


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



O construtor faz o seguinte:

1.  Chama [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar a plataforma de Media Foundation.
2.  Cria um evento de redefinição automática. Esse evento é usado ao fechar a sessão de mídia; consulte [Step 7: desligar a sessão de mídia](step-7--shut-down-the-media-session.md).

O destruidor desliga a sessão de mídia, conforme descrito na [etapa 7: desligar a sessão de mídia](step-7--shut-down-the-media-session.md).


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



Observe que o construtor e o destruidor são ambos métodos de classe protegidos. O aplicativo cria o objeto usando o `CreateInstance` método estático. Ele destrói o objeto chamando **IUnknown:: Release**, em vez de usar explicitamente **delete**.

Em seguida: [etapa 3: abrir um arquivo de mídia](step-3--open-a-media-file.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> <dt>

[Como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



