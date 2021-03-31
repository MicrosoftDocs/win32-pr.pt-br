---
title: Como interagir com a seleção atual
description: O usuário pode selecionar o texto em um controle de edição rico usando o mouse ou o teclado.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103640344"
---
# <a name="how-to-interact-with-the-current-selection"></a>Como interagir com a seleção atual

O usuário pode selecionar o texto em um controle de edição rico usando o mouse ou o teclado. A *seleção atual* é o intervalo de caracteres selecionados ou a posição do ponto de inserção se nenhum caractere for selecionado. Um aplicativo pode obter informações sobre a seleção atual, defini-la, determinar quando ela é alterada e mostrar ou ocultar o realce de seleção.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="interact-with-the-current-selection"></a>Interagir com a seleção atual

Para determinar a seleção atual em um controle de edição rico, use a mensagem em [**\_ EXGETSEL**](em-exgetsel.md) . Para definir a seleção atual, use a mensagem em [**\_ EXSETSEL**](em-exsetsel.md) . A estrutura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) é usada com as duas mensagens e especifica um intervalo de caracteres. Para recuperar informações sobre o conteúdo da seleção atual, você pode usar a mensagem [**de \_ SelectionType**](em-selectiontype.md) em em.

Um aplicativo pode detectar quando a seleção atual muda processando o código de notificação [en \_ SELCHANGE](en-selchange.md) . O código de notificação especifica uma estrutura [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que contém informações sobre a nova seleção. Um controle de edição rico envia esse código de notificação somente se você habilitá-lo usando a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

Por padrão, um controle rich edit mostra e oculta o realce de seleção quando ele ganha e perde o foco. Você pode mostrar ou ocultar o realce de seleção a qualquer momento usando a mensagem em [**\_ HIDESELECTION**](em-hideselection.md) . Por exemplo, um aplicativo pode fornecer uma caixa de diálogo de pesquisa para localizar texto em um controle de edição rico. O aplicativo pode selecionar texto correspondente sem fechar a caixa de diálogo; nesse caso, ele deve usar a mensagem em **\_ HIDESELECTION** para realçar a seleção.

Assim como com os controles de edição, você pode especificar o estilo de janela [**es \_ NOHIDESEL**](edit-control-styles.md) para impedir que um controle de edição rico oculte o realce de seleção quando ele perder o foco.

Como alternativa ao uso das mensagens [**em \_ EXGETSEL**](em-exgetsel.md) e [**em \_ EXSETSEL**](em-exsetsel.md) , você pode recuperar e definir a seleção atual usando as mensagens de controle de edição em [**\_ GETSEL**](em-getsel.md) e em [**\_ SETSEL**](em-setsel.md) . Os pacotes de mensagens em **\_ GETSEL** são índices de caracteres de 2 16 bits em seu valor de retorno de 32 bits e, portanto, funciona apenas para seleções que se enquadram inteiramente dentro dos primeiros 64K. No entanto, um controle de edição rico nunca conterá mais de 32K caracteres de texto, a menos que você estenda esse limite usando a mensagem em [**\_ LIMITTEXT**](em-limittext.md) ou em [**\_ EXLIMITTEXT**](em-exlimittext.md) . Para seleções que se estendem além do primeiro 64 KB de texto, a mensagem em **\_ GETSEL** retorna – 1. Nesse caso, você ainda pode usar os valores retornados em *wParam* e *lParam* para localizar os caracteres inicial e final da seleção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




