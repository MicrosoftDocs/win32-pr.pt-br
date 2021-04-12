---
description: Recupera todas as instâncias associadas a uma instância de origem específica.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: ASSOCIADOres de instrução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297176"
---
# <a name="associators-of-statement"></a><span data-ttu-id="66a66-103">ASSOCIADOres de instrução</span><span class="sxs-lookup"><span data-stu-id="66a66-103">ASSOCIATORS OF Statement</span></span>

<span data-ttu-id="66a66-104">A instrução ASSOCIATORS OF recupera todas as instâncias associadas a uma instância de origem específica.</span><span class="sxs-lookup"><span data-stu-id="66a66-104">The ASSOCIATORS OF statement retrieves all instances that are associated with a particular source instance.</span></span> <span data-ttu-id="66a66-105">As instâncias que são recuperadas são chamadas de pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="66a66-105">The instances that are retrieved are referred to as the endpoints.</span></span> <span data-ttu-id="66a66-106">Cada ponto de extremidade é retornado quantas vezes houver associações entre ele e o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="66a66-106">Each endpoint is returned as many times as there are associations between it and the source object.</span></span> <span data-ttu-id="66a66-107">Por exemplo, suponha que existam instâncias A, B, X e Y. Existem duas instâncias de associação, uma que vincula A e X e outra que vincula B e Y. A consulta a seguir retorna o único ponto de extremidade X:</span><span class="sxs-lookup"><span data-stu-id="66a66-107">For example, assume there are instances A, B, X, and Y. Two association instances exist, one that links A and X and another that links B and Y. The following query returns the single endpoint X:</span></span>


```sql
ASSOCIATORS OF {A}
```



<span data-ttu-id="66a66-108">No entanto, se houver outra associação vinculando A e X, a consulta acima retornará dois pontos de extremidade X.</span><span class="sxs-lookup"><span data-stu-id="66a66-108">However, if there is another association linking A and X, the above query returns two X endpoints.</span></span>

<span data-ttu-id="66a66-109">A sintaxe básica para a instrução ASSOCIATORS OF é:</span><span class="sxs-lookup"><span data-stu-id="66a66-109">The basic syntax for the ASSOCIATORS OF statement is:</span></span>

``` syntax
ASSOCIATORS OF {ObjectPath}
```

<span data-ttu-id="66a66-110">Observe que as chaves fazem parte da sintaxe.</span><span class="sxs-lookup"><span data-stu-id="66a66-110">Note that the braces are part of the syntax.</span></span> <span data-ttu-id="66a66-111">Qualquer caminho de objeto válido pode ser usado para ObjectPath.</span><span class="sxs-lookup"><span data-stu-id="66a66-111">Any valid object path can be used for ObjectPath.</span></span> <span data-ttu-id="66a66-112">Os tokens no caminho do objeto não podem conter nenhum espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="66a66-112">The tokens within the object path cannot contain any white space.</span></span> <span data-ttu-id="66a66-113">Por exemplo, a consulta na lista a seguir retorna as instâncias associadas ao disco lógico especificado:</span><span class="sxs-lookup"><span data-stu-id="66a66-113">For example, the query in the following list returns instances that are associated with the specified logical disk:</span></span>

<dl> <dt>

<span data-ttu-id="66a66-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá</span><span class="sxs-lookup"><span data-stu-id="66a66-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span data-ttu-id="66a66-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da</span><span class="sxs-lookup"><span data-stu-id="66a66-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="66a66-116">Assim como acontece com a [instrução SELECT](select-statement-for-data-queries.md), um associador de instrução pode incluir uma [cláusula WHERE](where-clause.md), mas a cláusula WHERE para uma instrução ASSOCIATORS of é muito diferente da cláusula SELECT statementWHERE.</span><span class="sxs-lookup"><span data-stu-id="66a66-116">As with the [SELECT statement](select-statement-for-data-queries.md), an ASSOCIATORS OF statement can include a [WHERE clause](where-clause.md), but the WHERE clause for an ASSOCIATORS OF statement is very different from the SELECT statementWHERE clause.</span></span>

<span data-ttu-id="66a66-117">A [cláusula WHERE](where-clause.md) da instrução ASSOCIATORS of pode incluir uma ou mais das seguintes palavras-chave predefinidas e seus valores:</span><span class="sxs-lookup"><span data-stu-id="66a66-117">The [WHERE clause](where-clause.md) of the ASSOCIATORS OF statement can include one or more of the following predefined keywords and their values:</span></span>


```sql
ASSOCIATORS OF {ObjectPath} WHERE
    AssocClass = AssocClassName
    ClassDefsOnly
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
```



<span data-ttu-id="66a66-118">Observe que as subcláusulas opcionais não são separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="66a66-118">Note that the optional subclauses are not separated by commas.</span></span>

<span data-ttu-id="66a66-119">A palavra-chave **AssocClass** indica que os pontos de extremidade retornados devem ser associados à origem por meio da classe especificada ou de uma de suas classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="66a66-119">The **AssocClass** keyword indicates that the returned endpoints must be associated with the source through the specified class or one of its derived classes.</span></span> <span data-ttu-id="66a66-120">Por exemplo, a consulta na lista a seguir retorna somente os pontos de extremidade associados à origem por meio da classe de associação [**Win32 \_ SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) ou qualquer uma de suas classes derivadas:</span><span class="sxs-lookup"><span data-stu-id="66a66-120">For example, the query in the following list returns only endpoints that are associated with the source through the [**Win32\_SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) association class or any of its derived classes:</span></span>

<dl> <dt>

<span data-ttu-id="66a66-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá</span><span class="sxs-lookup"><span data-stu-id="66a66-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span data-ttu-id="66a66-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da</span><span class="sxs-lookup"><span data-stu-id="66a66-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="66a66-123">A palavra-chave **ClassDefsOnly** indica que a cláusula retorna um conjunto de resultados de objetos de definição de classe em vez de instâncias reais das classes.</span><span class="sxs-lookup"><span data-stu-id="66a66-123">The **ClassDefsOnly** keyword indicates that the clause returns a result set of class definition objects rather than actual instances of the classes.</span></span> <span data-ttu-id="66a66-124">Esses objetos são as definições das classes às quais as instâncias de ponto de extremidade pertencem.</span><span class="sxs-lookup"><span data-stu-id="66a66-124">These objects are the definitions of classes to which the endpoint instances belong.</span></span> <span data-ttu-id="66a66-125">Por exemplo, a consulta na lista a seguir retorna definições para o [**\_ diretório Win32**](/windows/desktop/CIMWin32Prov/win32-directory) e as classes [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) :</span><span class="sxs-lookup"><span data-stu-id="66a66-125">For example, the query in the following list returns definitions for the [**Win32\_Directory**](/windows/desktop/CIMWin32Prov/win32-directory) and [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) classes:</span></span>

<dl> <dt>

<span data-ttu-id="66a66-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá</span><span class="sxs-lookup"><span data-stu-id="66a66-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span data-ttu-id="66a66-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da</span><span class="sxs-lookup"><span data-stu-id="66a66-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

<span data-ttu-id="66a66-128">As palavras-chave **ClassDefsOnly** e **ResultClass** são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="66a66-128">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="66a66-129">Usá-los juntos causa um erro de consulta inválido.</span><span class="sxs-lookup"><span data-stu-id="66a66-129">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="66a66-130">A palavra-chave **RequiredAssocQualifier** indica que os pontos de extremidade retornados devem ser associados ao objeto de origem por meio de uma classe de associação que inclui o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="66a66-130">The **RequiredAssocQualifier** keyword indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span> <span data-ttu-id="66a66-131">Esse tipo de filtragem é usado para eliminar intervalos amplos de pontos de extremidade, a menos que os pontos de extremidade estejam associados ao destino por meio de um determinado conjunto de classes de associação marcadas.</span><span class="sxs-lookup"><span data-stu-id="66a66-131">This type of filtering is used to eliminate broad ranges of endpoints unless the endpoints are associated with the target through a particular set of tagged association classes.</span></span> <span data-ttu-id="66a66-132">Por exemplo, a consulta na lista a seguir retorna instâncias de ponto de extremidade se a classe de associação inclui um qualificador chamado **Associação**.</span><span class="sxs-lookup"><span data-stu-id="66a66-132">For example, the query in the following list returns endpoint instances if the association class includes a qualifier called **Association**.</span></span>

<dl> <dt>

<span data-ttu-id="66a66-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá</span><span class="sxs-lookup"><span data-stu-id="66a66-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span data-ttu-id="66a66-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da</span><span class="sxs-lookup"><span data-stu-id="66a66-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="66a66-135">A palavra-chave **RequiredQualifier** indica que os pontos de extremidade retornados associados ao objeto de origem devem incluir o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="66a66-135">The **RequiredQualifier** keyword indicates that the returned endpoints associated with the source object must include the specified qualifier.</span></span> <span data-ttu-id="66a66-136">A palavra-chave **RequiredQualifier** pode ser usada para incluir tipos específicos de instâncias no conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="66a66-136">The **RequiredQualifier** keyword can be used to include particular types of instances in the result set.</span></span> <span data-ttu-id="66a66-137">Por exemplo, a consulta na lista a seguir retorna instâncias de ponto de extremidade que incluem um qualificador chamado [**locale**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="66a66-137">For example, the query in the following list returns endpoint instances that include a qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span>

<dl> <dt>

<span data-ttu-id="66a66-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá</span><span class="sxs-lookup"><span data-stu-id="66a66-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span data-ttu-id="66a66-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da</span><span class="sxs-lookup"><span data-stu-id="66a66-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="66a66-140">A palavra-chave **ResultClass** indica que os pontos de extremidade retornados associados ao objeto de origem devem pertencer ou ser derivados da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="66a66-140">The **ResultClass** keyword indicates that the returned endpoints associated with the source object must belong to or be derived from the specified class.</span></span> <span data-ttu-id="66a66-141">Por exemplo, a consulta na lista a seguir retorna instâncias de ponto de extremidade derivadas da classe de [**\_ diretório CIM**](/windows/desktop/CIMWin32Prov/cim-directory) :</span><span class="sxs-lookup"><span data-stu-id="66a66-141">For example, the query in the following list returns endpoint instances that are derived from the [**CIM\_Directory**](/windows/desktop/CIMWin32Prov/cim-directory) class:</span></span>

<dl> <dt>

<span data-ttu-id="66a66-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá</span><span class="sxs-lookup"><span data-stu-id="66a66-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span data-ttu-id="66a66-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da</span><span class="sxs-lookup"><span data-stu-id="66a66-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

<span data-ttu-id="66a66-144">As palavras-chave **ClassDefsOnly** e **ResultClass** são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="66a66-144">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="66a66-145">Usá-los juntos causa um erro de consulta inválido.</span><span class="sxs-lookup"><span data-stu-id="66a66-145">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="66a66-146">A palavra-chave **ResultRole** indica que os pontos de extremidade retornados devem reproduzir uma função específica em sua associação com o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="66a66-146">The **ResultRole** keyword indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="66a66-147">A função é definida pela propriedade especificada, uma propriedade de referência do tipo [ref](references.md). Por exemplo, a palavra-chave **ResultRole** pode ser usada para recuperar todos os pontos de extremidade que têm a propriedade **GroupComponent** em sua associação com um objeto de origem, como ilustra a consulta a seguir.</span><span class="sxs-lookup"><span data-stu-id="66a66-147">The role is defined by the specified property, a reference property of type [ref](references.md). For example, the **ResultRole** keyword can be used to retrieve all endpoints that have the **GroupComponent** property in their association with a source object, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="66a66-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá</span><span class="sxs-lookup"><span data-stu-id="66a66-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span data-ttu-id="66a66-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da</span><span class="sxs-lookup"><span data-stu-id="66a66-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="66a66-150">A palavra-chave **role** indica que os pontos de extremidade retornados participam de uma associação com o objeto de origem em que o objeto de origem desempenha uma função específica.</span><span class="sxs-lookup"><span data-stu-id="66a66-150">The **Role** keyword indicates that the returned endpoints participate in an association with the source object where the source object plays a particular role.</span></span> <span data-ttu-id="66a66-151">A função é definida pela propriedade especificada, uma propriedade de referência do tipo **ref**. Por exemplo, a palavra-chave **role** pode ser usada para recuperar todos os pontos de extremidade associados a um objeto de origem que tem a propriedade **GroupComponent** , como ilustra a consulta a seguir.</span><span class="sxs-lookup"><span data-stu-id="66a66-151">The role is defined by the specified property, a reference property of type **ref**. For example, the **Role** keyword can be used to retrieve all endpoints associated with a source object that have the **GroupComponent** property, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="66a66-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá</span><span class="sxs-lookup"><span data-stu-id="66a66-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span data-ttu-id="66a66-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da</span><span class="sxs-lookup"><span data-stu-id="66a66-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> <span data-ttu-id="66a66-154">Consultas complexas não podem usar "and" ou "or" para separar palavras-chave para ASSOCIAdores de e [referências de](references-of-statement.md) instruções.</span><span class="sxs-lookup"><span data-stu-id="66a66-154">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and [REFERENCES OF](references-of-statement.md) statements.</span></span> <span data-ttu-id="66a66-155">Além disso, o sinal de igual é o único operador válido que pode ser usado em tais consultas.</span><span class="sxs-lookup"><span data-stu-id="66a66-155">Furthermore, the equal sign is the only valid operator that can be used in such queries.</span></span> <span data-ttu-id="66a66-156">Por exemplo, a seguinte consulta é válido:</span><span class="sxs-lookup"><span data-stu-id="66a66-156">For example, the following query is valid:</span></span>

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> <span data-ttu-id="66a66-157">Os exemplos a seguir não são válidos.</span><span class="sxs-lookup"><span data-stu-id="66a66-157">The next examples are not valid.</span></span> <span data-ttu-id="66a66-158">O primeiro exemplo não usa o sinal de igual e o segundo exemplo tenta erroneamente usar a palavra-chave **and** .</span><span class="sxs-lookup"><span data-stu-id="66a66-158">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword.</span></span>

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
