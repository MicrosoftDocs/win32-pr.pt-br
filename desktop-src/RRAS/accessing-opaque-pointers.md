---
title: Acessando ponteiros opacos
description: Os clientes são capazes de acessar as informações armazenadas em destinos usando ponteiros opacos.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498740"
---
# <a name="accessing-opaque-pointers"></a>Acessando ponteiros opacos

Os clientes são capazes de acessar as informações armazenadas em destinos usando ponteiros opacos. Para usar o armazenamento, o cliente deve primeiro chamar [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) para obter o ponteiro. Sempre que uma alteração nas informações é necessária, o cliente deve primeiro bloquear o destino chamando [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) com o parâmetro *LockDest* definido como **true**. Depois que o destino estiver bloqueado, o cliente poderá fazer a alteração necessária. O destino pode ser desbloqueado usando outra chamada para **RtmLockDestination** com o parâmetro *LockDest* definido como **false**.

A função [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) também permite que um cliente use um bloqueio de leitura ou um bloqueio de gravação, usando o parâmetro *exclusivo* . Um cliente deve usar o bloqueio de gravação somente quando estiver fazendo alterações nas informações mantidas usando o ponteiro opaco. Os clientes podem usar o bloqueio de leitura para exibir as informações de ponteiro opacos armazenadas em um destino.

Para obter um exemplo de código que mostra como usar essas funções, consulte [acessar o ponteiro opaco em um destino](access-the-opaque-pointer-in-a-destination.md).

 

 




