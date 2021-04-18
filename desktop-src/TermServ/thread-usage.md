---
title: Uso de thread
description: Você deve ajustar e balancear o uso de threads de aplicativo para um ambiente multiusuário, multiprocessador Serviços de Área de Trabalho Remota.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764734"
---
# <a name="thread-usage"></a>Uso de thread

Os threads fornecem uma maneira conveniente de permitir que um aplicativo Maximize seu uso de recursos de CPU em um sistema, especialmente em uma configuração de processador múltiplo. Em um ambiente de Serviços de Área de Trabalho Remota, no entanto, vários usuários podem executar aplicativos multithread e todos os threads de todos os usuários conpetem para os recursos de CPU central do sistema. Com isso em mente, você deve ajustar e balancear o uso de threads de aplicativo para um ambiente multiusuário, multiprocessador Serviços de Área de Trabalho Remota. Embora um aplicativo multithread mal projetado com threads ociosos ou desperdiçados possa ser executado adequadamente em um computador cliente, o mesmo aplicativo pode não funcionar bem em um servidor de Serviços de Área de Trabalho Remota multiusuário.

 

 




