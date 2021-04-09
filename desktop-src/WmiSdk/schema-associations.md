---
description: 'As consultas de associação de esquema usam as mesmas instruções usadas em consultas de associação de dados: ASSOCIAdores de e referências de.'
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Associações de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171443"
---
# <a name="schema-associations"></a>Associações de esquema

As consultas de associação de esquema usam as mesmas instruções usadas em consultas de associação de dados: ASSOCIAdores de e referências de. No entanto, com consultas de associação de dados, as instâncias de classe são retornadas e, com consultas de associação de esquema, os nomes de classes que podem participar de relações de associação são retornados. Por exemplo, use uma consulta de esquema para localizar todas as classes de associação definidas no esquema que fazem referência a uma classe de origem.

A sintaxe para os ASSOCIAdores e referências de instruções é a mesma para consultas de associação de esquema, como é para consultas de associação de dados com as seguintes exceções:

-   O objeto de origem é uma classe em vez de uma instância.
-   Há uma palavra-chave adicional, **SchemaOnly**, que identifica a consulta como sendo aplicada a um esquema, e não aos dados.
-   A palavra-chave **ClassDefsOnly** não é válida.

O exemplo a seguir mostra a sintaxe completa dos ASSOCIAdores de instrução para uma consulta de esquema. Para obter uma sintaxe detalhada, consulte [ASSOCIATORS of Statement](associators-of-statement.md).


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



O exemplo a seguir mostra uma consulta que retorna as classes de **protocolo** e **Driver** , as duas classes que se referem à classe de origem.


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



A consulta a seguir retorna apenas a classe de **Driver** devido à restrição colocada pela palavra-chave **AssocClass** .


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



A sintaxe completa das referências de instrução para uma consulta de esquema é a seguinte. Para obter uma sintaxe detalhada, consulte [References of Statement](references-of-statement.md).


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> As consultas de associação de esquema podem retornar objetos duplicados.

 

Por exemplo, a consulta a seguir retornará a classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) várias vezes ao enumerar classes no namespace **raiz \\ cimv2** .


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
