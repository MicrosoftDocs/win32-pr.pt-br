---
title: Mensagens de controle
description: esta seção contém informações sobre como Windows mensagens são usadas para se comunicar com controles.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed60ebb66341332b6248b8427045abc5b62a2311427d56e46b25fe93b3d899ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921096"
---
# <a name="control-messages"></a>Mensagens de controle

esta seção contém informações sobre como Windows mensagens são usadas para se comunicar com controles.

Os tópicos a seguir são discutidos.

-   [Mensagens para controles comuns](#messages-to-common-controls)
-   [Notificações de controles](#notifications-from-controls)
-   [Tópicos relacionados](#related-topics)

## <a name="messages-to-common-controls"></a>Mensagens para controles comuns

Como os controles comuns são janelas, um aplicativo pode se comunicar com eles usando mensagens comuns do Microsoft Win32, como [**WM \_ GetFont**](/windows/desktop/winmsg/wm-getfont) ou [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext). Além disso, a classe Window de cada controle comum dá suporte a um conjunto de mensagens específicas de controle. Normalmente, um aplicativo usa [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) para passar mensagens para o controle (geralmente recebendo informações no valor de retorno).

Alguns controles comuns também têm um conjunto de macros que um aplicativo pode usar em vez de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Normalmente, as macros são mais fáceis de usar do que as funções. O código de exemplo a seguir recupera o texto do item de exibição de árvore selecionado, primeiro usando as mensagens brutas e segundo usando as macros equivalentes. Suponha que *HWND* é o identificador da janela de controle.


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



quando uma alteração é feita nas configurações de cores do sistema, Windows envia uma mensagem do [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) para todas as janelas de nível superior. A janela de nível superior deve encaminhar a mensagem do **WM \_ SYSCOLORCHANGE** para seus controles comuns; caso contrário, os controles não serão notificados sobre a alteração de cor. O encaminhamento da mensagem garante que as cores usadas por seus controles comuns sejam consistentes com as usadas por outros objetos da interface do usuário. Por exemplo, um controle Toolbar usa a cor "3D Objects" para desenhar seus botões. Se o usuário alterar a cor do objeto 3-D, mas a mensagem do **WM \_ SYSCOLORCHANGE** não for encaminhada para a barra de ferramentas, os botões da barra de ferramentas permanecerão na cor original (ou até mesmo mudarão para uma combinação de cores novas e antigas), enquanto a cor dos outros botões no sistema é alterada.

## <a name="notifications-from-controls"></a>Notificações de controles

Os controles são janelas filhas que enviam mensagens de notificação para a janela pai quando eventos, geralmente disparados pela entrada do usuário, ocorrem no controle. O aplicativo depende dessas mensagens de notificação para determinar a ação que o usuário deseja executar. Exceto para trackbars, que usam as mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) para notificar o pai das alterações, os controles comuns enviam notificações como o [**\_ comando do WM**](/windows/desktop/menurc/wm-command) ou mensagens de [**\_ notificação do WM**](wm-notify.md) , conforme especificado no tópico de referência para a notificação. Normalmente, as notificações mais antigas (aquelas que estavam na API há muito tempo) usam o **\_ comando do WM**.

O parâmetro *lParam* do [**WM \_ Notify**](wm-notify.md) é o endereço de uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) ou o endereço de uma estrutura maior que inclui **NMHDR** como seu primeiro membro. A estrutura contém o código de notificação e identifica o controle comum que enviou a mensagem de notificação. O significado dos membros da estrutura restantes, se houver, varia dependendo do código de notificação.

Cada tipo de controle comum tem um conjunto correspondente de códigos de notificação. A biblioteca de controle comum também fornece códigos de notificação que podem ser enviados por mais de um tipo de controle comum. Consulte a documentação do controle de interesse para determinar quais códigos de notificação serão enviados e qual será o formato adotado.

Por exemplo, código que mostra como lidar com mensagens de [**\_ notificação do WM**](wm-notify.md) , consulte o tópico de referência para essa mensagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle geral](common-control-reference.md)
</dt> </dl>

 

 
