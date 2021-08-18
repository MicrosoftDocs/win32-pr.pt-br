---
title: Pesquisando objetos
description: Ela deve encontrar números de telefone para todos os Gerentes de Programas que trabalham no Departamento 101. Ela pode criar um script que usa ADO e ADSI para fazer isso.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- procurando objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd41e87ad3396694b2f87158b15278c1dfbe28b044ad03ebbb09ddded705910a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973496"
---
# <a name="searching-for-objects"></a>Pesquisando objetos

Ela deve encontrar números de telefone para todos os Gerentes de Programas que trabalham no Departamento 101. Ela pode criar um script que usa ADO e ADSI para fazer isso.

Ao usar o provedor ADO para executar uma consulta, o conjunto de resultados retornará apenas os primeiros 1000 objetos. Por esse motivo, é importante usar uma consulta pageda para que você possa recuperar todos os objetos no conjunto de resultados, desde que o serviço de diretório não tenha sido definido para limitar o número de itens em um conjunto de resultados. Os conjuntos de retorno conterão o número de itens especificados no tamanho da página e os conjuntos de páginas continuarão sendo retornados até que todos os itens no conjunto de resultados sejam retornados.


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



Para executar uma pesquisa ADSI no Visual Basic ou em um ambiente de script, três componentes do ADO são necessários: **Conexão,** Comando e **Recordset**. O **objeto** Connection permite que você especifique o nome do provedor, as credenciais alternativas, se aplicável, e outros sinalizadores. O **objeto Command** permite que você especifique as preferências de pesquisa e a cadeia de caracteres de consulta. Você deve associar o **objeto Connection** a um **objeto Command** antes da execução da consulta. Por fim, **o objeto Conjunto** de Registros é usado para iterar o conjunto de resultados.

A ADSI dá suporte a dois tipos de cadeias de caracteres de consulta ou dialetos. O exemplo de código anterior usa o SQL dialeto. Você também pode usar o dialeto LDAP. A cadeia de caracteres de consulta do dialeto LDAP baseia-se no [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (um RFC é um documento Request For Comments, que é a base para o desenvolvimento de padrões LDAP). O exemplo anterior pode ser convertido no exemplo de código a seguir.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



Por que a palavra "subárvore" está no final da cadeia de caracteres? No mundo do diretório, você pode especificar o escopo da pesquisa. As opções são: "base", "onelevel" e "subtree". "base" é usado para ler o próprio objeto; "onelevel" refere-se aos filhos imediatos, semelhante ao **comando dir;** A "subárvore" é usada para pesquisar em vários níveis (semelhante a **dir /s**).

Com o SQL, você pode especificar o escopo na propriedade de comando, como no exemplo de código a seguir.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Se o escopo não for especificado, por padrão, ele usará uma pesquisa de subárvore.

> [!Note]  
> Se você usar C++, poderá usar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) da ADSI.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reorganização](reorganization.md)
</dt> </dl>

 

 




