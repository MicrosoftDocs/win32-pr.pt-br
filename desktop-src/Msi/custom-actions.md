---
description: o Windows Installer fornece muitas ações internas para executar o processo de instalação. Para obter uma lista dessas ações, consulte a referência de ações padrão.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3e2eb466934d7d332307e0d5288d6d328297d7664d884e62c406eb3409728a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947897"
---
# <a name="custom-actions"></a>Ações personalizadas

o Windows Installer fornece muitas ações internas para executar o processo de instalação. Para obter uma lista dessas ações, consulte a [referência de ações padrão](standard-actions-reference.md).

As ações padrão são suficientes para executar uma instalação na maioria dos casos. No entanto, há situações em que o desenvolvedor de um pacote de instalação descobre que é necessário gravar uma ação personalizada. Por exemplo:

-   Você deseja iniciar um executável durante a instalação que está instalado no computador do usuário ou que está sendo instalado com o aplicativo.
-   Você deseja chamar funções especiais durante uma instalação que são definidas em uma DLL (biblioteca de vínculo dinâmico).
-   você deseja usar funções escritas nas linguagens de desenvolvimento microsoft Visual Basic scripting Edition ou texto do script literal do microsoft JScript durante uma instalação.
-   Você deseja adiar a execução de algumas ações até a hora em que o script de instalação está sendo executado.
-   Você deseja adicionar informações de hora e progresso a um controle ProgressBar e a um controle de texto de tempo restante.

As seções a seguir descrevem as ações personalizadas e como incorporá-las a um pacote de instalação:

-   [Sobre ações personalizadas](about-custom-actions.md)
-   [Usando ações personalizadas](using-custom-actions.md)
-   [Referência de ação personalizada](custom-action-reference.md)
-   [Lista de Resumo de todos os tipos de ação personalizada](summary-list-of-all-custom-action-types.md)

 

 



