---
title: Como interceptar erros ADSI
description: O VBScript só oferece uma maneira de interceptar erros de manipulação de erro embutido.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa36b3e9b1027e1733009d58a572a0b27c7ef0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755488"
---
# <a name="how-to-trap-adsi-errors"></a><span data-ttu-id="77487-103">Como interceptar erros ADSI</span><span class="sxs-lookup"><span data-stu-id="77487-103">How to Trap ADSI Errors</span></span>

<span data-ttu-id="77487-104">O VBScript só oferece uma maneira de interceptar erros: tratamento de erro embutido.</span><span class="sxs-lookup"><span data-stu-id="77487-104">VBScript only offers one way to trap errors: inline error handling.</span></span> <span data-ttu-id="77487-105">Um manipulador de erro embutido começa com a **próxima instrução On Error retomar** .</span><span class="sxs-lookup"><span data-stu-id="77487-105">An inline error handler begins with the **On Error Resume Next** statement.</span></span> <span data-ttu-id="77487-106">Como se houver **erro, continuar** , impedirá que todos os erros interrompam a execução do script até que o final do escopo do qual o **erro retomar** seja chamado em seguida, você deverá verificar o valor de **Err** em todos os pontos após a **próxima instrução On Error retomar** , em que você espera que um erro ocorra.</span><span class="sxs-lookup"><span data-stu-id="77487-106">Since **On Error Resume Next** will prevent any errors from stopping execution of the script until the end of the scope from which **On Error Resume Next** is called, you must check the value of **Err** at every point after the **On Error Resume Next** statement where you expect an error might occur.</span></span> <span data-ttu-id="77487-107">O exemplo a seguir demonstra o tratamento de erros embutidos em um script ADSI:</span><span class="sxs-lookup"><span data-stu-id="77487-107">The following example demonstrates inline error handling in an ADSI script:</span></span>


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



<span data-ttu-id="77487-108">Depois de cada local em que o script provavelmente encontrar um erro, haverá uma instrução **If Err** .</span><span class="sxs-lookup"><span data-stu-id="77487-108">After each location where the script is likely to encounter an error, there is an **If Err** statement.</span></span> <span data-ttu-id="77487-109">O objeto **Err** contém o código de erro do último erro que ocorreu durante a execução do script; Se nenhum erro tiver ocorrido, o **erro** será sempre zero (0).</span><span class="sxs-lookup"><span data-stu-id="77487-109">The **Err** object contains the error code of the last error that occurred during execution of the script; if no error has occurred, **Err** will always be zero (0).</span></span> <span data-ttu-id="77487-110">No exemplo anterior, um erro fará com que a execução salte para a sub-rotina **AdsiErr** , que verifica o valor de **Err. Number** para os erros esperados.</span><span class="sxs-lookup"><span data-stu-id="77487-110">In the previous example, an error will cause execution to jump to the **AdsiErr** subroutine, which checks the value of **Err.Number** for expected errors.</span></span> <span data-ttu-id="77487-111">Em vez de curioso com uma mensagem de erro misteriosa, o script fornecerá uma explicação um pouco melhor para o motivo da parada da execução.</span><span class="sxs-lookup"><span data-stu-id="77487-111">Instead of dying with a cryptic error message, the script will give a somewhat better explanation for why it stopped running.</span></span>

<span data-ttu-id="77487-112">Lembre-se de que, dentro do escopo no qual o **erro retomar, avançar** é chamado, qualquer erro que ocorra após o erro se a **próxima** chamada será ignorado.</span><span class="sxs-lookup"><span data-stu-id="77487-112">Remember that within the scope in which **On Error Resume Next** is called, any error that occurs after the **On Error Resume Next** call will be ignored.</span></span> <span data-ttu-id="77487-113">Isso pode realmente tornar um script mais difícil de depurar se você esquecer de verificar o valor de **Err** em locais apropriados.</span><span class="sxs-lookup"><span data-stu-id="77487-113">This can actually make a script harder to debug if you forget to check the value of **Err** in appropriate locations.</span></span> <span data-ttu-id="77487-114">Sempre que você esperar que um erro seja provavelmente, certifique-se de verificar o valor de **Err**.</span><span class="sxs-lookup"><span data-stu-id="77487-114">Wherever you expect an error to be likely, be sure to check the value of **Err**.</span></span>

<span data-ttu-id="77487-115">(Quando você estiver Depurando inicialmente o script, convém simplesmente permitir que o script pare sua execução e exiba o número de linha incorreto em um erro e, em seguida, adicione os manipuladores de erro depois que o fluxo de programa básico estiver correto.)</span><span class="sxs-lookup"><span data-stu-id="77487-115">(When you are initially debugging the script you may want to simply let the script halt its execution and display the offending line number on an error, then add the error handlers after the basic program flow is correct.)</span></span>

 

 




