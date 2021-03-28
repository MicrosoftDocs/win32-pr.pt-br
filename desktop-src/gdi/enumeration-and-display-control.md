---
description: Para enumerar todos os dispositivos no computador, chame a função EnumDisplayDevices. As informações retornadas também indicam qual monitor faz parte da área de trabalho.
ms.assetid: 834dee04-66fa-42eb-adff-c08a74c6cea8
title: Enumeração e controle de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8cdfd5e3b1c6ebb5ff0d4ebdfa1ab44b45c2c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010731"
---
# <a name="enumeration-and-display-control"></a><span data-ttu-id="d5991-104">Enumeração e controle de exibição</span><span class="sxs-lookup"><span data-stu-id="d5991-104">Enumeration and Display Control</span></span>

<span data-ttu-id="d5991-105">Para enumerar todos os dispositivos no computador, chame a função [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) .</span><span class="sxs-lookup"><span data-stu-id="d5991-105">To enumerate all the devices on the computer, call the [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) function.</span></span> <span data-ttu-id="d5991-106">As informações retornadas também indicam qual monitor faz parte da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d5991-106">The information that is returned also indicates which monitor is part of the desktop.</span></span>

<span data-ttu-id="d5991-107">Para enumerar os dispositivos na área de trabalho que interseccionam uma região de recorte, chame [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span><span class="sxs-lookup"><span data-stu-id="d5991-107">To enumerate the devices on the desktop that intersect a clipping region, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span></span> <span data-ttu-id="d5991-108">Isso retorna o identificador HMONITOR para cada monitor, que é usado com [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="d5991-108">This returns the HMONITOR handle to each monitor, which is used with [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span> <span data-ttu-id="d5991-109">Para enumerar todos os dispositivos na tela virtual, use **EnumDisplayMonitors**.</span><span class="sxs-lookup"><span data-stu-id="d5991-109">To enumerate all the devices in the virtual screen, use **EnumDisplayMonitors**.</span></span> <span data-ttu-id="d5991-110">conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="d5991-110">as shown in the following code:</span></span>


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



<span data-ttu-id="d5991-111">Para obter informações sobre um dispositivo de vídeo, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) ou [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span><span class="sxs-lookup"><span data-stu-id="d5991-111">To get information about a display device, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) or [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span></span>

<span data-ttu-id="d5991-112">A função [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) é usada para controlar os dispositivos de exibição no computador.</span><span class="sxs-lookup"><span data-stu-id="d5991-112">The [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) function is used to control the display devices on the computer.</span></span> <span data-ttu-id="d5991-113">Ele pode modificar a configuração dos dispositivos, como especificar a posição de um monitor na área de trabalho virtual e alterar a profundidade de bits de qualquer exibição.</span><span class="sxs-lookup"><span data-stu-id="d5991-113">It can modify the configuration of the devices, such as specifying the position of a monitor on the virtual desktop and changing the bit depth of any display.</span></span> <span data-ttu-id="d5991-114">Normalmente, um aplicativo não usa essa função.</span><span class="sxs-lookup"><span data-stu-id="d5991-114">Typically, an application does not use this function.</span></span> <span data-ttu-id="d5991-115">Para adicionar um monitor de exibição a um sistema de vários monitores programaticamente, defina **DEVMODE. dmFields** para a \_ posição DM e especifique uma posição (usando **DEVMODE. dmPosition** ) para o monitor que você está adicionando, que é adjacente a pelo menos um pixel da área de exibição de um monitor existente.</span><span class="sxs-lookup"><span data-stu-id="d5991-115">To add a display monitor to a multiple-monitor system programmatically, set **DEVMODE.dmFields** to DM\_POSITION and specify a position (using **DEVMODE.dmPosition** ) for the monitor you are adding that is adjacent to at least one pixel of the display area of an existing monitor.</span></span> <span data-ttu-id="d5991-116">Para desanexar o monitor, defina **DEVMODE. dmFields** como DM \_ Position e defina **DEVMODE. DmPelsWidth** e **DEVMODE. dmPelsHeight** como zero.</span><span class="sxs-lookup"><span data-stu-id="d5991-116">To detach the monitor, set **DEVMODE.dmFields** to DM\_POSITION and set **DEVMODE.dmPelsWidth** and **DEVMODE.dmPelsHeight** to zero.</span></span>

<span data-ttu-id="d5991-117">O código a seguir demonstra como desanexar todos os dispositivos de vídeo secundários da área de trabalho:</span><span class="sxs-lookup"><span data-stu-id="d5991-117">The following code demonstrates how to detach all secondary display devices from the desktop:</span></span>


```
void DetachDisplay()
{
    BOOL            FoundSecondaryDisp = FALSE;
    DWORD           DispNum = 0;
    DISPLAY_DEVICE  DisplayDevice;
    LONG            Result;
    TCHAR           szTemp[200];
    int             i = 0;
    DEVMODE   defaultMode;

    // initialize DisplayDevice
    ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
    DisplayDevice.cb = sizeof(DisplayDevice);

    // get all display devices
    while (EnumDisplayDevices(NULL, DispNum, &DisplayDevice, 0))
        {
        ZeroMemory(&defaultMode, sizeof(DEVMODE));
        defaultMode.dmSize = sizeof(DEVMODE);
        if ( !EnumDisplaySettings((LPSTR)DisplayDevice.DeviceName, ENUM_REGISTRY_SETTINGS, &defaultMode) )
                  OutputDebugString("Store default failed\n");

        if ((DisplayDevice.StateFlags & DISPLAY_DEVICE_ATTACHED_TO_DESKTOP) &&
            !(DisplayDevice.StateFlags & DISPLAY_DEVICE_PRIMARY_DEVICE))
            {
            DEVMODE    DevMode;
            ZeroMemory(&DevMode, sizeof(DevMode));
            DevMode.dmSize = sizeof(DevMode);
            DevMode.dmFields = DM_PELSWIDTH | DM_PELSHEIGHT | DM_BITSPERPEL | DM_POSITION
                        | DM_DISPLAYFREQUENCY | DM_DISPLAYFLAGS ;
            Result = ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName, 
                                            &DevMode,
                                            NULL,
                                            CDS_UPDATEREGISTRY,
                                            NULL);

            //The code below shows how to re-attach the secondary displays to the desktop

            //ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName,
            //                       &defaultMode,
            //                       NULL,
            //                       CDS_UPDATEREGISTRY,
            //                       NULL);

            }

        // Reinit DisplayDevice just to be extra clean

        ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
        DisplayDevice.cb = sizeof(DisplayDevice);
        DispNum++;
        } // end while for all display devices
}
```



<span data-ttu-id="d5991-118">Para cada dispositivo de vídeo, o aplicativo pode salvar informações no registro que descrevem os parâmetros de configuração para o dispositivo, bem como parâmetros de localização.</span><span class="sxs-lookup"><span data-stu-id="d5991-118">For each display device, the application can save information in the registry that describes the configuration parameters for the device, as well as location parameters.</span></span> <span data-ttu-id="d5991-119">O aplicativo também pode determinar quais monitores fazem parte da área de trabalho e quais não estão, por meio do \_ dispositivo de vídeo \_ anexado \_ ao \_ sinalizador da área de trabalho na estrutura do [**\_ dispositivo de vídeo**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .</span><span class="sxs-lookup"><span data-stu-id="d5991-119">The application can also determine which displays are part of the desktop, and which are not, through the DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span> <span data-ttu-id="d5991-120">Depois que todas as informações de configuração são armazenadas no registro, o aplicativo pode chamar [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) novamente para alterar dinamicamente as configurações, sem necessidade de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="d5991-120">Once all the configuration information is stored in the registry, the application can call [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) again to dynamically change the settings, with no restart required.</span></span>

 

 



