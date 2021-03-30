---
title: Chaves que terminam captura
description: Chaves que terminam captura
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- Estrutura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a91d6ee7d07ed36c11cce7e888c9a9710f403cf9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640553"
---
# <a name="keys-ending-capture"></a>Chaves que terminam captura

Você pode permitir que o usuário anule uma sessão de captura pressionando uma tecla ou combinação de teclas do teclado ou pressionando o botão direito ou esquerdo do mouse. Se o usuário anular uma sessão de captura em tempo real, o conteúdo do arquivo de captura será Descartado. Se o usuário anular uma sessão de captura de quadro de etapa, o conteúdo do arquivo de captura até o ponto de anulação da captura será salvo.

Você pode recuperar as configurações para anular uma sessão de captura usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). A configuração de pressionamento de teclas atual é armazenada no membro **vKeyAbort** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) ; as configurações atuais do mouse são armazenadas nos membros **fAbortLeftMouse** e **fAbortRightMouse** . Você pode definir uma nova combinação de teclas ou teclas especificando a combinação de código-chave ou KeyCode (como em uma combinação de teclas CTRL ou SHIFT) como o valor de **vKeyAbort**, ou definir o botão esquerdo ou direito do mouse como a chave Abort, especificando o membro **fAbortLeftMouse** ou **fAbortRightMouse** . Depois de definir esses membros, envie a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). O valor padrão de **vKeyAbort** é VK \_ escape. Você deve chamar a função [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) antes de especificar um pressionamento de tecla que pode anular uma sessão de captura. Os valores padrão de **fAbortLeftMouse** e **fAbortRightMouse** são **true**.

 

 