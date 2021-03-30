---
title: Modificando um objeto ADSI do ADO
description: O ADSI para o Windows 2000 e o DS Client inclui um provedor de OLE DB somente leitura. Isso significa que você não pode, no momento, emitir a instrução UPDATE no dialeto SQL.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Modificando um objeto ADSI do ADO ADSI
- ADSI do objeto de dados ActiveX, modificando um objeto ADSI do ADO
- ADSI ADSI, código de exemplo C/C++, modificando um objeto ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7291088915a537231077e1d75161b57684caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634871"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Modificando um objeto ADSI do ADO

O ADSI para o Windows 2000 e o DS Client inclui um provedor de OLE DB somente leitura. Isso significa que você não pode, no momento, emitir a instrução UPDATE no dialeto SQL.

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



 

 




