---
description: WSPEventSelect se comporta exatamente como WSPAsyncSelect, exceto que, em vez de fazer com que uma mensagem do Windows seja enviada na ocorrência de qualquer \_ evento de rede do FD xxx indicado (por exemplo, FD \_ Read, FD \_ Write, etc.), um objeto de evento designado é definido.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Sinalização de objeto de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811673"
---
# <a name="event-object-signaling"></a>Sinalização de objeto de evento

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) se comporta exatamente como [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , exceto que, em vez de fazer com que uma mensagem do Windows seja enviada na ocorrência de qualquer \_ evento de rede do FD xxx indicado (por exemplo, FD \_ Read, FD \_ Write, etc.), um objeto de evento designado é definido.

Além disso, o fato de que um \_ evento de rede FD xxx específico ocorreu é lembrado pelo provedor de serviços. Isso é necessário, pois a ocorrência de qualquer e todos os eventos de rede indicados resultarão em um único objeto de evento sendo sinalizado. Uma chamada para [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) faz com que o conteúdo atual da memória de evento de rede seja copiado para um buffer fornecido pelo cliente e a memória de evento de rede seja apagada. O cliente também pode designar um objeto de evento específico para ser limpo atomicamente junto com a memória de evento de rede.

 

 
