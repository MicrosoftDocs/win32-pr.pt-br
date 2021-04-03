---
title: Chamando o WDS de forma programática
description: O Microsoft Windows Desktop Search (WDS) 2. x pode ser consultado programaticamente usando os métodos ExecuteQuery e ExecuteSQLQuery na interface ISearchDesktop.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc76264b7939311273fbda334292dfb255cde8f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641037"
---
# <a name="calling-wds-programmatically"></a><span data-ttu-id="d9553-103">Chamando o WDS de forma programática</span><span class="sxs-lookup"><span data-stu-id="d9553-103">Calling WDS Programmatically</span></span>

> [!NOTE]
> <span data-ttu-id="d9553-104">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d9553-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d9553-105">Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d9553-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="d9553-106">O Microsoft Windows Desktop Search (WDS) 2. x pode ser consultado programaticamente usando os métodos **executeQuery** e **ExecuteSQLQuery** na interface [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d9553-106">Microsoft Windows Desktop Search (WDS) 2.x can be queried programmatically using the **ExecuteQuery** and **ExecuteSQLQuery** methods in the [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) interface.</span></span> <span data-ttu-id="d9553-107">O método **executeQuery** retorna um conjunto de registros do índice com base no texto da consulta, nas colunas e nas restrições passadas como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d9553-107">The **ExecuteQuery** method returns a record set from the index based on the query text, columns, and restrictions passed as parameters.</span></span> <span data-ttu-id="d9553-108">O método **ExecuteSQLQuery** também retorna um conjunto de registros de resultados, mas exige que o comando exato de linguagem SQL (SQL) seja passado.</span><span class="sxs-lookup"><span data-stu-id="d9553-108">The **ExecuteSQLQuery** method also returns a record set of results but requires the exact Structured Query Language (SQL) command to be passed in.</span></span> <span data-ttu-id="d9553-109">**ExecuteQuery** deve ser usado na maioria dos cenários.</span><span class="sxs-lookup"><span data-stu-id="d9553-109">**ExecuteQuery** should be used in most scenarios.</span></span>

## <a name="regular-queries"></a><span data-ttu-id="d9553-110">Consultas regulares</span><span class="sxs-lookup"><span data-stu-id="d9553-110">Regular Queries</span></span>

<span data-ttu-id="d9553-111">As consultas regulares são aquelas digitadas na caixa de entrada do WDS pelo usuário, incluindo toda a [sintaxe de consulta avançada](-search-2x-wds-aqsreference.md).</span><span class="sxs-lookup"><span data-stu-id="d9553-111">Regular queries are those typed into the WDS input box by the user including all [Advanced Query Syntax](-search-2x-wds-aqsreference.md).</span></span> <span data-ttu-id="d9553-112">A consulta é passada para **executeQuery** junto com as colunas de [esquema](-search-2x-wds-schematable.md) do WDS 2. x a serem retornadas, a coluna e a ordem para classificar os resultados e quaisquer cláusulas para restringir os resultados.</span><span class="sxs-lookup"><span data-stu-id="d9553-112">The query is passed to **ExecuteQuery** along with the WDS 2.x [schema](-search-2x-wds-schematable.md) columns to return, the column and order to sort results, and any clauses to restrict results by.</span></span>

<span data-ttu-id="d9553-113">O método tem o formato:</span><span class="sxs-lookup"><span data-stu-id="d9553-113">The method has the form:</span></span>

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| <span data-ttu-id="d9553-114">Direção</span><span class="sxs-lookup"><span data-stu-id="d9553-114">Direction</span></span> | <span data-ttu-id="d9553-115">Variável</span><span class="sxs-lookup"><span data-stu-id="d9553-115">Variable</span></span>           | <span data-ttu-id="d9553-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9553-116">Description</span></span>                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9553-117">Em</span><span class="sxs-lookup"><span data-stu-id="d9553-117">In</span></span>        | <span data-ttu-id="d9553-118">lpcwstrQuery</span><span class="sxs-lookup"><span data-stu-id="d9553-118">lpcwstrQuery</span></span>       | <span data-ttu-id="d9553-119">O texto da consulta.</span><span class="sxs-lookup"><span data-stu-id="d9553-119">The query text.</span></span> <span data-ttu-id="d9553-120">Essa consulta é a mesma que uma consulta digitada na caixa de texto de pesquisa na interface do usuário do Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="d9553-120">This query is the same as a query typed into the search text box in the Windows Desktop Search user interface.</span></span> <br/> <span data-ttu-id="d9553-121">Por exemplo: `"from:Zara dinner plans"`</span><span class="sxs-lookup"><span data-stu-id="d9553-121">For example: `"from:Zara dinner plans"`</span></span><br/> |
| <span data-ttu-id="d9553-122">Em</span><span class="sxs-lookup"><span data-stu-id="d9553-122">In</span></span>        | <span data-ttu-id="d9553-123">lpcwstrColumn</span><span class="sxs-lookup"><span data-stu-id="d9553-123">lpcwstrColumn</span></span>      | <span data-ttu-id="d9553-124">As colunas a serem incluídas, separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="d9553-124">The columns to include, separated by commas.</span></span> <br/> <span data-ttu-id="d9553-125">Por exemplo: `"DocTitle, Url"`</span><span class="sxs-lookup"><span data-stu-id="d9553-125">For example: `"DocTitle, Url"`</span></span><br/>                                                                                            |
| <span data-ttu-id="d9553-126">Em</span><span class="sxs-lookup"><span data-stu-id="d9553-126">In</span></span>        | <span data-ttu-id="d9553-127">lpcwstrSort</span><span class="sxs-lookup"><span data-stu-id="d9553-127">lpcwstrSort</span></span>        | <span data-ttu-id="d9553-128">A coluna de substituição a ser classificada seguido por ASC para crescente ou DESC para decrescente.</span><span class="sxs-lookup"><span data-stu-id="d9553-128">The Override Column to sort by followed by ASC for ascending or DESC for descending.</span></span> <br/> <span data-ttu-id="d9553-129">Por exemplo: `"LastAuthor DESC"`</span><span class="sxs-lookup"><span data-stu-id="d9553-129">For example: `"LastAuthor DESC"`</span></span><br/>                                                  |
| <span data-ttu-id="d9553-130">Em</span><span class="sxs-lookup"><span data-stu-id="d9553-130">In</span></span>        | <span data-ttu-id="d9553-131">lpcwstrRestriction</span><span class="sxs-lookup"><span data-stu-id="d9553-131">lpcwstrRestriction</span></span> | <span data-ttu-id="d9553-132">Restrições para acrescentar cláusulas WHERE no Windows Desktop Search SELECT.</span><span class="sxs-lookup"><span data-stu-id="d9553-132">Restrictions to append through WHERE clauses in the Windows Desktop Search select.</span></span> <br/> <span data-ttu-id="d9553-133">Por exemplo: `"Contains(LastAuthor, 'Bill')"`</span><span class="sxs-lookup"><span data-stu-id="d9553-133">For example: `"Contains(LastAuthor, 'Bill')"`</span></span><br/>                                       |
| <span data-ttu-id="d9553-134">Saída</span><span class="sxs-lookup"><span data-stu-id="d9553-134">Out</span></span>       | <span data-ttu-id="d9553-135">ppiRs</span><span class="sxs-lookup"><span data-stu-id="d9553-135">ppiRs</span></span>              | <span data-ttu-id="d9553-136">O conjunto de registros resultante</span><span class="sxs-lookup"><span data-stu-id="d9553-136">The resulting record set</span></span><br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a><span data-ttu-id="d9553-137">Consultas SQL</span><span class="sxs-lookup"><span data-stu-id="d9553-137">SQL Queries</span></span>

<span data-ttu-id="d9553-138">O método **ISearchDesktop.ExecuteSQLQuery** é usado para enviar consultas diretas do banco de dados WDS.</span><span class="sxs-lookup"><span data-stu-id="d9553-138">The **ISearchDesktop.ExecuteSQLQuery** method is used to send direct WDS database queries.</span></span> <span data-ttu-id="d9553-139">A sintaxe para as consultas é semelhante àquela usada para o SharePoint Server, juntamente com a capacidade de usar as cláusulas GROUP BY do SQL do estilo Monarch.</span><span class="sxs-lookup"><span data-stu-id="d9553-139">The syntax for the queries is similar to that used for SharePoint Server, along with the ability to use Monarch-style SQL GROUP BY clauses.</span></span> <span data-ttu-id="d9553-140">A consulta é executada no índice exatamente como ele é passado sem nenhum processamento adicional da sintaxe de consulta avançada que a API ExecuteQuery faz.</span><span class="sxs-lookup"><span data-stu-id="d9553-140">The query is executed against the index exactly as it is passed in with no additional processing of Advanced Query Syntax as the ExecuteQuery API does.</span></span>

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

<span data-ttu-id="d9553-141">O método tem o formato:</span><span class="sxs-lookup"><span data-stu-id="d9553-141">The method has the form:</span></span>

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| <span data-ttu-id="d9553-142">Direção</span><span class="sxs-lookup"><span data-stu-id="d9553-142">Direction</span></span> | <span data-ttu-id="d9553-143">Variável</span><span class="sxs-lookup"><span data-stu-id="d9553-143">Variable</span></span>   | <span data-ttu-id="d9553-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9553-144">Description</span></span>                                    |
|-----------|------------|------------------------------------------------|
| <span data-ttu-id="d9553-145">Em</span><span class="sxs-lookup"><span data-stu-id="d9553-145">In</span></span>        | <span data-ttu-id="d9553-146">lpcwstrSQL</span><span class="sxs-lookup"><span data-stu-id="d9553-146">lpcwstrSQL</span></span> | <span data-ttu-id="d9553-147">A consulta SQL a ser executada no índice do WDS</span><span class="sxs-lookup"><span data-stu-id="d9553-147">The SQL query to execute against the WDS index</span></span> |
| <span data-ttu-id="d9553-148">Saída</span><span class="sxs-lookup"><span data-stu-id="d9553-148">Out</span></span>       | <span data-ttu-id="d9553-149">ppiRs</span><span class="sxs-lookup"><span data-stu-id="d9553-149">ppiRs</span></span>      | <span data-ttu-id="d9553-150">O conjunto de registros resultante</span><span class="sxs-lookup"><span data-stu-id="d9553-150">The resulting record set</span></span>                       |



 

<span data-ttu-id="d9553-151">Recursos:</span><span class="sxs-lookup"><span data-stu-id="d9553-151">Resources:</span></span>

-   <span data-ttu-id="d9553-152">Arquivos de suporte para a interface ISearchDesktop: https://addins.msn.com/support/WDSSDK.zip</span><span class="sxs-lookup"><span data-stu-id="d9553-152">Support files for the ISearchDesktop interface: https://addins.msn.com/support/WDSSDK.zip</span></span>
-   <span data-ttu-id="d9553-153">Exemplo de C# ISearchDesktop: https://addins.msn.com/support/WDSSample.zip</span><span class="sxs-lookup"><span data-stu-id="d9553-153">ISearchDesktop C# Sample: https://addins.msn.com/support/WDSSample.zip</span></span>

## <a name="sample-c-code"></a><span data-ttu-id="d9553-154">Código C++ de exemplo</span><span class="sxs-lookup"><span data-stu-id="d9553-154">Sample C++ Code</span></span>

> [!Note]
>
> <span data-ttu-id="d9553-155">ESSE CÓDIGO E AS INFORMAÇÕES SÃO FORNECIDOS "NO ESTADO EM QUE SE ENCONTRAM", SEM GARANTIAS DE QUALQUER TIPO, EXPRESSAS OU IMPLÍCITAS, INCLUINDO, MAS NÃO SE LIMITANDO ÀS GARANTIAS IMPLÍCITAS DE COMERCIALIZAÇÃO E/OU ADEQUAÇÃO A UMA FINALIDADE ESPECÍFICA.</span><span class="sxs-lookup"><span data-stu-id="d9553-155">THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.</span></span>
>
> <span data-ttu-id="d9553-156">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9553-156">Copyright (C) Microsoft.</span></span> <span data-ttu-id="d9553-157">Todos os direitos reservados.</span><span class="sxs-lookup"><span data-stu-id="d9553-157">All rights reserved.</span></span>

 


```
#include <stdio.h>
#include <wchar.h>
#include <windows.h>
#include <msnldl.h>
#include <adoint.h>
#include <adoguids.h>
 
HRESULT TestExecuteQuery(ISearchDesktop *psd)
{
ADORecordset *prs = NULL;
 
    HRESULT hr;
 
    hr = psd->ExecuteQuery( L"ToName:Moishe", 
                            L"DocTitle,DocFormat", 
                            L"PrimaryDate DESC", 
                            L"Contains('text')", 
                            &prs);
    if (SUCCEEDED(hr))
        prs->Release();
    return hr;
}
 
HRESULT TestExecuteSQLQuery(ISearchDesktop *psd)
{
    ADORecordset *prs = NULL;
    HRESULT hr;

    hr = psd->ExecuteSQLQuery(L"select DocTitle from MyIndex..Scope() where contains('text')", &prs);

    if (SUCCEEDED(hr))
      prs->Release();
    return hr;
}
 
extern "C" int __cdecl wmain( int argc, WCHAR * argv[] )
{
    SCODE sc = CoInitialize(0);
    ISearchDesktop *psd = NULL;
    HRESULT         hr;
     
    if (SUCCEEDED(hr = CoCreateInstance(__uuidof(SearchDesktop), NULL, CLSCTX_INPROC_SERVER, 
                                        __uuidof(ISearchDesktop), (void**)&psd)))
          {
             TestExecuteSQLQuery(psd);
             TestExecuteQuery(psd);
             psd->Release();
          }
          CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="d9553-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9553-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d9553-159">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d9553-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d9553-160">Sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="d9553-160">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="d9553-161">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="d9553-161">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="d9553-162">Chamando o WDS de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="d9553-162">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

