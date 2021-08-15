---
title: Estendendo ADSI
description: Com o modelo de extensão ADSI, você pode associar uma classe de diretório ao seu próprio objeto COM.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e9f5bd316fc4703cf522e2c5facfd6c32c5236da191668f6ba38ae6a904f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428449"
---
# <a name="extending-adsi"></a>Estendendo ADSI

Com o modelo de extensão ADSI, você pode associar uma classe de diretório ao seu próprio objeto COM. Da perspectiva de um programador adsi ou de um criador de script, a extensão se torna uma parte integral do ADSI. Por exemplo, quando um novo funcionário ingressar na Fabrikam, o administrador do Windows NT criará um objeto de usuário no diretório e o administrador da folha de pagamento precisará configurar algumas entradas nos sistemas de recursos humanos para esse usuário. Com uma extensão ADSI, esse processo pode ser simplificado em um único script.


```VB
Dim usr
Dim sUserName

On Error Resume Next

sUserName = InputBox ("Enter the name of the user to add:")

Set usr = ou.Create("user", "CN=" & sUserName)

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

// Insert code to set some attributes

usr.SetInfo

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

usr.AddToPayroll  'this is a custom method from an ADSI Extension

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

Debug.Print "User: " & usr.Name & "has been created"
```



Para obter mais informações, consulte [Extensões ADSI](adsi-extensions.md).

 

 




