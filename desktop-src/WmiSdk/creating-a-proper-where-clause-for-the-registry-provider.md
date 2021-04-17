---
title: Criando uma cláusula WHERE para o provedor de registro
description: Os principais pontos a serem considerados ao criar uma cláusula WHERE adequada para o provedor de registro do sistema é que cada consulta de evento deve ser completa e explícita. A conclusão da falha e explícita resultará em uma mensagem de erro.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d1c7031d376fbd6b9d946fb9e41561ce4c4b1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461314"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Criando uma cláusula WHERE para o provedor de registro

Os principais pontos a serem considerados ao criar uma cláusula WHERE adequada para o provedor de registro do sistema é que cada consulta de evento deve ser completa e explícita. A conclusão da falha e explícita resultará em uma mensagem de erro.

Para ser concluída, cada consulta de evento no parâmetro *bstrQuery* de [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) deve conter uma cláusula WHERE que inclua cada uma das propriedades na classe de evento especificada.

O exemplo a seguir mostra como definir *bstrQuery* para se registrar em eventos de alteração de árvore na \_ árvore "hKey local \_ Machine \\ software".


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Para ser explícito, o provedor deve ser capaz de inferir da consulta uma lista de valores possíveis para cada propriedade na classe de evento.

O exemplo a seguir mostra a consulta de evento que registra corretamente para eventos de alteração de árvore.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



Veja a seguir um exemplo de um registro incorreto.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Como não há como avaliar os valores possíveis para cada uma das propriedades, o WMI rejeita com o erro WBEM \_ E \_ muito \_ amplo qualquer consulta que não tenha uma cláusula WHERE ou se a cláusula Where for muito ampla para ser usada.

 

 



