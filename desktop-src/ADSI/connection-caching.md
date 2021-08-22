---
title: Caching de conexão
description: Quando uma conexão com um servidor é feita, o identificador de conexão é armazenado em cache no computador cliente para esse processo até que a conexão seja fechada.
ms.assetid: 927afd35-8703-4234-b6a8-6320a3667532
ms.tgt_platform: multiple
keywords:
- ADSI do cache de conexão
- cache de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0fbf63d65a6941e986069289db201a237deb9ddc7058f291218c1496d0a40e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429023"
---
# <a name="connection-caching"></a>Caching de conexão

Quando uma conexão com um servidor é feita, o identificador de conexão é armazenado em cache no computador cliente para esse processo até que a conexão seja fechada. se o mesmo servidor, porta e credenciais forem usados em uma conexão subsequente e somente os sinalizadores de autenticação de associação do **ads \_ FAST \_** ou do **ads \_ server \_** forem diferentes, a ADSI reutilizará a conexão existente. A ADSI executa esse cache de conexão em cada processo.

Para aumentar o desempenho, reutilize as conexões existentes quando possível.

O exemplo de código a seguir mostra como funciona o cache de conexão.


```VB
Dim cachedConn As IADs
Dim obj As IADs
Dim cachedName As String
Dim objName As String
 
' Connect to the server and maintain this handle to cache the connection.
Set cachedConn = GetObject("LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com")
 
cachedName = cachedConn.Get("distinguishedName")
Debug.Print (cachedName)
 
' Reuse the connection to MyMachine opened by cachedConn.
' Be aware that this line executes quickly because it is not required
' to transmit over the network again.
Set obj = GetObject("LDAP://MyMachine/CN=Bob,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection.
Set obj = Nothing
 
' Reuse the connection to MyMachine opened by cachedConn again.
Set obj = GetObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection again.
Set obj = Nothing
 
' Release the first connection.
Set cachedConn = Nothing
 
' The connection to MyMachine is closed.
```



 

 




