---
title: Criando uma cláusula WHERE para o provedor do Registro
description: Os principais pontos a serem considerados ao criar uma cláusula WHERE adequada para o provedor do Registro do Sistema são que cada consulta de evento deve ser completa e explícita. A falha ao ser concluída e explícita resultará em uma mensagem de erro.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0fc037b746233bd9eb2f9bdd4afad942d07dc832b4dfd60cd9ca6ae9f273efca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679826"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Criando uma cláusula WHERE para o provedor do Registro

Os principais pontos a serem considerados ao criar uma cláusula WHERE adequada para o provedor do Registro do Sistema são que cada consulta de evento deve ser completa e explícita. A falha ao ser concluída e explícita resultará em uma mensagem de erro.

Para ser concluída, cada consulta de evento no parâmetro *bstrQuery* [**de ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) deve conter uma cláusula WHERE que inclui cada uma das propriedades na classe de evento especificada.

O exemplo a seguir mostra como definir *bstrQuery para* registrar eventos de alteração de árvore na árvore "HKEY \_ LOCAL MACHINE \_ \\ Software".


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Para ser explícito, o provedor deve ser capaz de inferir da consulta uma lista de valores possíveis para cada propriedade na classe de evento.

O exemplo a seguir mostra a consulta de evento que se registra corretamente para eventos de alteração de árvore.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



A seguir está um exemplo de um registro incorreto.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Como não há nenhuma maneira de avaliar os valores possíveis para cada uma das propriedades, o WMI rejeita com o erro WBEM E TOO BROAD qualquer consulta que não tenha uma cláusula WHERE ou se a cláusula WHERE for muito ampla para ser \_ \_ de qualquer \_ uso.

 

 



