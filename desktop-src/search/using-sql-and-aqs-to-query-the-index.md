---
description: Há várias maneiras de usar o Windows Search para consultar o índice. Este tópico descreve a sintaxe de consulta avançada (AQS) e abordagens baseadas no linguagem SQL (SQL).
ms.assetid: 544f03b3-cdf8-4550-a6da-e4a3bfc44744
title: Usando abordagens SQL e AQS para consultar o índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641bea0e6109182b5896aa1f0f981695fd91b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763439"
---
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a>Usando abordagens SQL e AQS para consultar o índice

Há várias maneiras de usar o Windows Search para consultar o índice. Este tópico descreve a sintaxe de consulta avançada (AQS) e abordagens baseadas no linguagem SQL (SQL).

Este tópico é organizado da seguinte maneira:

- [Consultas baseadas em SQL](#sql-based-queries)
  - [Usando OLE DB](#using-ole-db)
  - [Usando ADO e ADO.NET](#using-ado-and-adonet)
  - [Usando o SQL em consultas locais e remotas](#using-sql-in-local-and-remote-queries)
- [Consultas baseadas em AQS](#aqs-based-queries)
  - [Usando ISearchQueryHelper](#using-isearchqueryhelper)
  - [Usando o protocolo Search-MS](#using-the-search-ms-protocol)
- [Tópicos relacionados](#related-topics)

## <a name="sql-based-queries"></a>Consultas baseadas em SQL

SQL é uma linguagem de texto que define consultas. O SQL é comum entre muitas tecnologias de banco de dados diferentes. O Windows Search usa o SQL, implementa um subconjunto dele e o estende adicionando elementos ao idioma. O SQL Search do Windows usado pelo Windows Search estende partes da sintaxe de consulta de banco de dados SQL-92 e SQL-99 padrão para aprimorar sua utilidade com pesquisas baseadas em texto. Todos os recursos do Windows Search SQL são compatíveis com o Windows Search no Windows XP e no Windows Server 2003 e posterior.

Para obter mais informações sobre como usar a sintaxe SQL do Windows Search, consulte [consultando o índice com a sintaxe SQL do Windows Search](-search-sql-windowssearch-entry.md) e [visão geral da sintaxe SQL do Windows Search](-search-sql-ovwofsearchquery.md).

As abordagens a seguir para consultar o índice são baseadas em SQL.

### <a name="using-ole-db"></a>Usando OLE DB

O banco de dados de vinculação e incorporação de objetos (OLE DB) é uma API de Component Object Model (COM) que permite que você acesse diferentes tipos de repositórios de armazenamento uniformemente, incluindo bancos de dados não relacionais como planilhas. OLE DB separa o armazenamento de dados do aplicativo que o acessa por meio de um conjunto de abstrações que incluem a fonte de dados do Shell, a sessão, o comando e os conjuntos de linhas. Um provedor de OLE DB é um componente de software que implementa a interface OLE DB para fornecer dados a aplicativos de um armazenamento de dados específico.

Você pode acessar o provedor de OLE DB do Windows Search de forma programática usando os objetos OleDbConnection e OleDbSession em C \# e usando o suporte a OLE DB interno ao Active Template Library (ATL) em C++ (via atlclidb. h). A única propriedade que deve ser definida é a cadeia de caracteres do provedor.

Você pode usar a seguinte cadeia de caracteres:

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

Como alternativa, você pode obter a cadeia de conexão chamando [**ISearchQueryHelper:: get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring). Consulte usando [ISearchQueryHelper](#using-isearchqueryhelper) para obter um exemplo.

> [!Note]  
> O provedor de OLE DB do Windows Search é somente leitura e dá suporte a instruções SELECT e GROUP ON. Não há suporte para instruções INSERT e DELETE.

```cpp
#include <atldbcli.h>
CDataSource cDataSource;
hr = cDataSource.OpenFromInitializationString(L"provider=Search.CollatorDSO.1;EXTENDED PROPERTIES=\"Application=Windows\"");

if (SUCCEEDED(hr))
{
    CSession cSession;
    hr = cSession.Open(cDataSource);

    if (SUCCEEDED(hr))
    {
        CCommand<CDynamicAccessor, CRowset> cCommand;
        hr = cCommand.Open(cSession, pszSQL);

        if (SUCCEEDED(hr))
        {
            for (hr = cCommand.MoveFirst(); S_OK == hr; hr = cCommand.MoveNext())
            {
                for (DBORDINAL i = 1; i <= cCommand.GetColumnCount(); i++)
                {
                    PCWSTR pszName = cCommand.GetColumnName(i);
                    // do something with the column here
                }
            }
            cCommand.Close();
        }
    }
}
```

Para obter mais informações sobre OLE DB, consulte [visão geral da programação de OLE DB](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx). Para obter informações sobre o Provedor de Dados de .NET Framework para OLE DB, consulte a documentação do [namespace System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .

### <a name="using-ado-and-adonet"></a>Usando ADO e ADO.NET

O Microsoft ActiveX Data Objects (ADO) e o ADO.NET permitem que você grave aplicativos cliente para acessar e manipular dados em um servidor de banco de dado por meio de um provedor. O Windows Search é uma tecnologia somente leitura: você pode recuperar dados usando a pesquisa da área de trabalho, mas não pode alterar os dados usando o Windows Search. No entanto, você pode passar os resultados de uma pesquisa para uma tecnologia que pode alterar dados.

Os exemplos de código a seguir demonstram como abrir uma conexão com a fonte de dados, criar e abrir um conjunto de registros com uma instrução SELECT do [SQL Search do Windows](-search-sql-ovwofsearchquery.md) e obter as URLs dos cinco maiores arquivos do índice.

> [!Note]  
> Para obter informações sobre como obter a cadeia de conexão, consulte [consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)e [ISearchQueryHelper:: get \_ Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).

#### <a name="ado-and-vbscript"></a>ADO e VBScript

```VB
'To run this snippet, save it to a file and run it using cscript.exe from a command line.
'Running the .vbs file with Windows Script Host may cause dialog boxes to open for each item returned from the index.

On Error Resume Next

Set objConnection = CreateObject("ADODB.Connection")
Set objRecordSet = CreateObject("ADODB.Recordset")

objConnection.Open "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"

objRecordSet.Open "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC", objConnection

objRecordSet.MoveFirst
Do Until objRecordset.EOF
    Wscript.Echo objRecordset.Fields.Item("System.ItemPathDisplay")
    objRecordset.MoveNext
Loop
```

#### <a name="ado-and-c"></a>ADO e C++

```cpp
#import "msado15.dll" rename_namespace("ADO") rename("EOF", "EndOfFile") implementation_only

ADO::_ConnectionPtr connection = NULL;
HRESULT hr = connection.CreateInstance(__uuidof(ADO::Connection));
if (SUCCEEDED(hr))
{
    ADO::_RecordsetPtr recordset = NULL;
    hr = recordset.CreateInstance(__uuidof(ADO::Recordset));
    if (SUCCEEDED(hr))
    {
        connection->CursorLocation = ADO::adUseClient;
        hr = connection->Open(L"Provider=Search.CollatorDSO;Extended Properties='Application=Windows';",
            L"", L"", ADO::adConnectUnspecified);
        if (SUCCEEDED(hr))
        {
            hr = recordset->Open("SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC",
            connection.GetInterfacePtr(), ADO::adOpenForwardOnly, ADO::adLockReadOnly, ADO::adCmdText);
            if (SUCCEEDED(hr))
            {
                while (!recordset->EndOfFile)
                {
                    _variant_t var;
                    var = recordset->Fields->GetItem(L"System.ItemPathDisplay")->GetValue();
                    std::cout << static_cast<char *>(_bstr_t(var.bstrVal)) << std::endl;
                    recordset->MoveNext();
                };
                recordset->Close();
            }
            connection->Close();
        }
    }
}

```

#### <a name="ado-and-visualbasic"></a>ADO e VisualBasic

Primeiro, adicione uma referência ao ADODB em seu projeto

```VB
Dim con As ADODB.Connection
Dim rst As ADODB.Recordset

con = New ADODB.Connection
rst = New ADODB.Recordset

Dim sConString As String
Dim sSQLString As String

sConString = "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"
con.Open(sConString)

sSQLString = "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC"

rst = con.Execute(sSQLString)

Do Until (rst.EOF)
    Print(1, rst("System.ItemPathDisplay").Value)
    rst.MoveNext
Loop

rst.Close
rst = Nothing

con.Close
con = Nothing
```

#### <a name="adonet-and-c"></a>ADO.NET e C\#

```csharp
string query = @"SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC";

using (OleDbConnection objConnection =
    new OleDbConnection
    ("Provider=Search.CollatorDSO.1;Extended?Properties='Application=Windows';"))
{
    objConnection.Open();
    OleDbCommand cmd = new OleDbCommand(query, objConnection);
    using (OleDbDataReader rdr = cmd.ExecuteReader())
    {
        for (int i = 0; i < rdr.FieldCount; i++)
        {
            Console.Write(rdr.GetName(i));
            Console.Write('\t');
        }
        while (rdr.Read())
        {
            Console.WriteLine();
            for (int i = 0; i < rdr.FieldCount; i++)
            {
                Console.Write(rdr[i]);
                Console.Write('\t');
            }
        }
        Console.ReadKey();
    }
}
```

### <a name="using-sql-in-local-and-remote-queries"></a>Usando o SQL em consultas locais e remotas

Você pode executar suas consultas de forma local ou remota. Uma consulta local usando a [cláusula from](-search-sql-from.md) é mostrada no exemplo a seguir. Uma consulta local pesquisa apenas o catálogo SystemIndex local.

```sql
FROM SystemIndex
```

Uma consulta remota usando a [cláusula from](-search-sql-from.md) é mostrada no exemplo a seguir. Adicionar ComputerName transforma o exemplo anterior em uma consulta remota.

```sql
FROM [<ComputerName>.]SystemIndex
```

Por padrão, o Windows XP e o Windows Server 2003 não têm o Windows Search instalado. Somente o Windows Search 4 (WS4) fornece suporte de consulta remota. As versões anteriores do Windows Desktop Search (WDS), como 3, 1 e anteriores, não oferecem suporte a consultas remotas. Com o Windows Explorer, você pode consultar o índice local de um computador remoto para itens do sistema de arquivos (itens manipulados pelo protocolo "file:").

Para recuperar um item pela consulta remota, o item deve atender aos seguintes requisitos:

- Ser acessível por meio do caminho UNC (Convenção de nomenclatura universal).
- Existem no computador remoto ao qual o cliente tem acesso.
- Tenha sua segurança definida para permitir que o cliente tenha acesso de leitura.

O Windows Explorer tem recursos para compartilhar itens, incluindo um compartilhamento "público" ( \\ \\ público de máquina... \\ \\ ) no **centro de rede e compartilhamento** e um compartilhamento de "usuários" ( \\ \\ usuários do computador \\ \\ ...) para itens compartilhados por meio do assistente de compartilhamento. Depois de compartilhar as pastas, você pode consultar o índice local especificando o nome da máquina do computador remoto na cláusula FROM e um caminho UNC no computador remoto na cláusula SCOPE, conforme mostrado no exemplo a seguir:

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a>Consultas baseadas em AQS

AQS é a sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir os parâmetros de pesquisa. Embora o AQS seja principalmente voltado para o usuário, ele pode ser usado por desenvolvedores para criar consultas programaticamente. No Windows 7 Canonical AQS foi introduzido e deve ser usado no Windows 7 e posterior, para gerar programaticamente consultas AQS. Para obter informações detalhadas sobre o AQS, consulte [usando a sintaxe de consulta avançada programaticamente](-search-3x-advancedquerysyntax.md).

As abordagens a seguir para consultar o índice são baseadas em AQS.

### <a name="using-isearchqueryhelper"></a>Usando ISearchQueryHelper

Você pode desenvolver um componente ou classe auxiliar para consultar o índice usando a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , que permite que você aproveite alguns recursos do sistema e simplifique o uso do Windows Search. Essa interface ajuda você a:

- Obtenha uma cadeia de conexão OLE DB para se conectar ao banco de dados de pesquisa do Windows.
- Converta as consultas de usuário de AQS para SQL do Windows Search.

Essa interface é implementada como uma classe auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) e é obtida chamando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), conforme mostrado no exemplo de C++ a seguir.

```cpp
HRESULT GetQueryHelper(ISearchQueryHelper **ppQueryHelper)
{
    *ppQueryHelper = NULL;

    // Create an instance of the search manager

    ISearchManager *pSearchManager;
    HRESULT hr = CoCreateInstance(__uuidof(CSearchManager), NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));
    if (SUCCEEDED(hr))
    {
        // Get the catalog manager from the search manager
        ISearchCatalogManager *pSearchCatalogManager;
        hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
        if (SUCCEEDED(hr))
        {
            // Get the query helper from the catalog manager
            hr = pSearchCatalogManager->GetQueryHelper(ppQueryHelper);
            pSearchCatalogManager->Release();
        }
        pSearchManager->Release();
    }

    return hr;
}
```

Para implementar a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , consulte [usando a interface ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md) e o tópico referência do [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .

> [!Note]  
> Compatibilidade do Microsoft Windows Desktop Search (WDS) 2x herdada: em computadores que executam o Windows XP e o Windows Server 2003 e posterior, o [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) foi preterido. Em vez disso, os desenvolvedores devem usar [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para obter uma cadeia de conexão, analisar a consulta do usuário em SQL e, em seguida, consultar OLE DB.

### <a name="using-the-search-ms-protocol"></a>Usando o protocolo Search-MS

O [protocolo de aplicativo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) **pesquisa-MS** é uma Convenção para iniciar um aplicativo, como o Windows Explorer, para consultar o índice do Windows Search. Ele permite que as consultas sejam criadas com argumentos de valor de parâmetro, incluindo argumentos de propriedade, pesquisas salvas anteriormente, sintaxe de consulta avançada (AQS), sintaxe de consulta natural (NQS) e identificadores de código de idioma (LCIDs) para o indexador e a própria consulta.

Para obter informações detalhadas sobre a sintaxe do protocolo Search-MS, consulte [consultando o índice com o protocolo Search-MS](-search-3x-wds-qryidx-searchms.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Consulta do índice de maneira programática](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Consultando o índice com o protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Consultando o índice com a sintaxe SQL do Windows Search](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Usando a sintaxe de consulta avançada programaticamente](-search-3x-advancedquerysyntax.md)
</dt> </dl>
