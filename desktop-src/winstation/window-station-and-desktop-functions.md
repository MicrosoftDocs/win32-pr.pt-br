---
title: Funções de estação de janela e área de trabalho
description: Os aplicativos podem usar as funções a seguir com objetos de estação de janela.
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6665f52de1f7f57930105edb0063c4512e375ac3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641113"
---
# <a name="window-station-and-desktop-functions"></a>Funções de estação de janela e área de trabalho

Os aplicativos podem usar as funções a seguir com objetos de [estação de janela](window-stations.md) .



| Função                                                     | Descrição                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | Fecha um identificador de estação de janela aberto.                                                                           |
| [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | Cria um objeto de estação de janela, associa-o ao processo atual e o atribui à sessão atual. |
| [**EnumWindowStations**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | Enumera todas as estações de janela na sessão atual.                                                          |
| [**GetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | Recupera um identificador para a estação de janela atual para o processo de chamada.                                       |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Recupera informações sobre a estação de janela ou o objeto da área de trabalho especificado.                                     |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Recupera informações de segurança para a estação de janela ou objeto de área de trabalho especificado.                              |
| [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | Abre a estação de janela especificada.                                                                             |
| [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | Atribui a estação de janela especificada ao processo de chamada.                                                    |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Define informações sobre a estação de janela ou o objeto da área de trabalho especificado.                                          |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Define informações de segurança para a estação de janela ou objeto de área de trabalho especificado.                                   |



 

Os aplicativos podem usar as seguintes funções com objetos de [área de trabalho](desktops.md) .



| Função                                                     | Descrição                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | Fecha um identificador aberto para um objeto de área de trabalho.                                                                                         |
| [**Createdesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | Cria uma nova área de trabalho, associa-a à estação da janela atual do processo de chamada e a atribui ao thread de chamada. |
| [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | Cria uma nova área de trabalho, associa-a à estação da janela atual do processo de chamada e a atribui ao thread de chamada. |
| [**EnumDesktops**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | Enumera todas as áreas de trabalho associadas à estação de janela atual do processo de chamada.                                         |
| [**EnumDesktopWindows**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | Enumera todas as janelas de nível superior associadas à área de trabalho especificada.                                                            |
| [**GetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | Recupera um identificador para a área de trabalho atribuída ao thread especificado.                                                                |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Obtém informações sobre uma estação de janela ou objeto de área de trabalho.                                                                         |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Obtém informações de segurança para uma estação de janela ou objeto de área de trabalho.                                                                  |
| [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | Abre o objeto da área de trabalho especificado.                                                                                                |
| [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | Abre a área de trabalho que recebe a entrada do usuário.                                                                                        |
| [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | Atribui a área de trabalho especificada ao thread de chamada.                                                                               |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Define informações sobre uma estação de janela ou um objeto de área de trabalho.                                                                         |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Define informações de segurança para uma estação de janela ou objeto de área de trabalho.                                                                  |
| [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | Tornar um desktop visível e ativá-lo. Isso permite que a área de trabalho receba entrada do usuário.                                 |



 

 

 