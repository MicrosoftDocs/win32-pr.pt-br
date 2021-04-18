---
description: As referências de instrução recuperam todas as instâncias de associação que se referem a uma instância de origem específica.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: REFERÊNCIAS da instrução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752174"
---
# <a name="references-of-statement"></a><span data-ttu-id="50b7a-103">REFERÊNCIAS da instrução</span><span class="sxs-lookup"><span data-stu-id="50b7a-103">REFERENCES OF Statement</span></span>

<span data-ttu-id="50b7a-104">As referências de instrução recuperam todas as instâncias de associação que se referem a uma instância de origem específica.</span><span class="sxs-lookup"><span data-stu-id="50b7a-104">The REFERENCES OF statement retrieves all association instances that refer to a particular source instance.</span></span> <span data-ttu-id="50b7a-105">As referências de instrução são semelhantes aos ASSOCIADOres de instrução em sua sintaxe.</span><span class="sxs-lookup"><span data-stu-id="50b7a-105">The REFERENCES OF statement is similar to the ASSOCIATORS OF statement in its syntax.</span></span> <span data-ttu-id="50b7a-106">No entanto, em vez de recuperar instâncias de ponto de extremidade, ele recupera as instâncias de associação intermediárias.</span><span class="sxs-lookup"><span data-stu-id="50b7a-106">However, rather than retrieving endpoint instances, it retrieves the intervening association instances.</span></span>

<span data-ttu-id="50b7a-107">As referências da cláusula WHERE podem incluir uma ou mais das seguintes palavras-chave predefinidas e seus valores:</span><span class="sxs-lookup"><span data-stu-id="50b7a-107">The REFERENCES OF WHERE clause can include one or more of the following predefined keywords and their values:</span></span>


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



<span data-ttu-id="50b7a-108">Para especificar um objeto de origem, use qualquer caminho de objeto válido para SourceObject.</span><span class="sxs-lookup"><span data-stu-id="50b7a-108">To specify a source object, use any valid object path for SourceObject.</span></span> <span data-ttu-id="50b7a-109">Assim como acontece com a instrução SELECT, a cláusula WHERE é opcional e é usada para definir ainda mais a consulta.</span><span class="sxs-lookup"><span data-stu-id="50b7a-109">As with the SELECT statement, the WHERE clause is optional and is used to further define the query.</span></span> <span data-ttu-id="50b7a-110">Ou seja, a seguinte instrução é perfeitamente válida:</span><span class="sxs-lookup"><span data-stu-id="50b7a-110">That is, the following statement is perfectly valid:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



<span data-ttu-id="50b7a-111">A palavra-chave **ClassDefsOnly** indica que a instrução retorna um conjunto de resultados de objetos de definição de classe em vez de instâncias reais das classes de associação.</span><span class="sxs-lookup"><span data-stu-id="50b7a-111">The **ClassDefsOnly** keyword indicates that the statement returns a result set of class definition objects rather than actual instances of the association classes.</span></span> <span data-ttu-id="50b7a-112">Esses objetos contêm definições de classes às quais as instâncias que fazem referência ao objeto de origem pertencem.</span><span class="sxs-lookup"><span data-stu-id="50b7a-112">These objects contain definitions of classes to which the instances that reference the source object belong.</span></span> <span data-ttu-id="50b7a-113">Por exemplo, a instrução a seguir retorna definições para as classes **AdapterDriver** e **AdapterProtocol** :</span><span class="sxs-lookup"><span data-stu-id="50b7a-113">For example, the following statement returns definitions for the **AdapterDriver** and **AdapterProtocol** classes:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



<span data-ttu-id="50b7a-114">A palavra-chave **RequiredQualifier** indica que os objetos de associação retornados devem incluir o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="50b7a-114">The **RequiredQualifier** keyword indicates that the returned association objects must include the specified qualifier.</span></span> <span data-ttu-id="50b7a-115">A palavra-chave **RequiredQualifier** pode ser usada para incluir instâncias específicas de associações no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="50b7a-115">The **RequiredQualifier** keyword can be used to include particular instances of associations in the result set.</span></span> <span data-ttu-id="50b7a-116">Por exemplo, a instrução a seguir retorna instâncias de associação que incluem um qualificador chamado **AdapterTag**:</span><span class="sxs-lookup"><span data-stu-id="50b7a-116">For example, the following statement returns association instances that include a qualifier called **AdapterTag**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



<span data-ttu-id="50b7a-117">A palavra-chave **ResultClass** indica que os objetos de associação retornados devem pertencer ou ser derivados da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="50b7a-117">The **ResultClass** keyword indicates that the returned association objects must belong to or be derived from the specified class.</span></span> <span data-ttu-id="50b7a-118">Por exemplo, a instrução a seguir retorna associações da classe **AdapterDriver** ou subclasses de **AdapterDriver**:</span><span class="sxs-lookup"><span data-stu-id="50b7a-118">For example, the following statement returns associations of the **AdapterDriver** class or subclasses of **AdapterDriver**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



<span data-ttu-id="50b7a-119">As palavras-chave **ClassDefsOnly** e **ResultClass** são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="50b7a-119">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="50b7a-120">Usá-los juntos causa um erro de consulta inválido.</span><span class="sxs-lookup"><span data-stu-id="50b7a-120">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="50b7a-121">A palavra-chave **role** indica que as associações retornadas são apenas aquelas nas quais o objeto de origem desempenha uma função específica.</span><span class="sxs-lookup"><span data-stu-id="50b7a-121">The **Role** keyword indicates that the returned associations are only those in which the source object plays a particular role.</span></span> <span data-ttu-id="50b7a-122">A função é definida pela propriedade especificada, uma propriedade de referência do tipo [ref](references.md). A palavra-chave **role** é útil em associações em que um determinado objeto pode reproduzir uma função em alguns casos e outra função em outros, como em associações hierárquicas.</span><span class="sxs-lookup"><span data-stu-id="50b7a-122">The role is defined by the specified property, a reference property of type [ref](references.md). The **Role** keyword is useful in associations where a certain object can play one role in some cases and another role in others, such as in hierarchical associations.</span></span> <span data-ttu-id="50b7a-123">A palavra-chave **role** pode ser usada para recuperar todas as associações nas quais o objeto de origem desempenha a função de pai, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="50b7a-123">The **Role** keyword can be used to retrieve all of the associations in which the source object plays the role of parent, for example.</span></span> <span data-ttu-id="50b7a-124">A instrução a seguir ilustra a sintaxe para recuperar associações que têm uma propriedade **pai** que faz referência ao objeto de origem como o pai:</span><span class="sxs-lookup"><span data-stu-id="50b7a-124">The following statement illustrates the syntax for retrieving associations that have a **parent** property referencing the source object as the parent:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> <span data-ttu-id="50b7a-125">Consultas complexas não podem usar "and" ou "or" para separar palavras-chave para ASSOCIAdores de e referências de instruções.</span><span class="sxs-lookup"><span data-stu-id="50b7a-125">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and REFERENCES OF statements.</span></span> <span data-ttu-id="50b7a-126">Além disso, o sinal de igual é o único operador válido que pode ser usado com as palavras-chave nessas consultas.</span><span class="sxs-lookup"><span data-stu-id="50b7a-126">Furthermore, the equal sign is the only valid operator that can be used with the keywords in these queries.</span></span> <span data-ttu-id="50b7a-127">Por exemplo, a seguinte consulta é válido:</span><span class="sxs-lookup"><span data-stu-id="50b7a-127">For example, the following query is valid:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> <span data-ttu-id="50b7a-128">Os exemplos a seguir não são válidos.</span><span class="sxs-lookup"><span data-stu-id="50b7a-128">The next examples are not valid.</span></span> <span data-ttu-id="50b7a-129">O primeiro exemplo não usa o sinal de igual e o segundo exemplo tenta erroneamente usar a palavra-chave **and** :</span><span class="sxs-lookup"><span data-stu-id="50b7a-129">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



