---
title: Mensagens de comando
description: Mensagens de comando
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Mensagens de comando MCI, sobre
- Mensagens de comando MCI, sintaxe
- Função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428c89f610f204cfeb75a6c23309c8f3f9846d3136ffac4dbcf0959c5bc4add3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807935"
---
# <a name="command-messages"></a>Mensagens de comando

A interface de mensagem de comando foi projetada para ser usada por aplicativos que exigem uma interface de linguagem C para controlar dispositivos multimídia. Ele usa um paradigma de passagem de mensagem para se comunicar com dispositivos MCI. Você pode enviar um comando usando a [**função mciSendCommand.**](/previous-versions//dd757160(v=vs.85))

A **função mciSendCommand** retornará zero se for bem-sucedida. Se a função falhar, a palavra de ordem baixa do valor de retorno conterá um código de erro. Você pode passar esse código de erro para a [**função mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obter uma descrição de texto do erro.

## <a name="syntax-of-command-messages"></a>Sintaxe de mensagens de comando

As mensagens de comando MCI consistem nos seguintes elementos:

-   Um valor de mensagem constante
-   Uma estrutura que contém parâmetros para o comando
-   Um conjunto de sinalizadores especificando opções para o comando e validando campos no bloco de parâmetros

O exemplo a seguir usa a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar o comando [**MCI \_ PLAY**](mci-play.md) para o dispositivo identificado por um identificador de dispositivo.


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



O identificador de dispositivo dado no primeiro parâmetro é recuperado quando o dispositivo é aberto usando o [**comando MCI \_ OPEN.**](mci-open.md) O último parâmetro é o endereço de uma estrutura [**MCI \_ PLAY \_ PARMS,**](mci-play-parms.md) que pode conter informações sobre onde começar e encerrar a reprodução. Muitas mensagens de comando MCI usam uma estrutura para conter parâmetros desse tipo. O primeiro membro de cada uma dessas estruturas identifica a janela que recebe uma mensagem [**MM \_ MCINOTIFY**](mm-mcinotify.md) quando a operação é final.

 

 