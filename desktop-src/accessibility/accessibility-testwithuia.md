---
description: Visão geral de como usar a automação da interface do usuário e outras ferramentas para testar seus aplicativos.
title: Teste de acessibilidade
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0d589c9b7bd598c0829ff9941ab2facabfaf10d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089587"
---
# <a name="testing-for-accessibility"></a>Teste de acessibilidade

Acesso programático e acesso ao teclado são requisitos críticos para dar suporte à acessibilidade em seu aplicativo. Testar a acessibilidade de seus aplicativos do Windows, ferramentas de tecnologia assistencial (AT) e estruturas de interface do usuário é crucial para garantir uma experiência de usuário bem-sucedida para pessoas com várias deficiências e limitações (incluindo visão, aprendizado, destreza/mobilidade e deficiências de linguagem/comunicação) ou aqueles que simplesmente preferem usar um teclado.

Sem acesso adequado por meio do, como leitores de tela e teclados na tela, os usuários com visão, aprendizado, destreza/mobilidade e deficiências ou limitações de comunicação/idioma (e os usuários que simplesmente preferem usar o teclado) não poderiam usar seu aplicativo.

Esta seção descreve as várias ferramentas que podem ser usadas para testar a implementação de acessibilidade de aplicativos da Web e do Windows.

> [!NOTE]
> Também é importante fazer testes manuais para verificar o acesso do teclado ao seu aplicativo.

## <a name="tools"></a>Ferramentas

[Informações de acessibilidade](https://accessibilityinsights.io/) – ajuda os desenvolvedores a localizar e corrigir problemas de acessibilidade em sites e aplicativos do Windows.

- O [insights de acessibilidade para a Web](https://accessibilityinsights.io/docs/web/overview) é uma extensão para o Chrome e [o Microsoft Edge Insider](https://www.microsoftedgeinsider.com) que ajuda os desenvolvedores a localizar e corrigir problemas de acessibilidade em sites e aplicativos Web. Ele dá suporte a dois cenários principais:
  - **FastPass** – um processo leve de duas etapas que ajuda os desenvolvedores a identificar problemas de acessibilidade comuns e de alto impacto em menos de cinco minutos.  
  - **Avaliação** – permite que qualquer pessoa Verifique se um site tem 100% em conformidade com os padrões e as diretrizes de acessibilidade. O [insights de acessibilidade](https://accessibilityinsights.io/) também permite que você revise elementos de automação da interface do usuário, propriedades, padrões de controle e eventos (semelhante às ferramentas herdadas [inspecionar](/windows/desktop/winauto/inspect-objects) e [AccEvent](/windows/desktop/winauto/accessible-event-watcher) descritas na seção a seguir).

- O [insights de acessibilidade para Windows](https://accessibilityinsights.io/docs/windows/overview) ajuda os desenvolvedores a localizar e corrigir problemas de acessibilidade em aplicativos do Windows. A ferramenta dá suporte a três cenários principais:
  - A **inspeção ao vivo** permite que os desenvolvedores verifiquem se um elemento em um aplicativo tem as propriedades de automação da interface do usuário corretas simplesmente passando o mouse sobre o elemento ou configurando o foco do teclado nele.
  - **FastPass** – um processo leve de duas etapas que ajuda os desenvolvedores a identificar problemas de acessibilidade comuns e de alto impacto em menos de cinco minutos.
  - A **solução de problemas** permite diagnosticar e corrigir problemas de acessibilidade específicos.

### <a name="legacy-testing-tools"></a>Ferramentas de teste herdadas

As ferramentas a seguir ainda estão disponíveis na SDK do Windows e estão documentadas aqui para obter suporte contínuo, mas é recomendável fazer a transição para [informações de acessibilidade](https://accessibilityinsights.io/).

- [Inspecionar](/windows/desktop/winauto/inspect-objects): permite que você exiba os dados de acessibilidade de qualquer elemento de interface do usuário. Ele é especialmente útil para garantir que propriedades e padrões de controle sejam definidos corretamente ao estender um controle comum ou criar um controle personalizado.
- [Inspetor de eventos acessível (AccEvent)](/windows/desktop/winauto/accessible-event-watcher): examina os dados de acessibilidade para validar os elementos da interface do usuário do aplicativo e garantir que os elementos da interface do usuário gerem eventos adequados de automação da interface do usuário e da Microsoft acessibilidade ativa em eventos AccEvent normalmente é usado para depurar problemas e para validar que os controles personalizados e estendidos estão funcionando corretamente.
- [AccScope](/windows/desktop/winauto/accscope): habilita a avaliação visual da acessibilidade de um aplicativo durante as fases de design e desenvolvimento iniciais. O AccScope ajuda a visualizar como um leitor de tela usa as informações de automação da interface do usuário fornecidas por um aplicativo e mostra onde adicionar informações ou suporte ao seu aplicativo pode melhorar sua acessibilidade.
- [Verificador de acessibilidade da interface do usuário](/windows/desktop/winauto/ui-accessibility-checker): verifica se os principais requisitos de acessibilidade da interface do usuário em um aplicativo são obtidos. O AccChecker inclui verificações de verificação para automação da interface do usuário, Microsoft Acessibilidade Ativa e ARIA (aplicativos avançados de Internet) acessíveis. Ele pode fornecer uma verificação estática de erros, como nomes ausentes, problemas de árvore e muito mais. Ele ajuda a verificar o acesso programático e inclui recursos avançados para automatizar o teste de acessibilidade.
- [Verificação de automação da interface do usuário](/windows/desktop/winauto/ui-automation-verify): uma estrutura para teste manual e automatizado da implementação da automação da interface do usuário em um controle ou aplicativo (os resultados podem ser registrados). Você pode integrar seu aplicativo no código de teste e realizar verificações regulares, automatizadas ou comparações de testes de seus cenários de automação da interface do usuário. Essa ferramenta é útil para verificar se as alterações em aplicativos com recursos estabelecidos não têm novos problemas ou regressões em áreas além dos novos recursos.
