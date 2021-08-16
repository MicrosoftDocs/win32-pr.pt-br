---
title: Modificando um objeto ADSI do ADO
description: o ADSI para Windows 2000 e o cliente DS inclui um provedor de OLE DB somente leitura. isso significa que você não pode, no momento, emitir a instrução UPDATE no dialeto SQL.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Modificando um objeto ADSI do ADO ADSI
- ActiveX ADSI do objeto de dados, modificando um objeto ADSI do ADO
- ADSI ADSI, código de exemplo C/C++, modificando um objeto ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4562e67043ea168a0b158088ffe3c2772f3ae28a0a2fa8881e102574cf2eb97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839446"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Modificando um objeto ADSI do ADO

o ADSI para Windows 2000 e o cliente DS inclui um provedor de OLE DB somente leitura. isso significa que você não pode, no momento, emitir a instrução UPDATE no dialeto SQL.

**Para modificar um objeto retornado de uma consulta ADO**

1.  Solicite o **ADsPath** ao especificar um nome de atributo, como em "Select ADsPath,..."
2.  Execute a consulta e obtenha o atributo **ADsPath** .
3.  Associe-se ao conjunto de registros usando **ADsPath** e modifique os atributos.

O exemplo de código a seguir mostra como modificar um objeto ADSI depois de executar as etapas descritas no exemplo anterior.


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




