---
title: Captura de término de chaves
description: Captura de término de chaves
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- Estrutura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5764f6b1853e1b161501f3c8df22ff0b7387649c517a28e7e36e7a094f35b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140046"
---
# <a name="keys-ending-capture"></a>Captura de término de chaves

Você pode permitir que o usuário anule uma sessão de captura pressionando uma combinação de teclas ou pressionando teclas do teclado ou pressionando o botão direito ou esquerdo do mouse. Se o usuário anular uma sessão de captura em tempo real, o conteúdo do arquivo de captura será descartado. Se o usuário anular uma sessão de captura de quadro de etapa, o conteúdo do arquivo de captura até o ponto de anular a captura será salvo.

Você pode recuperar as configurações para anular uma sessão de captura usando a mensagem [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (ou a [**macro capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) A configuração de teclas atual é armazenada no **membro vKeyAbort** da [**estrutura CAPTUREPARMS;**](/windows/win32/api/vfw/ns-vfw-captureparms) as configurações atuais do mouse são armazenadas nos **membros fAbortLeftMouse** e **fAbortRightMouse.** Você pode definir uma nova combinação de teclas ou teclas especificando a combinação de keycode ou keycode (como em uma combinação de teclas CTRL ou SHIFT) como o valor **de vKeyAbort** ou definir o botão esquerdo ou direito do mouse como a tecla de anulação especificando o membro **fAbortLeftMouse** ou **fAbortRightMouse.** Depois de definir esses membros, envie a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (ou a [**macro capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) O valor padrão de **vKeyAbort é** ESCAPE da VK. \_ Você deve chamar a [função RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) antes de especificar um controle de teclas que pode anular uma sessão de captura. Os valores padrão **de fAbortLeftMouse e** **fAbortRightMouse** são **TRUE.**

 

 