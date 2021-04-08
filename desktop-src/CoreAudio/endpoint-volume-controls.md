---
description: Controles de volume do ponto de extremidade
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Controles de volume do ponto de extremidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526403be9c600f67791650956bd7e5096f6c9afc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920409"
---
# <a name="endpoint-volume-controls"></a>Controles de volume do ponto de extremidade

As interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) permitem que os clientes controlem os níveis de volume de [sessões de áudio](audio-sessions.md), que são coleções de fluxos de áudio de modo compartilhado. Essas interfaces não funcionam com fluxos de áudio de modo exclusivo.

Os aplicativos que gerenciam fluxos de modo exclusivo podem controlar os níveis de volume desses fluxos por meio da interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) . Essa interface controla o nível de volume do [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md). Ele usará o controle de volume de hardware para o dispositivo de ponto de extremidade se o hardware de áudio implementar esse controle. Caso contrário, a interface **IAudioEndpointVolume** implementa o controle de volume no software.

Se um dispositivo tiver um controle de volume de hardware, as alterações feitas no controle por meio da interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) afetarão o nível de volume no modo compartilhado e no modo exclusivo. Se um dispositivo não tiver controles de áudio e de volume de hardware, as alterações feitas no volume de software e nos controles de áudio por meio dessa interface afetarão o nível de volume no modo compartilhado, mas não no modo exclusivo. No modo exclusivo, o aplicativo e o hardware de áudio trocam dados de áudio diretamente, ignorando os controles de software.

Como regra geral, os aplicativos devem evitar o uso da interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) para controlar os níveis de volume de fluxos de modo compartilhado. Em vez disso, os aplicativos devem usar a interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)ou [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) para essa finalidade.

Se um aplicativo exibir um controle de volume que usa a interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) para controlar o nível de volume de um dispositivo de ponto de extremidade de áudio, esse controle de volume deverá espelhar o controle de volume do ponto de extremidade exibido pelo programa de controle de volume do sistema, SNDVOL. Conforme explicado anteriormente, o controle de volume do ponto de extremidade aparece no lado esquerdo da janela do SNDVOL, na caixa de grupo rotulada **dispositivo**. Se o usuário alterar o volume do ponto de extremidade de um dispositivo por meio do controle de volume no SNDVOL, o controle de volume do ponto de extremidade correspondente no aplicativo deverá ser movido de forma não-em harmonia com o controle em SNDVOL. Da mesma forma, se o usuário alterar o nível de volume por meio do controle de volume do ponto de extremidade na janela do aplicativo, o controle de volume correspondente no SNDVOL deverá ser movido de maneira inigual com o controle de volume do aplicativo.

Para garantir que o controle de volume do ponto de extremidade em uma janela de aplicativo espelhe o controle de volume do ponto de extremidade em SNDVOL, o aplicativo deve implementar uma interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) e registrar essa interface para receber notificações. Depois disso, cada vez que o usuário alterar o nível de volume do ponto de extremidade em SNDVOL, o aplicativo receberá uma chamada de notificação por meio do método [**IAudioEndpointVolumeCallback:: OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) . Durante essa chamada, o método **OnNotify** pode atualizar o controle de volume do ponto de extremidade na janela do aplicativo para corresponder à configuração de controle mostrada em SNDVOL. Da mesma forma, cada vez que o usuário altera o nível de volume do ponto de extremidade por meio do controle de volume na janela do aplicativo, o SNDVOL recebe uma notificação e atualiza imediatamente seu controle de volume do ponto de extremidade para exibir o novo nível de volume.

O exemplo de código a seguir é um arquivo de cabeçalho que mostra uma possível implementação da interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) :


```C++
// Epvolume.h -- Implementation of IAudioEndpointVolumeCallback interface

#include <windows.h>
#include <commctrl.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

// Dialog handle from dialog box procedure
extern HWND g_hDlg;

// Client's proprietary event-context GUID
extern GUID g_guidMyContext;

// Maximum volume level on trackbar
#define MAX_VOL  100

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// Client implementation of IAudioEndpointVolumeCallback
// interface. When a method in the IAudioEndpointVolume
// interface changes the volume level or muting state of the
// endpoint device, the change initiates a call to the
// client's IAudioEndpointVolumeCallback::OnNotify method.
//-----------------------------------------------------------
class CAudioEndpointVolumeCallback : public IAudioEndpointVolumeCallback
{
    LONG _cRef;

public:
    CAudioEndpointVolumeCallback() :
        _cRef(1)
    {
    }

    ~CAudioEndpointVolumeCallback()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;

    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioEndpointVolumeCallback) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioEndpointVolumeCallback*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback method for endpoint-volume-change notifications.

    HRESULT STDMETHODCALLTYPE OnNotify(PAUDIO_VOLUME_NOTIFICATION_DATA pNotify)
    {
        if (pNotify == NULL)
        {
            return E_INVALIDARG;
        }
        if (g_hDlg != NULL && pNotify->guidEventContext != g_guidMyContext)
        {
            PostMessage(GetDlgItem(g_hDlg, IDC_CHECK_MUTE), BM_SETCHECK,
                        (pNotify->bMuted) ? BST_CHECKED : BST_UNCHECKED, 0);

            PostMessage(GetDlgItem(g_hDlg, IDC_SLIDER_VOLUME),
                        TBM_SETPOS, TRUE,
                        LPARAM((UINT32)(MAX_VOL*pNotify->fMasterVolume + 0.5)));
        }
        return S_OK;
    }
};
```



A classe CAudioEndpointVolumeCallback no exemplo de código anterior é uma implementação da interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) . Como **IAudioEndpointVolumeCallback** é herdado de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), a definição de classe contém implementações dos métodos **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). O método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) na definição de classe é chamado cada vez que um dos seguintes métodos altera o nível de volume do ponto de extremidade:

-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume:: setmudo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

A implementação do método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) no exemplo de código anterior envia mensagens para o controle de volume na janela do aplicativo para atualizar o nível de volume exibido.

Um aplicativo chama o método [**IAudioEndpointVolume:: RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) para registrar sua interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) para receber notificações. Quando o aplicativo não requer mais notificações, ele chama o método [**IAudioEndpointVolume:: UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) para excluir o registro.

O exemplo de código a seguir é um aplicativo do Windows que chama os métodos [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) e [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) para registrar e cancelar o registro da classe CAudioEndpointVolumeCallback no exemplo de código anterior:


```C++
// Epvolume.cpp -- WinMain and dialog box functions

#include "stdafx.h"
#include "Epvolume.h"

HWND g_hDlg = NULL;
GUID g_guidMyContext = GUID_NULL;

static IAudioEndpointVolume *g_pEndptVol = NULL;
static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define ERROR_CANCEL(hr)  \
              if (FAILED(hr)) {  \
                  MessageBox(hDlg, TEXT("The program will exit."),  \
                             TEXT("Fatal error"), MB_OK);  \
                  EndDialog(hDlg, TRUE); return TRUE; }

//-----------------------------------------------------------
// WinMain -- Registers an IAudioEndpointVolumeCallback
//   interface to monitor endpoint volume level, and opens
//   a dialog box that displays a volume control that will
//   mirror the endpoint volume control in SndVol.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    CAudioEndpointVolumeCallback EPVolEvents;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    hr = CoCreateGuid(&g_guidMyContext);
    EXIT_ON_ERROR(hr)

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioEndpointVolume),
                           CLSCTX_ALL, NULL, (void**)&g_pEndptVol);
    EXIT_ON_ERROR(hr)

    hr = g_pEndptVol->RegisterControlChangeNotify(
                     (IAudioEndpointVolumeCallback*)&EPVolEvents);
    EXIT_ON_ERROR(hr)

    InitCommonControls();
    DialogBox(hInstance, L"VOLUMECONTROL", NULL, (DLGPROC)DlgProc);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    if (pEnumerator != NULL)
    {
        g_pEndptVol->UnregisterControlChangeNotify(
                    (IAudioEndpointVolumeCallback*)&EPVolEvents);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(g_pEndptVol)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    HRESULT hr;
    BOOL bMute;
    float fVolume;
    int nVolume;
    int nChecked;

    switch (message)
    {
    case WM_INITDIALOG:
        g_hDlg = hDlg;
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMIN, FALSE, 0);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMAX, FALSE, MAX_VOL);
        hr = g_pEndptVol->GetMute(&bMute);
        ERROR_CANCEL(hr)
        SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK,
                           bMute ? BST_CHECKED : BST_UNCHECKED, 0);
        hr = g_pEndptVol->GetMasterVolumeLevelScalar(&fVolume);
        ERROR_CANCEL(hr)
        nVolume = (int)(MAX_VOL*fVolume + 0.5);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETPOS, TRUE, nVolume);
        return TRUE;

    case WM_HSCROLL:
        switch (LOWORD(wParam))
        {
        case SB_THUMBPOSITION:
        case SB_THUMBTRACK:
        case SB_LINERIGHT:
        case SB_LINELEFT:
        case SB_PAGERIGHT:
        case SB_PAGELEFT:
        case SB_RIGHT:
        case SB_LEFT:
            // The user moved the volume slider in the dialog box.
            SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK, BST_UNCHECKED, 0);
            hr = g_pEndptVol->SetMute(FALSE, &g_guidMyContext);
            ERROR_CANCEL(hr)
            nVolume = SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_GETPOS, 0, 0);
            fVolume = (float)nVolume/MAX_VOL;
            hr = g_pEndptVol->SetMasterVolumeLevelScalar(fVolume, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        }
        break;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDC_CHECK_MUTE:
            // The user selected the Mute check box in the dialog box.
            nChecked = SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_GETCHECK, 0, 0);
            bMute = (BST_CHECKED == nChecked);
            hr = g_pEndptVol->SetMute(bMute, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        case IDCANCEL:
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;
    }
    return FALSE;
}
```



No exemplo de código anterior, a função [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) chama a [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância da interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chama o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) do dispositivo de renderização padrão. **WinMain** chama o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para obter a interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) do dispositivo e chama [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) para registrar o aplicativo para receber notificações de alterações no volume do ponto de extremidade. Em seguida, **WinMain** abre uma caixa de diálogo para exibir um controle de volume de ponto de extremidade para o dispositivo. A caixa de diálogo também exibe uma caixa de seleção que indica se o dispositivo está mudo. A caixa de seleção controle de volume do ponto de extremidade e mudo na caixa de diálogo espelha as configurações da caixa de seleção controle de volume do ponto de extremidade e sem áudio exibida por SNDVOL. Para obter mais informações sobre **WinMain** e **CoCreateInstance**, consulte a documentação do SDK do Windows. Para obter mais informações sobre **IMMDeviceEnumerator** e **IMMDevice**, consulte [enumerando dispositivos de áudio](enumerating-audio-devices.md).

O procedimento da caixa de diálogo, DlgProc, no exemplo de código anterior, manipula as alterações que o usuário faz nas configurações de volume e mudo por meio dos controles na caixa de diálogo. Quando DlgProc chama [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) ou [**setmudo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), SNDVOL recebe a notificação da alteração e atualiza o controle correspondente em sua janela para refletir a nova configuração de volume ou de mudo. Se, em vez de usar a caixa de diálogo, o usuário atualizar as configurações de volume e mudo por meio dos controles na janela SNDVOL, o método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) na classe CAudioEndpointVolumeCallback atualizará os controles na caixa de diálogo para exibir as novas configurações.

Se o usuário alterar o volume por meio dos controles na caixa de diálogo, o método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) na classe CAudioEndpointVolumeCallback não enviará mensagens para atualizar os controles na caixa de diálogo. Para isso, seria redundante. **Onnotificar** atualiza os controles na caixa de diálogo somente se a alteração do volume tiver sido originada em SNDVOL ou em algum outro aplicativo. O segundo parâmetro nas chamadas de método [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) e [**setmudo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) na função DlgProc é um ponteiro para um GUID de contexto de evento que o método passa para **onnotificate**. **Onnotificar** verifica o valor do GUID do contexto de evento para determinar se a caixa de diálogo é a origem da alteração do volume. Para obter mais informações sobre GUIDs de contexto de evento, consulte **IAudioEndpointVolumeCallback:: Onnotificate**.

Quando o usuário sai da caixa de diálogo, a chamada [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) no exemplo de código anterior exclui o registro da classe CAudioEndpointVolumeCallback antes de o programa ser encerrado.

Você pode modificar facilmente o exemplo de código anterior para exibir os controles de volume e de mudo para o dispositivo de captura padrão. Na função [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) , altere o valor do primeiro parâmetro na chamada para o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender para eCapture.

O exemplo de código a seguir é o script de recurso que define os controles de volume e mudo que aparecem no exemplo de código anterior:


```C++
// Epvolume.rc -- Resource script

#include "resource.h"
#include "windows.h"
#include "commctrl.h"

//
// Dialog box
//
VOLUMECONTROL DIALOGEX 0, 0, 160, 60
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Audio Endpoint Volume"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    LTEXT      "Min",IDC_STATIC_MINVOL,10,10,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,130,10,20,12
    CONTROL    "",IDC_SLIDER_VOLUME,"msctls_trackbar32",
               TBS_BOTH | TBS_NOTICKS | WS_TABSTOP,10,20,140,12
    CONTROL    "Mute",IDC_CHECK_MUTE,"Button",
               BS_AUTOCHECKBOX | WS_TABSTOP,20,40,70,12
END
```



O exemplo de código a seguir é o arquivo de cabeçalho do recurso que define os identificadores de controle que aparecem nos exemplos de código anteriores:


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



Os exemplos de código anteriores são combinados para formar um aplicativo simples para controlar e monitorar o volume do ponto de extremidade do dispositivo de renderização padrão. Um aplicativo mais útil pode, adicionalmente, notificar o usuário quando o status do dispositivo for alterado. Por exemplo, o dispositivo pode estar desabilitado, desconectado ou removido. Para obter mais informações sobre como monitorar esses tipos de eventos, consulte [eventos de dispositivo](device-events.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles de volume](volume-controls.md)
</dt> </dl>

 

 
