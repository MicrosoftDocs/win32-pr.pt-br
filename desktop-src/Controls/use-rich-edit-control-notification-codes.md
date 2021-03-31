---
title: Como usar códigos de notificação de controle de edição avançados
description: Uma janela pai do controle de edição rico pode processar códigos de notificação para monitorar eventos que afetam o controle. Os controles de edição avançados dão suporte a todos os códigos de notificação usados com controles de edição, bem como a vários outros.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103917089"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>Como usar códigos de notificação de controle de edição avançados

Uma janela pai do controle de edição rico pode processar códigos de notificação para monitorar eventos que afetam o controle. Os controles de edição avançados dão suporte a todos os códigos de notificação usados com controles de edição, bem como a vários outros.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="use-a-rich-edit-control-notification-code"></a>Usar um código de notificação de controle de edição rico

Você pode determinar quais códigos de notificação um controle de edição avançado envia sua janela pai definindo sua máscara de evento. Para definir a máscara de evento para um controle de edição rico, use a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) . Você pode recuperar a máscara de evento atual para um controle de edição rico usando a mensagem em [**\_ GETEVENTMASK**](em-geteventmask.md) . Para obter uma lista de sinalizadores de máscara de evento, consulte [sinalizadores de máscara de evento de controle de edição avançada](rich-edit-control-event-mask-flags.md).

Uma janela pai do controle de edição rico pode filtrar todas as entradas de teclado e mouse para o controle processando o código de notificação [en \_ MSGFILTER](en-msgfilter.md) . A janela pai pode impedir que a mensagem de teclado ou mouse seja processada ou pode alterar a mensagem modificando a estrutura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) especificada.

Um aplicativo pode processar o código de notificação [ \_ protegido do en](en-protected.md) para detectar quando o usuário tenta modificar o texto protegido. Para marcar um intervalo de texto como protegido, você pode definir o efeito de caractere protegido.

Você pode habilitar o usuário a soltar arquivos em um controle de edição rico processando o código de notificação [en \_ DropFiles](en-dropfiles.md) . A estrutura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) especificada contém informações sobre os arquivos que estão sendo removidos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




