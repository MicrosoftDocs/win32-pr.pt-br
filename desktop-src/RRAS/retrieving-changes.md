---
title: Recuperando alterações
description: Depois que um cliente tiver se registrado para notificação de determinadas alterações e uma ou mais dessas alterações ocorrerem, o cliente receberá uma notificação do Gerenciador de tabelas de roteamento.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498654"
---
# <a name="retrieving-changes"></a>Recuperando alterações

Depois que um cliente tiver se registrado para notificação de determinadas alterações e uma ou mais dessas alterações ocorrerem, o cliente receberá uma notificação do Gerenciador de tabelas de roteamento. O Gerenciador de tabela de roteamento usa o retorno de chamada de retorno de chamada de [**\_ evento \_ RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) que foi fornecido em uma chamada anterior para [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity). O Gerenciador de tabela de roteamento indica que \_ ocorreu um evento de notificação de alteração RTM \_ .

Para obter um exemplo de código que mostra como usar essas funções, consulte [usar o retorno de chamada de notificação de evento](use-the-event-notification-callback.md).

 

 




