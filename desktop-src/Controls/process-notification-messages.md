---
title: Como processar mensagens de notificação
description: Uma folha de propriedades envia \_ mensagens de notificação do WM para recuperar informações das páginas e notificar as páginas de ações do usuário.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baf0c58fdbcbe5378dd46e828a2d29a7c91832174c9564660a82c5ab70997a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575476"
---
# <a name="how-to-process-notification-messages"></a>Como processar mensagens de notificação

Uma folha de propriedades envia mensagens de [**\_ notificação do WM**](wm-notify.md) para recuperar informações das páginas e notificar as páginas de ações do usuário.

O parâmetro *lParam* da mensagem é o endereço de uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , que contém o identificador para a caixa de diálogo da folha de propriedades, o identificador para a caixa de diálogo página e um código de notificação. A página deve responder a algumas mensagens de notificação definindo o \_ valor DWL MSGRESULT da página como **true** ou **false**.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="process-notification-messages"></a>Processar mensagens de notificação

O exemplo a seguir é um fragmento de código do procedimento da caixa de diálogo para uma página. Ele mostra como processar o código de notificação da [ \_ ajuda do PSN](psn-help.md) .


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando folhas de propriedades](using-property-sheets.md)
</dt> <dt>

[Windows de demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




