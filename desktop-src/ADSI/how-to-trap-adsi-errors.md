---
title: Como interceptar erros ADSI
description: O VBScript só oferece uma maneira de interceptar erros de manipulação de erro embutido.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd66283d2427c2c42162ce46a0a66ecbda87737cf2572d183ebdb0017232e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082530"
---
# <a name="how-to-trap-adsi-errors"></a>Como interceptar erros ADSI

O VBScript só oferece uma maneira de interceptar erros: tratamento de erro embutido. Um manipulador de erro embutido começa com a **próxima instrução On Error retomar** . Como se houver **erro, continuar** , impedirá que todos os erros interrompam a execução do script até que o final do escopo do qual o **erro retomar** seja chamado em seguida, você deverá verificar o valor de **Err** em todos os pontos após a **próxima instrução On Error retomar** , em que você espera que um erro ocorra. O exemplo a seguir demonstra o tratamento de erros embutidos em um script ADSI:


```VB
On Error Resume Next

Set myComputer = GetObject(computerPath)
If Err Then AdsiErr()

' Create the new user account
Set newUser = myComputer.Create("user", username)
newUser.SetInfo
If Err Then AdsiErr()

Sub AdsiErr()
    Dim s
    Dim e
    
    If Err.Number = &H8000500E Then
        WScript.Echo "The user " & username & " already exists."
    Elseif Err.Number = &H80005000 Then
        WScript.Echo "Computer " & computerPath & " not found.  Check the ADsPath and try again."
    Else
        e = Hex(Err.Number)
        WScript.Echo "Unexpected Error " & e & "(" & Err.Number & ")"
    End If
    WScript.Quit(1)

End Sub
```



Depois de cada local em que o script provavelmente encontrar um erro, haverá uma instrução **If Err** . O objeto **Err** contém o código de erro do último erro que ocorreu durante a execução do script; Se nenhum erro tiver ocorrido, o **erro** será sempre zero (0). No exemplo anterior, um erro fará com que a execução salte para a sub-rotina **AdsiErr** , que verifica o valor de **Err. Number** para os erros esperados. Em vez de curioso com uma mensagem de erro misteriosa, o script fornecerá uma explicação um pouco melhor para o motivo da parada da execução.

Lembre-se de que, dentro do escopo no qual o **erro retomar, avançar** é chamado, qualquer erro que ocorra após o erro se a **próxima** chamada será ignorado. Isso pode realmente tornar um script mais difícil de depurar se você esquecer de verificar o valor de **Err** em locais apropriados. Sempre que você esperar que um erro seja provavelmente, certifique-se de verificar o valor de **Err**.

(Quando você estiver Depurando inicialmente o script, convém simplesmente permitir que o script pare sua execução e exiba o número de linha incorreto em um erro e, em seguida, adicione os manipuladores de erro depois que o fluxo de programa básico estiver correto.)

 

 




