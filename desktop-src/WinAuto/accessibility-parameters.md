---
title: Parâmetros de acessibilidade
description: O sistema mantém um conjunto de parâmetros de acessibilidade que indicam se o usuário tem necessidades ou preferências especiais que exigem que os aplicativos alterem seu comportamento padrão.
ms.assetid: efa289bb-5965-4002-93df-116ab2621efc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a289162366f5d69c501ffbea55108167324c11a1c865184105afd587f36bcfd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327784"
---
# <a name="accessibility-parameters"></a>Parâmetros de acessibilidade

O sistema mantém um conjunto de parâmetros de acessibilidade que indicam se o usuário tem necessidades ou preferências especiais que exigem que os aplicativos alterem seu comportamento padrão. O usuário controla o estado desses parâmetros, normalmente usando a central de facilidade de acesso no painel de controle. Os aplicativos do painel de controle ou outros programas que permitem ao usuário personalizar o ambiente podem usar a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para definir os parâmetros de acessibilidade.

Se um usuário alterar esses parâmetros, o painel de controle enviará a mensagem do [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) . Os aplicativos devem responder a essa mensagem e usar [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para determinar o estado dos parâmetros de acessibilidade. Quando um parâmetro de acessibilidade é habilitado, o aplicativo deve modificar sua interface do usuário, se necessário, para acomodar as preferências do usuário.

o Windows dá suporte aos seguintes parâmetros de acessibilidade.



| Parâmetro                                                                    | Descrição                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alto contraste](high-contrast-parameter.md)                                 | Indica que os aplicativos devem fornecer alto contraste entre os visuais de primeiro e segundo plano.                                                                            |
| [Preferência de teclado](keyboard-preference-parameter.md)                     | Indica que os aplicativos devem exibir as interfaces de teclado que, de outra forma, seriam ocultas.                                                                                 |
| [Leitor de tela](screen-reader-parameter.md)                                 | Indica que os aplicativos devem fornecer informações textuais em situações em que, caso contrário, apresentaria as informações graficamente.                                     |
| [Mostrar sons (e sinalizador de descrição de áudio)](showsounds-parameter.md) | Indica que os aplicativos também devem fornecer um alerta visual ou uma indicação quando ele usa som para transmitir informações importantes ou fornecer uma descrição de áudio para elementos visuais. |
| [Animação da área do cliente](client-area-animation.md)                           | Indica que os aplicativos devem respeitar as preferências do usuário para exibir a animação na área do cliente.                                                                       |
| [Duração da mensagem](message-duration.md)                                     | Indica que os aplicativos que fornecem notificações pop-up devem monitorar os sinalizadores sobre a duração da mensagem e ajustar o tamanho da notificação.                                  |



 

Os parâmetros de sistema a seguir são úteis para aplicativos de acessibilidade. Para obter mais informações, consulte função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .



| Grupo de parâmetros      | Parâmetro                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parâmetros da área de trabalho   | SPI \_ GETWORKAREA, SPI \_ SETWORKAREA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Parâmetros de entrada     | SPI \_ GETKEYBOARDCUES, SPI \_ GETKEYBOARDDELAY, SPI \_ GETKEYBOARDPREF, SPI \_ GETKEYBOARDSPEED, SPI \_ GETMESSAGEDURATION, SPI \_ getrato, SPI \_ GETMOUSEHOVERHEIGHT, SPI \_ GETMOUSEHOVERTIME, SPI \_ GETMOUSEHOVERWIDTH, SPI GETMOUSESPEED, SPI GETMOUSETRAILS, SPI GETSNAPTODEFBUTTON, SPI GETWHEELSCROLLLINES, SPI setdoubleclicktime, SPI SETDOUBLECLKHEIGHT, SPI SETDOUBLECLKWIDTH, SPI SETKEYBOARDCUES, SPI SETKEYBOARDDELAY, SPI SETKEYBOARDPREF, SPI SETKEYBOARDSPEED, SPI setmouse, SPI SETMOUSEHOVERHEIGHT, SPI SETMOUSEHOVERTIME, SPI SETMOUSEHOVERWIDTH, \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ SPI \_ SETMOUSESPEED, SPI \_ SETMOUSETRAILS, SPI \_ SETSNAPTODEFBUTTON, SPI \_ SETWHEELSCROLLLINES |
| Parâmetros de efeito da interface do usuário | SPI \_ GETMENUUNDERLINES, SPI \_ SETMENUUNDERLINES                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Parâmetros da janela    | SPI \_ GETCARETWIDTH, SPI \_ GETFOREGROUNDFLASHCOUNT, SPI \_ GETFOREGROUNDLOCKTIMEOUT, SPI \_ SETCARETWIDTH, SPI \_ SETDRAGHEIGHT, SPI \_ SETDRAGWIDTH, SPI \_ SETFOREGROUNDFLASHCOUNT, SPI \_ SETFOREGROUNDLOCKTIMEOUT                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[sobre Windows recursos de acessibilidade](about-windows-accessibility-features.md)
</dt> </dl>

 

 