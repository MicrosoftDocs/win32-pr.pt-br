---
title: Como usar operações de área de transferência de edição rica
description: Um aplicativo pode colar o conteúdo da área de transferência em um controle de edição rico usando o melhor formato de área de transferência disponível ou um formato de área de transferência específico.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdeac2e892716880e4e2971d597c13047dc79cebf2c57888e2fa248c6b0c4beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132086"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>Como usar operações de área de transferência de edição rica

Um aplicativo pode colar o conteúdo da área de transferência em um controle de edição rico usando o melhor formato de área de transferência disponível ou um formato de área de transferência específico. Você também pode determinar se um controle de edição rico é capaz de colar um formato de área de transferência.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="use-a-rich-edit-clipboard-operation"></a>Usar uma operação de área de transferência de edição rica

Assim como com um controle de edição, você pode copiar ou recortar o conteúdo da seleção atual usando a [**mensagem WM \_ COPY**](/windows/desktop/dataxchg/wm-copy) ou [**WM \_ CUT.**](/windows/desktop/dataxchg/wm-cut) Da mesma forma, você pode colar o conteúdo da área de transferência em um controle de edição rico usando a [**mensagem WM \_ PASTE.**](/windows/desktop/dataxchg/wm-paste) O controle colará o primeiro formato disponível que reconhece, que, aparentemente, é o formato mais descritivo.

Para colar um formato de área de transferência específico, você pode usar a [**mensagem EM \_ PASTESPECIAL.**](em-pastespecial.md) Essa mensagem é útil para aplicativos com **um comando Colar Especial** que permite que o usuário selecione o formato da área de transferência. Você pode usar a [**mensagem EM \_ CANPASTE**](em-canpaste.md) para determinar se um determinado formato é reconhecido pelo controle .

Você também pode usar a [**mensagem EM \_ CANPASTE**](em-canpaste.md) para determinar se qualquer formato de área de transferência disponível é reconhecido por um controle de edição rico. Essa mensagem é útil ao processar a [**mensagem WM \_ INITMENUPOPUP.**](/windows/desktop/menurc/wm-initmenupopup) Um aplicativo pode habilitar ou cinza **seu comando Colar,** dependendo se o controle pode colar qualquer formato disponível.

Controles de edição rich registram dois formatos de área de transferência:

-   Formato Rich Text
-   Formato de rich text sem objetos
-   RichEdit Text and Objects

Um aplicativo pode registrar esses formatos usando a [**função RegisterClipboardFormat,**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) especificando os valores \_ RTF, CF \_ RTFNOOBJS e CF \_ RETEXTOBJ.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição rich](using-rich-edit-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 