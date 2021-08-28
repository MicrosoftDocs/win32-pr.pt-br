---
title: Sobre controles de barra de rebar
description: Um controle Rebar atua como um contêiner para janelas filho.
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d34f76ca745f0807b849bd7c42c81944f11e4429fe2dc9670fa318cbd575ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434816"
---
# <a name="about-rebar-controls"></a>Sobre controles de barra de rebar

Um *controle Rebar* atua como um contêiner para janelas filho. Ele pode conter uma ou mais *faixas* e cada banda pode ter qualquer combinação de uma barra de controle, um bitmap, um rótulo de texto e uma janela filho. Um aplicativo atribui uma janela filho , normalmente outro controle, a uma faixa de controle de barra de rebar. Conforme você reposiciona dinamicamente uma faixa de controle de barra de rebar, o controle de barra rebar gerencia o tamanho e a posição da janela filho atribuída a essa banda. Além disso, um aplicativo pode especificar um bitmap em segundo plano para uma banda e o controle de barra de rebar exibirá a janela filho da banda sobre o bitmap.

A captura de tela a seguir mostra um controle de barra de rebar que tem duas faixas. Uma contém uma barra de ferramentas e a outra contém uma caixa de combinação. Ambas as faixas têm um controle que permite que elas sejam movidas e recalizadas.

![captura de tela da caixa de diálogo mostrando um controle de barra de rebar com uma faixa que contém uma barra de ferramentas e uma faixa que contém uma caixa de combinação](images/rb-rebar.png)

> [!Note]  
> O controle rebar é implementado na versão 4.70 e posterior do Comctl32.dll.

 

## <a name="rebar-bands-and-child-windows"></a>Barras de barras e faixas filho Windows

Um aplicativo define as características de uma faixa de barras de rebar usando as mensagens [**RB \_ INSERTBAND**](rb-insertband.md) e [**RB \_ SETBANDINFO.**](rb-setbandinfo.md) Essas mensagens aceitam o endereço de uma [**estrutura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) como o *parâmetro lParam.* Os **membros da estrutura REBARBANDINFO** definem as características de uma determinada banda. Para definir as características de uma banda, de definir o membro **cbsize** para indicar o tamanho da estrutura, em bytes. Em seguida, de **definir o membro fMask** para indicar quais membros da estrutura seu aplicativo está preenchendo.

Para atribuir uma janela filho a uma banda, inclua o sinalizador RBBIM CHILD no membro \_ **fMask** da estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) e, em seguida, de definir o membro **hwndChild** como o alça da janela filho. Os aplicativos podem definir a largura e a altura mínimas de uma janela filho nos **membros cxMinChild** e **cyMinChild.**

Quando um controle de barra de rebar é destruído, ele destrói todas as janelas filho atribuídas às faixas dentro dele. Para impedir que o controle destrói janelas filho atribuídas a suas bandas, remova as faixas enviando a mensagem [**RB \_ DELETEBAND**](rb-deleteband.md) e use a mensagem [**RB \_ SETPARENT**](rb-setparent.md) para redefinir o pai para outra janela antes de destruir o controle de barra novamente.

## <a name="the-rebar-control-user-interface"></a>O controle Rebar Interface do Usuário

Todas as faixas de controle de barra de rebar podem ser resized, exceto aquelas que usam o estilo \_ RBBS FIXEDSIZE. Para reescalar ou alterar a ordem das faixas dentro do controle, clique e arraste a barra de controle de uma banda. O controle rebar reescala e reposiciona automaticamente as janelas filho atribuídas a suas faixas. Além disso, você pode alternar o tamanho de uma banda clicando no texto da banda, se houver algum.

## <a name="the-rebar-controls-image-list"></a>A lista de imagens do controle rebar

Se um aplicativo estiver usando uma lista de imagens com um controle rebar, ele deverá enviar a mensagem [**RB \_ SETBARINFO**](rb-setbarinfo.md) antes de adicionar faixas ao controle. Essa mensagem aceita o endereço de uma estrutura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) como o *parâmetro lParam.* Antes de enviar a mensagem, prepare a **estrutura REBARINFO** definindo o membro **cbSize** para o tamanho da estrutura, em bytes. Em seguida, se o controle rebar exibir imagens nas faixas, defina o membro **fMask** como o sinalizador IMAGELIST RBIM e atribua um alça de lista de imagens ao membro \_ **do himl.** Se a barra de rebar não usar imagens de banda, de definir **fMask** como zero.

## <a name="rebar-control-message-forwarding"></a>Rebar Control Message Forwarding

Um controle de barra de rebar encaminha todas [**as mensagens \_ da**](wm-notify.md) janela WM NOTIFY para sua janela pai. Além disso, um controle de barra rebar encaminha todas as mensagens enviadas a ele de janelas atribuídas a suas bandas, como [**WM \_ CHARTOITEM,**](wm-chartoitem.md) [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command)e outras.

 

 