---
title: Ferramentas de teste
description: Descreve as ferramentas para testar a implementação de acessibilidade do seu aplicativo para garantir que a interface do usuário esteja totalmente acessível aos aplicativos cliente e aos usuários que acessam seu aplicativo por meio do teclado.
ms.assetid: abacbec4-6ccd-4853-afcd-a92a6656f393
keywords:
- ferramentas de teste de acessibilidade
- ferramentas de teste, acessibilidade
- teste de acessibilidade
- UIA
- MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce653adb2602b8fdd46bebb72d3a7607185ffd84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084852"
---
# <a name="testing-tools"></a>Ferramentas de teste

Acesso programático e acesso ao teclado são requisitos críticos para dar suporte à acessibilidade em seu aplicativo. Sem o acesso adequado, muitos usuários da tecnologia assistencial (em), como o leitor de tela e os usuários de teclado na tela, não poderiam usar seu aplicativo. Certifique-se de testar exaustivamente a implementação de acessibilidade de seu aplicativo para confirmar que ele fornece informações adequadas sobre seus elementos de interface do usuário e que todos os seus cenários de aplicativo podem ser realizados apenas com o teclado.

Além de verificar o acesso programático, algumas das ferramentas podem ajudá-lo a avaliar a implementação do acesso ao teclado do seu aplicativo. No entanto, as ferramentas sozinhas não são suficientes. É importante verificar manualmente se todos os cenários podem ser realizados apenas com o teclado.

Para requisitos de programação e de teclado, não há uma ferramenta que possa verificar sua implementação completa. Tente usar uma variedade de ferramentas para verificar sua implementação e, quando possível, localizar usuários de tecnologias assistenciais, como leitores de tela, para usar sua interface do usuário.

Esta seção descreve as ferramentas disponíveis para testar as implementações do UIA (Microsoft UI Automation) e do Microsoft Acessibilidade Ativa (MSAA).

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

- [**Inspetor de eventos acessível**](accessible-event-watcher.md): a ferramenta AccEvent (Inspetor de eventos acessível) examina os dados de acessibilidade para ajudar a validar os elementos da interface do usuário do aplicativo, para garantir que os elementos da interface do usuário gerem eventos adequados de automação da interface do usuário e acessibilidade ativa da Microsoft quando ocorrem alterações na interface AccEvent geralmente é usado para depurar problemas e para validar que os controles personalizados e estendidos estão funcionando corretamente.

- [**Inspecionar**](inspect-objects.md): inspecionar permite que você exiba os dados de acessibilidade em qualquer elemento de interface do usuário. Ele é especialmente útil ao estender um controle comum ou criar um controle personalizado, para garantir que as propriedades e os padrões de controle sejam definidos corretamente.

- [**AccScope**](accscope.md): a ferramenta AccScope permite que os desenvolvedores avaliem visualmente a acessibilidade de seus aplicativos durante as fases de design e desenvolvimento iniciais. O AccScope ajuda a visualizar como um leitor de tela usa informações de automação da interface do usuário que um aplicativo fornece. Ele pode mostrar áreas em que a adição de informações ou suporte ao seu aplicativo pode melhorar sua acessibilidade.

- [**Verificador de acessibilidade**](ui-accessibility-checker.md)da interface do usuário: a ferramenta AccChecker (verificador de acessibilidade da interface do usuário) verifica se os principais requisitos de acessibilidade da interface do usuário foram O AccChecker inclui verificações de verificação para automação da interface do usuário, Microsoft Acessibilidade Ativa e ARIA (aplicativos avançados de Internet) acessíveis. Ele pode fornecer uma verificação estática procurando erros, como nomes ausentes, problemas de árvore e muito mais. Ele ajuda a verificar o acesso programático e tem recursos avançados para dar suporte à automatização de testes de acessibilidade.

- [**Verificação de automação da interface**](ui-automation-verify.md)do usuário: verificação de automação da interface do usuário (UIA Verify) é uma estrutura de teste para teste manual e automatizado da implementação de um controle ou do aplicativo da automação da interface do usuário. Ele também pode registrar os resultados do teste. Você pode integrar seu aplicativo no código de teste e realizar verificações regulares, automatizadas ou comparações de testes de seus cenários de automação da interface do usuário. Essa ferramenta é útil para verificar se as alterações em aplicativos com recursos estabelecidos não têm novos problemas ou regressões em áreas além dos novos recursos.

### <a name="obsolete-tools"></a>Ferramentas obsoletas

As ferramentas **acessíveis do Gerenciador** e **da interface do usuário** estão obsoletas e não estão mais disponíveis. Em vez disso, use [**inspecionar**](inspect-objects.md) ou [**AccScope**](accscope.md) .

## <a name="related-topics"></a>Tópicos relacionados

- [Hub de desenvolvedor de acessibilidade](https://developer.microsoft.com/windows/accessible-apps)
- [Acessibilidade da Microsoft](https://www.microsoft.com/accessibility/)