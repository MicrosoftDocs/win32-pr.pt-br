---
title: Acessando ponteiros opacos
description: Os clientes podem acessar as informações armazenadas em destinos usando ponteiros opacos.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b76e99a66b13c696951a0d46684726f79f29df5b0287e9c4923dc4054943e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030616"
---
# <a name="accessing-opaque-pointers"></a>Acessando ponteiros opacos

Os clientes podem acessar as informações armazenadas em destinos usando ponteiros opacos. Para usar o armazenamento, o cliente deve primeiro chamar [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) para obter o ponteiro. Sempre que uma alteração nas informações for necessária, o cliente deverá primeiro bloquear o destino chamando [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) com o parâmetro *LockDest* definido como **TRUE.** Depois que o destino é bloqueado, o cliente pode fazer a alteração necessária. O destino pode ser desbloqueado usando outra chamada para **RtmLockDestination** com o *parâmetro LockDest* definido como **FALSE.**

A [**função RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) também permite que um cliente use um bloqueio de leitura ou um bloqueio de gravação, usando o *parâmetro* Exclusive. Um cliente deve usar o bloqueio de gravação somente quando estiver fazendo alterações nas informações mantidas usando o ponteiro opaco. Os clientes podem usar o bloqueio de leitura para exibir as informações de ponteiro opaca armazenadas em um destino.

Para um código de exemplo que mostra como usar essas funções, consulte [Acessar o ponteiro opaco em um destino](access-the-opaque-pointer-in-a-destination.md).

 

 




