---
description: Descreva a instrução SELECT para uma consulta de dados.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Instrução SELECT para consultas de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763092"
---
# <a name="select-statement-for-data-queries"></a><span data-ttu-id="35e01-103">Instrução SELECT para consultas de dados</span><span class="sxs-lookup"><span data-stu-id="35e01-103">SELECT Statement for Data Queries</span></span>

<span data-ttu-id="35e01-104">Você pode usar uma variedade de instruções SELECT para consultar informações.</span><span class="sxs-lookup"><span data-stu-id="35e01-104">You can use a variety of SELECT statements to query for information.</span></span> <span data-ttu-id="35e01-105">As instruções podem ser instruções básicas ou podem ser mais restritivas para restringir o conjunto de resultados retornado pela consulta.</span><span class="sxs-lookup"><span data-stu-id="35e01-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="35e01-106">O exemplo a seguir é uma instrução SELECT básica que é usada para consultar dados.</span><span class="sxs-lookup"><span data-stu-id="35e01-106">The following example is a basic SELECT statement that is used to query for data.</span></span>


```sql
SELECT * FROM Class
```



<span data-ttu-id="35e01-107">Essa instrução retorna instâncias da classe especificada e de qualquer uma de suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="35e01-107">This statement returns instances of the specified class and any of its subclasses.</span></span> <span data-ttu-id="35e01-108">Todas as propriedades do sistema e definidas pelo usuário para as classes são incluídas.</span><span class="sxs-lookup"><span data-stu-id="35e01-108">All of the system and user-defined properties for the classes are included.</span></span> <span data-ttu-id="35e01-109">Se uma propriedade do sistema não for relevante para uma consulta específica, ela conterá **NULL**.</span><span class="sxs-lookup"><span data-stu-id="35e01-109">If a system property is not relevant for a particular query, it contains **NULL**.</span></span>

<span data-ttu-id="35e01-110">Você pode usar várias técnicas para reduzir a largura de banda necessária para recuperar o conjunto de resultados, se a execução da consulta resultar em muita sobrecarga e o usuário estiver interessado apenas em um subconjunto das propriedades.</span><span class="sxs-lookup"><span data-stu-id="35e01-110">You can use several techniques to reduce the bandwidth required to retrieve the result set, if the execution of the query results in too much overhead and the user is only interested in a subset of the properties.</span></span> <span data-ttu-id="35e01-111">Primeiro, as consultas podem substituir o asterisco pelas propriedades desejadas.</span><span class="sxs-lookup"><span data-stu-id="35e01-111">First, queries can replace the asterisk with the desired properties.</span></span>

<span data-ttu-id="35e01-112">O exemplo a seguir mostra como consultar propriedades específicas.</span><span class="sxs-lookup"><span data-stu-id="35e01-112">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM class
```



<span data-ttu-id="35e01-113">O conjunto de resultados inclui todas as propriedades do sistema e as propriedades não do sistema especificadas.</span><span class="sxs-lookup"><span data-stu-id="35e01-113">The result set includes all system properties and the specified nonsystem properties.</span></span>

<span data-ttu-id="35e01-114">Outra técnica para restringir o escopo do conjunto de resultados de uma consulta é usar a propriedade do sistema de [**\_ \_ classe**](wmi-system-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="35e01-114">Another technique for narrowing the scope of a query's result set is to use the [**\_\_CLASS**](wmi-system-properties.md) system property.</span></span> <span data-ttu-id="35e01-115">Por padrão, as consultas retornam todas as instâncias da classe especificada e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="35e01-115">Queries by default return all instances of the specified class and its subclasses.</span></span> <span data-ttu-id="35e01-116">Você pode usar a propriedade do sistema de **\_ \_ classe** para solicitar apenas instâncias da classe especificada, excluindo suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="35e01-116">You can use the **\_\_CLASS** system property to request only instances of the specified class, excluding its subclasses.</span></span>

<span data-ttu-id="35e01-117">O exemplo a seguir mostra como usar a propriedade do sistema de [**\_ \_ classe**](wmi-system-properties.md) em uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="35e01-117">The following example shows how to use the [**\_\_CLASS**](wmi-system-properties.md) system property in a WHERE clause.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



<span data-ttu-id="35e01-118">Você também pode usar a propriedade do sistema de [**\_ \_ classe**](wmi-system-properties.md) para restringir o conjunto de resultados a instâncias de subclasses específicas.</span><span class="sxs-lookup"><span data-stu-id="35e01-118">You can also use the [**\_\_CLASS**](wmi-system-properties.md) system property to restrict the result set to instances of particular subclasses.</span></span>

<span data-ttu-id="35e01-119">O exemplo a seguir mostra como restringir o conjunto de resultados para instâncias de subclasses específicas.</span><span class="sxs-lookup"><span data-stu-id="35e01-119">The following example shows how to restrict the result set to instances of particular subclasses.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> <span data-ttu-id="35e01-120">Se você construir uma consulta com um caminho inválido para um objeto inserido, sua consulta não retornará um erro ou nenhum resultado.</span><span class="sxs-lookup"><span data-stu-id="35e01-120">If you construct a query with an invalid path for an embedded object, your query does not return an error or any results.</span></span>

 

<span data-ttu-id="35e01-121">O exemplo a seguir retorna uma instância de **MainClass**, supondo que uma instância de **MainClass** exista contendo o objeto inserido **EmbedObj** com uma propriedade **P \_ UInt32** igual a "70011".</span><span class="sxs-lookup"><span data-stu-id="35e01-121">The following example returns an instance of **MainClass**, assuming that an instance of **MainClass** exists containing the embedded object **EmbedObj** with a property **P\_Uint32** that is equal to "70011".</span></span>


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



<span data-ttu-id="35e01-122">O exemplo a seguir não retorna nenhum resultado e não retorna um erro, supondo que o objeto inserido **EmbedObj** na instância de **MainClass** não tenha uma propriedade **inválida**.</span><span class="sxs-lookup"><span data-stu-id="35e01-122">The following example returns no results and does not return an error, assuming that the embedded object **EmbedObj** in the instance of **MainClass** does not have a property **INVALID**.</span></span>


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



