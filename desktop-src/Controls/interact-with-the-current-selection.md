---
title: Como interagir com a seleção atual
description: O usuário pode selecionar o texto em um controle de edição rico usando o mouse ou o teclado.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6e60ef0ba4aa9a8034256c8c272950f4983d16c0195737065563b378e14202
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434636"
---
# <a name="how-to-interact-with-the-current-selection"></a>Como interagir com a seleção atual

O usuário pode selecionar o texto em um controle de edição rico usando o mouse ou o teclado. A *seleção atual* é o intervalo de caracteres selecionados ou a posição do ponto de inserção se nenhum caractere for selecionado. Um aplicativo pode obter informações sobre a seleção atual, defini-la, determinar quando ele muda e mostrar ou ocultar o realçando da seleção.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="interact-with-the-current-selection"></a>Interagir com a seleção atual

Para determinar a seleção atual em um controle de edição rico, use a [**mensagem EM \_ EXGETSEL.**](em-exgetsel.md) Para definir a seleção atual, use a [**mensagem EM \_ EXSETSEL.**](em-exsetsel.md) A [**estrutura CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) é usada com as duas mensagens e especifica um intervalo de caracteres. Para recuperar informações sobre o conteúdo da seleção atual, você pode usar a [**mensagem EM \_ SELECTIONTYPE.**](em-selectiontype.md)

Um aplicativo pode detectar quando a seleção atual muda processando o código [de notificação EN \_ SELCHANGE.](en-selchange.md) O código de notificação especifica uma [**estrutura SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que contém informações sobre a nova seleção. Um controle de edição rich envia esse código de notificação somente se você habilita-o usando a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md)

Por padrão, um controle de edição rich mostra e oculta o realçamento da seleção quando ele obtém e perde o foco. Você pode mostrar ou ocultar o realçamento da seleção a qualquer momento usando a [**mensagem EM \_ HIDESELECTION.**](em-hideselection.md) Por exemplo, um aplicativo pode fornecer uma caixa de diálogo Pesquisar para encontrar texto em um controle de edição rico. O aplicativo pode selecionar texto correspondente sem fechar a caixa de diálogo; nesse caso, ele deve usar a mensagem **EM \_ HIDESELECTION** para realce da seleção.

Assim como acontece com controles de edição, você pode especificar o estilo de janela [**ES \_ NOHIDESEL**](edit-control-styles.md) para impedir que um controle de edição rico oculta o realce de seleção quando ele perde o foco.

Como alternativa ao uso das mensagens [**EM \_ EXGETSEL**](em-exgetsel.md) e [**EM \_ EXSETSEL,**](em-exsetsel.md) você pode recuperar e definir a seleção atual usando as mensagens de controle de edição [**EM \_ GETSEL**](em-getsel.md) e [**EM \_ SETSEL.**](em-setsel.md) A **mensagem EM \_ GETSEL** empacota dois índices de caracteres de 16 bits em seu valor de retorno de 32 bits e, portanto, funciona apenas para seleções que se enquadram inteiramente nos primeiros 64K. No entanto, um controle de edição rico nunca conterá mais de 32 mil caracteres de texto, a menos que você estenda esse limite usando a mensagem [**EM \_ LIMITTEXT**](em-limittext.md) [**ou EM \_ EXLIMITTEXT.**](em-exlimittext.md) Para seleções que se estendem além dos primeiros 64 KB de texto, a **mensagem EM \_ GETSEL** retorna –1. Nesse caso, você ainda pode usar os valores retornados em *wParam* e *lParam* para encontrar os caracteres inicial e final da seleção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição rich](using-rich-edit-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




