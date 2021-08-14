---
title: Referência de MCIWnd
description: Referência de MCIWnd
ms.assetid: 11fba6bb-17f1-4fbe-b148-4755a3c6216a
keywords:
- MCI (Interface de Controle de Mídia), Referência de MCIWnd
- Classe de janela MCIWnd, referência
- Janela MCIWnd, referência
- Referência de MCIWnd, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03249d5e0f0a0f4fef8110d878021437f7aee667085a0720a86de77c8cbdfe49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374352"
---
# <a name="mciwnd-reference"></a>Referência de MCIWnd

Esta seção descreve as funções, mensagens e macros associadas à classe de janela MCIWnd. Esses elementos são agrupados da seguinte forma.

## <a name="window-management"></a>Gerenciamento de janela

-   [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
-   [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
-   [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
-   [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass)

## <a name="file-and-device-management"></a>Arquivo e Gerenciamento de Dispositivos

-   [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose)
-   [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy)
-   [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
-   [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
-   [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
-   [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog)
-   [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave)
-   [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog)

## <a name="playback-options"></a>Opções de reprodução

-   [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
-   [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay)
-   [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
-   [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
-   [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
-   [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
-   [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)

## <a name="recording"></a>Gravação

-   [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord)

## <a name="positioning"></a>Posicionamento

-   [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)
-   [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
-   [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
-   [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
-   [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
-   [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
-   [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome)
-   [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
-   [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep)

## <a name="pause-and-resume-playback"></a>Pausar e retomar a reprodução

-   [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
-   [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay)
-   [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
-   [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
-   [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
-   [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
-   [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)

## <a name="performance-tuning"></a>Ajuste de desempenho

-   [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
-   [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
-   [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
-   [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
-   [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
-   [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)

## <a name="image-and-palette-adjustments"></a>Ajustes de imagem e paleta

-   [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
-   [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
-   [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
-   [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
-   [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource)
-   [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
-   [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)

## <a name="event-and-error-notification"></a>Notificação de evento e erro

-   [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
-   [**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)
-   [**MCIWNDM \_ NOTIFYMEDIA**](mciwndm-notifymedia.md)
-   [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md)
-   [**MCIWNDM \_ NOTIFYPOS**](mciwndm-notifypos.md)
-   [**MCIWNDM \_ NOTIFYSIZE**](mciwndm-notifysize.md)

## <a name="time-formats"></a>Formatos de hora

-   [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
-   [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
-   [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
-   [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
-   [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)

## <a name="status-updates"></a>Atualizações de status

-   [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
-   [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
-   [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
-   [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
-   [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)

## <a name="device-capabilities"></a>Funcionalidades do dispositivo

-   [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
-   [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
-   [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
-   [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
-   [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
-   [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)

## <a name="mci-device-settings"></a>Dispositivo MCI Configurações

-   [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
-   [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice)
-   [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
-   [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
-   [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)

## <a name="mci-command-string-interface"></a>MCI Command-String Interface

-   [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
-   [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classe de janela MCIWnd](mciwnd-window-class.md)
</dt> </dl>

 

 




