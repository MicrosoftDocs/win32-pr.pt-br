---
title: Mensagens e cadeias de caracteres de comando MCI
description: Mensagens e cadeias de caracteres de comando MCI
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- Cadeias de caracteres de comando MCI, sobre
- Mensagens de comando MCI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823771"
---
# <a name="mci-command-strings-and-messages"></a>Mensagens e cadeias de caracteres de comando MCI

O MCI dá suporte a [cadeias de comando](command-strings.md) e [mensagens de comando](command-messages.md). Você pode usar cadeias de caracteres ou mensagens, ou ambos, em seu aplicativo MCI.

-   A *interface de mensagem de comando* consiste em constantes e estruturas. Use a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar mensagens para um dispositivo MCI.
-   A *interface de cadeia de caracteres de comando* fornece uma versão textual das mensagens de comando. Use a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) para enviar cadeias de caracteres para um dispositivo MCI. Cadeias de caracteres de comando duplicam a funcionalidade das mensagens de comando. O sistema operacional converte as cadeias de caracteres de comando em mensagens de comando antes de enviá-las ao driver MCI para processamento.

As mensagens de comando que recuperam informações fazem isso na forma de estruturas, que são fáceis de interpretar em um aplicativo C. Essas estruturas podem conter informações sobre vários aspectos diferentes de um dispositivo. As cadeias de caracteres de comando que recuperam informações fazem isso na forma de cadeias de caracteres e só podem recuperar uma cadeia de caracteres de cada vez. Seu aplicativo deve analisar ou testar cada cadeia de caracteres para interpretá-la. Você pode achar que as mensagens de comando são mais fáceis de usar do que as cadeias de caracteres de comando em alguns casos, mas as cadeias de caracteres de comando são fáceis de lembrar e implementar. Alguns aplicativos MCI usam cadeias de caracteres de comando quando o valor de retorno não será usado (além de verificar o sucesso) e mensagens de comando ao recuperar informações do dispositivo.

Quando os comandos são discutidos, essa visão geral usa a forma de cadeia de caracteres do comando seguido pelo formulário da mensagem entre parênteses.

 

 