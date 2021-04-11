---
title: Parâmetro de duração da mensagem
description: Normalmente, os aplicativos usam janelas pop-up para exibir brevemente mensagens de notificação importantes para o usuário. Um aplicativo cria a janela, exibe-a para uma duração definida pelo aplicativo e, em seguida, destrói a janela.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366140"
---
# <a name="message-duration-parameter"></a>Parâmetro de duração da mensagem

Normalmente, os aplicativos usam janelas pop-up para exibir brevemente mensagens de notificação importantes para o usuário. Um aplicativo cria a janela, exibe-a para uma duração definida pelo aplicativo e, em seguida, destrói a janela.

Como os usuários com deficiências visuais ou condições cognitivas podem precisar de mais tempo para ler pop-ups de notificação, os aplicativos não devem embutir em código a duração. Em vez disso, um aplicativo deve definir a duração com base no valor do parâmetro de sistema **SPI \_ GETMESSAGEDURATION** . Para recuperar esse parâmetro, use a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .

Os aplicativos de tecnologia assistencial podem definir a duração da mensagem, com base na entrada do usuário, definindo o parâmetro do sistema **SPI \_ SETMESSAGEDURATION** .

 

 