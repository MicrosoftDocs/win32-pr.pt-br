---
title: Comunicando-se com dispositivos MCI
description: Comunicando-se com dispositivos MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- Macro MCIWndSendString
- função mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105752627"
---
# <a name="communicating-with-mci-devices"></a>Comunicando-se com dispositivos MCI

O driver de cada dispositivo MCI mantém uma lista de suas configurações e recursos atuais, de modo que ele pode emitir uma resposta precisa quando é consultado para obter informações.

Quando você quiser se comunicar com um dispositivo MCI, poderá usar macros e funções do MCIWnd. Muitos dos comandos e consultas MCI mais comuns são definidos como macros. No entanto, se a tarefa que você deseja executar não estiver disponível como uma função ou macro, você poderá enviar comandos MCI diretamente para o driver de dispositivo usando a macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) ou o formulário de mensagem ou a forma de cadeia de caracteres dos comandos MCI. O uso da macro **MCIWndSendString** é equivalente ao uso da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) da seguinte maneira:


```C++
mciSendString(sz, Null, 0, Null) 
```



Os parâmetros de [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) incluem apenas o identificador de janela e a forma de cadeia de caracteres do comando. Para recuperar as informações retornadas por um comando de cadeia de caracteres, use a macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .

Para obter mais informações sobre o MCI, consulte [MCI](mci.md).

> [!Note]  
> Você deve excluir o alias do dispositivo do comando MCI ao usar o **MCIWndSendString**. A biblioteca MCIWnd adiciona esse alias quando envia o comando para o dispositivo MCI.

 

 

 