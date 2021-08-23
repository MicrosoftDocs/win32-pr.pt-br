---
description: Há uma limitação no código que recebe pacotes encapsulados (encapsulados) e os demultiplexa para uma interface específica.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Pacotes com túnel de encaminhamento IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42138c746ea9d0ec8ea61bc3801b84a97a6bdd4c6fb6de0871e6b74447fdf28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132429"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>Pacotes com túnel de encaminhamento IPv6

Há uma limitação no código que recebe pacotes encapsulados (encapsulados) e os demultiplexa para uma interface específica. Se você quiser encaminhar pacotes de túnel recebidos por meio de um túnel configurado, será necessário habilitar o encaminhamento em qualquer interface de 6 sobre 4, bem como na interface \# 2. A habilitação apenas do encaminhamento na interface \# 2 não funcionará. Normalmente, ao configurar um roteador, você habilitaria o encaminhamento em todas as interfaces, exceto loopback.

 

 



