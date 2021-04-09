---
description: Consultas de dados de esquema usam a instrução SELECT com uma sintaxe semelhante àquela para consultas de dados.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Instrução SELECT para consultas de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171442"
---
# <a name="select-statement-for-schema-queries"></a><span data-ttu-id="174c7-103">Instrução SELECT para consultas de esquema</span><span class="sxs-lookup"><span data-stu-id="174c7-103">SELECT Statement for Schema Queries</span></span>

<span data-ttu-id="174c7-104">Consultas de dados de esquema usam a instrução SELECT com uma sintaxe semelhante àquela para [consultas de dados](select-statement-for-data-queries.md).</span><span class="sxs-lookup"><span data-stu-id="174c7-104">Schema data queries use the SELECT statement with a syntax similar to that for [data queries](select-statement-for-data-queries.md).</span></span> <span data-ttu-id="174c7-105">A diferença é o uso de uma classe especial chamada "meta \_ Class", que identifica a consulta como uma consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="174c7-105">The difference is the use of a special class called "meta\_class", which identifies the query as a schema query.</span></span>

<span data-ttu-id="174c7-106">O exemplo a seguir solicita todas as definições de classe que estão dentro do namespace atual.</span><span class="sxs-lookup"><span data-stu-id="174c7-106">The following example requests all class definitions that are within the current namespace.</span></span>


```sql
SELECT * FROM meta_class
```



<span data-ttu-id="174c7-107">As consultas de esquema só dão suporte a " \* ".</span><span class="sxs-lookup"><span data-stu-id="174c7-107">Schema queries only support "\*".</span></span> <span data-ttu-id="174c7-108">Para restringir o escopo das definições retornadas, um provedor pode adicionar uma cláusula WHERE que especifica uma classe específica.</span><span class="sxs-lookup"><span data-stu-id="174c7-108">To narrow the scope of the definitions returned, a provider can add a WHERE clause that specifies a particular class.</span></span>

<span data-ttu-id="174c7-109">O exemplo a seguir mostra como adicionar uma cláusula WHERE para especificar uma classe específica.</span><span class="sxs-lookup"><span data-stu-id="174c7-109">The following example shows how to add a WHERE clause to specify a particular class.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



<span data-ttu-id="174c7-110">A propriedade especial chamada **\_ \_ this** identifica a classe de destino para uma consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="174c7-110">The special property called **\_\_this** identifies the target class for a schema query.</span></span> <span data-ttu-id="174c7-111">Observe que o operador ISA deve ser usado com a propriedade **\_ \_ this** para solicitar definições para as subclasses da classe de destino.</span><span class="sxs-lookup"><span data-stu-id="174c7-111">Note that the ISA operator must be used with the **\_\_this** property to request definitions for the subclasses of the target class.</span></span> <span data-ttu-id="174c7-112">A consulta anterior retorna a definição para a classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e definições para todas as suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="174c7-112">The preceding query returns the definition for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="174c7-113">O exemplo a seguir mostra como solicitar uma definição de classe para uma única classe usando a propriedade do sistema de **\_ \_ classe** .</span><span class="sxs-lookup"><span data-stu-id="174c7-113">The following example shows how to request a class definition for a single class by using the **\_\_Class** system property.</span></span>


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



<span data-ttu-id="174c7-114">Essa consulta é equivalente à chamada do método [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) com o parâmetro Object Path definido como "Win32 \_ LogicalDisk".</span><span class="sxs-lookup"><span data-stu-id="174c7-114">This query is equivalent to calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or the [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) method with the object path parameter set to "Win32\_LogicalDisk".</span></span>

<span data-ttu-id="174c7-115">O exemplo de código VBScript a seguir recupera todas as classes filho de uma classe WMI de nível superior.</span><span class="sxs-lookup"><span data-stu-id="174c7-115">The following VBScript code sample retrieves all child classes of a top level WMI class.</span></span> <span data-ttu-id="174c7-116">A \_ \_ Propriedade do sistema WMI dinastia contém o nome da classe de nível superior da qual uma classe é derivada, que você pode usar para recuperar todas as classes em um namespace derivado de uma classe de nível superior, incluindo essa classe.</span><span class="sxs-lookup"><span data-stu-id="174c7-116">The \_\_Dynasty WMI system property holds the name of the top-level class from which a class is derived, which you can use to retrieve all classes in a namespace derived from a top level class, including that class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="174c7-117">O VBScript a seguir recupera as classes filho imediatas para uma classe WMI.</span><span class="sxs-lookup"><span data-stu-id="174c7-117">The following VBScript retrieves an immediate child classes for a WMI class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="174c7-118">O VBScript a seguir recupera classes de nível superior.</span><span class="sxs-lookup"><span data-stu-id="174c7-118">The following VBScript retrieves top level classes.</span></span> <span data-ttu-id="174c7-119">Para todas as classes de nível superior em um namespace WMI, a \_ \_ Propriedade do sistema de superclasse é nula.</span><span class="sxs-lookup"><span data-stu-id="174c7-119">For all the top level classes in a WMI namespace, the \_\_Superclass system property is Null.</span></span> <span data-ttu-id="174c7-120">Portanto, é possível recuperar as classes de nível superior pesquisando por uma superclasse nula.</span><span class="sxs-lookup"><span data-stu-id="174c7-120">Therefore, it is possible to retrieve the top level classes by searching for a Null superclass.</span></span>


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
