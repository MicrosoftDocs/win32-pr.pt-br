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
# <a name="endpoint-volume-controls"></a><span data-ttu-id="bf54e-103">Controles de volume do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="bf54e-103">Endpoint Volume Controls</span></span>

<span data-ttu-id="bf54e-104">As interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) permitem que os clientes controlem os níveis de volume de [sessões de áudio](audio-sessions.md), que são coleções de fluxos de áudio de modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="bf54e-104">The [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces enable clients to control the volume levels of [audio sessions](audio-sessions.md), which are collections of shared-mode audio streams.</span></span> <span data-ttu-id="bf54e-105">Essas interfaces não funcionam com fluxos de áudio de modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-105">These interfaces do not work with exclusive-mode audio streams.</span></span>

<span data-ttu-id="bf54e-106">Os aplicativos que gerenciam fluxos de modo exclusivo podem controlar os níveis de volume desses fluxos por meio da interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .</span><span class="sxs-lookup"><span data-stu-id="bf54e-106">Applications that manage exclusive-mode streams can control the volume levels of those streams through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface.</span></span> <span data-ttu-id="bf54e-107">Essa interface controla o nível de volume do [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="bf54e-107">This interface controls the volume level of the [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="bf54e-108">Ele usará o controle de volume de hardware para o dispositivo de ponto de extremidade se o hardware de áudio implementar esse controle.</span><span class="sxs-lookup"><span data-stu-id="bf54e-108">It uses the hardware volume control for the endpoint device if the audio hardware implements such a control.</span></span> <span data-ttu-id="bf54e-109">Caso contrário, a interface **IAudioEndpointVolume** implementa o controle de volume no software.</span><span class="sxs-lookup"><span data-stu-id="bf54e-109">Otherwise, the **IAudioEndpointVolume** interface implements the volume control in software.</span></span>

<span data-ttu-id="bf54e-110">Se um dispositivo tiver um controle de volume de hardware, as alterações feitas no controle por meio da interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) afetarão o nível de volume no modo compartilhado e no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-110">If a device has a hardware volume control, changes made to the control through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface affect the volume level both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="bf54e-111">Se um dispositivo não tiver controles de áudio e de volume de hardware, as alterações feitas no volume de software e nos controles de áudio por meio dessa interface afetarão o nível de volume no modo compartilhado, mas não no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-111">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through this interface affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="bf54e-112">No modo exclusivo, o aplicativo e o hardware de áudio trocam dados de áudio diretamente, ignorando os controles de software.</span><span class="sxs-lookup"><span data-stu-id="bf54e-112">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="bf54e-113">Como regra geral, os aplicativos devem evitar o uso da interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) para controlar os níveis de volume de fluxos de modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="bf54e-113">As a general rule, applications should avoid using the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume levels of shared-mode streams.</span></span> <span data-ttu-id="bf54e-114">Em vez disso, os aplicativos devem usar a interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)ou [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="bf54e-114">Instead, applications should use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), or [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interface for that purpose.</span></span>

<span data-ttu-id="bf54e-115">Se um aplicativo exibir um controle de volume que usa a interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) para controlar o nível de volume de um dispositivo de ponto de extremidade de áudio, esse controle de volume deverá espelhar o controle de volume do ponto de extremidade exibido pelo programa de controle de volume do sistema, SNDVOL.</span><span class="sxs-lookup"><span data-stu-id="bf54e-115">If an application displays a volume control that uses the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume level of an audio endpoint device, that volume control should mirror the endpoint volume control displayed by the system volume-control program, Sndvol.</span></span> <span data-ttu-id="bf54e-116">Conforme explicado anteriormente, o controle de volume do ponto de extremidade aparece no lado esquerdo da janela do SNDVOL, na caixa de grupo rotulada **dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="bf54e-116">As explained previously, the endpoint volume control appears on the left side of the Sndvol window, in the group box labeled **Device**.</span></span> <span data-ttu-id="bf54e-117">Se o usuário alterar o volume do ponto de extremidade de um dispositivo por meio do controle de volume no SNDVOL, o controle de volume do ponto de extremidade correspondente no aplicativo deverá ser movido de forma não-em harmonia com o controle em SNDVOL.</span><span class="sxs-lookup"><span data-stu-id="bf54e-117">If the user changes the endpoint volume of a device through the volume control in Sndvol, the corresponding endpoint volume control in the application should move in unison with the control in Sndvol.</span></span> <span data-ttu-id="bf54e-118">Da mesma forma, se o usuário alterar o nível de volume por meio do controle de volume do ponto de extremidade na janela do aplicativo, o controle de volume correspondente no SNDVOL deverá ser movido de maneira inigual com o controle de volume do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-118">Similarly, if the user changes the volume level through the endpoint volume control in the application window, the corresponding volume control in Sndvol should move in unison with the application's volume control.</span></span>

<span data-ttu-id="bf54e-119">Para garantir que o controle de volume do ponto de extremidade em uma janela de aplicativo espelhe o controle de volume do ponto de extremidade em SNDVOL, o aplicativo deve implementar uma interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) e registrar essa interface para receber notificações.</span><span class="sxs-lookup"><span data-stu-id="bf54e-119">To ensure that the endpoint volume control in an application window mirrors the endpoint volume control in Sndvol, the application should implement an [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface and register that interface to receive notifications.</span></span> <span data-ttu-id="bf54e-120">Depois disso, cada vez que o usuário alterar o nível de volume do ponto de extremidade em SNDVOL, o aplicativo receberá uma chamada de notificação por meio do método [**IAudioEndpointVolumeCallback:: OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) .</span><span class="sxs-lookup"><span data-stu-id="bf54e-120">Thereafter, each time the user changes the endpoint volume level in Sndvol, the application receives a notification call through its [**IAudioEndpointVolumeCallback::OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method.</span></span> <span data-ttu-id="bf54e-121">Durante essa chamada, o método **OnNotify** pode atualizar o controle de volume do ponto de extremidade na janela do aplicativo para corresponder à configuração de controle mostrada em SNDVOL.</span><span class="sxs-lookup"><span data-stu-id="bf54e-121">During this call, the **OnNotify** method can update the endpoint volume control in the application window to match the control setting shown in Sndvol.</span></span> <span data-ttu-id="bf54e-122">Da mesma forma, cada vez que o usuário altera o nível de volume do ponto de extremidade por meio do controle de volume na janela do aplicativo, o SNDVOL recebe uma notificação e atualiza imediatamente seu controle de volume do ponto de extremidade para exibir o novo nível de volume.</span><span class="sxs-lookup"><span data-stu-id="bf54e-122">Similarly, each time the user changes the endpoint volume level through volume control in the application window, Sndvol receives a notification and immediately updates its endpoint volume control to display the new volume level.</span></span>

<span data-ttu-id="bf54e-123">O exemplo de código a seguir é um arquivo de cabeçalho que mostra uma possível implementação da interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) :</span><span class="sxs-lookup"><span data-stu-id="bf54e-123">The following code example is a header file that shows a possible implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface:</span></span>


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



<span data-ttu-id="bf54e-124">A classe CAudioEndpointVolumeCallback no exemplo de código anterior é uma implementação da interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) .</span><span class="sxs-lookup"><span data-stu-id="bf54e-124">The CAudioEndpointVolumeCallback class in the preceding code example is an implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface.</span></span> <span data-ttu-id="bf54e-125">Como **IAudioEndpointVolumeCallback** é herdado de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), a definição de classe contém implementações dos métodos **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="bf54e-125">Because **IAudioEndpointVolumeCallback** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="bf54e-126">O método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) na definição de classe é chamado cada vez que um dos seguintes métodos altera o nível de volume do ponto de extremidade:</span><span class="sxs-lookup"><span data-stu-id="bf54e-126">The [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the class definition is called each time one of the following methods changes the endpoint volume level:</span></span>

-   [<span data-ttu-id="bf54e-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="bf54e-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [<span data-ttu-id="bf54e-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="bf54e-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [<span data-ttu-id="bf54e-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="bf54e-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [<span data-ttu-id="bf54e-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="bf54e-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [<span data-ttu-id="bf54e-131">**IAudioEndpointVolume:: setmudo**</span><span class="sxs-lookup"><span data-stu-id="bf54e-131">**IAudioEndpointVolume::SetMute**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [<span data-ttu-id="bf54e-132">**IAudioEndpointVolume::VolumeStepDown**</span><span class="sxs-lookup"><span data-stu-id="bf54e-132">**IAudioEndpointVolume::VolumeStepDown**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [<span data-ttu-id="bf54e-133">**IAudioEndpointVolume::VolumeStepUp**</span><span class="sxs-lookup"><span data-stu-id="bf54e-133">**IAudioEndpointVolume::VolumeStepUp**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

<span data-ttu-id="bf54e-134">A implementação do método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) no exemplo de código anterior envia mensagens para o controle de volume na janela do aplicativo para atualizar o nível de volume exibido.</span><span class="sxs-lookup"><span data-stu-id="bf54e-134">The implementation of the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the preceding code example sends messages to the volume control in the application window to update the displayed volume level.</span></span>

<span data-ttu-id="bf54e-135">Um aplicativo chama o método [**IAudioEndpointVolume:: RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) para registrar sua interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) para receber notificações.</span><span class="sxs-lookup"><span data-stu-id="bf54e-135">An application calls the [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) method to register its [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface to receive notifications.</span></span> <span data-ttu-id="bf54e-136">Quando o aplicativo não requer mais notificações, ele chama o método [**IAudioEndpointVolume:: UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) para excluir o registro.</span><span class="sxs-lookup"><span data-stu-id="bf54e-136">When the application no longer requires notifications, it calls the [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) method to delete the registration.</span></span>

<span data-ttu-id="bf54e-137">O exemplo de código a seguir é um aplicativo do Windows que chama os métodos [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) e [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) para registrar e cancelar o registro da classe CAudioEndpointVolumeCallback no exemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="bf54e-137">The following code example is a Windows application that calls the [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) and [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) methods to register and unregister the CAudioEndpointVolumeCallback class in the preceding code example:</span></span>


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



<span data-ttu-id="bf54e-138">No exemplo de código anterior, a função [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) chama a [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância da interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chama o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) do dispositivo de renderização padrão.</span><span class="sxs-lookup"><span data-stu-id="bf54e-138">In the preceding code example, the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="bf54e-139">**WinMain** chama o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para obter a interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) do dispositivo e chama [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) para registrar o aplicativo para receber notificações de alterações no volume do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="bf54e-139">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface, and it calls [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) to register the application to receive notifications of endpoint volume changes.</span></span> <span data-ttu-id="bf54e-140">Em seguida, **WinMain** abre uma caixa de diálogo para exibir um controle de volume de ponto de extremidade para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-140">Next, **WinMain** opens a dialog box to display an endpoint volume control for the device.</span></span> <span data-ttu-id="bf54e-141">A caixa de diálogo também exibe uma caixa de seleção que indica se o dispositivo está mudo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-141">The dialog box also displays a check box that indicates whether the device is muted.</span></span> <span data-ttu-id="bf54e-142">A caixa de seleção controle de volume do ponto de extremidade e mudo na caixa de diálogo espelha as configurações da caixa de seleção controle de volume do ponto de extremidade e sem áudio exibida por SNDVOL.</span><span class="sxs-lookup"><span data-stu-id="bf54e-142">The endpoint volume control and mute check box in the dialog box mirror the settings of the endpoint volume control and mute check box displayed by Sndvol.</span></span> <span data-ttu-id="bf54e-143">Para obter mais informações sobre **WinMain** e **CoCreateInstance**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="bf54e-143">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="bf54e-144">Para obter mais informações sobre **IMMDeviceEnumerator** e **IMMDevice**, consulte [enumerando dispositivos de áudio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="bf54e-144">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="bf54e-145">O procedimento da caixa de diálogo, DlgProc, no exemplo de código anterior, manipula as alterações que o usuário faz nas configurações de volume e mudo por meio dos controles na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-145">The dialog box procedure, DlgProc, in the preceding code example, handles the changes that the user makes to the volume and mute settings through the controls in the dialog box.</span></span> <span data-ttu-id="bf54e-146">Quando DlgProc chama [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) ou [**setmudo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), SNDVOL recebe a notificação da alteração e atualiza o controle correspondente em sua janela para refletir a nova configuração de volume ou de mudo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-146">When DlgProc calls [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) or [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), Sndvol receives notification of the change and updates the corresponding control in its window to reflect the new volume or mute setting.</span></span> <span data-ttu-id="bf54e-147">Se, em vez de usar a caixa de diálogo, o usuário atualizar as configurações de volume e mudo por meio dos controles na janela SNDVOL, o método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) na classe CAudioEndpointVolumeCallback atualizará os controles na caixa de diálogo para exibir as novas configurações.</span><span class="sxs-lookup"><span data-stu-id="bf54e-147">If, instead of using the dialog box, the user updates the volume and mute settings through the controls in the Sndvol window, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class updates the controls in the dialog box to display the new settings.</span></span>

<span data-ttu-id="bf54e-148">Se o usuário alterar o volume por meio dos controles na caixa de diálogo, o método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) na classe CAudioEndpointVolumeCallback não enviará mensagens para atualizar os controles na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-148">If the user changes the volume through the controls in the dialog box, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class does not send messages to update the controls in the dialog box.</span></span> <span data-ttu-id="bf54e-149">Para isso, seria redundante.</span><span class="sxs-lookup"><span data-stu-id="bf54e-149">To do so would be redundant.</span></span> <span data-ttu-id="bf54e-150">**Onnotificar** atualiza os controles na caixa de diálogo somente se a alteração do volume tiver sido originada em SNDVOL ou em algum outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf54e-150">**OnNotify** updates the controls in the dialog box only if the volume change originated in Sndvol or in some other application.</span></span> <span data-ttu-id="bf54e-151">O segundo parâmetro nas chamadas de método [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) e [**setmudo**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) na função DlgProc é um ponteiro para um GUID de contexto de evento que o método passa para **onnotificate**.</span><span class="sxs-lookup"><span data-stu-id="bf54e-151">The second parameter in the [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) and [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) method calls in the DlgProc function is a pointer to an event-context GUID that either method passes to **OnNotify**.</span></span> <span data-ttu-id="bf54e-152">**Onnotificar** verifica o valor do GUID do contexto de evento para determinar se a caixa de diálogo é a origem da alteração do volume.</span><span class="sxs-lookup"><span data-stu-id="bf54e-152">**OnNotify** checks the value of the event-context GUID to determine whether the dialog box is the source of the volume change.</span></span> <span data-ttu-id="bf54e-153">Para obter mais informações sobre GUIDs de contexto de evento, consulte **IAudioEndpointVolumeCallback:: Onnotificate**.</span><span class="sxs-lookup"><span data-stu-id="bf54e-153">For more information about event-context GUIDs, see **IAudioEndpointVolumeCallback::OnNotify**.</span></span>

<span data-ttu-id="bf54e-154">Quando o usuário sai da caixa de diálogo, a chamada [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) no exemplo de código anterior exclui o registro da classe CAudioEndpointVolumeCallback antes de o programa ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="bf54e-154">When the user exits the dialog box, the [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) call in the preceding code example deletes the registration of the CAudioEndpointVolumeCallback class before the program terminates.</span></span>

<span data-ttu-id="bf54e-155">Você pode modificar facilmente o exemplo de código anterior para exibir os controles de volume e de mudo para o dispositivo de captura padrão.</span><span class="sxs-lookup"><span data-stu-id="bf54e-155">You can easily modify the preceding code example to display volume and mute controls for the default capture device.</span></span> <span data-ttu-id="bf54e-156">Na função [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) , altere o valor do primeiro parâmetro na chamada para o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender para eCapture.</span><span class="sxs-lookup"><span data-stu-id="bf54e-156">In the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method from eRender to eCapture.</span></span>

<span data-ttu-id="bf54e-157">O exemplo de código a seguir é o script de recurso que define os controles de volume e mudo que aparecem no exemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="bf54e-157">The following code example is the resource script that defines the volume and mute controls that appear in the preceding code example:</span></span>


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



<span data-ttu-id="bf54e-158">O exemplo de código a seguir é o arquivo de cabeçalho do recurso que define os identificadores de controle que aparecem nos exemplos de código anteriores:</span><span class="sxs-lookup"><span data-stu-id="bf54e-158">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



<span data-ttu-id="bf54e-159">Os exemplos de código anteriores são combinados para formar um aplicativo simples para controlar e monitorar o volume do ponto de extremidade do dispositivo de renderização padrão.</span><span class="sxs-lookup"><span data-stu-id="bf54e-159">The preceding code examples combine to form a simple application for controlling and monitoring the endpoint volume of the default rendering device.</span></span> <span data-ttu-id="bf54e-160">Um aplicativo mais útil pode, adicionalmente, notificar o usuário quando o status do dispositivo for alterado.</span><span class="sxs-lookup"><span data-stu-id="bf54e-160">A more useful application might additionally notify the user when the status of the device changes.</span></span> <span data-ttu-id="bf54e-161">Por exemplo, o dispositivo pode estar desabilitado, desconectado ou removido.</span><span class="sxs-lookup"><span data-stu-id="bf54e-161">For example, the device might be disabled, unplugged, or removed.</span></span> <span data-ttu-id="bf54e-162">Para obter mais informações sobre como monitorar esses tipos de eventos, consulte [eventos de dispositivo](device-events.md).</span><span class="sxs-lookup"><span data-stu-id="bf54e-162">For more information about monitoring these types of events, see [Device Events](device-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf54e-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf54e-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf54e-164">Controles de volume</span><span class="sxs-lookup"><span data-stu-id="bf54e-164">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
