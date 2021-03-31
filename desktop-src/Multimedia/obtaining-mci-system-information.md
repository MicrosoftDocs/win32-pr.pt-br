---
title: Obtendo informações do sistema MCI
description: Obtendo informações do sistema MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- MCI_SYSINFO comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916174"
---
# <a name="obtaining-mci-system-information"></a>Obtendo informações do sistema MCI

O comando [sysinfo](sysinfo.md) (do [**MCI do \_ sysinfo**](mci-sysinfo.md)) obtém informações do sistema sobre dispositivos MCI. O MCI manipula esse comando sem retransmiti-lo para qualquer dispositivo MCI. Para a interface de mensagem de comando, o MCI retorna as informações do sistema na estrutura de [**\_ \_ parâmetros do sysinfo do MCI**](mci-sysinfo-parms.md) .

Você pode usar o comando **sysinfo** (do MCI do \_ sysinfo) para recuperar informações como o número de dispositivos MCI em um sistema, o número de dispositivos MCI de um tipo específico, o número de dispositivos MCI abertos e os nomes dos dispositivos. Esse comando geralmente é chamado mais de uma vez para recuperar uma determinada informação. Por exemplo, você pode recuperar o número de dispositivos de um tipo específico na primeira chamada e, em seguida, enumerar os nomes dos dispositivos no próximo.

 

 




