---
description: Um objeto InParameters contém a lista de parâmetros para chamar métodos de provedor ao usar um tipo ExecMethod de chamada.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Construindo objetos InParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc13a51687954331a050337fe785bab29b23ee9c72785ffde78d4f8a8e0d198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131578"
---
# <a name="constructing-inparameters-objects"></a>Construindo objetos InParameters

Um [**objeto InParameters**](swbemmethod-inparameters.md) contém a lista de parâmetros para chamar métodos de provedor ao usar **um tipo execMethod** de chamada. Os [**métodosSWbemObject.ExecMethod \_**](swbemobject-execmethod-.md),SWbemObject.Exe [**cMethodAsync, \_**](swbemobject-execmethodasync-.md)SWbemServices.Exe [**cMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) exigem um objeto **InParameters.**

O procedimento a seguir descreve como construir um [**objeto InParameters.**](swbemmethod-inparameters.md)

**Para construir o *parâmetro objwbemInParams***

1.  Conexão para WMI.
2.  Obtenha a definição da classe WMI que define o método que você deseja executar.
3.  Obtenha um [**objeto InParameters**](swbemmethod-inparameters.md) específico para o método de classe WMI que você deseja executar.

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  De definir as propriedades da instância como quaisquer valores apropriados. Certifique-se de dar valores para as propriedades de chave na classe WMI que contém o método que você deseja executar.

    Por exemplo, se você quiser definir um parâmetro de entrada chamado myinputparam com o valor "abc" em uma instância do [**InParameters**](swbemmethod-inparameters.md) chamada "INST", o código será assim.

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  Execute o método e obtenha o status de retorno do método que você está executando.

O exemplo de código a seguir ilustra a configuração do [**objeto InParameters**](swbemmethod-inparameters.md) para criar um novo objeto WMI que representa um compartilhamento. Para obter mais informações sobre o [**objeto OutParameters,**](swbemmethod-outparameters.md) consulte [Análise de objetos OutParameters](parsing-outparameters-objects.md). Este exemplo retornará um valor de retorno bem-sucedido (0) se houver uma pasta chamada "Compartilhamento" no local "C:/Share". Este exemplo permite que essa pasta seja compartilhada com outros usuários.


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



 

 



