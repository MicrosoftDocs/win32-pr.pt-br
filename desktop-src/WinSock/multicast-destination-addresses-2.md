---
description: Ao enviar para um endereço de destino multicast, o protocolo IPv6 da Microsoft normalmente exige que o aplicativo tenha uma interface de saída especificada.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: Endereços de destino multicast IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814411c89acc6eda759926f581066f939d4e9ac455e7d84789dbd9316c597a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822689"
---
# <a name="ipv6-multicast-destination-addresses"></a>Endereços de destino multicast IPv6

Ao enviar para um endereço de destino multicast, o protocolo IPv6 da Microsoft normalmente exige que o aplicativo tenha uma interface de saída especificada. Isso é feito com a opção de soquete **\_ IF MULTICAST \_ IPV6** ou vinculando o soquete a um endereço de origem específico.

Você também pode especificar uma interface padrão para um endereço multicast específico, um escopo de endereço multicast inteiro ou todos os endereços multicast. Isso é feito com uma rota que coloca o prefixo multicast no link para a interface de saída desejada. Para exemplos a seguir, mostre como isso pode ser especificado:

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



