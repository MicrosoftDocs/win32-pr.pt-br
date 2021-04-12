---
description: Medidores de pico
ms.assetid: 02f5d1b4-ba4f-424a-897f-b113d1f7cd6b
title: Medidores de pico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccd2f1ce0b8fd45fbf1cb3710c878c05544f7d4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089343"
---
# <a name="peak-meters"></a><span data-ttu-id="16b44-103">Medidores de pico</span><span class="sxs-lookup"><span data-stu-id="16b44-103">Peak Meters</span></span>

<span data-ttu-id="16b44-104">Para dar suporte a aplicativos do Windows que exibem medidores de pico, a [API EndpointVolume](endpointvolume-api.md) inclui uma interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) .</span><span class="sxs-lookup"><span data-stu-id="16b44-104">To support Windows applications that display peak meters, the [EndpointVolume API](endpointvolume-api.md) includes an [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface.</span></span> <span data-ttu-id="16b44-105">Essa interface representa um medidor de pico em um [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="16b44-105">This interface represents a peak meter on an [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="16b44-106">Para um dispositivo de renderização, o valor recuperado do medidor de pico representa o valor de exemplo máximo encontrado no fluxo de saída para o dispositivo durante o período de medição anterior.</span><span class="sxs-lookup"><span data-stu-id="16b44-106">For a rendering device, the value retrieved from the peak meter represents the maximum sample value encountered in the output stream to the device during the preceding metering period.</span></span> <span data-ttu-id="16b44-107">Para um dispositivo de captura, o valor recuperado do medidor de pico representa o valor de exemplo máximo encontrado no fluxo de entrada do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16b44-107">For a capture device, the value retrieved from the peak meter represents the maximum sample value encountered in the input stream from the device.</span></span>

<span data-ttu-id="16b44-108">Os valores de medidor de pico obtidos dos métodos na interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) são números de ponto flutuante no intervalo normalizado de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="16b44-108">The peak-meter values obtained from the methods in the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface are floating-point numbers in the normalized range from 0.0 to 1.0.</span></span> <span data-ttu-id="16b44-109">Por exemplo, se um fluxo PCM contiver amostras de 16 bits e o valor de exemplo de pico durante um período de medição específico for — 8914, o valor absoluto registrado pelo medidor de pico será 8914 e o valor de pico normalizado relatado pela interface **IAudioMeterInformation** será 8914/32768 = 0,272.</span><span class="sxs-lookup"><span data-stu-id="16b44-109">For example, if a PCM stream contains 16-bit samples, and the peak sample value during a particular metering period is —8914, then the absolute value recorded by the peak meter is 8914, and the normalized peak value reported by the **IAudioMeterInformation** interface is 8914/32768 = 0.272.</span></span>

<span data-ttu-id="16b44-110">Se o dispositivo de ponto de extremidade de áudio implementar o medidor de pico no hardware, a interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) usará o medidor de pico de hardware.</span><span class="sxs-lookup"><span data-stu-id="16b44-110">If the audio endpoint device implements the peak meter in hardware, the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface uses the hardware peak meter.</span></span> <span data-ttu-id="16b44-111">Caso contrário, a interface implementa o medidor de pico no software.</span><span class="sxs-lookup"><span data-stu-id="16b44-111">Otherwise, the interface implements the peak meter in software.</span></span>

<span data-ttu-id="16b44-112">Se um dispositivo tiver um medidor de pico de hardware, o medidor de pico estará ativo no modo compartilhado e no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="16b44-112">If a device has a hardware peak meter, the peak meter is active both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="16b44-113">Se um dispositivo não tiver um medidor de pico de hardware, o medidor de pico estará ativo no modo compartilhado, mas não no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="16b44-113">If a device lacks hardware peak meter, the peak meter is active in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="16b44-114">No modo exclusivo, o aplicativo e o hardware de áudio trocam dados de áudio diretamente, ignorando o medidor de pico de software (que sempre relata um valor de pico de 0,0).</span><span class="sxs-lookup"><span data-stu-id="16b44-114">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software peak meter (which always reports a peak value of 0.0).</span></span>

<span data-ttu-id="16b44-115">O exemplo de código C++ a seguir é um aplicativo do Windows que exibe um medidor de pico para o dispositivo de renderização padrão:</span><span class="sxs-lookup"><span data-stu-id="16b44-115">The following C++ code example is a Windows application that displays a peak meter for the default rendering device:</span></span>


```C++
// Peakmeter.cpp -- WinMain and dialog box functions

#include <windows.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);
static void DrawPeakMeter(HWND, float);

// Timer ID and period (in milliseconds)
#define ID_TIMER  1
#define TIMER_PERIOD  125

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// WinMain -- Opens a dialog box that contains a peak meter.
//   The peak meter displays the peak sample value that plays
//   through the default rendering device.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioMeterInformation *pMeterInfo = NULL;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get peak meter for default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioMeterInformation),
                           CLSCTX_ALL, NULL, (void**)&pMeterInfo);
    EXIT_ON_ERROR(hr)

    DialogBoxParam(hInstance, L"PEAKMETER", NULL, (DLGPROC)DlgProc, (LPARAM)pMeterInfo);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pMeterInfo)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    static IAudioMeterInformation *pMeterInfo = NULL;
    static HWND hPeakMeter = NULL;
    static float peak = 0;
    HRESULT hr;

    switch (message)
    {
    case WM_INITDIALOG:
        pMeterInfo = (IAudioMeterInformation*)lParam;
        SetTimer(hDlg, ID_TIMER, TIMER_PERIOD, NULL);
        hPeakMeter = GetDlgItem(hDlg, IDC_PEAK_METER);
        return TRUE;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDCANCEL:
            KillTimer(hDlg, ID_TIMER);
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;

    case WM_TIMER:
        switch ((int)wParam)
        {
        case ID_TIMER:
            // Update the peak meter in the dialog box.
            hr = pMeterInfo->GetPeakValue(&peak);
            if (FAILED(hr))
            {
                MessageBox(hDlg, TEXT("The program will exit."),
                           TEXT("Fatal error"), MB_OK);
                KillTimer(hDlg, ID_TIMER);
                EndDialog(hDlg, TRUE);
                return TRUE;
            }
            DrawPeakMeter(hPeakMeter, peak);
            return TRUE;
        }
        break;

    case WM_PAINT:
        // Redraw the peak meter in the dialog box.
        ValidateRect(hPeakMeter, NULL);
        DrawPeakMeter(hPeakMeter, peak);
        break;
    }
    return FALSE;
}

//-----------------------------------------------------------
// DrawPeakMeter -- Draws the peak meter in the dialog box.
//-----------------------------------------------------------

void DrawPeakMeter(HWND hPeakMeter, float peak)
{
    HDC hdc;
    RECT rect;

    GetClientRect(hPeakMeter, &rect);
    hdc = GetDC(hPeakMeter);
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DSHADOW+1));
    rect.left++;
    rect.top++;
    rect.right = rect.left +
                 max(0, (LONG)(peak*(rect.right-rect.left)-1.5));
    rect.bottom--;
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DHIGHLIGHT+1));
    ReleaseDC(hPeakMeter, hdc);
}
```



<span data-ttu-id="16b44-116">No exemplo de código anterior, a função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) chama a [**função CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância da interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chama o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) do dispositivo de renderização padrão.</span><span class="sxs-lookup"><span data-stu-id="16b44-116">In the preceding code example, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="16b44-117">**WinMain** chama o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para obter a interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) do dispositivo e abre uma caixa de diálogo para exibir um medidor de pico para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16b44-117">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface, and it opens a dialog box to display a peak meter for the device.</span></span> <span data-ttu-id="16b44-118">Para obter mais informações sobre **WinMain** e **CoCreateInstance**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="16b44-118">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="16b44-119">Para obter mais informações sobre **IMMDeviceEnumerator** e **IMMDevice**, consulte [enumerando dispositivos de áudio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="16b44-119">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="16b44-120">No exemplo de código anterior, a função DlgProc exibe o medidor de pico na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="16b44-120">In the preceding code example, the DlgProc function displays the peak meter in the dialog box.</span></span> <span data-ttu-id="16b44-121">Durante o processamento da \_ mensagem INITDIALOG do WM, DlgProc chama a função [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) para configurar um temporizador que gerará \_ mensagens de temporizador do WM em intervalos de tempo regulares.</span><span class="sxs-lookup"><span data-stu-id="16b44-121">During processing of the WM\_INITDIALOG message, DlgProc calls the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function to set up a timer that will generate WM\_TIMER messages at regular time intervals.</span></span> <span data-ttu-id="16b44-122">Quando o DlgProc recebe uma \_ mensagem de temporizador do WM, ele chama [**IAudioMeterInformation:: getpicovalue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) para obter a leitura mais recente do medidor de pico para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="16b44-122">When DlgProc receives a WM\_TIMER message, it calls [**IAudioMeterInformation::GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) to obtain the latest peak-meter reading for the stream.</span></span> <span data-ttu-id="16b44-123">Em seguida, DlgProc chama a função DrawPeakMeter para desenhar o medidor de pico atualizado na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="16b44-123">DlgProc then calls the DrawPeakMeter function to draw the updated peak meter in the dialog box.</span></span> <span data-ttu-id="16b44-124">Para obter mais informações sobre **SetTimer** e as \_ mensagens de temporizador do WM INITDIALOG e do WM \_ , consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="16b44-124">For more information about **SetTimer** and the WM\_INITDIALOG and WM\_TIMER messages, see the Windows SDK documentation.</span></span>

<span data-ttu-id="16b44-125">Você pode modificar facilmente o exemplo de código anterior para exibir um medidor de pico para o dispositivo de captura padrão.</span><span class="sxs-lookup"><span data-stu-id="16b44-125">You can easily modify the preceding code example to display a peak meter for the default capture device.</span></span> <span data-ttu-id="16b44-126">Na função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) , altere o valor do primeiro parâmetro na chamada para [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender para eCapture.</span><span class="sxs-lookup"><span data-stu-id="16b44-126">In the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) from eRender to eCapture.</span></span>

<span data-ttu-id="16b44-127">O exemplo de código a seguir é o script de recurso que define os controles que aparecem no exemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="16b44-127">The following code example is the resource script that defines the controls that appear in the preceding code example:</span></span>


```C++
// Peakmeter.rc -- Resource script

#include "resource.h"
#include "windows.h"

//
// Dialog
//
PEAKMETER DIALOGEX 0, 0, 150, 34
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Peak Meter"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    CTEXT      "",IDC_PEAK_METER,34,14,82,5
    LTEXT      "Min",IDC_STATIC_MINVOL,10,12,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,120,12,20,12
END
```



<span data-ttu-id="16b44-128">O exemplo de código a seguir é o arquivo de cabeçalho do recurso que define os identificadores de controle que aparecem nos exemplos de código anteriores:</span><span class="sxs-lookup"><span data-stu-id="16b44-128">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a><span data-ttu-id="16b44-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16b44-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b44-130">Controles de volume</span><span class="sxs-lookup"><span data-stu-id="16b44-130">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
