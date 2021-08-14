---
title: Recuperando alterações
description: Depois que um cliente tiver se registrado para notificação de determinadas alterações e uma ou mais dessas alterações ocorrerem, o cliente receberá uma notificação do gerenciador de tabelas de roteamento.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea0de478a1f46e2281b18644026c2d8db44d113679f4f4f9bd5b18a1123e9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788166"
---
# <a name="retrieving-changes"></a>Recuperando alterações

Depois que um cliente tiver se registrado para notificação de determinadas alterações e uma ou mais dessas alterações ocorrerem, o cliente receberá uma notificação do gerenciador de tabelas de roteamento. O gerenciador de tabela de roteamento usa o retorno de chamada DE RETORNO DE [**\_ \_ CHAMADA**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) DE EVENTO RTM fornecido em uma chamada anterior para [**RtmRegisterEntity.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) O gerenciador de tabela de roteamento indica que ocorreu um evento RTM \_ CHANGE \_ NOTIFICATION.

Para o código de exemplo que mostra como usar essas funções, [consulte Usar o retorno de chamada de notificação de evento](use-the-event-notification-callback.md).

 

 




