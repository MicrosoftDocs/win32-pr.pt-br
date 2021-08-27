---
description: Este tópico é a etapa 1 do tutorial como reproduzir arquivos de mídia com Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: 'Etapa 1: declarar a classe CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61f03a9054e96769414320811d32a549027defb80ff929aba2c27ad4aa5b5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112906"
---
# <a name="step-1-declare-the-cplayer-class"></a>Etapa 1: declarar a classe CPlayer

Este tópico é a etapa 1 do tutorial [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md). O código completo é mostrado no exemplo de [reprodução de sessão de mídia](media-session-playback-example.md)do tópico.

Neste tutorial, a funcionalidade de reprodução é encapsulada na `CPlayer` classe. A classe `CPlayer` é declarada da seguinte forma:


```C++
const UINT WM_APP_PLAYER_EVENT = WM_APP + 1;   

    // WPARAM = IMFMediaEvent*, WPARAM = MediaEventType

enum PlayerState
{
    Closed = 0,     // No session.
    Ready,          // Session was created, ready to open a file. 
    OpenPending,    // Session is opening a file.
    Started,        // Session is playing a file.
    Paused,         // Session is paused.
    Stopped,        // Session is stopped (ready to play). 
    Closing         // Application has closed the session, but is waiting for MESessionClosed.
};

class CPlayer : public IMFAsyncCallback
{
public:
    static HRESULT CreateInstance(HWND hVideo, HWND hEvent, CPlayer **ppPlayer);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP  GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP  Invoke(IMFAsyncResult* pAsyncResult);

    // Playback
    HRESULT       OpenURL(const WCHAR *sURL);
    HRESULT       Play();
    HRESULT       Pause();
    HRESULT       Stop();
    HRESULT       Shutdown();
    HRESULT       HandleEvent(UINT_PTR pUnkPtr);
    PlayerState   GetState() const { return m_state; }

    // Video functionality
    HRESULT       Repaint();
    HRESULT       ResizeVideo(WORD width, WORD height);
    
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }

protected:
    
    // Constructor is private. Use static CreateInstance method to instantiate.
    CPlayer(HWND hVideo, HWND hEvent);

    // Destructor is private. Caller should call Release.
    virtual ~CPlayer(); 

    HRESULT Initialize();
    HRESULT CreateSession();
    HRESULT CloseSession();
    HRESULT StartPlayback();

    // Media event handlers
    virtual HRESULT OnTopologyStatus(IMFMediaEvent *pEvent);
    virtual HRESULT OnPresentationEnded(IMFMediaEvent *pEvent);
    virtual HRESULT OnNewPresentation(IMFMediaEvent *pEvent);

    // Override to handle additional session events.
    virtual HRESULT OnSessionEvent(IMFMediaEvent*, MediaEventType) 
    { 
        return S_OK; 
    }

protected:
    long                    m_nRefCount;        // Reference count.

    IMFMediaSession         *m_pSession;
    IMFMediaSource          *m_pSource;
    IMFVideoDisplayControl  *m_pVideoDisplay;

    HWND                    m_hwndVideo;        // Video window.
    HWND                    m_hwndEvent;        // App window to receive events.
    PlayerState             m_state;            // Current state of the media session.
    HANDLE                  m_hCloseEvent;      // Event to wait on while closing.
};
```



Aqui estão algumas coisas a serem observadas `CPlayer` :

-   O **evento de \_ \_ player de \_ aplicativo do WM** constante define uma mensagem de janela privada. Essa mensagem é usada para notificar o aplicativo sobre eventos de sessão de mídia. Consulte [Step 5: tratar eventos de sessão de mídia](step-5--handle-media-session-events.md).
-   A `PlayerState` enumeração define os possíveis Estados do `CPlayer` objeto.
-   A `CPlayer` classe implementa a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , que é usada para obter notificações de eventos da sessão de mídia.
-   O `CPlayer` Construtor é privado. O aplicativo chama o `CreateInstance` método estático para criar uma instância da `CPlayer` classe.
-   O `CPlayer` destruidor também é privado. A `CPlayer` classe implementa **IUnknown**, portanto, o tempo de vida do objeto é controlado por meio de sua contagem de referência (*m \_ nRefCount*). Para destruir o objeto, o aplicativo chama **IUnknown:: Release**, não **delete**.
-   O `CPlayer` objeto gerencia a sessão de mídia e a origem da mídia.

## <a name="implement-iunknown"></a>Implementar IUnknown

A `CPlayer` classe implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), que herda **IUnknown**.

O código mostrado aqui é uma implementação razoavelmente padrão de **IUnknown**. Se preferir, você pode usar o Active Template Library (ATL) para implementar esses métodos. No entanto, `CPlayer` o não oferece suporte a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ou a qualquer recurso com avançado, portanto, não há um motivo impressionante para usar o ATL aqui.


```C++
HRESULT CPlayer::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CPlayer, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

ULONG CPlayer::AddRef()
{
    return InterlockedIncrement(&m_nRefCount);
}

ULONG CPlayer::Release()
{
    ULONG uCount = InterlockedDecrement(&m_nRefCount);
    if (uCount == 0)
    {
        delete this;
    }
    return uCount;
}
```



Em seguida: [etapa 2: criar o objeto CPlayer](step-2--create-the-cplayer-object.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> <dt>

[Como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
