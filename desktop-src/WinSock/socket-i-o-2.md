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
# <a name="socket-io"></a><span data-ttu-id="4c4d7-103">E/s de soquete</span><span class="sxs-lookup"><span data-stu-id="4c4d7-103">Socket I/O</span></span>

<span data-ttu-id="4c4d7-104">Há três maneiras principais de fazer e/s no Windows Sockets 2:</span><span class="sxs-lookup"><span data-stu-id="4c4d7-104">There are three primary ways of doing I/O in Windows Sockets 2:</span></span>

-   <span data-ttu-id="4c4d7-105">Bloqueando e/s.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-105">Blocking I/O.</span></span>
-   <span data-ttu-id="4c4d7-106">O não bloqueio de e/s junto com a notificação assíncrona de eventos de rede.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-106">Nonblocking I/O along with asynchronous notification of network events.</span></span>
-   <span data-ttu-id="4c4d7-107">E/s sobreposta com indicação de conclusão.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-107">Overlapped I/O with completion indication.</span></span>

<span data-ttu-id="4c4d7-108">Descrevemos cada método nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-108">We describe each method in the following sections.</span></span> <span data-ttu-id="4c4d7-109">O bloqueio de e/s é o comportamento padrão, o modo de não bloqueio pode ser usado em qualquer soquete que é colocado no modo de não bloqueio e e/s sobreposta pode ocorrer somente em soquetes que são criados com o atributo sobreposto.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-109">Blocking I/O is the default behavior, nonblocking mode can be used on any socket that is placed into nonblocking mode, and overlapped I/O can only occur on sockets that are created with the overlapped attribute.</span></span> <span data-ttu-id="4c4d7-110">Também é interessante observar que as duas chamadas para enviar: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e as duas chamadas para receber: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) cada uma implementam todos os três métodos de e/s.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-110">It is also interesting to note that the two calls for sending: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and the two calls for receiving: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) each implement all three methods of I/O.</span></span> <span data-ttu-id="4c4d7-111">Os provedores de serviço determinam como executar a operação de e/s com base em modos de soquete, atributos e valores de parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="4c4d7-111">Service providers determine how to perform the I/O operation based on socket modes, attributes, and the input parameter values.</span></span>

 

 
