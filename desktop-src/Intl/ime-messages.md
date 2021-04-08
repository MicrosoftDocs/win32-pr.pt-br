---
description: O sistema operacional envia mensagens de janela do IME para o procedimento de janela de um aplicativo quando ocorrem determinados eventos que afetam as janelas do IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Mensagens do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010562"
---
# <a name="ime-messages"></a>Mensagens do IME

O sistema operacional envia mensagens de janela do IME para o procedimento de janela de um aplicativo quando ocorrem determinados eventos que afetam as janelas do IME. Por exemplo, o sistema operacional envia a [**mensagem \_ \_ SetContext do WM IME**](wm-ime-setcontext.md) para o aplicativo quando uma janela é ativada. Os aplicativos sem reconhecimento de IME passam essas mensagens para a função [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , que as envia para a janela do IME padrão correspondente. Os aplicativos que reconhecem o IME processam essas mensagens ou as encaminham para suas janelas do IME.

Seu aplicativo pode direcionar uma janela IME para executar um comando, por exemplo, alterar a posição de uma janela de composição usando a mensagem [**de \_ \_ controle IME do WM**](wm-ime-control.md) . O IME notifica o aplicativo sobre as alterações na cadeia de caracteres de composição usando a mensagem de [**\_ \_ composição IME do WM**](wm-ime-composition.md) e sobre as alterações gerais no status das janelas do IME enviando a mensagem de [**notificação do WM \_ \_ IME**](wm-ime-notify.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
