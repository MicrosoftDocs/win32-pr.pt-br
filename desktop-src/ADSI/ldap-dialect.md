---
title: Dialeto LDAP
description: O dialeto LDAP é um formato para instruções de consulta que usam a sintaxe de filtro de pesquisa LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- ADSI do dialeto LDAP
- dialetos ADSI, dialeto LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c231d3c4d619775cca2ed9542733bff51219d92ff31d922f6d38ea7b1bcd2e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509976"
---
# <a name="ldap-dialect"></a>Dialeto LDAP

O dialeto LDAP é um formato para instruções de consulta que usam a sintaxe de filtro de [pesquisa LDAP](search-filter-syntax.md). Use uma instrução de consulta LDAP com as seguintes interfaces de pesquisa ADSI:

-   As [interfaces ActiveX objeto de dados (ADO),](searching-with-activex-data-objects-ado.md) que são interfaces de Automação que usam OLE DB.
-   [OLE DB](searching-with-ole-db.md), que é um conjunto de interfaces C/C++ para consultar bancos de dados.
-   [**IDirectorySearch,**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)que é a interface C/C++ do Active Directory.

Uma cadeia de caracteres de dialeto LDAP consiste em quatro partes separadas por ponto e vírgula (;).

-   Nome diferenciado básico. Por exemplo:

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   Filtros de pesquisa LDAP. Para obter mais informações sobre filtros de pesquisa, consulte [Sintaxe de filtro de pesquisa](search-filter-syntax.md).
-   O nome de exibição LDAP dos atributos a recuperar. Vários atributos são separados por uma vírgula.
-   Especifica o escopo da pesquisa. Os valores válidos são "base", "onelevel" e "subtree". O escopo especificado em uma cadeia de caracteres de consulta LDAP substitui qualquer escopo de pesquisa especificado pela propriedade "SearchScope" do objeto comando ADO.

A seguir está um exemplo de código do dialeto LDAP na ADSI que pesquisa todos os objetos na subárvore.


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



Nem todas as opções de pesquisa (tamanho da página de pesquisa, por exemplo) podem ser expressas no dialeto LDAP, portanto, você deve definir as opções antes que a execução real da consulta seja iniciada.

## <a name="example-code-for-performing-an-ldap-query"></a>Código de exemplo para executar uma consulta LDAP

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



Para obter detalhes sobre a sintaxe de consulta, consulte [Sintaxe de filtro de pesquisa](search-filter-syntax.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de filtro de pesquisa](search-filter-syntax.md)
</dt> <dt>

[SQL dialeto](sql-dialect.md)
</dt> <dt>

[Pesquisando com a interface IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Pesquisando com objetos ActiveX dados](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Pesquisando com OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




