---
title: Pesquisando com ActiveX Data Objects (ADO)
description: O modelo ADO (ActiveX Data Object) consiste em objetos listados na tabela a seguir.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI, pesquisando com ADO
- Pesquisando com ActiveX Data Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105755452"
---
# <a name="searching-with-activex-data-objects-ado"></a>Pesquisando com ActiveX Data Objects (ADO)

O modelo ADO (ActiveX Data Object) consiste em objetos listados na tabela a seguir.



| Objeto         | Descrição                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| **Conexão** | Uma conexão aberta com uma fonte de dados OLE DB como ADSI.                                                                          |
| **Comando**    | Define um comando específico a ser executado na fonte de dados.                                                                         |
| **Parâmetro**  | Uma coleção opcional para quaisquer parâmetros a serem fornecidos ao objeto de comando.                                                        |
| **Registros**  | Um conjunto de registros de uma tabela, objeto de comando ou sintaxe SQL. Um conjunto de registros pode ser criado sem nenhum objeto de conexão subjacente. |
| **Campo**      | Uma única coluna de dados em um conjunto de registros.                                                                                            |
| **Propriedade**   | Uma coleção de valores fornecidos pelo provedor para ADO.                                                                           |
| **Erro**      | Contém dados sobre erros de acesso a dados. Atualizado quando ocorre um erro em uma única operação.                                      |



 

Para que o ADO se comunique com a ADSI, deve haver, pelo menos, dois objetos ADO: **Connection** e **Recordset**. Esses objetos ADO servem para autenticar usuários e enumerar resultados, respectivamente. Normalmente, você também usará um objeto de **comando** para manter uma conexão ativa, especificar parâmetros de consulta, como o tamanho da página e o escopo da pesquisa, e executar uma consulta. Para obter mais informações sobre a sintaxe do filtro de pesquisa, consulte [sintaxe do filtro de pesquisa](search-filter-syntax.md).

O objeto de **conexão** carrega o provedor de OLE DB e valida as credenciais do usuário. Em Visual Basic, chame a função **CreateObject** com "ADODB. Conexão "para criar uma instância de um objeto de **conexão** e, em seguida, defina a propriedade do **provedor** do objeto de **conexão** como" ADsDSOObject ". ActiveX. Conexão "é o ProgID do objeto de **conexão** e" ADsDSOObject "é o nome do provedor de OLE DB no ADSI. Se nenhuma credencial for especificada, as credenciais do usuário conectado no momento serão usadas.

O exemplo de código a seguir mostra como criar uma instância de um objeto de **conexão** .


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



O exemplo de código a seguir mostra como criar uma instância de um objeto de **conexão** .


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



O exemplo de código a seguir mostra como criar uma instância de um objeto de **conexão** . Lembre-se de que você deve incluir a biblioteca de tipos do ADO (msadoXX.dll) como uma das referências no projeto Visual Basic.


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



Especifique os dados de autenticação de usuário definindo as propriedades do objeto de **conexão** . A tabela a seguir lista as propriedades de autenticação de usuário com suporte ADSI.



| Propriedade           | Descrição                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "ID de usuário"          | Uma cadeia de caracteres que identifica o usuário cujo contexto de segurança é usado ao executar a pesquisa. Para obter mais informações sobre o formato da cadeia de caracteres de nome de usuário, consulte [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Se não for especificado, o padrão será o usuário conectado ou o usuário representado pelo processo de chamada. |
| "Password"         | Uma cadeia de caracteres que especifica a senha do usuário identificada por "ID de usuário".                                                                                                                                                                                                                                                                      |
| "Criptografar senha" | Um valor booliano que especifica se a senha é criptografada. O padrão é **false**.                                                                                                                                                                                                                                                    |
| "Sinalizador ADSI"        | Um conjunto de sinalizadores da enumeração de enumeração de [**\_ \_ autenticação do ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) que especificam as opções de autenticação de associação. O padrão é zero.                                                                                                                                                                         |



 

O exemplo de código a seguir mostra como as propriedades são definidas antes da criação do objeto de **comando** .


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



O segundo objeto ADO é o objeto **Command** . O ProgID do objeto de **comando** é "ADODB. Command". Esse objeto permite que você emita instruções de consulta e outros comandos para a ADSI usando a conexão ativa. O objeto **Command** usa sua propriedade **ActiveConnection** para manter uma conexão ativa. Ele também mantém a propriedade **CommandText** para manter instruções de consulta emitidas por um usuário. As instruções de consulta são expressas no [dialeto SQL](sql-dialect.md) ou no [dialeto LDAP](ldap-dialect.md).

Os exemplos de código a seguir mostram como criar um objeto de **comando** .


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



No exemplo de código a seguir, inclua a biblioteca de tipos do ADO (msadoXX.dll) como uma das referências.


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



As opções de pesquisa para o objeto de **comando** são especificadas definindo a propriedade **Properties** . A tabela a seguir lista as propriedades nomeadas aceitáveis para **Propriedades**.



| Propriedade nomeada      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manipulador      | Um valor booliano que especifica se a pesquisa é síncrona ou assíncrona. O padrão é false (síncrono). Um bloco de pesquisa síncrono até que o servidor retorne todo o resultado, ou para uma pesquisa paginada, a página inteira. Um bloco de pesquisa assíncrono até que uma linha dos resultados da pesquisa esteja disponível ou até que o tempo especificado pela propriedade "Timeout" decorra.                           |
| "Resultados do cache"     | Um valor booliano que especifica se o resultado deve ser armazenado em cache no lado do cliente. O padrão é **true**; O ADSI armazena em cache o conjunto de resultados. Desativar essa opção pode ser desejável para grandes conjuntos de resultados.                                                                                                                                                                                                    |
| "Perseguir referências"   | Um valor dos anúncios buscam [**\_ \_ \_ enums de referências**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) que especifica como a pesquisa procura referências. O padrão é **ADS \_ Chase \_ referências \_ nunca**. Para obter mais informações sobre essa propriedade, consulte [referências](/windows/desktop/AD/referrals).<br/>                                                                                                                                           |
| "Somente nomes de coluna" | Um valor booliano que indica que a pesquisa deve recuperar somente o nome dos atributos aos quais os valores foram atribuídos. O padrão é **false**.                                                                                                                                                                                                                                                       |
| "Aliases Deref"     | Um valor booliano que especifica se os aliases de objetos encontrados são resolvidos. O padrão é **false**.                                                                                                                                                                                                                                                                                                        |
| "Tamanho da página"         | Um valor inteiro que ativa a paginação e especifica o número máximo de objetos a serem retornados em um conjunto de resultados. O padrão é nenhum tamanho de página. Para obter mais informações, consulte [recuperando conjuntos de resultados grandes](retrieving-large-results-sets.md).                                                                                                                                                                       |
| SearchScope       | Um valor da enumeração [**\_ SCOPEENUM ADS**](/windows/win32/api/iads/ne-iads-ads_scopeenum) que especifica o escopo da pesquisa. O padrão é **a \_ \_ subárvore de escopo ADS**.                                                                                                                                                                                                                                                                  |
| "Limite de tamanho"        | Um valor inteiro que especifica o limite de tamanho para a pesquisa. Por Active Directory, o limite de tamanho especifica o número máximo de objetos retornados. O servidor para de Pesquisar quando o limite de tamanho é atingido e retorna os resultados acumulados. O padrão é sem limite.                                                                                                                                  |
| "Classificar em"           | Uma cadeia de caracteres que especifica uma lista separada por vírgulas de atributos a serem usados como chaves de classificação. Essa propriedade funciona somente para servidores de diretório que dão suporte ao controle LDAP para classificação no lado do servidor. O Active Directory dá suporte ao controle de classificação, mas pode afetar o desempenho do servidor, especialmente se o conjunto de resultados for grande. Lembre-se de que Active Directory dá suporte apenas a uma única chave de classificação. O padrão é sem classificação. |
| "Limite de tempo"        | Um valor inteiro que especifica o limite de tempo, em segundos, para a pesquisa. Quando o limite de tempo é atingido, o servidor para de Pesquisar e retorna os resultados acumulados. O padrão é sem limite de tempo.                                                                                                                                                                                                      |
| Cedido           | Um valor inteiro que especifica o valor de tempo limite do lado do cliente, em segundos. Esse valor indica a hora em que o cliente aguarda os resultados do servidor antes de parar a pesquisa. O padrão não é tempo limite.                                                                                                                                                                                                  |



 

O exemplo de código a seguir mostra como definir opções de pesquisa.


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



O terceiro objeto ADO é **Recordset**. Você obtém esse objeto ao invocar o método **Execute** em um objeto **Command** . A função principal do objeto **Recordset** é enumerar o conjunto de resultados e obter os dados. O conjunto de resultados pode conter valores para atributos que têm valores únicos ou múltiplos. Obter um atributo de valor único é simples, semelhante a obter o valor da coluna no banco de dados relacional, por exemplo:


```VB
Fields('name').Value
```



No entanto, obter um atributo com vários valores é mais desafiador. Nesse caso, o **campo. Value** é uma matriz e você deve verificar o limite inferior e superior da matriz, conforme mostrado no exemplo de código a seguir.


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



O exemplo de código a seguir desabilita as contas de usuário em um servidor LDAP.


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



Para obter mais informações sobre o modelo de objeto ADO, consulte [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).

 

