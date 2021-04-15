---
title: Mensagens de comando
description: Mensagens de comando
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Mensagens de comando MCI, sobre
- Mensagens de comando MCI, sintaxe
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499020"
---
# <a name="command-messages"></a>Mensagens de comando

A interface de mensagem de comando é projetada para ser usada por aplicativos que exigem uma interface de linguagem C para controlar dispositivos multimídia. Ele usa um paradigma de passagem de mensagens para se comunicar com dispositivos MCI. Você pode enviar um comando usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .

A função **mciSendCommand** retornará zero se for bem-sucedida. Se a função falhar, a palavra de ordem inferior do valor de retorno conterá um código de erro. Você pode passar esse código de erro para a função [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obter uma descrição de texto do erro.

## <a name="syntax-of-command-messages"></a>Sintaxe das mensagens de comando

As mensagens de comando MCI consistem nos seguintes elementos:

-   Um valor de mensagem constante
-   Uma estrutura que contém parâmetros para o comando
-   Um conjunto de sinalizadores que especificam opções para o comando e validação de campos no bloco de parâmetro

O exemplo a seguir usa a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar o comando [**MCI \_ Play**](mci-play.md) para o dispositivo identificado por um identificador de dispositivo.


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



O identificador de dispositivo fornecido no primeiro parâmetro é recuperado quando o dispositivo é aberto usando o comando [**MCI \_ Open**](mci-open.md) . O último parâmetro é o endereço de uma estrutura de [**\_ \_ parâmetros de reprodução MCI**](mci-play-parms.md) , que pode conter informações sobre onde começar e terminar a reprodução. Muitas mensagens de comando MCI usam uma estrutura para conter parâmetros desse tipo. O primeiro membro de cada uma dessas estruturas identifica a janela que recebe uma mensagem [**mm \_ MCINOTIFY**](mm-mcinotify.md) quando a operação é concluída.

 

 