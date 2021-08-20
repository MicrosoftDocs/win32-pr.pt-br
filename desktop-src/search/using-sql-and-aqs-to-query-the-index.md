---
description: Há várias maneiras de usar o Windows Search para consultar o índice. Este tópico descreve as abordagens baseadas em AQS (Advanced Query Syntax) e linguagem SQL (SQL).
ms.assetid: 544f03b3-cdf8-4550-a6da-e4a3bfc44744
title: Usando SQL e abordagens do AQS para consultar o índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b19265efba27c1e523dcdded2c8d41568d279b0f713d48ba95a8968535f4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862393"
---
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a>Usando SQL e abordagens do AQS para consultar o índice

Há várias maneiras de usar o Windows Search para consultar o índice. Este tópico descreve as abordagens baseadas em AQS (Advanced Query Syntax) e linguagem SQL (SQL).

Este tópico é organizado da seguinte forma:

- [SQL Consultas baseadas](#sql-based-queries)
  - [Usando OLE DB](#using-ole-db)
  - [Usando ADO e ADO.NET](#using-ado-and-adonet)
  - [Usando SQL em consultas locais e remotas](#using-sql-in-local-and-remote-queries)
- [Consultas baseadas no AQS](#aqs-based-queries)
  - [Usando ISearchQueryHelper](#using-isearchqueryhelper)
  - [Usando o protocolo search-ms](#using-the-search-ms-protocol)
- [Tópicos relacionados](#related-topics)

## <a name="sql-based-queries"></a>SQL Consultas baseadas

SQL é um idioma de texto que define consultas. SQL é comum em muitas tecnologias de banco de dados diferentes. Windows A pesquisa SQL, implementa um subconjunto dele e o estende adicionando elementos à linguagem. O SQL Windows Search usado pelo Windows Search estende partes da sintaxe de consulta de banco de dados padrão SQL-92 e SQL-99 para aprimorar sua utilidade com pesquisas baseadas em texto. Todos os recursos do Windows Search SQL são compatíveis com o Windows Search no Windows XP e Windows Server 2003 e posterior.

Para obter mais informações sobre como usar Windows search SQL sintaxe, consulte Consultando o índice com sintaxe SQL [search](-search-sql-windowssearch-entry.md) Windows e Visão geral da sintaxe SQL do [Windows Search](-search-sql-ovwofsearchquery.md).

As abordagens a seguir para consultar o índice são baseadas SQL dados.

### <a name="using-ole-db"></a>Usando OLE DB

O banco de dados de vinculação e incorporação de objeto (OLE DB) é uma API de Component Object Model (COM) que permite que você acesse diferentes tipos de armazenamentos de dados uniformemente, incluindo bancos de dados não relacionais, como planilhas. OLE DB separa o armazenamento de dados do aplicativo que o acessa por meio de um conjunto de abstrações que incluem a fonte de dados do Shell, a sessão, o comando e os conjuntos de linhas. Um OLE DB de dados é um componente de software que implementa a interface OLE DB para fornecer dados a aplicativos de um armazenamento de dados específico.

Você pode acessar o provedor do Windows Search OLE DB programaticamente usando os objetos OleDbConnection e OleDbSession em C e usando o suporte do OLE DB integrado ao \# Active Template Library (ATL) em C++ (via atlclidb.h). A única propriedade que precisa ser definida é a cadeia de caracteres do provedor.

Você pode usar a seguinte cadeia de caracteres:

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

Como alternativa, você pode obter a cadeia de conexão chamando [**ISearchQueryHelper::get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring). Consulte Using [ISearchQueryHelper (Usando ISearchQueryHelper)](#using-isearchqueryhelper) para ver um exemplo.

> [!Note]  
> O Windows de OLE DB Search é somente leitura e é suportado por instruções SELECT e GROUP ON. Não há suporte para instruções INSERT e DELETE.

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

Para obter mais informações sobre OLE DB, consulte [Visão geral OLE DB programação.](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx) Para obter informações sobre o .NET Framework Provedor de Dados para OLE DB, consulte a documentação do [Namespace System.Data.OleDb.](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1)

### <a name="using-ado-and-adonet"></a>Usando ADO e ADO.NET

O Microsoft ActiveX ADO (Data Objects) e ADO.NET permitem que você escreva aplicativos cliente para acessar e manipular dados em um servidor de banco de dados por meio de um provedor. Windows A pesquisa é uma tecnologia somente leitura: você pode recuperar dados usando a Pesquisa de Área de Trabalho, mas não pode alterar os dados usando Windows Search. No entanto, você pode passar os resultados de uma pesquisa para uma tecnologia que pode alterar os dados.

Os exemplos de código a seguir demonstram como abrir uma conexão com a fonte de dados, criar e abrir um RecordSet com uma instrução SELECT do [Windows Search SQL](-search-sql-ovwofsearchquery.md) e obter as URLs dos cinco maiores arquivos do índice.

> [!Note]  
> Para obter informações sobre como obter a cadeia de conexão, consulte Consultando o índice com [ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)e [ISearchQueryHelper::get \_ Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).

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

### <a name="using-sql-in-local-and-remote-queries"></a>Usando SQL em consultas locais e remotas

Você pode executar suas consultas localmente ou remotamente. Uma consulta local usando a [cláusula FROM](-search-sql-from.md) é mostrada no exemplo a seguir. Uma consulta local consulta apenas o catálogo SystemIndex local.

```sql
FROM SystemIndex
```

Uma consulta remota usando a [cláusula FROM](-search-sql-from.md) é mostrada no exemplo a seguir. Adicionar ComputerName transforma o exemplo anterior em uma consulta remota.

```sql
FROM [<ComputerName>.]SystemIndex
```

Por padrão, Windows XP e Windows Server 2003 não têm o Windows Search instalado. Somente Windows Search 4 (WS4) fornece suporte à consulta remota. As versões anteriores Windows Pesquisa de Área de Trabalho (WDS), como a 3.01 e anteriores, não suportam consultas remotas. Com Windows Explorer, você pode consultar o índice local de um computador remoto para itens do sistema de arquivos (itens manipulados pelo protocolo "file:").

Para recuperar um item por consulta remota, o item deve atender aos seguintes requisitos:

- Ser acessível por meio do caminho UNC (Convenção Universal de Nomenização).
- Existem no computador remoto ao qual o cliente tem acesso.
- Ter sua segurança definida para permitir que o cliente tenha acesso de Leitura.

Windows O Explorer tem recursos para compartilhar itens, incluindo um compartilhamento "Público" ( Computador Público ...) no Central de Rede e Compartilhamento e um compartilhamento \\ \\ \\ \\ de "Usuários" (  \\ \\ \\ \\ Usuários do Computador ...) para itens compartilhados por meio do Assistente de Compartilhamento. Depois de compartilhar as pastas, você pode consultar o índice local especificando o nome do computador remoto na cláusula FROM e um caminho UNC no computador remoto na cláusula SCOPE, conforme mostrado no exemplo a seguir:

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a>Consultas baseadas no AQS

O AQS é a sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir parâmetros de pesquisa. Embora o AQS seja voltado principalmente para o usuário, ele pode ser usado por desenvolvedores para criar consultas programaticamente. No Windows 7 O AQS canônico foi introduzido e deve ser usado no Windows 7 e posterior, para gerar consultas do AQS programaticamente. Para obter informações detalhadas sobre o AQS, consulte [Using Advanced Query Syntax Programmatically](-search-3x-advancedquerysyntax.md).

As abordagens a seguir para consultar o índice são baseadas em AQS.

### <a name="using-isearchqueryhelper"></a>Usando ISearchQueryHelper

Você pode desenvolver um componente ou classe auxiliar para consultar o índice usando a interface [**ISearchQueryHelper,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) que permite que você aproveite alguns recursos do sistema e simplifique o uso do Windows Search. Essa interface ajuda você a:

- Obtenha uma cadeia OLE DB conexão para se conectar ao banco de dados Windows Search.
- Converta consultas de usuário do AQS para Windows Search SQL.

Essa interface é implementada como uma classe auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) e é obtida chamando [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), conforme mostrado no exemplo C++ a seguir.

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

Para implementar a interface [**ISearchQueryHelper,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) consulte Usando a [interface ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md) e o tópico de referência [**ISearchQueryHelper.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

> [!Note]  
> Compatibilidade 2x herdada do WDS (Microsoft Windows Desktop Search) : em computadores que executam o Windows XP e o Windows Server 2003 e posterior, [**o ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) foi preterido. Em vez disso, os desenvolvedores devem usar [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para obter uma cadeia de conexão, analisar a consulta do usuário no SQL e, em seguida, consultar por meio de OLE DB.

### <a name="using-the-search-ms-protocol"></a>Usando o protocolo search-ms

O **protocolo de aplicativo search-ms** [](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) é uma convenção para iniciar um aplicativo, como Windows Explorer, para consultar o índice Windows Search. Ele permite que as consultas sejam criadas com argumentos de parâmetro-valor, incluindo argumentos de propriedade, pesquisas salvas anteriormente, AQS (Sintaxe de Consulta Avançada), NQS (Sintaxe de Consulta Natural) e LCIDs (identificadores de código de idioma) para o indexador e a própria consulta.

Para obter informações detalhadas sobre a sintaxe do protocolo search-ms, consulte Consultando o [índice com o protocolo search-ms](-search-3x-wds-qryidx-searchms.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Consulta do índice de maneira programática](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Consultando o índice com o protocolo search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Consultando o índice com a sintaxe Windows pesquisa SQL pesquisa](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Usando a sintaxe de consulta avançada programaticamente](-search-3x-advancedquerysyntax.md)
</dt> </dl>
