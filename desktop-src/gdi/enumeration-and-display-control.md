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
# <a name="enumeration-and-display-control"></a>Enumeração e controle de exibição

Para enumerar todos os dispositivos no computador, chame a função [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) . As informações retornadas também indicam qual monitor faz parte da área de trabalho.

Para enumerar os dispositivos na área de trabalho que interseccionam uma região de recorte, chame [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors). Isso retorna o identificador HMONITOR para cada monitor, que é usado com [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa). Para enumerar todos os dispositivos na tela virtual, use **EnumDisplayMonitors**. conforme mostrado no código a seguir:


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



Para obter informações sobre um dispositivo de vídeo, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) ou [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).

A função [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) é usada para controlar os dispositivos de exibição no computador. Ele pode modificar a configuração dos dispositivos, como especificar a posição de um monitor na área de trabalho virtual e alterar a profundidade de bits de qualquer exibição. Normalmente, um aplicativo não usa essa função. Para adicionar um monitor de exibição a um sistema de vários monitores programaticamente, defina **DEVMODE. dmFields** para a \_ posição DM e especifique uma posição (usando **DEVMODE. dmPosition** ) para o monitor que você está adicionando, que é adjacente a pelo menos um pixel da área de exibição de um monitor existente. Para desanexar o monitor, defina **DEVMODE. dmFields** como DM \_ Position e defina **DEVMODE. DmPelsWidth** e **DEVMODE. dmPelsHeight** como zero.

O código a seguir demonstra como desanexar todos os dispositivos de vídeo secundários da área de trabalho:


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



Para cada dispositivo de vídeo, o aplicativo pode salvar informações no registro que descrevem os parâmetros de configuração para o dispositivo, bem como parâmetros de localização. O aplicativo também pode determinar quais monitores fazem parte da área de trabalho e quais não estão, por meio do \_ dispositivo de vídeo \_ anexado \_ ao \_ sinalizador da área de trabalho na estrutura do [**\_ dispositivo de vídeo**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) . Depois que todas as informações de configuração são armazenadas no registro, o aplicativo pode chamar [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) novamente para alterar dinamicamente as configurações, sem necessidade de reinicialização.

 

 



