---
title: Como usar códigos de notificação de controle de edição rich
description: A janela pai de um controle de edição rica pode processar códigos de notificação para monitorar eventos que afetam o controle. Controles de edição rich suportam todos os códigos de notificação usados com controles de edição, bem como vários outros.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6bc730c648e76137db480f14895d540a9142ae6a80ffa58533e38ef513653ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828628"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>Como usar códigos de notificação de controle de edição rich

A janela pai de um controle de edição rica pode processar códigos de notificação para monitorar eventos que afetam o controle. Controles de edição rich suportam todos os códigos de notificação usados com controles de edição, bem como vários outros.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="use-a-rich-edit-control-notification-code"></a>Usar um código de notificação de controle de edição rich

Você pode determinar quais códigos de notificação um controle de edição rich envia sua janela pai definindo sua máscara de evento. Para definir a máscara de evento para um controle de edição rich, use a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md) Você pode recuperar a máscara de evento atual para um controle de edição rich usando a [**mensagem EM \_ GETEVENTMASK.**](em-geteventmask.md) Para ver uma lista de sinalizadores de máscara de evento, consulte [Sinalizadores de](rich-edit-control-event-mask-flags.md)Máscara de Evento de Controle de Edição Rich .

A janela pai de um controle de edição rica pode filtrar todas as entradas do teclado e do mouse para o controle processando o código de notificação [ \_ EN MSGFILTER.](en-msgfilter.md) A janela pai pode impedir que a mensagem do teclado ou mouse seja processada ou pode alterar a mensagem modificando a estrutura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) especificada.

Um aplicativo pode processar o [código de notificação EN \_ PROTECTED](en-protected.md) para detectar quando o usuário tenta modificar o texto protegido. Para marcar um intervalo de texto como protegido, você pode definir o efeito de caractere protegido.

Você pode permitir que o usuário solte arquivos em um controle de edição avançado habilitando o código [de notificação EN \_ DROPFILES.](en-dropfiles.md) A estrutura [**ENDROPFILES especificada**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) contém informações sobre os arquivos que estão sendo descartados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição rich](using-rich-edit-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




