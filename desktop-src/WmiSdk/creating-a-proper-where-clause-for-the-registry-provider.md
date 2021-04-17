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
# <a name="creating-a-where-clause-for-the-registry-provider"></a><span data-ttu-id="8d19a-104">Criando uma cláusula WHERE para o provedor de registro</span><span class="sxs-lookup"><span data-stu-id="8d19a-104">Creating a WHERE clause for the registry provider</span></span>

<span data-ttu-id="8d19a-105">Os principais pontos a serem considerados ao criar uma cláusula WHERE adequada para o provedor de registro do sistema é que cada consulta de evento deve ser completa e explícita.</span><span class="sxs-lookup"><span data-stu-id="8d19a-105">The main points to consider when creating a proper WHERE clause for the System Registry provider is that each event query must be complete and explicit.</span></span> <span data-ttu-id="8d19a-106">A conclusão da falha e explícita resultará em uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="8d19a-106">Failure to be complete and explicit will result in an error message.</span></span>

<span data-ttu-id="8d19a-107">Para ser concluída, cada consulta de evento no parâmetro *bstrQuery* de [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) deve conter uma cláusula WHERE que inclua cada uma das propriedades na classe de evento especificada.</span><span class="sxs-lookup"><span data-stu-id="8d19a-107">To be complete, each event query in the *bstrQuery* parameter of [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) must contain a WHERE clause that includes each of the properties in the specified event class.</span></span>

<span data-ttu-id="8d19a-108">O exemplo a seguir mostra como definir *bstrQuery* para se registrar em eventos de alteração de árvore na \_ árvore "hKey local \_ Machine \\ software".</span><span class="sxs-lookup"><span data-stu-id="8d19a-108">The following example shows how to set *bstrQuery* to register for tree change events in the "HKEY\_LOCAL\_MACHINE\\Software" tree.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



<span data-ttu-id="8d19a-109">Para ser explícito, o provedor deve ser capaz de inferir da consulta uma lista de valores possíveis para cada propriedade na classe de evento.</span><span class="sxs-lookup"><span data-stu-id="8d19a-109">To be explicit, the provider should be able to infer from the query a list of possible values for every property in the event class.</span></span>

<span data-ttu-id="8d19a-110">O exemplo a seguir mostra a consulta de evento que registra corretamente para eventos de alteração de árvore.</span><span class="sxs-lookup"><span data-stu-id="8d19a-110">The following example shows the event query that correctly registers for tree change events.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



<span data-ttu-id="8d19a-111">Veja a seguir um exemplo de um registro incorreto.</span><span class="sxs-lookup"><span data-stu-id="8d19a-111">The following is an example of an incorrect registration.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



<span data-ttu-id="8d19a-112">Como não há como avaliar os valores possíveis para cada uma das propriedades, o WMI rejeita com o erro WBEM \_ E \_ muito \_ amplo qualquer consulta que não tenha uma cláusula WHERE ou se a cláusula Where for muito ampla para ser usada.</span><span class="sxs-lookup"><span data-stu-id="8d19a-112">Because there is no way to evaluate the possible values for each of the properties, WMI rejects with the error WBEM\_E\_TOO\_BROAD any query that either does not have a WHERE clause or if the WHERE clause is too broad to be of any use.</span></span>

 

 



