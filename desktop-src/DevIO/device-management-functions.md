---
description: As funções a seguir são usadas no gerenciamento de dispositivos.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Funções de gerenciamento de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920315"
---
# <a name="device-management-functions"></a>Funções de gerenciamento de dispositivo

As funções a seguir são usadas no gerenciamento de dispositivos.



| Função                                                             | Descrição                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | Envia um código de controle diretamente para um driver de dispositivo especificado.                           |
| [**InstallNewDevice**](installnewdevice.md)                         | Instala um novo dispositivo. O usuário é solicitado a selecionar o dispositivo.                     |
| [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | Registra o dispositivo ou tipo de dispositivo para o qual uma janela receberá notificações. |
| [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | Fecha o identificador de notificação do dispositivo especificado.                                      |



 

As funções a seguir são usadas com unidades de CD-ROM e DVD.



| Função                                                               | Descrição                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CdromDisableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | Desabilita a reprodução digital para a unidade de CD-ROM ou DVD especificada.                                    |
| [**CdromEnableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | Habilita a reprodução digital para a unidade de CD-ROM ou DVD especificada.                                     |
| [**CdromIsDigitalPlaybackEnabled**](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | Determina se a reprodução digital está habilitada para a unidade de CD-ROM ou DVD especificada.               |
| [**CdromKnownGoodDigitalPlayback**](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | Determina se a unidade de CD-ROM ou DVD especificada tem reprodução digital conhecida como boa. |
| [**DvdLauncher**](dvdlauncher.md)                                     | Verifica se a região de mídia na unidade de DVD corresponde à região da unidade de DVD.                       |



 

 

 
