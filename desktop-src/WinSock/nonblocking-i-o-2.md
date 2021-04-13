---
description: Se um soquete estiver no modo de não bloqueio, qualquer operação de e/s deverá ser concluída imediatamente ou retornar o código de erro WSAEWOULDBLOCK indicando que a operação não pode ser concluída de imediato.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Entrada/saída de não bloqueio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501681"
---
# <a name="nonblocking-inputoutput"></a>Entrada/saída de não bloqueio

Se um soquete estiver no modo de não bloqueio, qualquer operação de e/s deverá ser concluída imediatamente ou retornar o código de erro WSAEWOULDBLOCK indicando que a operação não pode ser concluída de imediato. No último caso, um mecanismo é necessário para descobrir quando é apropriado tentar a operação novamente com a expectativa de que a operação terá sucesso. Um conjunto de eventos de rede foi definido para essa finalidade. Esses eventos podem ser sondados ou aguardados usando [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), ou podem ser registrados para entrega assíncrona chamando [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) ou [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Consulte [notificação de eventos de rede](notification-of-network-events-2.md) para obter mais informações.

 

 
