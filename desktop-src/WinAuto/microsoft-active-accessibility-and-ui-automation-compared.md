---
title: Microsoft Acessibilidade Ativa e automação da interface do usuário comparada
description: Este tópico fornece um resumo das principais diferenças entre o Microsoft Acessibilidade Ativa e a automação da interface do usuário.
ms.assetid: ba963e53-6fb8-4bc1-8883-62547f52b0e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c90c4bffd0646aea592e19adc51ca020b2c90d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105769089"
---
# <a name="microsoft-active-accessibility-and-ui-automation-compared"></a>Microsoft Acessibilidade Ativa e automação da interface do usuário comparada

A API de automação do Windows consiste em duas tecnologias: Microsoft Acessibilidade Ativa e automação da interface do usuário da Microsoft. O Microsoft Acessibilidade Ativa é a tecnologia de acessibilidade herdada que foi introduzida como um suplemento de plataforma para o Windows 95, enquanto a automação da interface do usuário é uma tecnologia mais nova e mais compatível que supera as limitações inerentes ao Microsoft Acessibilidade Ativa.

Este tópico fornece um resumo das principais diferenças entre o Microsoft Acessibilidade Ativa e a automação da interface do usuário. Ele inclui as seguintes seções:

-   [Princípios básicos de design](#basic-design-principles)
-   [Propriedades e padrões de controle](#properties-and-control-patterns)
-   [Funções de MSAA e padrões de controle de automação da interface do usuário](#msaa-roles-and-ui-automation-control-patterns)
-   [Navegação de modelo de objeto](#object-model-navigation)
-   [Extensibilidade do modelo de objeto](#object-model-extensibility)
-   [Transição do MSAA](#transitioning-from-msaa)
-   [Escolhendo o Microsoft Acessibilidade Ativa, a automação da interface do usuário ou o IAccessibleEx](#choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex)
    -   [Novos aplicativos e controles](#new-applications-and-controls)
    -   [Implementações existentes do Microsoft Acessibilidade Ativa](#existing-microsoft-active-accessibility-implementations)
-   [Tópicos relacionados](#related-topics)

## <a name="basic-design-principles"></a>Princípios básicos de design

Embora o Microsoft Acessibilidade Ativa e a automação da interface do usuário sejam duas tecnologias diferentes, os princípios básicos de design são semelhantes. A finalidade de ambas as tecnologias é expor informações ricas sobre os elementos da interface do usuário usados em aplicativos do Windows. Os desenvolvedores de ferramentas de acessibilidade podem usar essas informações para criar software que torna os aplicativos em execução no Windows mais acessíveis a pessoas com deficiências visuais, auditivas ou motoras.

O Microsoft Acessibilidade Ativa e a automação da interface do usuário expõem o modelo de objeto da interface do usuário como uma árvore hierárquica, com raiz na área de trabalho. O Microsoft Acessibilidade Ativa representa elementos individuais da interface do usuário como *objetos acessíveis* e a automação da interface do usuário os representa como *elementos de automação*. Ambos referem-se à ferramenta de acessibilidade ou ao programa de automação de software como o *cliente*. No entanto, o Microsoft Acessibilidade Ativa refere-se ao aplicativo ou controle que oferece a interface do usuário para acessibilidade como o *servidor*, enquanto a automação da interface do usuário se refere a isso como o *provedor*.

## <a name="properties-and-control-patterns"></a>Propriedades e padrões de controle

O Microsoft Acessibilidade Ativa oferece uma única interface de Component Object Model (com) com um conjunto fixo e pequeno de propriedades. A automação da interface do usuário oferece um conjunto mais rico de propriedades, bem como um conjunto de interfaces estendidas chamadas de *padrões de controle* para manipular objetos acessíveis de maneiras que o Microsoft acessibilidade ativa não pode.

Para obter mais informações, consulte Visão [Geral das propriedades de automação da IU](uiauto-propertiesoverview.md) e [visão geral dos padrões de controle de automação de IU](uiauto-controlpatternsoverview.md).

## <a name="msaa-roles-and-ui-automation-control-patterns"></a>Funções de MSAA e padrões de controle de automação da interface do usuário

A Microsoft projetou o modelo de objeto do Microsoft Acessibilidade Ativa ao mesmo tempo que o Windows 95 foi lançado. O modelo se baseia em "funções" definidas há uma década e você não pode dar suporte a novos comportamentos de interface do usuário ou mesclar duas ou mais funções juntas. Não há nenhum modelo de objeto de texto, por exemplo, para ajudar as tecnologias assistenciais a lidar com conteúdo da Web complexo. A automação da interface do usuário supera essas limitações introduzindo padrões de controle que permitem que objetos ofereçam suporte a mais de uma função, e o padrão de controle de [texto](uiauto-implementingtextandtextrange.md) de automação da interface do usuário oferece um modelo de objeto de texto completo.

## <a name="object-model-navigation"></a>Navegação de modelo de objeto

Outra limitação do Microsoft Acessibilidade Ativa envolve a navegação no modelo de objeto. O Microsoft Acessibilidade Ativa representa a interface do usuário como uma hierarquia de objetos acessíveis. Os clientes navegam de um objeto acessível para outro usando interfaces e métodos disponíveis no objeto acessível. Os servidores podem expor os filhos de um objeto acessível com as propriedades da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou com a interface com [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) padrão. Os clientes, no entanto, devem ser capazes de lidar com as duas abordagens para qualquer servidor. Essa ambiguidade significa trabalho extra para implementadores de cliente e modelos de objeto acessíveis desfeitos para implementadores de servidor.

A automação da interface do usuário representa a interface do usuário como uma árvore hierárquica de elementos de automação e fornece uma única interface para navegar na árvore. Os clientes podem personalizar a exibição de elementos na árvore por escopo e filtragem.

## <a name="object-model-extensibility"></a>Extensibilidade do modelo de objeto

As propriedades e funções do Microsoft Acessibilidade Ativa não podem ser estendidas sem interromper ou alterar a especificação de interface com do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . O resultado é que o novo comportamento de controle não pode ser exposto por meio do modelo de objeto; Ela tende a ser estática.

Com a automação da interface do usuário, à medida que novos elementos da interface do usuário são criados, os desenvolvedores de aplicativos podem introduzir Propriedades personalizadas, padrões de controle e eventos para descrever os novos elementos. Para obter mais informações, consulte [Propriedades personalizadas, eventos e padrões de controle](uiauto-custompropertieseventscontrolpatterns.md).

## <a name="transitioning-from-msaa"></a>Transição do MSAA

A estrutura da API de automação do Windows fornece suporte para a transição de servidores do Microsoft Acessibilidade Ativa para provedores de automação da interface do usuário. A interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permite que o suporte para propriedades de automação de interface do usuário específicas e padrões de controle sejam adicionados a servidores herdados do Microsoft acessibilidade ativa sem a necessidade de reescrever toda a implementação. A interface **IAccessibleEx** também permite que clientes em processo do Microsoft acessibilidade ativa acessem interfaces do provedor de automação de interface do usuário diretamente, em vez de interfaces cliente de automação da interface do usuário. Para obter mais informações, consulte [a interface IAccessibleEx](iaccessibleex.md).

## <a name="choosing-microsoft-active-accessibility-ui-automation-or-iaccessibleex"></a>Escolhendo o Microsoft Acessibilidade Ativa, a automação da interface do usuário ou o IAccessibleEx

Esta seção ajuda você a determinar qual solução de API de automação do Windows usar para implementar um produto de tecnologia assistencial ou para tornar seu aplicativo acessível a produtos de tecnologia assistencial.

### <a name="new-applications-and-controls"></a>Novos aplicativos e controles

Se você estiver desenvolvendo um novo aplicativo ou controle, a Microsoft recomenda usar a automação da interface do usuário. Embora o Microsoft Acessibilidade Ativa possa ser mais fácil de implementar a curto prazo, as limitações inerentes a essa tecnologia, como o modelo de objeto de envelhecimento e a incapacidade de dar suporte a novos comportamentos de interface do usuário ou funções de mesclagem, tornam isso mais difícil e dispendioso em longo prazo. Essas limitações se tornam especialmente aparentes ao introduzir novos controles.

O modelo de objeto de automação da interface do usuário é mais fácil de usar e é mais flexível do que o do Microsoft Acessibilidade Ativa. Os elementos de automação da interface do usuário refletem a evolução das interfaces de usuários e os desenvolvedores podem definir padrões, propriedades e eventos de controle de automação de IU personalizados.

O Microsoft Acessibilidade Ativa tende a ser executado lentamente para clientes que ficam fora do processo. Para melhorar o desempenho, os desenvolvedores de programas de ferramentas de acessibilidade geralmente optam por conectar e executar seus programas no processo do aplicativo de destino: uma abordagem extremamente difícil e arriscada. A automação da interface do usuário é muito mais fácil de ser implementada para clientes fora do processo e oferece desempenho e confiabilidade muito melhores.

### <a name="existing-microsoft-active-accessibility-implementations"></a>Implementações existentes do Microsoft Acessibilidade Ativa

Se você estiver atualizando um aplicativo ou controle existente baseado no Microsoft Acessibilidade Ativa, considere adicionar suporte para automação da interface do usuário implementando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Primeiro, verifique se seu aplicativo ou controle atende aos seguintes requisitos:

-   A hierarquia de objetos acessíveis do Microsoft Acessibilidade Ativa Server de linha de base deve ser bem organizada e sem erros. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) não pode corrigir problemas com hierarquias de objeto acessíveis existentes.
-   Sua implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) deve estar em conformidade com a especificação de acessibilidade ativa da Microsoft e a especificação de automação da interface do usuário. A Microsoft fornece um conjunto de ferramentas para validar a conformidade com ambas as especificações. Para obter mais informações, consulte [Testing Tools](testing-tools.md).

Se um desses requisitos não for atendido, considere implementar a automação da interface do usuário nativamente. Você pode manter implementações herdadas do Microsoft Acessibilidade Ativa Server para compatibilidade com versões anteriores, se necessário. Da perspectiva do cliente de automação da interface do usuário, não há nenhuma diferença entre os provedores de automação da interface do usuário e os servidores do Microsoft Acessibilidade Ativa que implementam [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) corretamente.

Para obter mais informações, consulte [a interface IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da API de automação do Windows](windows-automation-api-overview.md)
</dt> <dt>

[Acessibilidade Ativa da Microsoft](microsoft-active-accessibility.md)
</dt> <dt>

[Automação da Interface do Usuário](entry-uiauto-win32.md)
</dt> <dt>

[A interface IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 