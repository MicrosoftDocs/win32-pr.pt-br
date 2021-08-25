---
title: Obtendo o MCI Informações do Sistema
description: Obtendo o MCI Informações do Sistema
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fa6cc0757bc09aa16216f2f20385bf31b44bb88e27ea64e091ff3909d8d57e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893216"
---
# <a name="obtaining-mci-system-information"></a>Obtendo o MCI Informações do Sistema

O [comando sysinfo](sysinfo.md) ([**MCI \_ SYSINFO**](mci-sysinfo.md)) obtém informações do sistema sobre dispositivos MCI. A MCI trata esse comando sem retransmiti-lo para nenhum dispositivo MCI. Para a interface de mensagem de comando, a MCI retorna as informações do sistema na estrutura [**\_ MCI SYSINFO \_ PARMS.**](mci-sysinfo-parms.md)

Você pode usar o comando **sysinfo** (MCI SYSINFO) para recuperar informações como o número de dispositivos MCI em um sistema, o número de dispositivos MCI de um tipo específico, o número de dispositivos MCI abertos e os nomes dos \_ dispositivos. Esse comando geralmente é chamado mais de uma vez para recuperar uma determinada informação. Por exemplo, você pode recuperar o número de dispositivos de um tipo específico na primeira chamada e, em seguida, enumerar os nomes dos dispositivos na próxima.

 

 




