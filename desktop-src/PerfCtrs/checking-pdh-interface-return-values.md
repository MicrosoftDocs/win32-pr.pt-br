---
description: O valor de retorno das funções PDH indica o êxito ou a falha da chamada de função, que é diferente do status dos dados do contador.
ms.assetid: 00ea5521-bc28-4a87-aba9-46c911631503
title: Verificando códigos de status de dados do contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c433e1c45badd3a2211a0e53051ad40d495f63a67b0ca509ae74a5cd99972
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978876"
---
# <a name="checking-counter-data-status-codes"></a>Verificando códigos de status de dados do contador

O valor de retorno das funções PDH indica o êxito ou a falha da chamada de função, que é diferente do status dos dados do contador. Sempre verifique o **membro CStatus** de um valor de contador retornado nas estruturas PDH para garantir que os dados retornados são válidos antes de usá-los. Se o valor do **membro CStatus** não indicar êxito, não use os dados. A seguir estão os valores de status possíveis para contadores:



| Valor                              | Significado                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDH \_ CSTATUS \_ NO \_ MACHINE          | O PDH não pôde se conectar ao computador especificado no caminho do contador. Se esse status for retornado quando o contador estiver sendo adicionado, o contador não será completamente inicializado. Sempre que a consulta é atualizada, o PDH recupera a conexão. Quando a conexão é estabelecida, a coleta de dados normal é retomada.                                                                  |
| PDH \_ CSTATUS \_ NO \_ OBJECT           | O computador especificado foi encontrado, mas o objeto de desempenho especificado foi encontrado no computador. Se esse status for retornado quando o contador estiver sendo adicionado, o contador especificado não será incluído na consulta. Se esse status for retornado por um contador ativo, os dados desse contador serão inválidos. Sempre que os dados são solicitados, o PDH tenta obter esses dados do contador. |
| PDH \_ CSTATUS \_ NO \_ INSTANCE         | A instância especificada não foi encontrada no objeto . Se esse status for retornado enquanto o contador estiver sendo adicionado à consulta, o contador será adicionado com êxito à consulta, mas nenhum dado estará disponível até que a instância específica seja exibida e um status bem-sucedido seja retornado.                                                                                                  |
| PDH \_ CSTATUS \_ NO \_ COUNTER          | O contador especificado não foi encontrado no objeto especificado. Se esse status for retornado quando o contador estiver sendo adicionado, o contador não será adicionado à consulta. Se esse status for retornado após a coleta de dados, os dados desse contador serão inválidos. Sempre que os dados são solicitados, o PDH tenta obter esses dados do contador.                                             |
| DADOS INVÁLIDOS DO PDH \_ CSTATUS \_ \_        | O contador foi encontrado com êxito, mas os dados retornados não são válidos. Esse erro poderá ocorrer se o valor do contador for menor que o valor anterior. (Como os valores do contador sempre são incrementados, o valor do contador é rolado para zero quando ele atinge seu valor máximo.) Outra causa possível é um temporizador do sistema que não está correto.                                              |
| DADOS \_ VÁLIDOS DO PDH CSTATUS \_ \_          | Os dados do contador foram retornados com êxito, mas não foram alterados da última vez em que o contador foi lido.                                                                                                                                                                                                                                                                    |
| PDH \_ CSTATUS \_ NEW \_ DATA            | Os dados do contador foram retornados com êxito e são diferentes da última vez em que o contador foi lido. PDH CSTATUS NEW DATA pode ser retornado em um contador de taxa, mesmo que a taxa resultante seja a mesma \_ \_ que a última \_ amostra. Isso porque o valor de dados brutos usado na determinação desse valor de status foi alterado, não a taxa computada.                  |
| PDH \_ MORE \_ DATA                    | O buffer fornecido não era grande o suficiente para armazenar todos os dados do contador. Aloce um buffer maior e execute a função novamente.                                                                                                                                                                                                                                              |
| ITEM \_ CSTATUS PDH \_ NÃO \_ \_ VALIDADO | O contador foi adicionado à consulta, mas não foi validado nem acessado. Nenhuma informação de status adicional neste contador está disponível.                                                                                                                                                                                                                                 |
| PDH \_ CSTATUS \_ NO \_ COUNTERNAME      | Nenhum nome de contador foi especificado na consulta.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ CSTATUS \_ NO \_ COUNTER          | Não foi possível encontrar o nome do contador especificado.                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ NO \_ OBJECT           | Não foi possível encontrar o objeto de desempenho especificado.                                                                                                                                                                                                                                                                                                                             |
| DENOMINADOR \_ NEGATIVO PDH CALC \_ \_   | Um contador tem um valor de denominador negativo.                                                                                                                                                                                                                                                                                                                                      |
| BASE DE TEMPO NEGATIVA DO PDH \_ CALC \_ \_      | Um contador tem um valor negativo de base de tempo.                                                                                                                                                                                                                                                                                                                                         |
| VALOR NEGATIVO \_ DE PDH CALC \_ \_         | Um contador tem um valor negativo.                                                                                                                                                                                                                                                                                                                                                  |
| PDH \_ CSTATUS \_ NO \_ COUNTERNAME      | Nenhum caminho de contador foi especificado.                                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ BAD \_ COUNTERNAME     | O formato do caminho do contador está incorreto.                                                                                                                                                                                                                                                                                                                                            |



 

 

 



