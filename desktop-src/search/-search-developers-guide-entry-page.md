---
description: Terceiros podem criar aplicativos que consultam o índice em busca de dados programaticamente e podem estender o Windows Search para indexar dados de formatos de arquivo personalizados e armazenamentos de dados.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Guia do desenvolvedor do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460990"
---
# <a name="windows-search-developers-guide"></a>Guia do desenvolvedor do Windows Search

Terceiros podem criar aplicativos que consultam o índice em busca de dados programaticamente e podem estender o Windows Search para indexar dados de formatos de arquivo personalizados e armazenamentos de dados. Para criar aplicativos de pesquisa do Windows, os desenvolvedores de terceiros devem primeiro implementar um armazenamento de dados do Shell para obter uma experiência de usuário razoável. Para obter mais informações, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Você também deve baixar o [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para as bibliotecas de pesquisa do Windows. Os [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contêm exemplos de código úteis e um assembly de interoperabilidade para o desenvolvimento com código gerenciado. Para obter mais informações sobre como usar os exemplos de código, consulte [exemplos de código do Windows Search](-search-3x-wds-sampleentry.md).

Esta seção é organizada da seguinte maneira:

- [Gerenciar o índice](-search-3x-wds-mngidx-overview.md)
- [Consulta do índice de maneira programática](-search-3x-wds-qryidx-overview.md)
- [Estendendo o índice](-search-3x-wds-extidx-overview.md)
- [Estendendo recursos de idioma](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Recursos adicionais

- Para ver os quadros de mensagens de perguntas e discussões com suporte da Comunidade em tecnologias de pesquisa, consulte [Fórum do MSDN: desenvolvimento do Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
- Para baixar os exemplos de código de pesquisa:
  - [Exemplos do Windows Search](-search-samples-ovw.md)
- Para baixar o SDK do Windows:
  - Para Windows 10: [SDK do Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - Para o Windows 7: [SDK do Windows para Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Tópicos relacionados

[Visão geral do Windows Search](-search-3x-wds-overview.md)

[Referência do Windows Search](-search-reference-entry-page.md)

[Exemplos de código do Windows Search](-search-samples-ovw.md)

[Pesquisa federada no Windows](-search-federated-search-overview.md)

[Tecnologias de pesquisa relacionadas](-search-3x-wds-sampleentry.md)

[Glossário do Windows Search](search-glossary.md)
