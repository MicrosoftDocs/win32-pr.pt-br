---
title: Como redimensionar automaticamente os controles de edição avançados
description: Um aplicativo pode redimensionar um controle de edição rico conforme necessário para que seja sempre o mesmo tamanho que seu conteúdo.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008456"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>Como redimensionar automaticamente os controles de edição avançados

Um aplicativo pode redimensionar um controle de edição rico conforme necessário para que seja sempre o mesmo tamanho que seu conteúdo. Um controle de edição rico dá suporte a essa chamada de funcionalidade *inferior* , enviando sua janela pai um código de notificação [en \_ REQUESTRESIZE](en-requestresize.md) sempre que o tamanho do conteúdo do controle é alterado.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="automatically-resize-a-rich-edit-control"></a>Redimensionar automaticamente um controle de edição rico

Ao processar o código de notificação [en \_ REQUESTRESIZE](en-requestresize.md) , um aplicativo deve redimensionar o controle para as dimensões na estrutura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) especificada. Um aplicativo também pode mover qualquer informação que esteja perto do controle para acomodar a alteração do controle na altura. Para redimensionar o controle, você pode usar a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .

Você pode forçar um controle de edição mais baixo para enviar um código de notificação [en \_ REQUESTRESIZE](en-requestresize.md) usando a mensagem em [**\_ REQUESTRESIZE**](em-requestresize.md) . Essa mensagem pode ser útil ao processar a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) .

## <a name="remarks"></a>Comentários

Para receber códigos de notificação do [en \_ REQUESTRESIZE](en-requestresize.md) , você deve habilitar a notificação usando a mensagem em [ \_ SETEVENTMASK](em-seteventmask.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 