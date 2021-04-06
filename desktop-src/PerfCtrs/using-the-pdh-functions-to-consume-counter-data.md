---
description: Você usa as funções de PDH para coletar dados de desempenho.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Usando as funções de PDH para consumir dados de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828374"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a>Usando as funções de PDH para consumir dados de contador

Use as funções de PDH para coletar dados de desempenho. As funções de PDH são mais fáceis de usar do que as [funções de registro](using-the-registry-functions-to-consume-counter-data.md) e podem ser usadas para acessar dados de contador de provedores v1 e v2. A PDH tem APIs para coletar dados de desempenho atuais, salvar dados de desempenho em arquivos de log e ler dados de arquivos de log.

> [!Note]
> Você não poderá usar as funções de camada de abstração do auxiliar de dados de desempenho se estiver escrevendo aplicativos do Windows OneCore. Em vez disso, use as [funções de consumidor do PerfLib v2](using-the-perflib-functions-to-consume-counter-data.md).

A PDH é uma API de alto nível que simplifica a coleta de dados do contador de desempenho. Ele ajuda na análise de consultas, no cache de metadados, na correspondência de instâncias entre amostras, na computação de valores formatados de valores brutos, na leitura de dados de arquivos de log e no salvamento de dados em arquivos de log. A PDH usa automaticamente [as funções de registro](using-the-registry-functions-to-consume-counter-data.md) ao coletar dados de **provedores v1** e usa as [funções de consumidor v2](using-the-perflib-functions-to-consume-counter-data.md) ao coletar dados de **provedores v2**.

Para coletar dados de desempenho usando as funções de PDH, execute as etapas a seguir.

1. [Criar uma consulta](creating-a-query.md)
2. [Adicionar contadores à consulta](creating-a-query.md)
3. [Coletar os dados de desempenho](collecting-performance-data.md)
4. [Exibir os dados de desempenho](displaying-performance-data.md)
5. [Fechar a consulta](creating-a-query.md)

Você pode coletar dados de desempenho de fontes em tempo real ou arquivos de log. Para obter mais informações sobre como gravar dados de desempenho em arquivos de log, consulte [trabalhando com arquivos de log](working-with-log-files.md).

## <a name="see-also"></a>Confira também

- [Coletando dados de desempenho](collecting-performance-data.md)
- [Contadores de navegação](browsing-counters.md)
- [Verificando valores de retorno da interface PDH](checking-pdh-interface-return-values.md)
- [Exemplos](examples.md)
