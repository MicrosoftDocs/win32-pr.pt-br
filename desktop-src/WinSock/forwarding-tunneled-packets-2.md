---
description: Há uma limitação no código que recebe pacotes encapsulados (encapsulados) e os desmultiplexa para uma interface específica.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Pacotes de túnel de encaminhamento IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827114"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>Pacotes de túnel de encaminhamento IPv6

Há uma limitação no código que recebe pacotes encapsulados (encapsulados) e os desmultiplexa para uma interface específica. Se você quiser encaminhar pacotes encapsulados recebidos por meio de um túnel configurado, será necessário habilitar o encaminhamento em qualquer interface 6-over-4, bem como na interfaces \# 2. Apenas habilitar o encaminhamento na interface \# 2 não funcionará. Normalmente, ao configurar um roteador, você permitiria o encaminhamento em todas as interfaces, exceto loopback.

 

 



