---
description: Um objeto de inparâmetros contém a lista de parâmetros para chamar métodos de provedor ao usar um tipo de chamada de ExecMethod.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Construindo objetos de inparâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827847"
---
# <a name="constructing-inparameters-objects"></a>Construindo objetos de inparâmetros

Um objeto de [**inparâmetros**](swbemmethod-inparameters.md) contém a lista de parâmetros para chamar métodos de provedor ao usar um tipo de chamada de **ExecMethod** . Os métodos [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) requerem um objeto de **inparâmetros** .

O procedimento a seguir descreve como construir um objeto de [**inparâmetros**](swbemmethod-inparameters.md) .

**Para construir o parâmetro *objwbemInParams***

1.  Conecte-se ao WMI.
2.  Obtenha a definição da classe WMI que define o método que você deseja executar.
3.  Obtenha um objeto de [**inparâmetros**](swbemmethod-inparameters.md) específico para o método de classe WMI que você deseja executar.

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  Defina as propriedades da instância para quaisquer valores apropriados. Certifique-se de atribuir valores às propriedades de chave na classe WMI que contém o método que você deseja executar.

    Por exemplo, se você quiser definir um parâmetro de entrada chamado myinputparam para o valor "ABC" em uma instância de [**inparâmetros**](swbemmethod-inparameters.md) chamada "Inst", o código ficaria assim.

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  Execute o método e obtenha o status de retorno do método que você está executando.

O exemplo de código a seguir ilustra a configuração do objeto [**Parameters**](swbemmethod-inparameters.md) para criar um novo objeto WMI que representa um compartilhamento. Para obter mais informações sobre o objeto [**Parameters**](swbemmethod-outparameters.md) , consulte [analisando objetos de Parameters](parsing-outparameters-objects.md). Este exemplo retorna um valor de retorno com êxito (0) se houver uma pasta chamada "compartilhamento" no local "C:/compartilhamento". Este exemplo permite que essa pasta seja compartilhada com outros usuários.


```VB
' Connect to WMI.
Set objServices = GetObject("winmgmts:root\cimv2")

' Obtain the definition of the WMI class that defines
' the method you want to execute.
Set objShare = objServices.Get("Win32_Share")

' Obtain an InParameters object specific
' to the WMI class method you want to execute.
Set objInParam = objShare.Methods_("Create"). _
    inParameters.SpawnInstance_()

' Set the properties of the instance to whatever
' values are appropriate.
objInParam.Properties_.Item("Access") = objSecDescriptor
objInParam.Properties_.Item("Description") = _
    "New share created by WMI script"
objInParam.Properties_.Item("Name") = "share"
objInParam.Properties_.Item("Path") = "C:\share"
objInParam.Properties_.Item("Type") = 0
'optional - default is 'max allowed'
objInParam.Properties_.Item("MaximumAllowed") = 100
'optional - default is no password
objInParam.Properties_.Item("Password") = "Password"

' Execute the method and obtain the return status. 
' The OutParameters object in objOutParams
' is created by the provider. 
Set objOutParams = objShare.ExecMethod_("Create", objInParam)    
wscript.echo objOutParams.ReturnValue
```



 

 



