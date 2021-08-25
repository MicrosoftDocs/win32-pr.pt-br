---
description: Visão geral de como usar Automação da Interface do Usuário e outras ferramentas para testar seus aplicativos.
title: Teste de acessibilidade
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0cc1d118c84e2689b6cf329da29bb518a566fb8588c311229be17fcd28825ddc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896576"
---
# <a name="testing-for-accessibility"></a>Teste de acessibilidade

O acesso programático e o acesso ao teclado são requisitos críticos para dar suporte à acessibilidade em seu aplicativo. Testar a acessibilidade de seus aplicativos do Windows, ferramentas de AT (tecnologia adaptativa) e estruturas de interface do usuário é crucial para garantir uma experiência do usuário bem-sucedida para pessoas com várias deficiências e limitações (incluindo visão, aprendizado, mobilidade/mobilidade e deficiências de linguagem/comunicação) ou aquelas que simplesmente preferem usar um teclado.

Sem acesso adequado por meio de AT, como leitores de tela e teclados na tela, os usuários com visão, aprendizado, deficiência/mobilidade e deficiências ou limitações de linguagem/comunicação (e usuários que simplesmente preferem usar o teclado) não poderão usar seu aplicativo.

Esta seção descreve as várias ferramentas que podem ser usadas para testar a implementação de acessibilidade de Windows e aplicativos Web.

> [!NOTE]
> Também é importante fazer testes manuais para verificar o acesso do teclado ao seu aplicativo.

## <a name="tools"></a>Ferramentas

[Acessibilidade Insights](https://accessibilityinsights.io/) – ajuda os desenvolvedores a encontrar e corrigir problemas de acessibilidade em sites e Windows aplicativos.

- [A Insights para Web](https://accessibilityinsights.io/docs/web/overview) é uma extensão para Chrome e [Microsoft Edge Insider](https://www.microsoftedgeinsider.com) que ajuda os desenvolvedores a encontrar e corrigir problemas de acessibilidade em aplicativos Web e sites. Ele dá suporte a dois cenários principais:
  - **FastPass** – um processo leve de duas etapas que ajuda os desenvolvedores a identificar problemas comuns de acessibilidade de alto impacto em menos de cinco minutos.  
  - **Avaliação** – permite que qualquer pessoa verifique se um site está 100% em conformidade com padrões e diretrizes de acessibilidade. [A Insights](https://accessibilityinsights.io/) acessibilidade também permite examinar elementos, propriedades, padrões de controle e eventos do Automação da Interface do Usuário (semelhantes às ferramentas herdadas [Inspecionar](/windows/desktop/winauto/inspect-objects) e [AccEvent](/windows/desktop/winauto/accessible-event-watcher) descritas na seção a seguir).

- [A Insights para Windows](https://accessibilityinsights.io/docs/windows/overview) ajuda os desenvolvedores a encontrar e corrigir problemas de acessibilidade em Windows aplicativos. A ferramenta dá suporte a três cenários principais:
  - **O Live Inspect** permite que os desenvolvedores verifiquem se um elemento em um aplicativo tem as propriedades corretas Automação da Interface do Usuário simplesmente focalizando o elemento ou definindo o foco do teclado nele.
  - **FastPass** – um processo leve de duas etapas que ajuda os desenvolvedores a identificar problemas comuns de acessibilidade de alto impacto em menos de cinco minutos.
  - **A solução de** problemas permite diagnosticar e corrigir problemas de acessibilidade específicos.

### <a name="legacy-testing-tools"></a>Ferramentas de teste herdou

As ferramentas a seguir ainda estão disponíveis no SDK do Windows e estão documentadas aqui para suporte contínuo, mas é recomendável fazer a transição para Acessibilidade [Insights](https://accessibilityinsights.io/).

- [Inspecionar](/windows/desktop/winauto/inspect-objects): permite exibir os dados de acessibilidade de qualquer elemento de interface do usuário. É especialmente útil para garantir que as propriedades e os padrões de controle sejam definidos corretamente ao estender um controle comum ou criar um controle personalizado.
- [AccEvent (Acessador](/windows/desktop/winauto/accessible-event-watcher)de Eventos) : examina os dados de acessibilidade para validar os elementos da interface do usuário do aplicativo e garantir que os elementos da interface do usuário aumentem eventos Microsoft Active Accessibility e Automação da Interface do Usuário eventos da interface do usuário. O AccEvent normalmente é usado para depurar problemas e validar se os controles personalizados e estendidos estão funcionando corretamente.
- [AccScope:](/windows/desktop/winauto/accscope)habilita a avaliação visual da acessibilidade de um aplicativo durante as fases de design e desenvolvimento antecipadas. O AccScope ajuda a visualizar como um leitor de tela usa Automação da Interface do Usuário informações fornecidas por um aplicativo e mostra onde adicionar informações ou suporte ao seu aplicativo pode melhorar sua acessibilidade.
- [Verificador de Acessibilidade da](/windows/desktop/winauto/ui-accessibility-checker)Interface do Usuário: verifica se os principais requisitos de acessibilidade da interface do usuário em um aplicativo são atingidos. O AccChecker inclui verificações de Automação da Interface do Usuário, Microsoft Active Accessibility e ARIA (Aplicativos de Internet Rich) acessíveis. Ele pode fornecer uma verificação estática de erros, como nomes ausentes, problemas de árvore e muito mais. Ele ajuda a verificar o acesso programático e inclui recursos avançados para automatizar testes de acessibilidade.
- [Automação da Interface do Usuário Verificar:](/windows/desktop/winauto/ui-automation-verify)uma estrutura para testes manuais e automatizados da implementação Automação da Interface do Usuário em um controle ou aplicativo (os resultados podem ser registrados). Você pode integrar seu aplicativo ao código de teste e realizar testes regulares automatizados ou verificações spot de seus cenários Automação da Interface do Usuário dados. Essa ferramenta é útil para verificar se as alterações em aplicativos com recursos estabelecidos não têm novos problemas ou regressões em áreas além dos novos recursos.
