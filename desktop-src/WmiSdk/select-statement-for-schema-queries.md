---
description: As consultas de dados de esquema usam a instrução SELECT com uma sintaxe semelhante à consulta de dados.
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

Consultas de dados de esquema usam a instrução SELECT com uma sintaxe semelhante à de [consultas de dados](select-statement-for-data-queries.md). A diferença é o uso de uma classe especial chamada "meta class", que identifica a consulta como uma \_ consulta de esquema.

O exemplo a seguir solicita todas as definições de classe que estão dentro do namespace atual.


```sql
SELECT * FROM meta_class
```



As consultas de esquema só são suportadas por " \* ". Para restringir o escopo das definições retornadas, um provedor pode adicionar uma cláusula WHERE que especifica uma classe específica.

O exemplo a seguir mostra como adicionar uma cláusula WHERE para especificar uma classe específica.


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



A propriedade especial chamada **\_ \_ isso** identifica a classe de destino para uma consulta de esquema. Observe que o operador ISA deve ser usado com essa **\_ \_ propriedade** para solicitar definições para as subclasses da classe de destino. A consulta anterior retorna a definição para a classe [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e as definições para todas as suas subclasses.

O exemplo a seguir mostra como solicitar uma definição de classe para uma única classe usando a **\_ \_ propriedade Sistema** de classe.


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



Essa consulta é equivalente a chamar o [**método IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) com o parâmetro de caminho do objeto definido como "Win32 \_ LogicalDisk".

O exemplo de código VBScript a seguir recupera todas as classes filho de uma classe WMI de nível superior. A propriedade do sistema WMI Descarado contém o nome da classe de nível superior da qual uma classe é derivada, que você pode usar para recuperar todas as classes em um namespace derivado de uma classe de nível superior, incluindo essa \_ \_ classe.


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



O VBScript a seguir recupera uma classe filho imediata para uma classe WMI.


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



O VBScript a seguir recupera classes de nível superior. Para todas as classes de nível superior em um namespace WMI, a propriedade do sistema \_ \_ Superclasse é Null. Portanto, é possível recuperar as classes de nível superior pesquisando uma superclasse Null.


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
