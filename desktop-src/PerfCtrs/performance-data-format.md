---
description: O formato dos dados recuperados pela função RegQueryValueEx começa com uma estrutura de cabeçalho de comprimento fixo, o PERF \_ Data \_ Block.
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: Formato de dados de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88029634594843a50fd6010993eb6517dce831f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558732"
---
# <a name="performance-data-format"></a>Formato de dados de desempenho

O formato dos dados recuperados pela função [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) começa com uma estrutura de cabeçalho de comprimento fixo, o [**perf \_ Data \_ Block**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block). A estrutura de **\_ \_ bloco de dados perf** descreve o sistema e os dados de desempenho. A estrutura de **\_ \_ bloco de dados perf** é seguida por um número variável de itens de dados de objeto de comprimento variável. O cabeçalho de cada item de objeto contém o deslocamento do próximo item de objeto na lista. O diagrama a seguir mostra a estrutura de dados de desempenho básico.

![estrutura de dados de desempenho](images/perfdata.png)

Há dois formatos para os itens de dados de objeto: um que dá suporte a várias instâncias e o outro que não oferece suporte a várias instâncias.

Cada bloco de item de dados de objeto contém uma estrutura de [**\_ \_ tipo de objeto perf**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) , que descreve os dados de desempenho para o objeto. A estrutura de **\_ \_ tipo de objeto perf** é seguida por uma lista de estruturas de [**definição de \_ contador \_ de desempenho**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) , uma para cada contador definido para o objeto. Para um objeto com apenas uma instância, a lista de estruturas de **\_ \_ definição de contador de desempenho** é seguida por uma única estrutura de [**\_ \_ bloco de contador de desempenho**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) , seguida pelos dados do contador. Cada estrutura de **\_ \_ definição de contador de desempenho** contém o deslocamento do início da estrutura de **\_ \_ bloco de contador de desempenho** para os dados do contador correspondente. O diagrama a seguir mostra a estrutura de um objeto de desempenho que não oferece suporte a várias instâncias.

![estrutura do objeto de desempenho que não oferece suporte a várias instâncias](images/perfnoinst.png)

Para um tipo de objeto que dá suporte a várias instâncias, a lista de estruturas de [**\_ \_ definição de contador de desempenho**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) é seguida por uma lista de blocos de informações de instância (um para cada instância). Cada bloco de informações de instância contém uma estrutura de [**\_ \_ definição de instância perf**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) , o nome da instância e uma estrutura de [**\_ \_ bloco de contador perf**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) . O diagrama a seguir mostra a estrutura de um objeto de desempenho que dá suporte a duas instâncias.

![estrutura de um objeto de desempenho que dá suporte a duas instâncias](images/perfinst.png)

Para obter um exemplo que usa os deslocamentos, consulte [exibindo nomes de objeto, instância e contador](displaying-object-instance-and-counter-names.md).

 

 
