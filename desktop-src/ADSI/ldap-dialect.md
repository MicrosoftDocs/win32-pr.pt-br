---
title: Dialeto LDAP
description: O dialeto LDAP é um formato para instruções de consulta que usam a sintaxe de filtro de pesquisa LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- ADSI de dialeto LDAP
- dialeto ADSI, dialeto LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822204"
---
# <a name="ldap-dialect"></a>Dialeto LDAP

O dialeto LDAP é um formato para instruções de consulta que usam a [sintaxe de filtro de pesquisa LDAP](search-filter-syntax.md). Use uma instrução de consulta LDAP com as seguintes interfaces de pesquisa ADSI:

-   As interfaces [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , que são interfaces de automação que usam OLE DB.
-   [OLE DB](searching-with-ole-db.md), que é um conjunto de interfaces C/C++ para consultar bancos de dados.
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), que é a interface C/C++ para Active Directory.

Uma cadeia de caracteres de dialeto LDAP consiste em quatro partes separadas por ponto e vírgula (;).

-   Nome distinto base. Por exemplo:

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   Filtros de pesquisa LDAP. Para obter mais informações sobre filtros de pesquisa, consulte [sintaxe do filtro de pesquisa](search-filter-syntax.md).
-   O nome de exibição LDAP dos atributos a serem recuperados. Vários atributos são separados por uma vírgula.
-   Especifica o escopo da pesquisa. Os valores válidos são "base", "OneLevel" e "Subtree". O escopo especificado em uma cadeia de caracteres de consulta LDAP substitui qualquer escopo de pesquisa especificado pela propriedade "SearchScope" do objeto de comando ADO.

Veja a seguir um exemplo de código do dialeto LDAP no ADSI que pesquisa todos os objetos na subárvore.


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



Nem todas as opções de pesquisa (o tamanho da página de pesquisa, por exemplo) podem ser expressas no dialeto LDAP, portanto, você deve definir as opções antes que a execução real da consulta seja iniciada.

## <a name="example-code-for-performing-an-ldap-query"></a>Exemplo de código para executar uma consulta LDAP

O exemplo de código a seguir mostra como usar uma consulta LDAP


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



Para obter detalhes sobre a sintaxe de consulta, consulte [sintaxe do filtro de pesquisa](search-filter-syntax.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe do filtro de pesquisa](search-filter-syntax.md)
</dt> <dt>

[Dialeto SQL](sql-dialect.md)
</dt> <dt>

[Pesquisando com a interface IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Pesquisando com OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




