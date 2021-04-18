---
description: Para abrir um arquivo de log para leitura, chame PdhOpenQuery e especifique um caminho para o arquivo de log.
ms.assetid: 1d8f8662-df1f-4f84-8b65-c152f79cc5c6
title: Trabalhando com arquivos de log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2032b90036f8f58c07d8c7e80e7e7ac2b2701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758287"
---
# <a name="working-with-log-files"></a>Trabalhando com arquivos de log

Para abrir um arquivo de log para leitura, chame [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) e especifique um caminho para o arquivo de log. Para abrir um arquivo de log para gravação, você deve chamar [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Para fechar um arquivo de log, chame [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) ou [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) dependendo da função usada para abrir o arquivo de log.

## <a name="reading-from-a-log-file"></a>Lendo de um arquivo de log

Ler dados de desempenho de um arquivo de log é o mesmo que ler dados de uma fonte em tempo real – você abre uma consulta, adiciona contadores à consulta e chama [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) para coletar um exemplo do arquivo de log. **PdhCollectQueryData** retorna a PDH que \_ não \_ mais \_ dados quando você chega ao final do arquivo de log.

Cada exemplo no arquivo de log contém um carimbo de data/hora para quando ele foi originalmente coletado e gravado no arquivo de log. Para recuperar o carimbo de data/hora da primeira e da última amostra no arquivo de log, chame a função [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) . Se você quiser limitar os exemplos lidos do log para um intervalo de tempo específico, consulte [definindo um intervalo de tempo para uma consulta](setting-a-time-range-for-a-query.md).

Se você não souber quais objetos e contadores de desempenho existem no arquivo de log, você pode chamar [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) para determinar a lista de objetos. Dado um objeto, você pode chamar [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) ou [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) para recuperar uma lista das instâncias e dos contadores do objeto contidos no arquivo de log.

Se você chamar [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa), use a instância e as listas de contadores para criar um caminho para cada combinação possível de instância e contador. Quando você chamar [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) para adicionar o contador à consulta, a função falhará se o arquivo de log não contiver a combinação determinada.

Se você usar [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha), poderá criar um caminho que contém um caractere curinga para o nome da instância e o contador, por exemplo, \\ Object ( \* ) \\ \* . A função retornará o \_ \_ caminho inválido da PDH se o objeto não contiver uma instância. Nesse caso, chame **PdhExpandWildCardPath** usando um curinga somente para Counter, por exemplo, \\ Object \\ \* .

Sistemas operacionais mais recentes podem ler arquivos de log que foram gerados em sistemas operacionais mais antigos; no entanto, os arquivos de log criados no Windows Vista e sistemas operacionais posteriores não podem ser lidos em sistemas operacionais anteriores.

Para obter um exemplo que lê dados de um arquivo de log, consulte [lendo dados de desempenho de um arquivo de log](reading-performance-data-from-a-log-file.md).

## <a name="reading-from-multiple-log-files"></a>Lendo de vários arquivos de log

Se você precisar criar uma consulta que leia de vários arquivos de log, chame o [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) para associar os arquivos de log ao mesmo tempo. Em seguida, você precisa usar funções de PDH que terminem em ' H ', por exemplo, [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh).

## <a name="writing-to-a-log-file"></a>Gravando em um arquivo de log

Antes de gravar em um arquivo de log, chame [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) para criar uma consulta e especificar a origem dos dados de desempenho, tanto os dados em tempo real quanto um arquivo de log. Em seguida, adicione os contadores que você deseja consultar.

Para abrir o arquivo de destino, chame [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Especifique a consulta ao abrir o arquivo de log. Para coletar os dados de desempenho e gravá-los no arquivo de log, chame [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

Se os dados do contador estiverem sendo gravados em um arquivo de log delimitado por vírgula (. csv) ou delimitado por tabulação (. tsv) e o caminho contiver uma instância curinga, o caminho será expandido e somente as instâncias existentes no momento em que o caminho for expandido serão incluídas no arquivo de log. No entanto, para arquivos de log binários (. blg) ou SQL, o curinga não é expandido para que o arquivo de log contenha instâncias criadas durante o registro em log.

Para obter um exemplo que grava dados em um arquivo de log, consulte [gravando dados de desempenho em um arquivo de log](writing-performance-data-to-a-log-file.md).

## <a name="compressing-a-log-file"></a>Compactando um arquivo de log

Você pode usar a função [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) para compactar um arquivo de log. Por exemplo, leia dez registros de um arquivo de log, chame **PdhComputeCounterStatistics** para calcular o valor médio e, em seguida, grave o valor médio em um arquivo de log de saída.

O tópico a seguir fornece informações adicionais sobre como usar um arquivo de log.

-   [Obtendo o tamanho de um arquivo de log](getting-the-size-of-a-log-file.md)

 

 



