---
title: Pesquisando objetos
description: Julie Bankert deve encontrar números de telefone para todos os gerentes de programa que trabalham no departamento 101. Ela pode criar um script que usa ADO e ADSI para fazer isso.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- Pesquisando objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103823581"
---
# <a name="searching-for-objects"></a>Pesquisando objetos

Julie Bankert deve encontrar números de telefone para todos os gerentes de programa que trabalham no departamento 101. Ela pode criar um script que usa ADO e ADSI para fazer isso.

Ao usar o provedor ADO para executar uma consulta, o conjunto de resultados retornará apenas os primeiros 1000 objetos. Por esse motivo, é importante usar uma consulta paginada para que você possa recuperar todos os objetos no conjunto de resultados, desde que o serviço de diretório não tenha sido definido para limitar o número de itens em um conjunto de resultados. Os conjuntos de retorno conterão o número de itens que você especificar no tamanho da página e os conjuntos paginados continuarão a ser retornados até que todos os itens no conjunto de resultados tenham sido retornados.


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



Para executar uma pesquisa de ADSI no Visual Basic ou em um ambiente de script, três componentes do ADO são necessários: **conexão**, **comando** e **conjunto de registros**. O objeto **Connection** permite que você especifique o nome do provedor, credenciais alternativas, se aplicável e outros sinalizadores. O objeto **Command** permite que você especifique as preferências de pesquisa e a cadeia de caracteres de consulta. Você deve associar o objeto de **conexão** a um objeto de **comando** antes da execução da consulta. Por fim, o objeto **Recordset** é usado para iterar o conjunto de resultados.

A ADSI dá suporte a dois tipos de cadeias de caracteres de consulta ou dialetos. O exemplo de código anterior usa o dialeto SQL. Você também pode usar o dialeto LDAP. A cadeia de caracteres de consulta de dialeto LDAP é baseada em [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (um RFC é um documento de solicitação de comentários, que é a base para o desenvolvimento de padrões LDAP). O exemplo anterior pode ser traduzido para o exemplo de código a seguir.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



Por que a palavra "subárvore" no final da cadeia de caracteres? No mundo do diretório, você pode especificar o escopo da pesquisa. As opções são: "base", "OneLevel" e "Subtree". "base" é usado para ler o objeto em si; "OneLevel" refere-se aos filhos imediatos, semelhante ao comando **dir** ; "Subtree" é usado para pesquisar vários níveis de profundidade ou para baixo (semelhante a **dir/s**).

Com o dialeto SQL, você pode especificar o escopo na Propriedade Command, como no exemplo de código a seguir.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Se o escopo não for especificado, por padrão ele usará uma pesquisa de subárvore.

> [!Note]  
> Se você usar o C++, poderá usar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) do ADSI.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reorganização](reorganization.md)
</dt> </dl>

 

 




