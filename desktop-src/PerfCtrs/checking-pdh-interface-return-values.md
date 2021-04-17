---
description: O valor de retorno das funções de PDH indica o êxito ou a falha da chamada de função, que é diferente do status dos dados do contador.
ms.assetid: 00ea5521-bc28-4a87-aba9-46c911631503
title: Verificando códigos de status de dados do contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7daed51ba6e8df385170b9a23b419267409ef497
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787478"
---
# <a name="checking-counter-data-status-codes"></a>Verificando códigos de status de dados do contador

O valor de retorno das funções de PDH indica o êxito ou a falha da chamada de função, que é diferente do status dos dados do contador. Sempre verifique o membro **CStatus** de um valor de contador retornado nas estruturas PDH para garantir que os dados retornados sejam válidos antes de usá-lo. Se o valor do membro **CStatus** não indicar êxito, não use os dados. A seguir estão os valores de status possíveis para os contadores:



| Valor                              | Significado                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDH \_ CSTATUS \_ nenhum \_ computador          | A PDH não pôde se conectar ao computador especificado no caminho do contador. Se esse status for retornado quando o contador estiver sendo adicionado, o contador não será completamente inicializado. Cada vez que a consulta é atualizada, a PDH tenta novamente a conexão. Quando a conexão é estabelecida, a coleta de dados normal é retomada.                                                                  |
| PDH \_ CSTATUS \_ nenhum \_ objeto           | O computador especificado foi encontrado, mas o objeto de desempenho especificado foi encontrado no computador. Se esse status for retornado quando o contador estiver sendo adicionado, o contador especificado não será incluído na consulta. Se esse status for retornado por um contador ativo, os dados desse contador serão inválidos. Cada vez que os dados são solicitados, a PDH tenta obter esses dados do contador. |
| \_CSTATUS PDH \_ sem \_ instância         | A instância especificada não foi encontrada no objeto. Se esse status for retornado enquanto o contador estiver sendo adicionado à consulta, o contador será adicionado com êxito à consulta, mas nenhum dado estará disponível até que a instância específica seja exibida e um status bem-sucedido seja retornado.                                                                                                  |
| \_CSTATUS PDH \_ sem \_ contador          | O contador especificado não foi encontrado no objeto especificado. Se esse status for retornado quando o contador estiver sendo adicionado, o contador não será adicionado à consulta. Se esse status for retornado após a coleta de dados, os dados desse contador serão inválidos. Cada vez que os dados são solicitados, a PDH tenta obter esses dados do contador.                                             |
| \_ \_ dados inválidos do CSTATUS PDH \_        | O contador foi encontrado com êxito, mas os dados retornados não são válidos. Esse erro pode ocorrer se o valor do contador for menor que o valor anterior. (Como os valores do contador sempre são incrementados, o valor do contador passa para zero quando atinge seu valor máximo.) Outra causa possível é um temporizador do sistema que não está correto.                                              |
| \_ \_ dados válidos do PDH CSTATUS \_          | Os dados do contador foram retornados com êxito, mas não foram alterados desde a última vez que o contador foi lido.                                                                                                                                                                                                                                                                    |
| \_ \_ novos \_ dados do PDH CSTATUS            | Os dados do contador foram retornados com êxito e são diferentes da última vez em que o contador foi lido. Os \_ novos dados do PDH CSTATUS \_ \_ podem ser retornados em um contador de taxa, mesmo se a taxa resultante for a mesma do último exemplo. Isso ocorre porque o valor de dados brutos que é usado na determinação desse valor de status foi alterado, não a taxa calculada.                  |
| \_mais \_ dados da PDH                    | O buffer fornecido não era grande o suficiente para armazenar todos os dados do contador. Aloque um buffer maior e execute a função novamente.                                                                                                                                                                                                                                              |
| \_item de CSTATUS PDH \_ \_ não \_ validado | O contador foi adicionado à consulta, mas não foi validado nem acessado. Não há informações de status adicionais sobre esse contador disponíveis.                                                                                                                                                                                                                                 |
| PDH \_ CSTATUS \_ sem \_ COUNTERNAME      | Nenhum nome de contador foi especificado na consulta.                                                                                                                                                                                                                                                                                                                                      |
| \_CSTATUS PDH \_ sem \_ contador          | Não foi possível encontrar o nome do contador especificado.                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ nenhum \_ objeto           | O objeto de desempenho especificado não pôde ser encontrado.                                                                                                                                                                                                                                                                                                                             |
| \_ \_ denominador de cálculo negativo do PDH \_   | Um contador tem um valor de denominador negativo.                                                                                                                                                                                                                                                                                                                                      |
| \_banco de \_ dados negativo de cálculo de PDH \_      | Um contador tem um valor de base de timenegativo.                                                                                                                                                                                                                                                                                                                                         |
| \_ \_ valor negativo de cálculo de PDH \_         | Um contador tem um valor negativo.                                                                                                                                                                                                                                                                                                                                                  |
| PDH \_ CSTATUS \_ sem \_ COUNTERNAME      | Nenhum caminho de contador foi especificado.                                                                                                                                                                                                                                                                                                                                                   |
| CSTATUS de PDH \_ \_ inválido \_ COUNTERNAME     | O formato do caminho do contador está incorreto.                                                                                                                                                                                                                                                                                                                                            |



 

 

 



