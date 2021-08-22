---
title: Como exibir dicas de ferramenta para botões
description: Quando você especifica o estilo TBSTYLE \_ TOOLTIPS, a barra de ferramentas cria e gerencia um controle de dica de ferramenta. O controle de dica de ferramenta fica oculto e aparece somente quando os usuários movem o ponteiro sobre um botão de barra de ferramentas e o deixam lá por aproximadamente um segundo.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f169c6cc9324c98ed085b38f14802fcaa3c5cfbc8bd7ee9aa29af62ef41a6adc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319996"
---
# <a name="how-to-display-tooltips-for-buttons"></a>Como exibir dicas de ferramenta para botões

Quando você especifica o [**estilo TBSTYLE \_ TOOLTIPS,**](toolbar-control-and-button-styles.md) a barra de ferramentas cria e gerencia um controle de dica de ferramenta. O controle de dica de ferramenta fica oculto e aparece somente quando os usuários movem o ponteiro sobre um botão de barra de ferramentas e o deixam lá por aproximadamente um segundo.

Seu aplicativo pode fornecer texto para o controle de dica de ferramenta de qualquer uma das seguintes maneiras:

-   De definir o texto da dica de ferramenta como o **membro iString** da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) para cada botão. Você também deve enviar uma mensagem [**TB \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md) e definir o máximo de linhas de texto como 0, para que o texto não apareça como o rótulo do botão em vez de como uma dica de ferramenta.
-   Crie a barra de ferramentas com o [**estilo TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) e, em seguida, de definir o estilo estendido [**TBSTYLE \_ EX \_ MIXEDBUTTONS.**](toolbar-extended-styles.md) Os rótulos são mostrados somente para botões que têm o estilo [**BTNS \_ SHOWTEXT.**](toolbar-control-and-button-styles.md) Para botões que não têm esse estilo, é mostrada uma dica de ferramenta que contém o texto do botão.
-   Responda ao código [de notificação \_ GETDISPINFO do TTN.](ttn-getdispinfo.md)
-   Responda ao código [de notificação \_ GETINFOTIP do TBN.](tbn-getinfotip.md)

Um aplicativo que precisa enviar mensagens diretamente para o controle de dica de ferramenta pode recuperar o controle usando a [**mensagem \_ GETTOOLTIPS**](tb-gettooltips.md) do TB. Um aplicativo pode substituir o controle de dica de ferramenta de uma barra de ferramentas por outro controle de dica de ferramenta usando a [**mensagem TB \_ SETTOOLTIPS.**](tb-settooltips.md)

A maneira mais flexível de fornecer texto de dica de ferramenta é responder ao código de notificação [ \_ TTN GETDISPINFO](ttn-getdispinfo.md) ou [TBN \_ GETINFOTIP](tbn-getinfotip.md) enviado pelo controle da barra de ferramentas para seu pai na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) Para [TTN \_ GETDISPINFO](ttn-getdispinfo.md), o parâmetro *lParam* inclui um ponteiro para uma estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (também definida como **LPTOOLTIPTEXT**) que especifica o identificador de comando do botão para o qual o texto da Ajuda é necessário. Esse identificador está no **membro NMTTDISPINFO.hdr.idFrom.** Um aplicativo pode copiar o texto da Ajuda para a estrutura, especificar o endereço de uma cadeia de caracteres que contém o texto da Ajuda ou especificar o identificador de instância e o identificador de recurso de um recurso de cadeia de caracteres.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="display-a-tooltip-for-a-button"></a>Exibir uma dica de ferramenta para um botão

O código de exemplo a seguir trata o código de notificação da dica de ferramenta [ \_ TTN GETDISPINFO](ttn-getdispinfo.md) fornecendo texto de identificadores de recurso.


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

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




