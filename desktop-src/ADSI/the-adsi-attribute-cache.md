---
title: O cache de atributo ADSI
description: O modelo de objeto ADSI fornece um cache de atributos do lado do cliente para cada objeto ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- O ADSI do cache de atributo ADSI
- ADSI, usando, acessando e manipulando dados com ADSI, cache de atributos
- atributos ADSI, cache de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634860"
---
# <a name="the-adsi-attribute-cache"></a>O cache de atributo ADSI

O modelo de objeto ADSI fornece um cache de atributos do lado do cliente para cada objeto ADSI. O cache de atributo é comparável a uma tabela na memória que contém os nomes e valores da maioria dos atributos de objeto que foram baixados. Alguns atributos, como atributos operacionais, não são armazenados em cache. A ADSI usa o cache de propriedades para aprimorar o desempenho da manipulação de atributos e adicionar capacidade de transacionamento para operações de leitura e gravação de atributo. Esse recurso é essencial para clientes escritos em linguagens que não têm um mecanismo de envio em lote nativo para a configuração de atributos, como o sistema de desenvolvimento Microsoft Visual Basic. Sem o cache de propriedades ADSI, esses clientes teriam que acessar o servidor sempre que um atributo for lido ou gravado.

Quando um objeto é criado ou associado primeiro a, o cache de propriedades do objeto está vazio. Quando o método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) é chamado, a ADSI carrega os atributos solicitados para o objeto do serviço de diretório subjacente no cache local. Quando um valor de atributo específico é lido e o cache está vazio, a ADSI faz uma chamada implícita para o método **IADs:: GetInfo** . Quando o cache é preenchido, todas as operações de leitura de atributo funcionam apenas no conteúdo do cache.

Quando um valor de atributo é gravado, o novo valor é armazenado no cache local até que o método [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) seja chamado. Quando o método **IADs:: setinfo** é chamado, os atributos no cache são confirmados no serviço de diretório subjacente. Depois que o método **IADs:: setinfo** é chamado, os valores permanecem no cache até que sejam explicitamente atualizados com outra chamada para o método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .

> [!IMPORTANT]
> O método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) deve ser usado com cuidado porque esse método sempre substituirá os valores de atributo no cache do serviço de diretório subjacente, mesmo que o valor em cache tenha sido alterado. Ou seja, ele substituirá os valores de atributo que foram alterados no cache, mas não confirmados no serviço de diretório subjacente com uma chamada para o método [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

 

A figura a seguir mostra os diferentes métodos usados para operar no cache.

![cache de atributo ADSI](images/ds2propc.png)

 

 




