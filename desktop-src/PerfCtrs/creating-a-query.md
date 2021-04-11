---
description: Para criar uma nova consulta que coleta dados de desempenho de um arquivo de origem ou de log em tempo real, chame a função PdhOpenQuery. A função retorna um identificador para a consulta que você usa em chamadas de função PDH subsequentes.
ms.assetid: 6fd4716e-b163-47a3-b0cb-5f9599f8681f
title: Criando uma consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9d50ec52966529a3476a6d375606ba3d0b538b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091637"
---
# <a name="creating-a-query"></a>Criando uma consulta

Para criar uma nova consulta que coleta dados de desempenho de um arquivo de origem ou de log em tempo real, chame a função [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) . A função retorna um identificador para a consulta que você usa em chamadas de função PDH subsequentes.

Depois de criar a consulta, chame a função [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) para cada contador que você deseja adicionar à consulta. Você pode usar um dos métodos a seguir para fornecer o caminho do contador totalmente qualificado.

-   Defina o caminho do contador como uma cadeia de caracteres estática. Use esse método se você sempre monitorar o mesmo contador e se estiver familiarizado com a sintaxe correta de um caminho de contador. Para obter informações sobre a sintaxe correta usada para especificar um contador, consulte [especificando um caminho de contador](specifying-a-counter-path.md).
-   Inicialize uma estrutura de [**\_ elementos do \_ caminho \_ do contador PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) com os nomes do computador, objeto, contador e instância. Passe essa estrutura para [**PdhMakeCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha) , que retornará um caminho de contador para os elementos especificados.
-   Especifique um caminho de contador que contenha caracteres curinga e chame [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) para obter uma lista de nomes de contadores que correspondem aos caracteres curinga no caminho. Examine a lista de nomes de contadores e adicione à consulta os contadores desejados nesta lista.
-   Chame a função [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) para exibir uma caixa de diálogo que permite ao usuário procurar e Selecionar contadores de desempenho. Para obter mais informações, consulte [procurar contadores](browsing-counters.md).

Observe que, se uma instância do contador for especificada e não existir, o [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) não relatará uma condição de erro. Em vez disso, retorna o êxito do erro \_ . O motivo para esse comportamento é que ele não é conhecido se uma instância de contador não existente tiver sido especificada ou uma que existirá, mas ainda não tiver sido criada.

A instância do contador ausente será relatada por [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata), [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)ou [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue). Ao chamar **PdhCollectQueryData** para apenas uma instância do contador, e a instância do contador ainda não existir, supõe-se que a instância do contador não exista e a função retorna PDH \_ sem \_ dados. No entanto, se mais de um contador for consultado, **PdhCollectQueryData** poderá ainda retornar \_ um êxito de erro mesmo que uma das instâncias do contador ainda não exista. Nesse caso, chame **PdhGetRawCounterValue** ou **PdhGetFormattedCounterValue** para cada uma das instâncias de contador de interesse. Se a instância não existir ao chamar **PdhGetRawCounterValue**, a função retornará êxito de erro \_ e definirá o membro **CStatus** do [**\_ \_ contador bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) para o status de PDH \_ \_ sem \_ instância. Se a instância não existir ao chamar **PdhGetFormattedCounterValue**, a função retornará \_ dados inválidos \_ da PDH e definirá o membro **CStatus** do [**\_ \_ metavalor PDH fmt**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue) para PDH \_ CStatus \_ nenhuma \_ instância.

Observe que o caminho do contador especificado na função [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) deve ser localizado. A função [**PdhAddEnglishCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera) fornece uma maneira neutra de localidade para adicionar contadores de desempenho à consulta. Essa função é a maneira recomendada para adicionar contadores neutros à localidade a uma consulta.

Para remover um contador de uma consulta, chame a função [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter) .

Depois de concluir a coleta de dados de uma consulta, chame a função [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) para fechar a consulta e liberar todos os recursos de sistema alocados. **PdhCloseQuery** fecha todos os identificadores de contador associados à consulta.

 

 



