---
description: Esta seção fornece informações conceituais necessárias para a implementação, a extensão e o teste de manipuladores de protocolo.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: desenvolvendo manipuladores de protocolo para pesquisa de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ef01d36e565471756ee9d6680833401054a6e29b9c570dad7852d316797067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597826"
---
# <a name="developing-protocol-handlers-for-windows-search"></a>desenvolvendo manipuladores de protocolo para pesquisa de Windows

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
-   para estender Windows pesquisa para indexar o conteúdo e as propriedades dos novos formatos de arquivo e armazenamentos de dados, consulte [estendendo o índice](-search-3x-wds-extidx-overview.md).
-   Para obter visões gerais do Gerenciador de catálogo e do CSM (Gerenciador de pesquisa de catálogo), consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).

Para obter um plano de fundo conceitual sobre os tipos de arquivo e manipuladores, consulte os seguintes tópicos:

-   Para estender o shell com manipuladores de tipo de arquivo, consulte [criando manipuladores de extensão de shell](../shell/handlers.md).
-   Para obter informações conceituais sobre manipuladores de filtro, consulte [desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md).
-   Para obter informações sobre como criar manipuladores, consulte [introdução a associações de arquivos](../shell/fa-intro.md), [registro de extensões de shell](../shell/reg-shell-exts.md), criação de [manipuladores de extensão de shell](../shell/handlers.md), menu de [contexto](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))e [gerenciadores de visualização](../shell/preview-handlers.md).

Para obter informações sobre tecnologias relacionadas e sobre como implementar um armazenamento de dados, consulte os seguintes tópicos:

-   Windows os manipuladores de protocolo de pesquisa usam especificações de design semelhantes ao SharePoint Server e, em geral, podem ser usados de maneira intercambiável. para obter mais informações, consulte [SharePoint Server developer Center](https://developer.microsoft.com/office/docs).
-   no Windows 7 e posterior, o SharePoint search Server 2008 e o MOSS 2007 SP2 também oferecem suporte à pesquisa federada. para obter mais informações sobre a pesquisa federada e a implantação do servidor de pesquisa 2008 com Office SharePoint server 2007, consulte [servidor de pesquisa de pesquisa federada \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)).
-   Para criar um armazenamento de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Para obter exemplos de código, consulte as seguintes páginas do portal:

-   para obter exemplos de código de pesquisa, consulte [exemplos de SDK de pesquisa Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).
-   Para obter exemplos de código de Shell, consulte [shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).

 

 
