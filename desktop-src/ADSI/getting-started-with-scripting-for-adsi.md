---
title: Introdução com scripts para ADSI
description: O script é útil para administradores de sistema que desejam criar scripts de lote para tarefas usadas com frequência.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- Introdução com scripts para ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a85a9ea110ca80f45c3a0f0f1917e8d25c08ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915897"
---
# <a name="getting-started-with-scripting-for-adsi"></a><span data-ttu-id="984ab-104">Introdução com scripts para ADSI</span><span class="sxs-lookup"><span data-stu-id="984ab-104">Getting Started with Scripting for ADSI</span></span>

<span data-ttu-id="984ab-105">O script é útil para administradores de sistema que desejam criar scripts de lote para tarefas usadas com frequência.</span><span class="sxs-lookup"><span data-stu-id="984ab-105">Scripting is useful for system administrators who want to create batch scripts for frequently used tasks.</span></span>

<span data-ttu-id="984ab-106">Para iniciar o script com ADSI, você deve ter um computador que execute o Windows ou que esteja conectado a um domínio que contenha dados para contas de computador no diretório.</span><span class="sxs-lookup"><span data-stu-id="984ab-106">To start scripting with ADSI, you must have a computer that runs Windows or be logged on to a domain that contains data for computer accounts in the directory.</span></span>

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a><span data-ttu-id="984ab-107">Um exemplo de script simples: Localizando nomes e locais de contas de computador</span><span class="sxs-lookup"><span data-stu-id="984ab-107">A Simple Scripting Sample: Finding Names and Locations of Computer Accounts</span></span>

<span data-ttu-id="984ab-108">Crie um novo arquivo de texto usando um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="984ab-108">Create a new text file using a text editor.</span></span> <span data-ttu-id="984ab-109">O exemplo de código a seguir mostra como localizar nomes e locais de contas de computador.</span><span class="sxs-lookup"><span data-stu-id="984ab-109">The following code example shows how to find names and locations of computer accounts.</span></span>


```VB
'---------------------------------------------------------------
' Returns the name and location for all the computer accounts in 
' Active Directory.
'--------------------------------------------------------------- 
Const ADS_SCOPE_SUBTREE = 2
Set objConnection = CreateObject("ADODB.Connection")
Set objCommand =   CreateObject("ADODB.Command")
objConnection.Provider = "ADsDSOObject"
objConnection.Open "Active Directory Provider"
Set objCommand.ActiveConnection = objConnection
objCommand.CommandText = "Select Name, Location from 'LDAP://DC=fabrikam,DC=com' " & "where objectClass='computer'"  
objCommand.Properties("Page Size") = 1000
objCommand.Properties("Timeout") = 30 
objCommand.Properties("Searchscope") = ADS_SCOPE_SUBTREE 
objCommand.Properties("Cache Results") = False 
Set objRecordSet = objCommand.Execute
objRecordSet.MoveFirst
Do Until objRecordSet.EOF
    Wscript.Echo "Computer Name: " & objRecordSet.Fields("Name").Value
    Wscript.Echo "Location: " & objRecordSet.Fields("Location").Value
    objRecordSet.MoveNext
Loop
```



<span data-ttu-id="984ab-110">Salve o arquivo como First.vbs.</span><span class="sxs-lookup"><span data-stu-id="984ab-110">Save the file as First.vbs.</span></span> <span data-ttu-id="984ab-111">Modifique a linha que começa com "objCommand. CommandText" para alterar o caminho para o seu domínio.</span><span class="sxs-lookup"><span data-stu-id="984ab-111">Modify the line that begins with "objCommand.CommandText" to change the path to your domain.</span></span> <span data-ttu-id="984ab-112">No prompt de comando, digite **cscript First.vbs** para uma linha de comando ou First.vbs para scripts do Windows.</span><span class="sxs-lookup"><span data-stu-id="984ab-112">At the command prompt, type **cscript First.vbs** for a command line or First.vbs for Windows scripting.</span></span> <span data-ttu-id="984ab-113">Os resultados devem ser retornados no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="984ab-113">The results should be returned in the command prompt.</span></span>

<span data-ttu-id="984ab-114">Para obter mais informações sobre scripts para ADSI, consulte [Active Directory script interfaces de serviço](adsi-scripting-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="984ab-114">For more information about scripting for ADSI, see [Active Directory Service Interfaces Scripting](adsi-scripting-tutorial.md).</span></span>

 

 




