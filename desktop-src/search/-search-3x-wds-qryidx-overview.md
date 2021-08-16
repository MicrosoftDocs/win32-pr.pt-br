---
description: há várias maneiras de usar Windows pesquisa para consultar o índice.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Consulta do índice de maneira programática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76f98d12e4a0615bf19dfb165766a67b8c9e58700ad2d0c897782e2a16ba9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094937"
---
# <a name="querying-the-index-programmatically"></a>Consulta do índice de maneira programática

há várias maneiras de usar Windows pesquisa para consultar o índice.

Esta seção fornece a estrutura conceitual para consultar o índice programaticamente:

-   [usando as abordagens SQL e AQS para consultar o índice](using-sql-and-aqs-to-query-the-index.md)
-   [Consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [Consultando o índice com o protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)
-   [consultando o índice com Windows sintaxe de SQL de pesquisa](-search-sql-windowssearch-entry.md)
-   [Usando a sintaxe de consulta avançada programaticamente](-search-3x-advancedquerysyntax.md)

> [!Note]  
> compatibilidade do Microsoft Windows Desktop Search (WDS) 2x herdada: em computadores que executam o Windows XP e posterior, o [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) é preterido. em vez disso, os desenvolvedores devem usar [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) para obter uma cadeia de conexão e analisar a consulta do usuário em linguagem SQL (SQL) e consultar o banco de dados de incorporação e vinculação de objetos (OLE DB).

 

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter informações sobre OLE DB, consulte [visão geral da programação de OLE DB](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx). para obter informações sobre o Provedor de Dados de .NET Framework para OLE DB, consulte o [Namespace System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).
-   Para obter mais informações sobre como usar as propriedades na consulta, consulte os seguintes tópicos:
    -   [Sistema de propriedades](../properties/building-property-handlers.md)
    -   [Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   Para obter informações sobre como criar e modificar pastas de pesquisa, consulte [**interface ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).
-   para ver os quadros de mensagens de perguntas e discussões com suporte da comunidade em tecnologias de pesquisa, consulte [fórum do MSDN: desenvolvimento Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Para baixar os exemplos de código do SDK de pesquisa:
    -   para Windows 7: [exemplos de pesquisa Windows no GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   para o Windows Vista: [exemplos de SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   para baixar o SDK do Windows:
    -   para Windows 7: [SDK do Windows para Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   para o Windows vista: [SDK do Windows para Windows vista e .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Pesquisar guia de desenvolvimento](-search-developers-guide-entry-page.md)
</dt> <dt>

[Gerenciar o índice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[estendendo o índice de pesquisa de Windows](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[Estendendo recursos de idioma](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
