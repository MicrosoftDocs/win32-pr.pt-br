---
description: Consultas de dados de esquema usam a instrução SELECT com uma sintaxe semelhante àquela para consultas de dados.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Instrução SELECT para consultas de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd08cffa3fccc9a8cc2bf50452dcefcc1b7bfc0a62e512069b2db098bc6d13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315670"
---
# <a name="select-statement-for-schema-queries"></a>Instrução SELECT para consultas de esquema

Consultas de dados de esquema usam a instrução SELECT com uma sintaxe semelhante àquela para [consultas de dados](select-statement-for-data-queries.md). A diferença é o uso de uma classe especial chamada "meta \_ Class", que identifica a consulta como uma consulta de esquema.

O exemplo a seguir solicita todas as definições de classe que estão dentro do namespace atual.


```sql
SELECT * FROM meta_class
```



As consultas de esquema só dão suporte a " \* ". Para restringir o escopo das definições retornadas, um provedor pode adicionar uma cláusula WHERE que especifica uma classe específica.

O exemplo a seguir mostra como adicionar uma cláusula WHERE para especificar uma classe específica.


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



A propriedade especial chamada **\_ \_ this** identifica a classe de destino para uma consulta de esquema. Observe que o operador ISA deve ser usado com a propriedade **\_ \_ this** para solicitar definições para as subclasses da classe de destino. A consulta anterior retorna a definição para a classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e definições para todas as suas subclasses.

O exemplo a seguir mostra como solicitar uma definição de classe para uma única classe usando a propriedade do sistema de **\_ \_ classe** .


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



Essa consulta é equivalente à chamada do método [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) com o parâmetro Object Path definido como "Win32 \_ LogicalDisk".

O exemplo de código VBScript a seguir recupera todas as classes filho de uma classe WMI de nível superior. A \_ \_ Propriedade do sistema WMI dinastia contém o nome da classe de nível superior da qual uma classe é derivada, que você pode usar para recuperar todas as classes em um namespace derivado de uma classe de nível superior, incluindo essa classe.


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



O VBScript a seguir recupera as classes filho imediatas para uma classe WMI.


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



O VBScript a seguir recupera classes de nível superior. Para todas as classes de nível superior em um namespace WMI, a \_ \_ Propriedade do sistema de superclasse é nula. Portanto, é possível recuperar as classes de nível superior pesquisando por uma superclasse nula.


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
