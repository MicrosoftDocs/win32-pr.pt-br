---
description: O Windows Installer fornece muitas ações internas para executar o processo de instalação. Para obter uma lista dessas ações, consulte a referência de ações padrão.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011156"
---
# <a name="custom-actions"></a>Ações personalizadas

O Windows Installer fornece muitas ações internas para executar o processo de instalação. Para obter uma lista dessas ações, consulte a [referência de ações padrão](standard-actions-reference.md).

As ações padrão são suficientes para executar uma instalação na maioria dos casos. No entanto, há situações em que o desenvolvedor de um pacote de instalação descobre que é necessário gravar uma ação personalizada. Por exemplo:

-   Você deseja iniciar um executável durante a instalação que está instalado no computador do usuário ou que está sendo instalado com o aplicativo.
-   Você deseja chamar funções especiais durante uma instalação que são definidas em uma DLL (biblioteca de vínculo dinâmico).
-   Você deseja usar funções escritas no texto linguagens de desenvolvimento Microsoft Visual Basic Scripting Edition ou script literal do Microsoft JScript, durante uma instalação.
-   Você deseja adiar a execução de algumas ações até a hora em que o script de instalação está sendo executado.
-   Você deseja adicionar informações de hora e progresso a um controle ProgressBar e a um controle de texto de tempo restante.

As seções a seguir descrevem as ações personalizadas e como incorporá-las a um pacote de instalação:

-   [Sobre ações personalizadas](about-custom-actions.md)
-   [Usando ações personalizadas](using-custom-actions.md)
-   [Referência de ação personalizada](custom-action-reference.md)
-   [Lista de Resumo de todos os tipos de ação personalizada](summary-list-of-all-custom-action-types.md)

 

 



