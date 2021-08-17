---
title: O sinalizador Wait
description: O sinalizador Wait
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT sinalizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311e1a55e756cfc3c1038f6ab3ccb4b708bb066dde962afff31006dcf39b7c4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801430"
---
# <a name="the-wait-flag"></a>O sinalizador Wait

Os comandos MCI geralmente retornam ao usuário imediatamente, mesmo se levar vários minutos para concluir a ação iniciada pelo comando. Você pode usar o sinalizador "wait" (MCI WAIT) para direcionar o dispositivo a aguardar até que a ação solicitada seja concluída antes de retornar o controle \_ para o aplicativo.

Por exemplo, o comando [**play a**](play.md) seguir não retornará o controle para o aplicativo até que a reprodução seja concluída:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> O usuário pode cancelar uma operação de espera pressionando uma tecla de quebra. Por padrão, essa chave é CTRL+BREAK. Os aplicativos podem redefinir essa chave usando o [**comando break**](break.md) ([**MCI \_ BREAK**](mci-break.md)). (**A MCI \_ BREAK** usa a estrutura [**\_ MCI BREAK \_ PARMS.)**](mci-break-parms.md) Quando uma operação de espera é cancelada, a MCI tenta retornar o controle para o aplicativo sem interromper o comando associado ao sinalizador "wait".

 

 

 




