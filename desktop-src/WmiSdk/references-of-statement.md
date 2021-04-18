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
# <a name="references-of-statement"></a>REFERÊNCIAS da instrução

As referências de instrução recuperam todas as instâncias de associação que se referem a uma instância de origem específica. As referências de instrução são semelhantes aos ASSOCIADOres de instrução em sua sintaxe. No entanto, em vez de recuperar instâncias de ponto de extremidade, ele recupera as instâncias de associação intermediárias.

As referências da cláusula WHERE podem incluir uma ou mais das seguintes palavras-chave predefinidas e seus valores:


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



Para especificar um objeto de origem, use qualquer caminho de objeto válido para SourceObject. Assim como acontece com a instrução SELECT, a cláusula WHERE é opcional e é usada para definir ainda mais a consulta. Ou seja, a seguinte instrução é perfeitamente válida:


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



A palavra-chave **ClassDefsOnly** indica que a instrução retorna um conjunto de resultados de objetos de definição de classe em vez de instâncias reais das classes de associação. Esses objetos contêm definições de classes às quais as instâncias que fazem referência ao objeto de origem pertencem. Por exemplo, a instrução a seguir retorna definições para as classes **AdapterDriver** e **AdapterProtocol** :


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



A palavra-chave **RequiredQualifier** indica que os objetos de associação retornados devem incluir o qualificador especificado. A palavra-chave **RequiredQualifier** pode ser usada para incluir instâncias específicas de associações no conjunto de resultados. Por exemplo, a instrução a seguir retorna instâncias de associação que incluem um qualificador chamado **AdapterTag**:


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



A palavra-chave **ResultClass** indica que os objetos de associação retornados devem pertencer ou ser derivados da classe especificada. Por exemplo, a instrução a seguir retorna associações da classe **AdapterDriver** ou subclasses de **AdapterDriver**:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



As palavras-chave **ClassDefsOnly** e **ResultClass** são mutuamente exclusivas. Usá-los juntos causa um erro de consulta inválido.

A palavra-chave **role** indica que as associações retornadas são apenas aquelas nas quais o objeto de origem desempenha uma função específica. A função é definida pela propriedade especificada, uma propriedade de referência do tipo [ref](references.md). A palavra-chave **role** é útil em associações em que um determinado objeto pode reproduzir uma função em alguns casos e outra função em outros, como em associações hierárquicas. A palavra-chave **role** pode ser usada para recuperar todas as associações nas quais o objeto de origem desempenha a função de pai, por exemplo. A instrução a seguir ilustra a sintaxe para recuperar associações que têm uma propriedade **pai** que faz referência ao objeto de origem como o pai:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> Consultas complexas não podem usar "and" ou "or" para separar palavras-chave para ASSOCIAdores de e referências de instruções. Além disso, o sinal de igual é o único operador válido que pode ser usado com as palavras-chave nessas consultas. Por exemplo, a seguinte consulta é válido:

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> Os exemplos a seguir não são válidos. O primeiro exemplo não usa o sinal de igual e o segundo exemplo tenta erroneamente usar a palavra-chave **and** :

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



