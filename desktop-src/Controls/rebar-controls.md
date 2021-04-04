---
title: Sobre controles de rebar
description: Um controle rebar atua como um contêiner para janelas filhas.
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bc68629db7387f4ba408a769f7d87a64256000
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008471"
---
# <a name="about-rebar-controls"></a>Sobre controles de rebar

Um *controle rebar* atua como um contêiner para janelas filhas. Ele pode conter uma ou mais *bandas*, e cada banda pode ter qualquer combinação de uma barra de garra, um bitmap, um rótulo de texto e uma janela filho. Um aplicativo atribui uma janela filho, normalmente outro controle, a uma faixa de controle rebar. À medida que você reposiciona dinamicamente uma faixa de controle rebar, o controle rebar gerencia o tamanho e a posição da janela filho atribuída a essa banda. Além disso, um aplicativo pode especificar um bitmap em segundo plano para uma banda, e o controle rebar exibirá a janela filho da banda sobre o bitmap.

A captura de tela a seguir mostra um controle rebar que tem duas faixas. Uma delas contém uma barra de ferramentas e a outra contém uma ComboBox. Ambas as faixas têm uma garra que permite que elas sejam movidas e redimensionadas.

![captura de tela da caixa de diálogo mostrando um controle rebar com uma faixa que contém uma barra de ferramentas e uma faixa contendo uma caixa de combinação](images/rb-rebar.png)

> [!Note]  
> O controle rebar é implementado na versão 4,70 e posterior do Comctl32.dll.

 

## <a name="rebar-bands-and-child-windows"></a>Faixas de rebar e janelas filhas

Um aplicativo define as características de uma banda de rebar usando as mensagens [**\_ SETBANDINFO**](rb-setbandinfo.md) [**RB \_ INSERTBAND**](rb-insertband.md) e RB. Essas mensagens aceitam o endereço de uma estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) como o parâmetro *lParam* . Os membros da estrutura **REBARBANDINFO** definem as características de uma determinada faixa. Para definir as características de uma faixa, defina o membro **cbSize** para indicar o tamanho da estrutura, em bytes. Em seguida, defina o membro **fMask** para indicar quais membros da estrutura seu aplicativo está preenchendo.

Para atribuir uma janela filho a uma faixa, inclua o \_ sinalizador filho RBBIM no membro **fMask** da estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) e, em seguida, defina o membro **hWndChild** como a alça da janela filho. Os aplicativos podem definir a largura e a altura mínimas permitidas de uma janela filho nos membros **cxMinChild** e **cyMinChild** .

Quando um controle rebar é destruído, ele destrói todas as janelas filhas atribuídas às faixas dentro dela. Para impedir que o controle destrua as janelas filhas atribuídas a suas bandas, remova as faixas enviando a mensagem [**\_ DELETEBAND RB**](rb-deleteband.md) e, em seguida, use a mensagem [**RB \_ setpai**](rb-setparent.md) para redefinir o pai para outra janela antes de destruir o controle rebar.

## <a name="the-rebar-control-user-interface"></a>A interface do usuário do controle rebar

Todas as bandas de controle rebar podem ser redimensionadas, exceto aquelas que usam o \_ estilo RBBS FIXEDSIZE. Para redimensionar ou alterar a ordem das faixas dentro do controle, clique e arraste a barra de garra de uma faixa. O controle rebar redimensiona automaticamente e reposiciona as janelas filhas atribuídas a suas bandas. Além disso, você pode alternar o tamanho de uma banda clicando no texto da faixa, se houver.

## <a name="the-rebar-controls-image-list"></a>A lista de imagens do controle rebar

Se um aplicativo estiver usando uma lista de imagens com um controle rebar, ele deverá enviar a mensagem [**RB \_ SETBARINFO**](rb-setbarinfo.md) antes de adicionar faixas ao controle. Essa mensagem aceita o endereço de uma estrutura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) como o parâmetro *lParam* . Antes de enviar a mensagem, prepare a estrutura **REBARINFO** definindo o membro **cbSize** como o tamanho da estrutura, em bytes. Em seguida, se o controle rebar exibir imagens nas faixas, defina o membro **fMask** como o \_ sinalizador IMAGELIST RBIM e atribua um identificador de lista de imagens ao membro **himl** . Se o rebar não usar imagens de banda, defina **fMask** como zero.

## <a name="rebar-control-message-forwarding"></a>Encaminhamento de mensagens de controle rebar

Um controle rebar encaminha todas as mensagens da janela de [**\_ notificação do WM**](wm-notify.md) para sua janela pai. Além disso, um controle rebar encaminha todas as mensagens enviadas a ele do Windows atribuídas a suas bandas, como o [**WM \_ CHARTOITEM**](wm-chartoitem.md), o [**\_ comando do WM**](/windows/desktop/menurc/wm-command)e outros.

 

 