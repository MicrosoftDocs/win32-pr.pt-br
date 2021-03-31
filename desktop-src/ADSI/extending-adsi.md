---
title: Estendendo ADSI
description: Com o modelo de extensão ADSI, você pode associar uma classe de diretório com seu próprio objeto COM.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e597d4b2dd2cf6a3b4a81f1fff3515289418b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634877"
---
# <a name="extending-adsi"></a>Estendendo ADSI

Com o modelo de extensão ADSI, você pode associar uma classe de diretório com seu próprio objeto COM. De uma perspectiva de programador ADSI ou gravador de script, a extensão se torna parte integrante da ADSI. Por exemplo, quando um novo funcionário ingressar na Fabrikam, o administrador do Windows NT criará um objeto de usuário no diretório e o administrador da folha de pagamento precisará configurar algumas entradas nos sistemas de recursos humanos para esse usuário. Com uma extensão ADSI, esse processo pode ser simplificado em um único script.


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



Para obter mais informações, consulte [extensões ADSI](adsi-extensions.md).

 

 




