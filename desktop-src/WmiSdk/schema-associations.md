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
# <a name="schema-associations"></a><span data-ttu-id="cad3a-103">Associações de esquema</span><span class="sxs-lookup"><span data-stu-id="cad3a-103">Schema Associations</span></span>

<span data-ttu-id="cad3a-104">As consultas de associação de esquema usam as mesmas instruções usadas em consultas de associação de dados: ASSOCIAdores de e referências de.</span><span class="sxs-lookup"><span data-stu-id="cad3a-104">Schema association queries use the same statements as are used in data association queries: ASSOCIATORS OF and REFERENCES OF.</span></span> <span data-ttu-id="cad3a-105">No entanto, com consultas de associação de dados, as instâncias de classe são retornadas e, com consultas de associação de esquema, os nomes de classes que podem participar de relações de associação são retornados.</span><span class="sxs-lookup"><span data-stu-id="cad3a-105">However, with data association queries, class instances are returned, and with schema association queries, names of classes that can participate in association relationships are returned.</span></span> <span data-ttu-id="cad3a-106">Por exemplo, use uma consulta de esquema para localizar todas as classes de associação definidas no esquema que fazem referência a uma classe de origem.</span><span class="sxs-lookup"><span data-stu-id="cad3a-106">For example, use a schema query to find all of the association classes defined in the schema that reference a source class.</span></span>

<span data-ttu-id="cad3a-107">A sintaxe para os ASSOCIAdores e referências de instruções é a mesma para consultas de associação de esquema, como é para consultas de associação de dados com as seguintes exceções:</span><span class="sxs-lookup"><span data-stu-id="cad3a-107">The syntax for the ASSOCIATORS OF and REFERENCES OF statements is the same for schema association queries as it is for data association queries with the following exceptions:</span></span>

-   <span data-ttu-id="cad3a-108">O objeto de origem é uma classe em vez de uma instância.</span><span class="sxs-lookup"><span data-stu-id="cad3a-108">The source object is a class rather than an instance.</span></span>
-   <span data-ttu-id="cad3a-109">Há uma palavra-chave adicional, **SchemaOnly**, que identifica a consulta como sendo aplicada a um esquema, e não aos dados.</span><span class="sxs-lookup"><span data-stu-id="cad3a-109">There is an additional keyword, **SchemaOnly**, which identifies the query as applying to a schema rather than to data.</span></span>
-   <span data-ttu-id="cad3a-110">A palavra-chave **ClassDefsOnly** não é válida.</span><span class="sxs-lookup"><span data-stu-id="cad3a-110">The **ClassDefsOnly** keyword is not valid.</span></span>

<span data-ttu-id="cad3a-111">O exemplo a seguir mostra a sintaxe completa dos ASSOCIAdores de instrução para uma consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="cad3a-111">The following example shows the complete syntax of the ASSOCIATORS OF statement for a schema query.</span></span> <span data-ttu-id="cad3a-112">Para obter uma sintaxe detalhada, consulte [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="cad3a-112">For detailed syntax, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>


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



<span data-ttu-id="cad3a-113">O exemplo a seguir mostra uma consulta que retorna as classes de **protocolo** e **Driver** , as duas classes que se referem à classe de origem.</span><span class="sxs-lookup"><span data-stu-id="cad3a-113">The following example shows a query that returns the **Protocol** and **Driver** classes, the two classes that refer to the source class.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



<span data-ttu-id="cad3a-114">A consulta a seguir retorna apenas a classe de **Driver** devido à restrição colocada pela palavra-chave **AssocClass** .</span><span class="sxs-lookup"><span data-stu-id="cad3a-114">The following query returns only the **Driver** class because of the restriction placed by the **AssocClass** keyword.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



<span data-ttu-id="cad3a-115">A sintaxe completa das referências de instrução para uma consulta de esquema é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="cad3a-115">The complete syntax of the REFERENCES OF statement for a schema query is as follows.</span></span> <span data-ttu-id="cad3a-116">Para obter uma sintaxe detalhada, consulte [References of Statement](references-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="cad3a-116">For detailed syntax, see [REFERENCES OF Statement](references-of-statement.md).</span></span>


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> <span data-ttu-id="cad3a-117">As consultas de associação de esquema podem retornar objetos duplicados.</span><span class="sxs-lookup"><span data-stu-id="cad3a-117">Schema association queries may return duplicate objects.</span></span>

 

<span data-ttu-id="cad3a-118">Por exemplo, a consulta a seguir retornará a classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) várias vezes ao enumerar classes no namespace **raiz \\ cimv2** .</span><span class="sxs-lookup"><span data-stu-id="cad3a-118">For example, the following query will return the class [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) several times when enumerating classes in the **root\\cimv2** namespace.</span></span>


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
