---
title: Testando uma interface do usuário
description: esta seção descreve detalhadamente algumas das tarefas associadas ao teste de uma interface do usuário para um aplicativo Windows.
ms.assetid: d628e530-7a0b-4a8d-9a9f-253aec275fa9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f3d6686cdcd892aa5608944cf8c1a20df0d44106a0fdac01b2bbbd855fe523
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507426"
---
# <a name="testing-a-user-interface"></a>Testando uma interface do usuário

esta seção descreve detalhadamente algumas das tarefas associadas ao teste de uma interface do usuário para um aplicativo Windows.

-   [Introdução](#introduction)
-   [Testes de usabilidade](#usability-testing)
-   [Teste de acessibilidade](#accessibility-testing)

## <a name="introduction"></a>Introdução

Para determinar completamente a eficácia e a usabilidade geral de uma interface do usuário do aplicativo, ela deve ser testada. O teste expõe como é fácil ou difícil usar a interface do usuário para o público mais amplo possível. O tempo necessário para testar um aplicativo é muito importante.

Este tópico se concentra em três cenários principais de teste: usabilidade, acessibilidade e automação gerais.

## <a name="usability-testing"></a>Teste de usabilidade

Os testes de usabilidade oferecem a oportunidade de avaliar um produto, estudando como os usuários reais realmente usam o produto. Essa análise garante que as principais suposições sobre os usuários pretendidos e designs de interface tenham suporte (ou desafiados) com dados reais. Somente ao coletar esses dados do empírica, você descobrirá como a interface do usuário de um produto atende às necessidades e às expectativas dos seus usuários.

Ao observar a interação do usuário com o produto e ouvir os comentários do usuário, recursos importantes que podem ser difíceis de encontrar e usar são identificados. Com base nesses resultados, os ajustes podem ser feitos na interface do usuário, conforme necessário. É quase impossível criar um produto útil sem algum nível de teste de usabilidade, pois os resultados fornecem a base para tomar decisões melhores sobre o produto e melhorar a experiência geral do usuário.

O teste de usabilidade fornece um retorno significativo apenas quando está bem integrado a todo o ciclo de vida do projeto. Um único estudo de usabilidade pode identificar problemas, mas sem testes de acompanhamento, é difícil determinar se as soluções resolveram esses problemas ou introduziu novos.

Os principais cenários de teste de usabilidade são:

-   Se você for um fornecedor de produtos de software, o teste de usuários reais de seu produto significa que você está avaliando o design. Com base em como você projetou o aplicativo, os usuários podem concluir as tarefas que precisam fazer? Testar os usuários reais fazer tarefas reais também pode indicar se as diretrizes da interface do usuário que você está seguindo estão trabalhando dentro do contexto do seu produto e quando a consistência ajuda ou impede a capacidade de um usuário realizar seu trabalho.
-   Se você for um comprador de produtos de software, poderá fazer testes de usabilidade para avaliar um produto para compra. Por exemplo, sua empresa pode considerar a compra de um produto para seus 20000 funcionários. Antes de a empresa gastar seu dinheiro, ela quer ter certeza de que o produto em questão realmente ajudará os funcionários a realizar seus trabalhos melhor. O teste de usabilidade também pode ser útil para ver se o aplicativo proposto segue as diretrizes de estilo da interface do usuário publicadas (internas ou externas). É melhor usar as diretrizes de interface do usuário como uma fonte auxiliar, em vez de primária, de informações para tomar decisões de compra.

Para obter mais informações, consulte [usabilidade na prática: teste de usabilidade](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing).

## <a name="accessibility-testing"></a>Teste de acessibilidade

O teste de acessibilidade abrange duas áreas de um design de interface do usuário: suporte para usuários com deficiências e acesso programático por estruturas de teste automatizadas.

Garantir que um aplicativo seja acessível aos usuários com deficiências envolve o teste para:

-   Conformidade – o aplicativo está em conformidade com vários requisitos legais em relação à acessibilidade?
-   Eficácia – os usuários com deficiências podem usar o aplicativo?
-   Utilidade – o aplicativo expõe a funcionalidade adequada para usuários com deficiências?
-   Satisfação – como o aplicativo é percebido por usuários com deficiências?

O teste para esses aspectos de um aplicativo pode ser realizado por meio de uma auditoria de acessibilidade, que envolve uma revisão manual do aplicativo por um especialista em acessibilidade e um estudo de usabilidade focado de usuários desabilitados e dispositivos de tecnologia assistencial.

Embora pareça não-relacionado, há uma correlação próxima entre os requisitos de acesso programático de estruturas de teste automatizadas e os de dispositivos de tecnologia assistencial. O suporte a um tem o benefício adicional de habilitar o outro. para obter mais informações sobre acessibilidade e automação de teste em aplicativos Windows, consulte [acessibilidade](/windows/desktop/accessibility), [ferramentas de teste](/windows/desktop/WinAuto/testing-tools)e a API de [automação de Windows](/windows/desktop/WinAuto/windows-automation-api-portal).

 

 