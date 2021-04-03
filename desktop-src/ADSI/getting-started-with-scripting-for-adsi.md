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
# <a name="getting-started-with-scripting-for-adsi"></a>Introdução com scripts para ADSI

O script é útil para administradores de sistema que desejam criar scripts de lote para tarefas usadas com frequência.

Para iniciar o script com ADSI, você deve ter um computador que execute o Windows ou que esteja conectado a um domínio que contenha dados para contas de computador no diretório.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Um exemplo de script simples: Localizando nomes e locais de contas de computador

Crie um novo arquivo de texto usando um editor de texto. O exemplo de código a seguir mostra como localizar nomes e locais de contas de computador.


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



Salve o arquivo como First.vbs. Modifique a linha que começa com "objCommand. CommandText" para alterar o caminho para o seu domínio. No prompt de comando, digite **cscript First.vbs** para uma linha de comando ou First.vbs para scripts do Windows. Os resultados devem ser retornados no prompt de comando.

Para obter mais informações sobre scripts para ADSI, consulte [Active Directory script interfaces de serviço](adsi-scripting-tutorial.md).

 

 




