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

O sistema mantém um conjunto de parâmetros de acessibilidade que indicam se o usuário tem necessidades ou preferências especiais que exigem que os aplicativos alterem seu comportamento padrão. O usuário controla o estado desses parâmetros, normalmente usando o Central de Facilidade de Acesso em Painel de Controle. Painel de Controle aplicativos ou outros programas que permitem que o usuário personalize o ambiente podem usar a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para definir os parâmetros de acessibilidade.

Se um usuário altera esses parâmetros, o Painel de Controle envia a [**mensagem WM \_ SETTINGCHANGE.**](/windows/desktop/winmsg/wm-settingchange) Os aplicativos devem responder a essa mensagem e usar [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para determinar o estado dos parâmetros de acessibilidade. Quando um parâmetro de acessibilidade é habilitado, o aplicativo deve modificar sua interface do usuário, se necessário, para acomodar as preferências do usuário.

Windows dá suporte aos seguintes parâmetros de acessibilidade.



| Parâmetro                                                                    | Descrição                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alto contraste](high-contrast-parameter.md)                                 | Indica que os aplicativos devem fornecer alto contraste entre visuais em primeiro plano e em segundo plano.                                                                            |
| [Preferência de teclado](keyboard-preference-parameter.md)                     | Indica que os aplicativos devem exibir interfaces de teclado que, de outra forma, seriam ocultas.                                                                                 |
| [Leitor de tela](screen-reader-parameter.md)                                 | Indica que os aplicativos devem fornecer informações textuais em situações em que, de outra forma, apresentariam as informações graficamente.                                     |
| [Mostrar sons (e sinalizador de descrição de áudio)](showsounds-parameter.md) | Indica que os aplicativos também devem fornecer um alerta visual ou uma indicação quando ele usa som para transmitir informações importantes ou fornecer uma descrição de áudio para elementos visuais. |
| [Animação da área do cliente](client-area-animation.md)                           | Indica que os aplicativos devem respeitar as preferências do usuário para exibir animação na área do cliente.                                                                       |
| [Duração da mensagem](message-duration.md)                                     | Indica que os aplicativos que fornecem notificações pop-up devem monitorar sinalizadores sobre a duração da mensagem e ajustar o comprimento da notificação.                                  |



 

Os parâmetros do sistema a seguir são úteis para aplicativos de acessibilidade. Para obter mais informações, consulte [**Função SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)



| Grupo de parâmetros      | Parâmetro                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parâmetros da área de trabalho   | SPI \_ GETWORKAREA, SPI \_ SETWORKAREA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Parâmetros de entrada     | SPI \_ GETKEYBOARDCUES, SPI \_ GETKEYBOARDDELAY, SPI \_ GETKEYBOARDPREF, SPI \_ GETKEYBOARDSPEED, SPI \_ GETMESSAGEDURATION, SPI \_ GETMOUSE, SPI \_ GETMOUSEHOVERHEIGHT, SPI \_ GETMOUSEHOVERTIME, SPI \_ GETMOUSEHOVERWIDTH, SPI \_ GETMOUSESPEED, SPI \_ GETMOUSETRAILS, SPI \_ GETSNAPTODEFBUTTON, SPI \_ GETWHEELSCROLLLINES, SPI \_ SETDOUBLECLICKTIME, SPI \_ SETDOUBLECLKHEIGHT, SPI \_ SETDOUBLECLKWIDTH, SPI \_ SETKEYBOARDCUES, SPI \_ SETKEYBOARDDELAY, SPI \_ SETKEYBOARDPREF, SPI \_ SETKEYBOARDSPEED, SPI \_ SETMOUSE, SPI \_ SETMOUSEHOVERHEIGHT, SPI \_ SETMOUSEHOVERTIME, SPI \_ SETMOUSEHOVERWIDTH, SPI \_ SETMOUSESPEED, SPI \_ SETMOUSETRAILS, SPI \_ SETSNAPTODEFBUTTON, SPI \_ SETWHEELSCROLLLINES |
| Parâmetros de efeito da interface do usuário | SPI \_ GETMENUUNDERLINES, SPI \_ SETMENUUNDERLINES                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Parâmetros de janela    | SPI \_ GETCARETWIDTH, SPI \_ GETFOREGROUNDFLASHCOUNT, SPI \_ GETFOREGROUNDLOCKTIMEOUT, SPI \_ SETCARETWIDTH, SPI \_ SETDRAGHEIGHT, SPI \_ SETDRAGWIDTH, SPI \_ SETFOREGROUNDFLASHCOUNT, SPI \_ SETFOREGROUNDLOCKTIMEOUT                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Windows recursos de acessibilidade](about-windows-accessibility-features.md)
</dt> </dl>

 

 