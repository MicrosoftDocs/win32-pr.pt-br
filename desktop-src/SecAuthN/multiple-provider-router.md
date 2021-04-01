---
description: O roteador de vários provedores (MPR) lida com a comunicação entre o sistema operacional Windows e os provedores de rede instalados. Ele permite que o Windows apresente uma rede integrada ao usuário.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Roteador de vários provedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829453"
---
# <a name="multiple-provider-router"></a>Roteador de vários provedores

O [*roteador de vários provedores*](../secgloss/m-gly.md) (MPR) lida com a comunicação entre o sistema operacional Windows e os provedores de rede instalados. Ele permite que o Windows apresente uma rede integrada ao usuário.

Quando o MPR é iniciado, ele verifica o registro para determinar quais provedores de rede estão instalados no sistema e a ordem em que eles devem ser alternados. Ele carrega todas as DLLs de provedor de rede registradas e as usa para processar chamadas WNet subsequentes feitas pela interface do usuário ou por outros aplicativos.

Para obter mais informações sobre as funções do WNet, consulte [sistema de rede do Windows](../wnet/windows-networking-wnet-.md).

 

 
