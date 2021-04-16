---
description: Você pode estender o Windows Search para indexar o conteúdo e as propriedades de novos formatos de arquivo e armazenamentos de dados usando interfaces de suplemento de dados.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Estender o índice (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765666"
---
# <a name="extending-the-index-windows-search"></a>Estender o índice (Windows Search)

Você pode estender o Windows Search para indexar o conteúdo e as propriedades de novos formatos de arquivo e armazenamentos de dados usando [interfaces de suplemento de dados](./-search-data-addins-interfaces-entry-page.md). Para criar suplementos de pesquisa do Windows, os desenvolvedores de terceiros devem primeiro implementar um armazenamento de dados do Shell e, em seguida, desenvolver um manipulador de protocolo para que o Windows Search possa acessar os dados para indexação. Se você tiver um formato de arquivo personalizado, deverá desenvolver um manipulador de filtro para indexar o conteúdo do arquivo e um manipulador de propriedades para cada tipo de arquivo para indexar Propriedades.

A pesquisa do Windows atualmente dá suporte à indexação de mais de 200 tipos de itens (como. txt,. html e formatos de arquivo. xml) e pode trabalhar com vários tipos de armazenamentos de dados (como o sistema de arquivos NTFS e o Microsoft Outlook). O Windows Search usa a tecnologia de filtro e manipulador de protocolo semelhante ao SharePoint Server. Portanto, se você já tiver implementações para o formato de arquivo, poderá atualizar as implementações a serem inicializadas com um fluxo usando [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) para que o filtro funcione com o Windows Search.

> [!Note]  
> Manipuladores de filtro, manipuladores de propriedade e manipuladores de protocolo devem ser escritos em código nativo. Isso ocorre devido a possíveis problemas de controle de versão de Common Language Runtime (CLR) com o processo em que vários suplementos são executados.

 

Esta seção sobre como estender o índice com suplementos contém os seguintes tópicos:

-   [Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)
-   [Desenvolvendo manipuladores de propriedade para o Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
-   [Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a>Recursos adicionais

Para obter exemplos de código relacionados, consulte [exemplos de código do Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de desenvolvimento do Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Gerenciar o índice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Consulta do índice de maneira programática](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Estendendo recursos de idioma](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
