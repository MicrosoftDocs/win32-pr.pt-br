---
description: WSPEventSelect se comporta exatamente como WSPAsyncSelect, exceto que, em vez de fazer com que uma mensagem de Windows seja enviada na ocorrência de qualquer \_ evento de rede do fd XXX indicado (por exemplo, FD \_ READ, fd \_ WRITE, etc.), um objeto de evento designado é definido.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Sinalização de objeto de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eed237db696298a2f8053fb61cb0009d9d25d7f37497e0a19d58044d27d8dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132616"
---
# <a name="event-object-signaling"></a>Sinalização de objeto de evento

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) se comporta exatamente como [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , exceto que, em vez de fazer com que uma mensagem de Windows seja enviada na ocorrência de qualquer \_ evento de rede do fd XXX indicado (por exemplo, FD \_ READ, fd \_ WRITE, etc.), um objeto de evento designado é definido.

Além disso, o fato de que um \_ evento de rede FD xxx específico ocorreu é lembrado pelo provedor de serviços. Isso é necessário, pois a ocorrência de qualquer e todos os eventos de rede indicados resultarão em um único objeto de evento sendo sinalizado. Uma chamada para [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) faz com que o conteúdo atual da memória de evento de rede seja copiado para um buffer fornecido pelo cliente e a memória de evento de rede seja apagada. O cliente também pode designar um objeto de evento específico para ser limpo atomicamente junto com a memória de evento de rede.

 

 
