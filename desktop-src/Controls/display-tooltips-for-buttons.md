---
title: Como exibir dicas de ferramentas para botões
description: Quando você especifica o \_ estilo de dicas de ferramenta TBSTYLE, a barra de ferramentas cria e gerencia um controle ToolTip. O controle ToolTip é ocultado e aparece somente quando os usuários movem o ponteiro sobre um botão da barra de ferramentas e deixam-o lá por aproximadamente um segundo.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103823613"
---
# <a name="how-to-display-tooltips-for-buttons"></a>Como exibir dicas de ferramentas para botões

Quando você especifica o estilo de [**\_ dicas de ferramenta TBSTYLE**](toolbar-control-and-button-styles.md) , a barra de ferramentas cria e gerencia um controle ToolTip. O controle ToolTip é ocultado e aparece somente quando os usuários movem o ponteiro sobre um botão da barra de ferramentas e deixam-o lá por aproximadamente um segundo.

Seu aplicativo pode fornecer texto ao controle ToolTip em qualquer uma das seguintes maneiras:

-   Defina o texto da dica de ferramenta como o membro **isastring** da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) para cada botão. Você também deve enviar uma [**mensagem \_ SETMAXTEXTROWS TB**](tb-setmaxtextrows.md) e definir o máximo de linhas de texto como 0, para que o texto não apareça como o rótulo do botão, e não como uma dica de ferramenta.
-   Crie a barra de ferramentas com o estilo de [**\_ lista TBSTYLE**](toolbar-control-and-button-styles.md) e defina o estilo estendido [**TBSTYLE \_ ex \_ MIXEDBUTTONS**](toolbar-extended-styles.md) . Os rótulos são mostrados apenas para botões que têm o estilo de [**\_ texto BTNS**](toolbar-control-and-button-styles.md) . Para botões que não têm esse estilo, é mostrada uma dica de ferramenta que contém o texto do botão.
-   Responda ao código de notificação [TTN \_ GETDISPINFO](ttn-getdispinfo.md) .
-   Responda ao código de notificação [tbn \_ GETINFOTIP](tbn-getinfotip.md) .

Um aplicativo que precisa enviar mensagens diretamente para o controle ToolTip pode recuperar o identificador para o controle usando a mensagem [**TB \_ GetToolTips**](tb-gettooltips.md) . Um aplicativo pode substituir o controle ToolTip de uma barra de ferramentas por outro controle ToolTip usando a mensagem [**TB \_ SetToolTips**](tb-settooltips.md) .

A maneira mais flexível de fornecer texto de dica de ferramenta é responder ao código de notificação [TTN \_ GETDISPINFO](ttn-getdispinfo.md) ou [tbn \_ GETINFOTIP](tbn-getinfotip.md) enviado pelo controle Toolbar para seu pai na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . Para [TTN \_ GETDISPINFO](ttn-getdispinfo.md), o parâmetro *lParam* inclui um ponteiro para uma estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (também definida como **LPTOOLTIPTEXT**) que especifica o identificador de comando do botão para o qual o texto de ajuda é necessário. Esse identificador está no membro **NMTTDISPINFO. HDR. idFrom** . Um aplicativo pode copiar o texto de ajuda para a estrutura, especificar o endereço de uma cadeia de caracteres que contém o texto da ajuda ou especificar o identificador de instância e o manipulador de recursos de um recurso de cadeia de caracteres.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="display-a-tooltip-for-a-button"></a>Exibir uma dica de ferramenta para um botão

O código de exemplo a seguir manipula o código de notificação da dica de ferramenta [TTN \_ GETDISPINFO](ttn-getdispinfo.md) fornecendo texto de identificadores de recurso.


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles da barra de ferramentas](using-toolbar-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




