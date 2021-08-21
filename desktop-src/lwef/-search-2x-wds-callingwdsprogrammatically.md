---
title: Chamando o WDS programaticamente
description: O Microsoft Windows Desktop Search (WDS) 2.x pode ser consultado programaticamente usando os métodos ExecuteQuery e ExecuteSQLQuery na interface ISearchDesktop.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8879001bcf284affd03ff472ac9327445b799acd44465b5bae9a8cb2d819b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976896"
---
# <a name="calling-wds-programmatically"></a>Chamando o WDS programaticamente

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use [Windows Search.](../search/-search-3x-wds-overview.md)

O Microsoft Windows Desktop Search (WDS) 2.x pode ser consultado programaticamente usando os métodos **ExecuteQuery** e **ExecuteSQLQuery** na interface [**ISearchDesktop.**](/previous-versions//aa965729(v=vs.85)) O **método ExecuteQuery** retorna um conjunto de registros do índice com base no texto de consulta, nas colunas e nas restrições passadas como parâmetros. O **método ExecuteSQLQuery** também retorna um conjunto de registros de resultados, mas requer que o comando linguagem SQL (SQL) exato seja passado. **ExecuteQuery** deve ser usado na maioria dos cenários.

## <a name="regular-queries"></a>Consultas regulares

Consultas regulares são aquelas digitadas na caixa de entrada do WDS pelo usuário, incluindo toda a [Sintaxe de Consulta Avançada](-search-2x-wds-aqsreference.md). A consulta é passada para **ExecuteQuery juntamente** com [](-search-2x-wds-schematable.md) as colunas de esquema do WDS 2.x para retornar, a coluna e a ordem para classificar os resultados e quaisquer cláusulas pelas que restringir os resultados.

O método tem o formato:

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| Direção | Variável           | Descrição                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Em        | lpcwstrQuery       | O texto da consulta. Essa consulta é a mesma que uma consulta digitada na caixa de texto de pesquisa na interface do usuário Windows Desktop Search. <br/> Por exemplo: `"from:Zara dinner plans"`<br/> |
| Em        | lpcwstrColumn      | As colunas a incluir, separadas por vírgulas. <br/> Por exemplo: `"DocTitle, Url"`<br/>                                                                                            |
| Em        | lpcwstrSort        | A Coluna de Substituição a ser classificação seguida por ASC para crescente ou DESC para ordem decrescente. <br/> Por exemplo: `"LastAuthor DESC"`<br/>                                                  |
| Em        | lpcwstrRestriction | Restrições para anexar por meio de cláusulas WHERE na Windows Desktop Search selecione. <br/> Por exemplo: `"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| Saída       | ppiRs              | O conjunto de registros resultante<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>Consultas SQL

O **ISearchDesktop.Exemétodo cuteSQLQuery** é usado para enviar consultas diretas de banco de dados WDS. A sintaxe das consultas é semelhante à usada para o SharePoint Server, juntamente com a capacidade de usar cláusulas GROUP BY no estilo SQL. A consulta é executada no índice exatamente como é passada sem processamento adicional da Sintaxe de Consulta Avançada, como a API ExecuteQuery faz.

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

O método tem o formato:

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| Direção | Variável   | Descrição                                    |
|-----------|------------|------------------------------------------------|
| Em        | lpcwstrSQL | A SQL consulta a ser executada no índice WDS |
| Saída       | ppiRs      | O conjunto de registros resultante                       |



 

Recursos:

-   Arquivos de suporte para a interface ISearchDesktop: https://addins.msn.com/support/WDSSDK.zip
-   Exemplo de C# ISearchDesktop: https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>Código C++ de exemplo

> [!Note]
>
> ESSE CÓDIGO E INFORMAÇÕES SÃO FORNECIDOS "NO ESTADO EM QUE SE ESTÃO" SEM GARANTIA DE QUALQUER TIPO, EXPRESSAS OU IMPLÍCITAS, INCLUINDO, MAS NÃO SE LIMITANDO ÀS GARANTIAS IMPLÍCITAS DE COMERCIALIZAÇÃO E/OU ADEQUAÇÃO A UMA FINALIDADE ESPECÍFICA.
>
> Copyright (C) Microsoft. All rights reserved.

 


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Sintaxe de consulta avançada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipos percebidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Chamando o WDS de páginas da Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

