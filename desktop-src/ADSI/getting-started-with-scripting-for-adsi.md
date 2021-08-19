---
title: Ponto de Partida script para ADSI
description: O script é útil para administradores de sistema que querem criar scripts em lotes para tarefas usadas com frequência.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- Ponto de Partida scripts para ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a83da0194fb03cdb31430f389dbfbf64327806b1b142be3b9c1c5813696548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839949"
---
# <a name="getting-started-with-scripting-for-adsi"></a>Ponto de Partida script para ADSI

O script é útil para administradores de sistema que querem criar scripts em lotes para tarefas usadas com frequência.

Para iniciar o script com ADSI, você deve ter um computador que seja executado Windows ou estar conectado a um domínio que contenha dados para contas de computador no diretório.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Um exemplo de script simples: localizando nomes e locais de contas de computador

Crie um novo arquivo de texto usando um editor de texto. O exemplo de código a seguir mostra como encontrar nomes e locais de contas de computador.


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



Salve o arquivo como First.vbs. Modifique a linha que começa com "objCommand.CommandText" para alterar o caminho para seu domínio. No prompt de comando, digite **cscript First.vbs** para uma linha de comando ou First.vbs para Windows script. Os resultados devem ser retornados no prompt de comando.

Para obter mais informações sobre scripts para ADSI, consulte [Scripts de interfaces de serviço do Active Directory.](adsi-scripting-tutorial.md)

 

 




