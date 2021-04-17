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
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a><span data-ttu-id="61b92-104">Usando abordagens SQL e AQS para consultar o índice</span><span class="sxs-lookup"><span data-stu-id="61b92-104">Using SQL and AQS Approaches to Query the Index</span></span>

<span data-ttu-id="61b92-105">Há várias maneiras de usar o Windows Search para consultar o índice.</span><span class="sxs-lookup"><span data-stu-id="61b92-105">There are several ways to use Windows Search to query the index.</span></span> <span data-ttu-id="61b92-106">Este tópico descreve a sintaxe de consulta avançada (AQS) e abordagens baseadas no linguagem SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="61b92-106">This topic outlines Advanced Query Syntax (AQS) and Structured Query Language (SQL) based approaches.</span></span>

<span data-ttu-id="61b92-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="61b92-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="61b92-108">Consultas baseadas em SQL</span><span class="sxs-lookup"><span data-stu-id="61b92-108">SQL Based Queries</span></span>](#sql-based-queries)
  - [<span data-ttu-id="61b92-109">Usando OLE DB</span><span class="sxs-lookup"><span data-stu-id="61b92-109">Using OLE DB</span></span>](#using-ole-db)
  - [<span data-ttu-id="61b92-110">Usando ADO e ADO.NET</span><span class="sxs-lookup"><span data-stu-id="61b92-110">Using ADO and ADO.NET</span></span>](#using-ado-and-adonet)
  - [<span data-ttu-id="61b92-111">Usando o SQL em consultas locais e remotas</span><span class="sxs-lookup"><span data-stu-id="61b92-111">Using SQL in Local and Remote Queries</span></span>](#using-sql-in-local-and-remote-queries)
- [<span data-ttu-id="61b92-112">Consultas baseadas em AQS</span><span class="sxs-lookup"><span data-stu-id="61b92-112">AQS Based Queries</span></span>](#aqs-based-queries)
  - [<span data-ttu-id="61b92-113">Usando ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="61b92-113">Using ISearchQueryHelper</span></span>](#using-isearchqueryhelper)
  - [<span data-ttu-id="61b92-114">Usando o protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="61b92-114">Using the search-ms Protocol</span></span>](#using-the-search-ms-protocol)
- [<span data-ttu-id="61b92-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61b92-115">Related topics</span></span>](#related-topics)

## <a name="sql-based-queries"></a><span data-ttu-id="61b92-116">Consultas baseadas em SQL</span><span class="sxs-lookup"><span data-stu-id="61b92-116">SQL Based Queries</span></span>

<span data-ttu-id="61b92-117">SQL é uma linguagem de texto que define consultas.</span><span class="sxs-lookup"><span data-stu-id="61b92-117">SQL is a text language that defines queries.</span></span> <span data-ttu-id="61b92-118">O SQL é comum entre muitas tecnologias de banco de dados diferentes.</span><span class="sxs-lookup"><span data-stu-id="61b92-118">SQL is common across many different database technologies.</span></span> <span data-ttu-id="61b92-119">O Windows Search usa o SQL, implementa um subconjunto dele e o estende adicionando elementos ao idioma.</span><span class="sxs-lookup"><span data-stu-id="61b92-119">Windows Search uses SQL, implements a subset of it, and extends it by adding elements to the language.</span></span> <span data-ttu-id="61b92-120">O SQL Search do Windows usado pelo Windows Search estende partes da sintaxe de consulta de banco de dados SQL-92 e SQL-99 padrão para aprimorar sua utilidade com pesquisas baseadas em texto.</span><span class="sxs-lookup"><span data-stu-id="61b92-120">The Windows Search SQL used by Windows Search extends portions of the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span> <span data-ttu-id="61b92-121">Todos os recursos do Windows Search SQL são compatíveis com o Windows Search no Windows XP e no Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61b92-121">All features of Windows Search SQL are compatible with Windows Search on Windows XP and Windows Server 2003, and later.</span></span>

<span data-ttu-id="61b92-122">Para obter mais informações sobre como usar a sintaxe SQL do Windows Search, consulte [consultando o índice com a sintaxe SQL do Windows Search](-search-sql-windowssearch-entry.md) e [visão geral da sintaxe SQL do Windows Search](-search-sql-ovwofsearchquery.md).</span><span class="sxs-lookup"><span data-stu-id="61b92-122">For more information about using Windows Search SQL syntax, see [Querying the Index with Windows Search SQL Syntax](-search-sql-windowssearch-entry.md) and [Overview of Windows Search SQL Syntax](-search-sql-ovwofsearchquery.md).</span></span>

<span data-ttu-id="61b92-123">As abordagens a seguir para consultar o índice são baseadas em SQL.</span><span class="sxs-lookup"><span data-stu-id="61b92-123">The following approaches for querying the index are SQL based.</span></span>

### <a name="using-ole-db"></a><span data-ttu-id="61b92-124">Usando OLE DB</span><span class="sxs-lookup"><span data-stu-id="61b92-124">Using OLE DB</span></span>

<span data-ttu-id="61b92-125">O banco de dados de vinculação e incorporação de objetos (OLE DB) é uma API de Component Object Model (COM) que permite que você acesse diferentes tipos de repositórios de armazenamento uniformemente, incluindo bancos de dados não relacionais como planilhas.</span><span class="sxs-lookup"><span data-stu-id="61b92-125">The Object Linking and Embedding Database (OLE DB) is a Component Object Model (COM) API that enables you to access different types of data stores uniformly, including non-relational databases like spreadsheets.</span></span> <span data-ttu-id="61b92-126">OLE DB separa o armazenamento de dados do aplicativo que o acessa por meio de um conjunto de abstrações que incluem a fonte de dados do Shell, a sessão, o comando e os conjuntos de linhas.</span><span class="sxs-lookup"><span data-stu-id="61b92-126">OLE DB separates the data store from the application accessing it through a set of abstractions that include the Shell data source, session, command, and rowsets.</span></span> <span data-ttu-id="61b92-127">Um provedor de OLE DB é um componente de software que implementa a interface OLE DB para fornecer dados a aplicativos de um armazenamento de dados específico.</span><span class="sxs-lookup"><span data-stu-id="61b92-127">An OLE DB provider is a software component that implements the OLE DB interface to provide data to applications from a particular data store.</span></span>

<span data-ttu-id="61b92-128">Você pode acessar o provedor de OLE DB do Windows Search de forma programática usando os objetos OleDbConnection e OleDbSession em C \# e usando o suporte a OLE DB interno ao Active Template Library (ATL) em C++ (via atlclidb. h).</span><span class="sxs-lookup"><span data-stu-id="61b92-128">You can access the Windows Search OLE DB provider programmatically by using the OleDbConnection and OleDbSession objects in C\# and by using the OLE DB support built into Active Template Library (ATL) in C++ (via atlclidb.h).</span></span> <span data-ttu-id="61b92-129">A única propriedade que deve ser definida é a cadeia de caracteres do provedor.</span><span class="sxs-lookup"><span data-stu-id="61b92-129">The only property that has to be set is the provider string.</span></span>

<span data-ttu-id="61b92-130">Você pode usar a seguinte cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="61b92-130">You can use the following string:</span></span>

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

<span data-ttu-id="61b92-131">Como alternativa, você pode obter a cadeia de conexão chamando [**ISearchQueryHelper:: get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="61b92-131">Alternatively, you can get the connection string by calling [**ISearchQueryHelper::get\_ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span> <span data-ttu-id="61b92-132">Consulte usando [ISearchQueryHelper](#using-isearchqueryhelper) para obter um exemplo.</span><span class="sxs-lookup"><span data-stu-id="61b92-132">See Using [ISearchQueryHelper](#using-isearchqueryhelper) for an example.</span></span>

> [!Note]  
> <span data-ttu-id="61b92-133">O provedor de OLE DB do Windows Search é somente leitura e dá suporte a instruções SELECT e GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="61b92-133">The Windows Search OLE DB provider is read-only, and support SELECT and GROUP ON statements.</span></span> <span data-ttu-id="61b92-134">Não há suporte para instruções INSERT e DELETE.</span><span class="sxs-lookup"><span data-stu-id="61b92-134">INSERT and DELETE statements are not supported.</span></span>

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

<span data-ttu-id="61b92-135">Para obter mais informações sobre OLE DB, consulte [visão geral da programação de OLE DB](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="61b92-135">For more information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span></span> <span data-ttu-id="61b92-136">Para obter informações sobre o Provedor de Dados de .NET Framework para OLE DB, consulte a documentação do [namespace System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .</span><span class="sxs-lookup"><span data-stu-id="61b92-136">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) documentation.</span></span>

### <a name="using-ado-and-adonet"></a><span data-ttu-id="61b92-137">Usando ADO e ADO.NET</span><span class="sxs-lookup"><span data-stu-id="61b92-137">Using ADO and ADO.NET</span></span>

<span data-ttu-id="61b92-138">O Microsoft ActiveX Data Objects (ADO) e o ADO.NET permitem que você grave aplicativos cliente para acessar e manipular dados em um servidor de banco de dado por meio de um provedor.</span><span class="sxs-lookup"><span data-stu-id="61b92-138">Microsoft ActiveX Data Objects (ADO) and ADO.NET enable you to write client applications to access and manipulate data in a database server through a provider.</span></span> <span data-ttu-id="61b92-139">O Windows Search é uma tecnologia somente leitura: você pode recuperar dados usando a pesquisa da área de trabalho, mas não pode alterar os dados usando o Windows Search.</span><span class="sxs-lookup"><span data-stu-id="61b92-139">Windows Search is a read-only technology: you can retrieve data using Desktop Search but you can't change data using Windows Search.</span></span> <span data-ttu-id="61b92-140">No entanto, você pode passar os resultados de uma pesquisa para uma tecnologia que pode alterar dados.</span><span class="sxs-lookup"><span data-stu-id="61b92-140">You can, however, pass the results of a search over to a technology that can change data.</span></span>

<span data-ttu-id="61b92-141">Os exemplos de código a seguir demonstram como abrir uma conexão com a fonte de dados, criar e abrir um conjunto de registros com uma instrução SELECT do [SQL Search do Windows](-search-sql-ovwofsearchquery.md) e obter as URLs dos cinco maiores arquivos do índice.</span><span class="sxs-lookup"><span data-stu-id="61b92-141">The following code examples demonstrate how to open a connection to the data source, create and open a RecordSet with a [Windows Search SQL](-search-sql-ovwofsearchquery.md) SELECT statement, and get the URLs of the five largest files from the index.</span></span>

> [!Note]  
> <span data-ttu-id="61b92-142">Para obter informações sobre como obter a cadeia de conexão, consulte [consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)e [ISearchQueryHelper:: get \_ Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="61b92-142">For information on how to obtain the connection string, see [Querying the Index with ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md), and [ISearchQueryHelper::get\_Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span>

#### <a name="ado-and-vbscript"></a><span data-ttu-id="61b92-143">ADO e VBScript</span><span class="sxs-lookup"><span data-stu-id="61b92-143">ADO and VBScript</span></span>

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

#### <a name="ado-and-c"></a><span data-ttu-id="61b92-144">ADO e C++</span><span class="sxs-lookup"><span data-stu-id="61b92-144">ADO and C++</span></span>

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

#### <a name="ado-and-visualbasic"></a><span data-ttu-id="61b92-145">ADO e VisualBasic</span><span class="sxs-lookup"><span data-stu-id="61b92-145">ADO and VisualBasic</span></span>

<span data-ttu-id="61b92-146">Primeiro, adicione uma referência ao ADODB em seu projeto</span><span class="sxs-lookup"><span data-stu-id="61b92-146">First add a reference to ADODB in your project</span></span>

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

#### <a name="adonet-and-c"></a><span data-ttu-id="61b92-147">ADO.NET e C\#</span><span class="sxs-lookup"><span data-stu-id="61b92-147">ADO.NET and C\#</span></span>

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

### <a name="using-sql-in-local-and-remote-queries"></a><span data-ttu-id="61b92-148">Usando o SQL em consultas locais e remotas</span><span class="sxs-lookup"><span data-stu-id="61b92-148">Using SQL in Local and Remote Queries</span></span>

<span data-ttu-id="61b92-149">Você pode executar suas consultas de forma local ou remota.</span><span class="sxs-lookup"><span data-stu-id="61b92-149">You can execute your queries either locally or remotely.</span></span> <span data-ttu-id="61b92-150">Uma consulta local usando a [cláusula from](-search-sql-from.md) é mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="61b92-150">A local query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="61b92-151">Uma consulta local pesquisa apenas o catálogo SystemIndex local.</span><span class="sxs-lookup"><span data-stu-id="61b92-151">A local query queries the local SystemIndex catalog only.</span></span>

```sql
FROM SystemIndex
```

<span data-ttu-id="61b92-152">Uma consulta remota usando a [cláusula from](-search-sql-from.md) é mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="61b92-152">A remote query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="61b92-153">Adicionar ComputerName transforma o exemplo anterior em uma consulta remota.</span><span class="sxs-lookup"><span data-stu-id="61b92-153">Adding ComputerName transforms the previous example into a remote query.</span></span>

```sql
FROM [<ComputerName>.]SystemIndex
```

<span data-ttu-id="61b92-154">Por padrão, o Windows XP e o Windows Server 2003 não têm o Windows Search instalado.</span><span class="sxs-lookup"><span data-stu-id="61b92-154">By default, Windows XP and Windows Server 2003 do not have Windows Search installed.</span></span> <span data-ttu-id="61b92-155">Somente o Windows Search 4 (WS4) fornece suporte de consulta remota.</span><span class="sxs-lookup"><span data-stu-id="61b92-155">Only Windows Search 4 (WS4) provides remote query support.</span></span> <span data-ttu-id="61b92-156">As versões anteriores do Windows Desktop Search (WDS), como 3, 1 e anteriores, não oferecem suporte a consultas remotas.</span><span class="sxs-lookup"><span data-stu-id="61b92-156">Previous versions of Windows Desktop Search (WDS), such as 3.01 and earlier, do not support remote querying.</span></span> <span data-ttu-id="61b92-157">Com o Windows Explorer, você pode consultar o índice local de um computador remoto para itens do sistema de arquivos (itens manipulados pelo protocolo "file:").</span><span class="sxs-lookup"><span data-stu-id="61b92-157">With Windows Explorer you can query the local index of a remote computer for file system items (items handled by the "file:" protocol).</span></span>

<span data-ttu-id="61b92-158">Para recuperar um item pela consulta remota, o item deve atender aos seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="61b92-158">To retrieve an item by remote query, the item must meet the following requirements:</span></span>

- <span data-ttu-id="61b92-159">Ser acessível por meio do caminho UNC (Convenção de nomenclatura universal).</span><span class="sxs-lookup"><span data-stu-id="61b92-159">Be accessible via Universal Naming Convention (UNC) path.</span></span>
- <span data-ttu-id="61b92-160">Existem no computador remoto ao qual o cliente tem acesso.</span><span class="sxs-lookup"><span data-stu-id="61b92-160">Exist on the remote computer to which the client has access.</span></span>
- <span data-ttu-id="61b92-161">Tenha sua segurança definida para permitir que o cliente tenha acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="61b92-161">Have its security set to allow the client to have Read access.</span></span>

<span data-ttu-id="61b92-162">O Windows Explorer tem recursos para compartilhar itens, incluindo um compartilhamento "público" ( \\ \\ público de máquina... \\ \\ ) no **centro de rede e compartilhamento** e um compartilhamento de "usuários" ( \\ \\ usuários do computador \\ \\ ...) para itens compartilhados por meio do assistente de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="61b92-162">Windows Explorer has features for sharing items including a "Public" share (\\\\Machine\\Public\\...) in the **Network and Sharing Center**, and a "Users" share (\\\\Machine\\Users\\...) for items shared through the Sharing Wizard.</span></span> <span data-ttu-id="61b92-163">Depois de compartilhar as pastas, você pode consultar o índice local especificando o nome da máquina do computador remoto na cláusula FROM e um caminho UNC no computador remoto na cláusula SCOPE, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="61b92-163">After you share the folder(s), you can query the local index by specifying the remote computer's machine name in the FROM clause, and a UNC path on the remote machine in the SCOPE clause, as shown in the following example:</span></span>

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a><span data-ttu-id="61b92-164">Consultas baseadas em AQS</span><span class="sxs-lookup"><span data-stu-id="61b92-164">AQS Based Queries</span></span>

<span data-ttu-id="61b92-165">AQS é a sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir os parâmetros de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="61b92-165">AQS is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="61b92-166">Embora o AQS seja principalmente voltado para o usuário, ele pode ser usado por desenvolvedores para criar consultas programaticamente.</span><span class="sxs-lookup"><span data-stu-id="61b92-166">While AQS is primarily user facing, it can be used by developers to build queries programmatically.</span></span> <span data-ttu-id="61b92-167">No Windows 7 Canonical AQS foi introduzido e deve ser usado no Windows 7 e posterior, para gerar programaticamente consultas AQS.</span><span class="sxs-lookup"><span data-stu-id="61b92-167">In Windows 7 canonical AQS was introduced, and must be used in Windows 7 and later, to programmatically generate AQS queries.</span></span> <span data-ttu-id="61b92-168">Para obter informações detalhadas sobre o AQS, consulte [usando a sintaxe de consulta avançada programaticamente](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="61b92-168">For detailed information on AQS, see [Using Advanced Query Syntax Programmatically](-search-3x-advancedquerysyntax.md).</span></span>

<span data-ttu-id="61b92-169">As abordagens a seguir para consultar o índice são baseadas em AQS.</span><span class="sxs-lookup"><span data-stu-id="61b92-169">The following approaches for querying the index are AQS based.</span></span>

### <a name="using-isearchqueryhelper"></a><span data-ttu-id="61b92-170">Usando ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="61b92-170">Using ISearchQueryHelper</span></span>

<span data-ttu-id="61b92-171">Você pode desenvolver um componente ou classe auxiliar para consultar o índice usando a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , que permite que você aproveite alguns recursos do sistema e simplifique o uso do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="61b92-171">You can develop a component or helper class to query the index by using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, which enables you to take advantage of some features of the system and simplify your use of Windows Search.</span></span> <span data-ttu-id="61b92-172">Essa interface ajuda você a:</span><span class="sxs-lookup"><span data-stu-id="61b92-172">This interface helps you:</span></span>

- <span data-ttu-id="61b92-173">Obtenha uma cadeia de conexão OLE DB para se conectar ao banco de dados de pesquisa do Windows.</span><span class="sxs-lookup"><span data-stu-id="61b92-173">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
- <span data-ttu-id="61b92-174">Converta as consultas de usuário de AQS para SQL do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="61b92-174">Convert user queries from AQS to Windows Search SQL.</span></span>

<span data-ttu-id="61b92-175">Essa interface é implementada como uma classe auxiliar para [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) e é obtida chamando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), conforme mostrado no exemplo de C++ a seguir.</span><span class="sxs-lookup"><span data-stu-id="61b92-175">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), as shown in the following C++ example.</span></span>

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

<span data-ttu-id="61b92-176">Para implementar a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) , consulte [usando a interface ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md) e o tópico referência do [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="61b92-176">To implement the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, see [Using the ISearchQueryHelper Interface](-search-3x-wds-qryidx-searchqueryhelper.md) and the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) reference topic.</span></span>

> [!Note]  
> <span data-ttu-id="61b92-177">Compatibilidade do Microsoft Windows Desktop Search (WDS) 2x herdada: em computadores que executam o Windows XP e o Windows Server 2003 e posterior, o [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) foi preterido.</span><span class="sxs-lookup"><span data-stu-id="61b92-177">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and Windows Server 2003 and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="61b92-178">Em vez disso, os desenvolvedores devem usar [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para obter uma cadeia de conexão, analisar a consulta do usuário em SQL e, em seguida, consultar OLE DB.</span><span class="sxs-lookup"><span data-stu-id="61b92-178">Instead, developers should use [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string, parse the user's query into SQL, and then query through OLE DB.</span></span>

### <a name="using-the-search-ms-protocol"></a><span data-ttu-id="61b92-179">Usando o protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="61b92-179">Using the search-ms Protocol</span></span>

<span data-ttu-id="61b92-180">O [protocolo de aplicativo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) **pesquisa-MS** é uma Convenção para iniciar um aplicativo, como o Windows Explorer, para consultar o índice do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="61b92-180">The **search-ms** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for starting an application, like Windows Explorer, to query the Windows Search index.</span></span> <span data-ttu-id="61b92-181">Ele permite que as consultas sejam criadas com argumentos de valor de parâmetro, incluindo argumentos de propriedade, pesquisas salvas anteriormente, sintaxe de consulta avançada (AQS), sintaxe de consulta natural (NQS) e identificadores de código de idioma (LCIDs) para o indexador e a própria consulta.</span><span class="sxs-lookup"><span data-stu-id="61b92-181">It enables queries to be built with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="61b92-182">Para obter informações detalhadas sobre a sintaxe do protocolo Search-MS, consulte [consultando o índice com o protocolo Search-MS](-search-3x-wds-qryidx-searchms.md).</span><span class="sxs-lookup"><span data-stu-id="61b92-182">For detailed information on the search-ms protocol syntax, see [Querying the Index with the search-ms Protocol](-search-3x-wds-qryidx-searchms.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61b92-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61b92-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61b92-184">Consulta do índice de maneira programática</span><span class="sxs-lookup"><span data-stu-id="61b92-184">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="61b92-185">Consultando o índice com ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="61b92-185">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="61b92-186">Consultando o índice com o protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="61b92-186">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="61b92-187">Consultando o índice com a sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="61b92-187">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="61b92-188">Usando a sintaxe de consulta avançada programaticamente</span><span class="sxs-lookup"><span data-stu-id="61b92-188">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>
