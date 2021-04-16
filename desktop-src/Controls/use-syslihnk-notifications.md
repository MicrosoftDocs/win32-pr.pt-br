---
title: Como usar notificações do SysLink
description: Há duas mensagens de notificação associadas ao controle SysLink \ 8212; uma para o mouse (NM \_ Click (Syslink)) e outra para o teclado (nm \_ Return).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "105753780"
---
# <a name="how-to-use-syslink-notifications"></a>Como usar notificações do SysLink

Há duas mensagens de notificação associadas ao controle SysLink — uma para o mouse ([nm \_ Click (Syslink)](nm-click-syslink.md)) e outra para o teclado ([nm \_ Return](nm-return.md)).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="use-syslink-notifications"></a>Usar notificações do SysLink

O código de exemplo a seguir mostra como processar as notificações SysLink que são geradas quando o usuário clica em qualquer um dos dois links no [exemplo anterior](create-syslink-controls.md). Quando o usuário clica na URL da Internet, a página da Web associada é aberta no navegador padrão. Quando o usuário clica no hiperlink definido pelo aplicativo, uma caixa de mensagem é exibida.


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles SysLink](using-syslink-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




