---
title: Registros de recursos
description: Um registro de recurso, conhecido como RR, é a unidade de entrada de informações nos arquivos de zona DNS; RRs são os blocos de construção básicos de nome de host e informações de IP e são usados para resolver todas as consultas DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636668"
---
# <a name="resource-records"></a>Registros de recursos

Um registro de recurso, conhecido como RR, é a unidade de entrada de informações nos arquivos de zona DNS; RRs são os blocos de construção básicos de nome de host e informações de IP e são usados para resolver todas as consultas DNS. Os registros de recursos existem tantos tipos para fornecer serviços de resolução de nomes estendidos.

Tipos diferentes de RRs têm formatos diferentes, pois contêm dados diferentes. Em geral, no entanto, muitos RRs compartilham um formato comum, como ilustra o exemplo de registros de recursos de endereço a seguir. O exemplo fictício a seguir explica os campos encontrados em um registro de recurso:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   O primeiro campo (microsoft.com) denota o proprietário.
-   O segundo campo (600) é o parâmetro time-to-Live (TTL), em segundos.
-   O terceiro campo (em) é o campo de classe que representa a família de protocolos, que é quase sempre no, para classe de Internet.
-   O quarto campo (A) é o tipo de recurso que o RR está representando.
-   O quinto campo (150.150.150.1) são os dados do recurso ou RDATA. Este campo é um tipo de variável que fornece informações apropriadas para o tipo de recurso; Nesse caso, é um endereço IP de 32 bits.

Os seguintes tipos de registro de recurso são comumente usados no DNS:

-   Início de autoridade (SOA)
-   Servidor de nomes (NS)
-   [*Registro de ponteiro*](p-gly.md) (PTR)
-   Endereço (A)
-   Endereço IPv6 (AAAA)
-   Troca de email (MX)
-   [*Nome canônico*](c-gly.md) (CNAME)
-   Internet Serviço de Nomenclatura do Windows (WINS)
-   Pesquisa inversa do WINS (WINSr)

Há muitos outros tipos de registro de recurso no DNS. Para obter mais informações, consulte [referência do provedor WMI de DNS](dns-wmi-provider-reference.md).

 

 




