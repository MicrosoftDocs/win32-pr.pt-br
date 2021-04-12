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
# <a name="associators-of-statement"></a>ASSOCIADOres de instrução

A instrução ASSOCIATORS OF recupera todas as instâncias associadas a uma instância de origem específica. As instâncias que são recuperadas são chamadas de pontos de extremidade. Cada ponto de extremidade é retornado quantas vezes houver associações entre ele e o objeto de origem. Por exemplo, suponha que existam instâncias A, B, X e Y. Existem duas instâncias de associação, uma que vincula A e X e outra que vincula B e Y. A consulta a seguir retorna o único ponto de extremidade X:


```sql
ASSOCIATORS OF {A}
```



No entanto, se houver outra associação vinculando A e X, a consulta acima retornará dois pontos de extremidade X.

A sintaxe básica para a instrução ASSOCIATORS OF é:

``` syntax
ASSOCIATORS OF {ObjectPath}
```

Observe que as chaves fazem parte da sintaxe. Qualquer caminho de objeto válido pode ser usado para ObjectPath. Os tokens no caminho do objeto não podem conter nenhum espaço em branco. Por exemplo, a consulta na lista a seguir retorna as instâncias associadas ao disco lógico especificado:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Assim como acontece com a [instrução SELECT](select-statement-for-data-queries.md), um associador de instrução pode incluir uma [cláusula WHERE](where-clause.md), mas a cláusula WHERE para uma instrução ASSOCIATORS of é muito diferente da cláusula SELECT statementWHERE.

A [cláusula WHERE](where-clause.md) da instrução ASSOCIATORS of pode incluir uma ou mais das seguintes palavras-chave predefinidas e seus valores:


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



Observe que as subcláusulas opcionais não são separadas por vírgulas.

A palavra-chave **AssocClass** indica que os pontos de extremidade retornados devem ser associados à origem por meio da classe especificada ou de uma de suas classes derivadas. Por exemplo, a consulta na lista a seguir retorna somente os pontos de extremidade associados à origem por meio da classe de associação [**Win32 \_ SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) ou qualquer uma de suas classes derivadas:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

A palavra-chave **ClassDefsOnly** indica que a cláusula retorna um conjunto de resultados de objetos de definição de classe em vez de instâncias reais das classes. Esses objetos são as definições das classes às quais as instâncias de ponto de extremidade pertencem. Por exemplo, a consulta na lista a seguir retorna definições para o [**\_ diretório Win32**](/windows/desktop/CIMWin32Prov/win32-directory) e as classes [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

As palavras-chave **ClassDefsOnly** e **ResultClass** são mutuamente exclusivas. Usá-los juntos causa um erro de consulta inválido.

A palavra-chave **RequiredAssocQualifier** indica que os pontos de extremidade retornados devem ser associados ao objeto de origem por meio de uma classe de associação que inclui o qualificador especificado. Esse tipo de filtragem é usado para eliminar intervalos amplos de pontos de extremidade, a menos que os pontos de extremidade estejam associados ao destino por meio de um determinado conjunto de classes de associação marcadas. Por exemplo, a consulta na lista a seguir retorna instâncias de ponto de extremidade se a classe de associação inclui um qualificador chamado **Associação**.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

A palavra-chave **RequiredQualifier** indica que os pontos de extremidade retornados associados ao objeto de origem devem incluir o qualificador especificado. A palavra-chave **RequiredQualifier** pode ser usada para incluir tipos específicos de instâncias no conjunto de resultados. Por exemplo, a consulta na lista a seguir retorna instâncias de ponto de extremidade que incluem um qualificador chamado [**locale**](swbemobjectpath-locale.md).

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

A palavra-chave **ResultClass** indica que os pontos de extremidade retornados associados ao objeto de origem devem pertencer ou ser derivados da classe especificada. Por exemplo, a consulta na lista a seguir retorna instâncias de ponto de extremidade derivadas da classe de [**\_ diretório CIM**](/windows/desktop/CIMWin32Prov/cim-directory) :

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

As palavras-chave **ClassDefsOnly** e **ResultClass** são mutuamente exclusivas. Usá-los juntos causa um erro de consulta inválido.

A palavra-chave **ResultRole** indica que os pontos de extremidade retornados devem reproduzir uma função específica em sua associação com o objeto de origem. A função é definida pela propriedade especificada, uma propriedade de referência do tipo [ref](references.md). Por exemplo, a palavra-chave **ResultRole** pode ser usada para recuperar todos os pontos de extremidade que têm a propriedade **GroupComponent** em sua associação com um objeto de origem, como ilustra a consulta a seguir.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

A palavra-chave **role** indica que os pontos de extremidade retornados participam de uma associação com o objeto de origem em que o objeto de origem desempenha uma função específica. A função é definida pela propriedade especificada, uma propriedade de referência do tipo **ref**. Por exemplo, a palavra-chave **role** pode ser usada para recuperar todos os pontos de extremidade associados a um objeto de origem que tem a propriedade **GroupComponent** , como ilustra a consulta a seguir.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Consultá
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Da
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> Consultas complexas não podem usar "and" ou "or" para separar palavras-chave para ASSOCIAdores de e [referências de](references-of-statement.md) instruções. Além disso, o sinal de igual é o único operador válido que pode ser usado em tais consultas. Por exemplo, a seguinte consulta é válido:

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> Os exemplos a seguir não são válidos. O primeiro exemplo não usa o sinal de igual e o segundo exemplo tenta erroneamente usar a palavra-chave **and** .

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
