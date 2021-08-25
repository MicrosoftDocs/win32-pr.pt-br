---
title: Registros de recursos
description: Saiba mais sobre registros de recursos. Um registro de recurso é a unidade de entrada de informações em arquivos de zona DNS, que é usado para resolver todas as consultas DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606d74f41e18fefa144ff21d3ed88d9683938304b0c8aa0bc7d94e2fbaa624cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825056"
---
# <a name="resource-records"></a>Registros de recursos

Um registro de recurso, normalmente conhecido como RR, é a unidade de entrada de informações em arquivos de zona DNS; RRs são os blocos de construção básicos de informações ip e nome do host e são usados para resolver todas as consultas DNS. Os registros de recursos existem quantos tipos fornecerem serviços estendidos de resolução de nomes.

Diferentes tipos de RRs têm formatos diferentes, pois contêm dados diferentes. Em geral, no entanto, muitas RRs compartilham um formato comum, como ilustra o exemplo de registros de recursos de endereço a seguir. O exemplo fictício a seguir explica os campos encontrados em um registro de recurso A:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   O primeiro campo (microsoft.com) indica o proprietário.
-   O segundo campo (600) é o parâmetro TTL (vida real), em segundos.
-   O terceiro campo (IN) é o campo de classe que representa a família de protocolos, que é quase sempre IN, para a classe da Internet.
-   O quarto campo (A) é o tipo de recurso que o RR está representando.
-   O quinto campo (150.150.150.1) são os dados do recurso ou RDATA. Esse campo é um tipo de variável que fornece informações apropriadas para o tipo de recurso; nesse caso, é um endereço IP de 32 bits.

Os seguintes tipos de registro de recurso são comumente usados no DNS:

-   SOA (início da autoridade)
-   Servidor de nomes (NS)
-   [*Registro de ponteiro*](p-gly.md) (PTR)
-   Endereço (A)
-   Endereço IPv6 (AAAA)
-   Troca de email (MX)
-   [*Nome canônico*](c-gly.md) (CNAME)
-   Windows WINS (Internet Serviço de Nomenclatura)
-   Wins Reverse Look up (WINSR)

Há muitos outros tipos de registro de recurso no DNS. Para obter mais informações, consulte [Referência do provedor WMI DNS](dns-wmi-provider-reference.md).

 

 




