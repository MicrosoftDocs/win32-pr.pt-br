---
description: Usando o bloqueio de e/s, o não bloqueio de e/s com notificação assíncrona de eventos de rede e e/s sobreposta com indicação de conclusão no Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: E/s de soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090355"
---
# <a name="socket-io"></a>E/s de soquete

Há três maneiras principais de fazer e/s no Windows Sockets 2:

-   Bloqueando e/s.
-   O não bloqueio de e/s junto com a notificação assíncrona de eventos de rede.
-   E/s sobreposta com indicação de conclusão.

Descrevemos cada método nas seções a seguir. O bloqueio de e/s é o comportamento padrão, o modo de não bloqueio pode ser usado em qualquer soquete que é colocado no modo de não bloqueio e e/s sobreposta pode ocorrer somente em soquetes que são criados com o atributo sobreposto. Também é interessante observar que as duas chamadas para enviar: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e as duas chamadas para receber: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) cada uma implementam todos os três métodos de e/s. Os provedores de serviço determinam como executar a operação de e/s com base em modos de soquete, atributos e valores de parâmetro de entrada.

 

 
