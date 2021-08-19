---
description: Terceiros podem criar aplicativos que consultam o índice para dados programaticamente e podem estender Windows Search para indexar dados de formatos de arquivo personalizados e armazenamentos de dados.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Windows Guia do desenvolvedor de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84773f23f5e82ce5cbb15c163b0ff2421f9b7c92b18129c9875729be37518b02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864185"
---
# <a name="windows-search-developers-guide"></a>Windows Guia do desenvolvedor de pesquisa

Terceiros podem criar aplicativos que consultam o índice para dados programaticamente e podem estender Windows Search para indexar dados de formatos de arquivo personalizados e armazenamentos de dados. Para criar aplicativos Windows Search, os desenvolvedores de terceiros devem primeiro implementar um armazenamento de dados do Shell para alcançar uma experiência de usuário razoável. Para obter mais informações, [consulte Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Você também deve baixar o [SDK Windows para](https://msdn.microsoft.com/windowsvista/bb980924.aspx) as bibliotecas Windows Search. Os [exemplos Windows SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) de Pesquisa de Dados contêm exemplos de código úteis e um assembly de interopbilidade para desenvolvimento com código gerenciado. Para obter mais informações sobre como usar os exemplos de código, [consulte Windows exemplos de código de pesquisa.](-search-3x-wds-sampleentry.md)

Esta seção é organizada da seguinte forma:

- [Gerenciar o índice](-search-3x-wds-mngidx-overview.md)
- [Consulta do índice de maneira programática](-search-3x-wds-qryidx-overview.md)
- [Estendendo o índice](-search-3x-wds-extidx-overview.md)
- [Estendendo recursos de linguagem](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Recursos adicionais

- Para ver os boards de mensagens de discussão e perguntas com suporte da comunidade sobre tecnologias de pesquisa, consulte Fórum do [MSDN: Windows Desenvolvimento de Pesquisa de](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads)Área de Trabalho.
- Para baixar os Exemplos de Código de Pesquisa:
  - [Windows Exemplos de pesquisa](-search-samples-ovw.md)
- Para baixar o Windows SDK:
  - Para Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - Por Windows 7: [Windows SDK para Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Tópicos relacionados

[Visão geral do Windows Search](-search-3x-wds-overview.md)

[Windows Referência de pesquisa](-search-reference-entry-page.md)

[Windows Exemplos de código de pesquisa](-search-samples-ovw.md)

[Pesquisa federada no Windows](-search-federated-search-overview.md)

[Tecnologias de pesquisa relacionadas](-search-3x-wds-sampleentry.md)

[Windows Glossário de pesquisa](search-glossary.md)
