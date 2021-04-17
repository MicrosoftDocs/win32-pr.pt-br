---
description: Há várias maneiras de usar o Windows Search para consultar o índice.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Consulta do índice de maneira programática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755238"
---
# <a name="querying-the-index-programmatically"></a>Consulta do índice de maneira programática

Há várias maneiras de usar o Windows Search para consultar o índice.

Esta seção fornece a estrutura conceitual para consultar o índice programaticamente:

-   [Usando abordagens SQL e AQS para consultar o índice](using-sql-and-aqs-to-query-the-index.md)
-   [Consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [Consultando o índice com o protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)
-   [Consultando o índice com a sintaxe SQL do Windows Search](-search-sql-windowssearch-entry.md)
-   [Usando a sintaxe de consulta avançada programaticamente](-search-3x-advancedquerysyntax.md)

> [!Note]  
> Compatibilidade do Microsoft Windows Desktop Search (WDS) 2x herdada: em computadores que executam o Windows XP e posterior, o [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) foi preterido. Em vez disso, os desenvolvedores devem usar [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) para obter uma cadeia de conexão e analisar a consulta do usuário em linguagem SQL (SQL) e consultar o banco de dados de incorporação e vinculação de objetos (OLE DB).

 

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter informações sobre OLE DB, consulte [visão geral da programação de OLE DB](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx). Para obter informações sobre o Provedor de Dados de .NET Framework para OLE DB, consulte o [namespace System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).
-   Para obter mais informações sobre como usar as propriedades na consulta, consulte os seguintes tópicos:
    -   [Sistema de propriedades](../properties/building-property-handlers.md)
    -   [Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   Para obter informações sobre como criar e modificar pastas de pesquisa, consulte [**interface ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).
-   Para ver os quadros de mensagens de perguntas e discussões com suporte da Comunidade em tecnologias de pesquisa, consulte [Fórum do MSDN: desenvolvimento do Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Para baixar os exemplos de código do SDK de pesquisa:
    -   Para o Windows 7: [exemplos do Windows Search no GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   Para o Windows Vista: [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   Para baixar o SDK do Windows:
    -   Para o Windows 7: [SDK do Windows para Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   Para o Windows Vista: [SDK do Windows para Windows Vista e .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de desenvolvimento do Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Gerenciar o índice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Estendendo o índice do Windows Search](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[Estendendo recursos de idioma](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
