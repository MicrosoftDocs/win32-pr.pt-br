---
title: O sinalizador de espera
description: O sinalizador de espera
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- Sinalizador de MCI_WAIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006176"
---
# <a name="the-wait-flag"></a>O sinalizador de espera

Os comandos MCI geralmente retornam ao usuário imediatamente, mesmo que demore alguns minutos para concluir a ação iniciada pelo comando. Você pode usar o sinalizador "Wait" ( \_ espera de MCI) para direcionar o dispositivo para aguardar até que a ação solicitada seja concluída antes de retornar o controle para o aplicativo.

Por exemplo, o comando de [**reprodução**](play.md) a seguir não retornará o controle para o aplicativo até que a reprodução seja concluída:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> O usuário pode cancelar uma operação de espera pressionando uma tecla Break. Por padrão, essa chave é CTRL + BREAK. Os aplicativos podem redefinir essa chave usando o comando [**Break**](break.md) ([**MCI \_ Break**](mci-break.md)). (**A \_ interrupção do MCI** usa a estrutura de [**parâmetros de \_ interrupção \_ do MCI**](mci-break-parms.md) .) Quando uma operação de espera é cancelada, o MCI tenta retornar o controle ao aplicativo sem interromper o comando associado ao sinalizador "Wait".

 

 

 




