---
description: O WMI fornece uma variedade de técnicas para recuperar e manipular informações de classe e instância do WMI, usando o Microsoft PowerShell, o Visual&\# 160; Basic Scripting Edition (VBScript) e C++.
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: Manipulando informações de classe e instância
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815470"
---
# <a name="manipulating-class-and-instance-information"></a>Manipulando informações de classe e instância

O WMI fornece uma variedade de técnicas para recuperar e manipular informações de classe e instância do WMI, usando o Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) e C++.

A tabela a seguir lista os tópicos que discutem as técnicas para recuperar e manipular informações de classe e instância do WMI.



| Tópico                                                                                  | Descrição                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recuperando dados de instância ou classe WMI](retrieving-class-or-instance-data.md)         | Recuperar e definir dados de e para o repositório de informações do WMI.                                                                                                                 |
| [Modificando uma propriedade de instância](modifying-an-instance-property.md)                   | Altere as informações na instância depois que ela for recuperada.                                                                                                                     |
| [Alterando a herança de uma instância](changing-the-inheritance-of-an-instance.md) | Altere a classe pai de uma instância.                                                                                                                                           |
| [Modificando um método](modifying-a-method.md)                                           | Modifique os parâmetros de uma instância.                                                                                                                                             |
| [Enumerando o WMI](enumerating-wmi.md)                                                 | Enumerar objetos WMI.                                                                                                                                                            |
| [Consultando o WMI](querying-wmi.md)                                                       | Consultar objetos WMI.                                                                                                                                                                |
| [Chamando um método](calling-a-method.md)                                               | Use os métodos associados criados pela Microsoft ou por outros desenvolvedores de terceiros para manipular mais objetos WMI ou, caso contrário, afetam diretamente o objeto que o objeto WMI representa. |
| [Acessando uma coleção](accessing-a-collection.md)                                   | Enumere as coleções no script.                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a>Manipulando dados usando o VBScript

Você pode usar o acesso direto para acessar as propriedades WMI de uma instância ou classe WMI diretamente em um [**SWbemObject**](swbemobject.md), em vez de por meio da [coleção](accessing-a-collection.md) de propriedades desse objeto. Você também pode executar métodos nesse objeto no estilo nativo da linguagem de programação em vez de usar o [**SWbemServices.Exechamada cMethod**](swbemservices-execmethod.md) . Por exemplo, o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) no [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) tinha três parâmetros no Windows 2000, mas tem quatro parâmetros no Windows Server 2003.

Usando o acesso direto, você pode tratar Propriedades e métodos do WMI como se fossem Propriedades de automação e métodos de [**SWbemObject**](swbemobject.md).

O exemplo a seguir mostra como você pode acessar uma propriedade.


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



O exemplo a seguir mostra como você pode acessar uma propriedade quando você tem acesso direto.


```VB
VolumeName = MyDisk.VolumeName
```



O encadeamento de objetos também é aceitável.

O exemplo a seguir mostra como acessar uma propriedade de um objeto inserido em outro objeto.


```VB
value = MyComputer.MyDisk.VolumeName
```



O exemplo a seguir mostra como acessar uma propriedade com a notação de subscrito de matriz.


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



O exemplo de código VBScript a seguir mostra como gerar uma instância dos parâmetros de entrada para o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) na classe de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) como um [**SWbemObject**](swbemobject.md), preencher as propriedades de entrada e executar o método **Create** usando [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).

A propriedade [**SWbemObject. \_ Methods**](swbemobject-methods-.md) retorna uma coleção [**SWbemMethodSet**](swbemmethodset.md) dos métodos de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) . Os membros do conjunto de métodos são objetos [**SWbemMethod**](swbemmethod.md) e [**SWbemMethod. Parameters**](swbemmethod-inparameters.md) retorna os parâmetros de entrada para o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . O parâmetro de entrada de *linha de comando* necessário está definido como "calc.exe". O método é executado por [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), resultando na inicialização de um processo de calc.exe.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set obj = Services.Get("Win32_Process")
Set objIns = obj.Methods_("Create").InParameters.SpawnInstance_
objIns.CommandLine = "calc.exe"
Set objOut = Services.ExecMethod("Win32_Process", "Create", objIns)
MsgBox "Return value = " & objOut.returnvalue & VBCRLF & "Process ID = " & objOut.processid
```



O exemplo de código a seguir mostra como executar a operação anterior usando o acesso direto.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set Obj = Services.Get("Win32_Process")
returnvalue = Obj.create("calc.exe",,,processid)
MsgBox "Return value = " & returnvalue & VBCRLF & "Process ID = " & processid
```



Para obter mais informações, consulte [chamando um método de provedor](calling-a-provider-method.md) e [script com SWbemObject](scripting-with-swbemobject.md).

 

 
