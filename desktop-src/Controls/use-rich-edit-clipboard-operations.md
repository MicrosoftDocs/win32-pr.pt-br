---
title: Como usar operações de edição de área de transferência avançadas
description: Um aplicativo pode colar o conteúdo da área de transferência em um controle de edição rico usando o melhor formato de área de transferência disponível ou um formato de área de transferência específico.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917726"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>Como usar operações de edição de área de transferência avançadas

Um aplicativo pode colar o conteúdo da área de transferência em um controle de edição rico usando o melhor formato de área de transferência disponível ou um formato de área de transferência específico. Você também pode determinar se um controle de edição rico é capaz de colar um formato de área de transferência.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="use-a-rich-edit-clipboard-operation"></a>Usar uma operação de edição rica da área de transferência

Assim como com um controle de edição, você pode copiar ou recortar o conteúdo da seleção atual usando a mensagem do [**WM \_ Copy**](/windows/desktop/dataxchg/wm-copy) ou o [**\_ recortar do WM**](/windows/desktop/dataxchg/wm-cut) . Da mesma forma, você pode colar o conteúdo da área de transferência em um controle de edição rico usando a mensagem de [**\_ colagem do WM**](/windows/desktop/dataxchg/wm-paste) . O controle cola o primeiro formato disponível que ele reconhece, o que presumivelmente é o formato mais descritivo.

Para colar um formato de área de transferência específico, você pode usar a mensagem em [**\_ PASTESPECIAL**](em-pastespecial.md) . Essa mensagem é útil para aplicativos com um comando **colar especial** que permite ao usuário selecionar o formato da área de transferência. Você pode usar a mensagem em [**\_ CanPaste**](em-canpaste.md) para determinar se um determinado formato é reconhecido pelo controle.

Você também pode usar a mensagem em [**\_ CanPaste**](em-canpaste.md) para determinar se qualquer formato de área de transferência disponível é reconhecido por um controle de edição rico. Essa mensagem é útil ao processar a [**mensagem \_ INITMENUPOPUP do WM**](/windows/desktop/menurc/wm-initmenupopup) . Um aplicativo pode habilitar ou cinza o comando **Paste** , dependendo se o controle pode colar qualquer formato disponível.

Os controles de edição avançados registram dois formatos de área de transferência:

-   Formato de Rich Text
-   Formato de Rich Text sem objetos
-   Texto e objetos RichEdit

Um aplicativo pode registrar esses formatos usando a função [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) , especificando os valores do CF \_ RTF, CF \_ RTFNOOBJS e CF \_ RETEXTOBJ.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 