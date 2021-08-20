---
title: Acessando interfaces em Apartments
description: Acessando interfaces em Apartments
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89e82fa29e768328e6c110349627d32e92ab010ce61fdf64141ad3ca7fe9a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048914"
---
# <a name="accessing-interfaces-across-apartments"></a>Acessando interfaces em Apartments

COM fornece uma maneira para qualquer Apartment em um processo obter acesso a uma interface implementada em um objeto em qualquer outro apartamento no processo. Isso é feito por meio da interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Essa interface tem três métodos, que permitem que você faça o seguinte:

-   Registrar uma interface como uma interface *global* (processwide).
-   Obtenha um ponteiro para essa interface de qualquer outro apartamento por meio de um cookie.
-   Revogue o registro global de uma interface.

A interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) é uma maneira eficiente para um processo armazenar um ponteiro de interface em um local de memória que pode ser acessado de vários Apartments dentro do processo, como variáveis de todo o processo e objetos *Agile* (objetos de thread livre, empacotados) que contêm ponteiros de interface para outros objetos.

Um objeto ágil não reconhece a infraestrutura COM subjacente na qual ele é executado; em outras palavras, o apartamento, o contexto e o thread em que ele está sendo executado. O objeto pode estar mantendo as interfaces específicas para um apartamento ou contexto. Por esse motivo, chamar essas interfaces a partir de onde o componente Agile está em execução pode nem sempre funcionar corretamente. A tabela de interface global evita esse problema garantindo que um proxy válido (ou ponteiro direto) para o objeto seja usado, com base em onde o objeto Agile está sendo executado.

> [!Note]  
> A tabela de interface global não é portátil entre os limites do processo ou da máquina, portanto, não pode ser usada no lugar do mecanismo de passagem de parâmetro normal.

 

Para obter informações sobre como criar e usar uma tabela de interface global, consulte os seguintes tópicos:

-   [Criando a tabela de interface global](creating-the-global-interface-table.md)
-   [Quando usar a tabela de interface global](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escolhendo o modelo de Threading](choosing-the-threading-model.md)
</dt> <dt>

[Apartments multithread](multithreaded-apartments.md)
</dt> <dt>

[Problemas de Threading do servidor em processo](in-process-server-threading-issues.md)
</dt> <dt>

[Processos, threads e Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicação de thread único e multithread](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartments de thread único](single-threaded-apartments.md)
</dt> </dl>

 

 




