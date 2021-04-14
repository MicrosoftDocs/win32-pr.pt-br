---
description: Ao enviar para um endereço de destino multicast, o protocolo Microsoft IPv6 normalmente requer que o aplicativo tenha uma interface de saída especificada.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: Endereços de destino multicast IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aa516713fb47f6af03d8564c464a07a19cf0f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461113"
---
# <a name="ipv6-multicast-destination-addresses"></a>Endereços de destino multicast IPv6

Ao enviar para um endereço de destino multicast, o protocolo Microsoft IPv6 normalmente requer que o aplicativo tenha uma interface de saída especificada. Isso é feito com o **\_ multicast IPv6 \_ se** opção de soquete ou ligando o soquete a um endereço de origem específico.

Você também pode especificar uma interface padrão para um endereço de multicast específico, um escopo inteiro de endereço de multicast ou todos os endereços multicast. Isso é feito com uma rota que coloca o prefixo multicast no link para a interface de saída desejada. Os exemplos a seguir mostram como isso pode ser especificado:

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



