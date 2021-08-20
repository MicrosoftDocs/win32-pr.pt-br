---
description: o roteador de vários provedores (MPR) lida com a comunicação entre o sistema operacional Windows e os provedores de rede instalados. ele permite que Windows apresente uma rede integrada ao usuário.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Roteador de vários provedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788a6b5dc7ec2db1f75d4bdf7d04df4127e90670b7f798682423dac4567a6fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786574"
---
# <a name="multiple-provider-router"></a>Roteador de vários provedores

o [*roteador de vários provedores*](../secgloss/m-gly.md) (MPR) lida com a comunicação entre o sistema operacional Windows e os provedores de rede instalados. ele permite que Windows apresente uma rede integrada ao usuário.

Quando o MPR é iniciado, ele verifica o registro para determinar quais provedores de rede estão instalados no sistema e a ordem em que eles devem ser alternados. Ele carrega todas as DLLs de provedor de rede registradas e as usa para processar chamadas WNet subsequentes feitas pela interface do usuário ou por outros aplicativos.

para obter mais informações sobre as funções do WNet, consulte [Windows rede](../wnet/windows-networking-wnet-.md).

 

 
