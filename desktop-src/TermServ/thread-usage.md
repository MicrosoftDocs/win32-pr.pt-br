---
title: Uso de thread
description: Você deve ajustar e balancear o uso de thread de aplicativo para um ambiente multiusuário Serviços de Área de Trabalho Remota multiprocessador.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22959c6950458c95670d71479a2efe04fdafea765048508b9bd371b0a215064d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869516"
---
# <a name="thread-usage"></a>Uso de thread

Os threads fornecem uma maneira conveniente de permitir que um aplicativo maximize seu uso de recursos de CPU em um sistema, especialmente em uma configuração de vários processadores. Em um Serviços de Área de Trabalho Remota, no entanto, vários usuários podem estar executando aplicativos multithread e todos os threads para todos os usuários competem pelos recursos centrais da CPU desse sistema. Com isso em mente, você deve ajustar e equilibrar o uso do thread de aplicativo para um ambiente multiusuário e multiprocessador Serviços de Área de Trabalho Remota aplicativo. Embora um aplicativo multithread mal projetado com threads ociosos ou perdidos possa ter um desempenho adequado em um computador cliente, o mesmo aplicativo pode não ter um bom desempenho em um servidor multiusuário Serviços de Área de Trabalho Remota usuário.

 

 




