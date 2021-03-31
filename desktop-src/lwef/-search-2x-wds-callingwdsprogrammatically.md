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
# <a name="calling-wds-programmatically"></a>Chamando o WDS de forma programática

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

O Microsoft Windows Desktop Search (WDS) 2. x pode ser consultado programaticamente usando os métodos **executeQuery** e **ExecuteSQLQuery** na interface [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) . O método **executeQuery** retorna um conjunto de registros do índice com base no texto da consulta, nas colunas e nas restrições passadas como parâmetros. O método **ExecuteSQLQuery** também retorna um conjunto de registros de resultados, mas exige que o comando exato de linguagem SQL (SQL) seja passado. **ExecuteQuery** deve ser usado na maioria dos cenários.

## <a name="regular-queries"></a>Consultas regulares

As consultas regulares são aquelas digitadas na caixa de entrada do WDS pelo usuário, incluindo toda a [sintaxe de consulta avançada](-search-2x-wds-aqsreference.md). A consulta é passada para **executeQuery** junto com as colunas de [esquema](-search-2x-wds-schematable.md) do WDS 2. x a serem retornadas, a coluna e a ordem para classificar os resultados e quaisquer cláusulas para restringir os resultados.

O método tem o formato:

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| Direção | Variável           | Descrição                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Em        | lpcwstrQuery       | O texto da consulta. Essa consulta é a mesma que uma consulta digitada na caixa de texto de pesquisa na interface do usuário do Windows Desktop Search. <br/> Por exemplo: `"from:Zara dinner plans"`<br/> |
| Em        | lpcwstrColumn      | As colunas a serem incluídas, separadas por vírgulas. <br/> Por exemplo: `"DocTitle, Url"`<br/>                                                                                            |
| Em        | lpcwstrSort        | A coluna de substituição a ser classificada seguido por ASC para crescente ou DESC para decrescente. <br/> Por exemplo: `"LastAuthor DESC"`<br/>                                                  |
| Em        | lpcwstrRestriction | Restrições para acrescentar cláusulas WHERE no Windows Desktop Search SELECT. <br/> Por exemplo: `"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| Saída       | ppiRs              | O conjunto de registros resultante<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>Consultas SQL

O método **ISearchDesktop.ExecuteSQLQuery** é usado para enviar consultas diretas do banco de dados WDS. A sintaxe para as consultas é semelhante àquela usada para o SharePoint Server, juntamente com a capacidade de usar as cláusulas GROUP BY do SQL do estilo Monarch. A consulta é executada no índice exatamente como ele é passado sem nenhum processamento adicional da sintaxe de consulta avançada que a API ExecuteQuery faz.

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

O método tem o formato:

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| Direção | Variável   | Descrição                                    |
|-----------|------------|------------------------------------------------|
| Em        | lpcwstrSQL | A consulta SQL a ser executada no índice do WDS |
| Saída       | ppiRs      | O conjunto de registros resultante                       |



 

Recursos:

-   Arquivos de suporte para a interface ISearchDesktop: https://addins.msn.com/support/WDSSDK.zip
-   Exemplo de C# ISearchDesktop: https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>Código C++ de exemplo

> [!Note]
>
> ESSE CÓDIGO E AS INFORMAÇÕES SÃO FORNECIDOS "NO ESTADO EM QUE SE ENCONTRAM", SEM GARANTIAS DE QUALQUER TIPO, EXPRESSAS OU IMPLÍCITAS, INCLUINDO, MAS NÃO SE LIMITANDO ÀS GARANTIAS IMPLÍCITAS DE COMERCIALIZAÇÃO E/OU ADEQUAÇÃO A UMA FINALIDADE ESPECÍFICA.
>
> Copyright (C) Microsoft. Todos os direitos reservados.

 


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

[Tipos observados](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Chamando o WDS de páginas da Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

