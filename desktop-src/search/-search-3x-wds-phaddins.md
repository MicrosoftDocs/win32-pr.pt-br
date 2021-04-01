---
description: Esta seção fornece informações conceituais necessárias para a implementação, a extensão e o teste de manipuladores de protocolo.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Desenvolvendo manipuladores de protocolo para o Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646881"
---
# <a name="developing-protocol-handlers-for-windows-search"></a>Desenvolvendo manipuladores de protocolo para o Windows Search

Esta seção fornece informações conceituais necessárias para a implementação, a extensão e o teste de manipuladores de protocolo.

-   [Noções básicas sobre manipuladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
-   [Notificando o índice das alterações](-search-3x-wds-notifyingofchanges.md)
-   [Adicionando ícones e menus de contexto](-search-3x-wds-ph-ui-extensions.md)
-   [Exemplo de código: extensões de Shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
-   [Instalando e Registrando manipuladores de protocolo](-search-3x-wds-ph-install-registration.md)
-   [Criando um conector de pesquisa para um manipulador de protocolo](-search-3x-wds-ph-search-connector.md)
-   [Depuração de manipuladores de protocolo](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a>Recursos adicionais

Para obter informações conceituais sobre indexação, consulte os seguintes tópicos:

-   Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
-   Para estender o Windows Search para indexar o conteúdo e as propriedades de novos formatos de arquivo e armazenamentos de dados, consulte [estendendo o índice](-search-3x-wds-extidx-overview.md).
-   Para obter visões gerais do Gerenciador de catálogo e do CSM (Gerenciador de pesquisa de catálogo), consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).

Para obter um plano de fundo conceitual sobre os tipos de arquivo e manipuladores, consulte os seguintes tópicos:

-   Para estender o shell com manipuladores de tipo de arquivo, consulte [criando manipuladores de extensão de shell](../shell/handlers.md).
-   Para obter informações conceituais sobre manipuladores de filtro, consulte [desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md).
-   Para obter informações sobre como criar manipuladores, consulte [introdução a associações de arquivos](../shell/fa-intro.md), [registro de extensões de shell](../shell/reg-shell-exts.md), criação de [manipuladores de extensão de shell](../shell/handlers.md), menu de [contexto](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))e [gerenciadores de visualização](../shell/preview-handlers.md).

Para obter informações sobre tecnologias relacionadas e sobre como implementar um armazenamento de dados, consulte os seguintes tópicos:

-   Os manipuladores de protocolo de pesquisa do Windows usam especificações de design semelhantes ao SharePoint Server e, em geral, podem ser usados de maneira intercambiável. Para obter mais informações, consulte [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).
-   No Windows 7 e posterior, o SharePoint Search Server 2008 e o MOSS 2007 SP2 também oferecem suporte à pesquisa federada. Para obter mais informações sobre a pesquisa federada e a implantação do servidor de pesquisa 2008 com o Office SharePoint Server 2007, consulte [servidor de pesquisa de pesquisa federada \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)).
-   Para criar um armazenamento de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Para obter exemplos de código, consulte as seguintes páginas do portal:

-   Para obter exemplos de código de pesquisa, consulte [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).
-   Para obter exemplos de código de Shell, consulte [shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).

 

 
