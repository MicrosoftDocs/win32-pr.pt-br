---
title: Usando automação de interface do usuário para testes automatizados
description: Esta visão geral descreve como a automação da interface do usuário da Microsoft pode ser útil como uma estrutura de acesso programático em cenários de teste automatizados.
ms.assetid: 192162f9-55bf-4111-9f15-c0d3b5af2ab7
keywords:
- clientes, teste automatizado de automação da interface do usuário
- clientes, teste automatizado
- clientes, teste
- clientes, ferramentas para teste automatizado
- clientes, ferramentas de automação da interface do usuário para teste automatizado
- clientes, teste de automação da interface do usuário
- Automação da interface do usuário, teste automatizado
- Automação da interface do usuário, teste
- Automação da interface do usuário, ferramentas para teste automatizado
- testes automatizados
- ferramentas para testes automatizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269ff32cae26f8bb8ea6bb5b55ac91f1e0486685
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005526"
---
# <a name="using-ui-automation-for-automated-testing"></a>Usando automação de interface do usuário para testes automatizados

Esta visão geral descreve como a automação da interface do usuário da Microsoft pode ser útil como uma estrutura de acesso programático em cenários de teste automatizados.

A automação da interface do usuário fornece um modelo de objeto unificado que permite que todas as estruturas da interface do usuário exponham funcionalidades complexas e sofisticadas de maneira acessível e facilmente automatizada.

A automação da interface do usuário foi desenvolvida como um sucessor do Microsoft Acessibilidade Ativa, uma estrutura projetada para fornecer uma solução para tornar os controles e aplicativos acessíveis. O Microsoft Acessibilidade Ativa não foi projetado com a automação de teste em mente, embora tenha evoluído nessa função devido aos requisitos semelhantes de acessibilidade e automação. A automação da interface do usuário foi projetada especificamente para fornecer uma funcionalidade robusta para testes automatizados, além de fornecer soluções mais refinadas para acessibilidade. Por exemplo, o Microsoft Acessibilidade Ativa se baseia em uma única interface para expor informações sobre a interface do usuário e para coletar as informações necessárias para produtos de tecnologia assistencial; A automação da interface do usuário separa os dois modelos.

Um provedor e um cliente são necessários para implementar a automação da interface do usuário para que ele seja útil como uma ferramenta de teste automatizada. Os provedores de automação de interface do usuário são aplicativos, como o Microsoft Word, o Microsoft Excel e outros aplicativos ou controles de terceiros baseados no sistema operacional Windows. Os clientes de automação da interface do usuário incluem scripts de teste automatizados e aplicativos de tecnologia assistencial.

Este tópico inclui as seções a seguir.

-   [Automação da interface do usuário em provedores](#ui-automation-in-providers)
-   [Automação da interface do usuário em clientes](#ui-automation-in-clients)
    -   [Acesso programático](#programmatic-access)
-   [Propriedades de chave para automação de teste](#key-properties-for-test-automation)
-   [Ferramentas e tecnologias relacionadas](#related-tools-and-technologies)
-   [Tópicos relacionados](#related-topics)

## <a name="ui-automation-in-providers"></a>Automação da interface do usuário em provedores

Para automatizar um elemento da interface do usuário, o desenvolvedor deve examinar as ações que um usuário final pode executar no objeto da interface do usuário usando a interação padrão do teclado e do mouse. Depois que essas ações de chave forem identificadas, os padrões de controle de automação da interface do usuário que espelham a funcionalidade e o comportamento do elemento de interface do usuário devem ser implementados no controle. Por exemplo, a interação do usuário com um controle caixa de combinação normalmente envolve expandir e recolher a caixa de combinação para exibir ou ocultar uma lista de itens, selecionar um item da lista ou adicionar um novo valor por meio de entrada do teclado.

Com outros modelos de acessibilidade, os desenvolvedores devem reunir informações diretamente de botões, menus ou outros controles individuais. Cada tipo de controle vem em dezenas de variações secundárias. Em outras palavras, mesmo que 10 variações de um botão de pressão funcionem da mesma maneira e executem a mesma função, elas devem ser tratadas como controles exclusivos. Não é possível saber que esses controles são funcionalmente equivalentes. Padrões de controle de automação da interface do usuário foram desenvolvidos para representar esses comportamentos de controle comuns. Para obter mais informações, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).

Sem o modelo unificado de padrões de controle fornecido pela automação da interface do usuário, as ferramentas de teste e os desenvolvedores devem ter informações específicas da estrutura para expor propriedades e comportamentos de controle nessa estrutura. Como várias estruturas de interface do usuário diferentes podem estar presentes ao mesmo tempo em sistemas operacionais Windows, incluindo o Microsoft Win32, o Windows Forms e o Windows Presentation Foundation (WPF), pode ser uma tarefa assustadora para testar vários aplicativos com controles que parecem semelhantes. Por exemplo, a tabela a seguir lista os nomes de propriedade específicos da estrutura necessários para recuperar o nome ou o texto associado a um controle de botão e mostra a propriedade de automação da interface do usuário equivalente.



| Tipo de controle | Estrutura de interface do usuário | Propriedade específica da estrutura | Propriedade de automação da interface do usuário |
|--------------|--------------|-----------------------------|------------------------|
| Botão       | WPF          | Conteúdo                     | Propriedade Name          |
| Botão       | Win32        | Legenda                     | Propriedade Name          |
| Imagem        | HTML         | alt                         | Propriedade Name          |



 

Os provedores de automação da interface do usuário são responsáveis por mapear as propriedades específicas da estrutura de seus controles para as propriedades equivalentes de automação da interface do usuário. Para obter informações sobre como implementar a automação de interface do usuário em um provedor, consulte [Guia do programador do provedor de automação de IU](uiauto-providerportal.md). Para obter informações sobre como implementar padrões de controle, consulte [implementando padrões de controle de automação da interface do usuário](uiauto-implementinguiautocontrolpatterns.md).

## <a name="ui-automation-in-clients"></a>Automação da interface do usuário em clientes

O objetivo das ferramentas e cenários de teste automatizados é a manipulação consistente e reproduzível da interface do usuário. Por exemplo, isso pode envolver controles específicos de teste de unidade e registrar e executar scripts de teste que iteram por meio de uma série de ações genéricas em um grupo de controles.

Uma complicação em aplicativos automatizados é a dificuldade de sincronizar um teste com um destino dinâmico, por exemplo, um controle de caixa de listagem, como o Gerenciador de tarefas do Windows, que exibe uma lista de aplicativos em execução no momento. Como os itens na caixa de listagem são atualizados dinamicamente fora do controle do aplicativo de teste, uma tentativa de repetir a seleção de um item específico na caixa de listagem com qualquer consistência é impossível. Problemas semelhantes podem surgir ao tentar repetir alterações de foco simples em uma interface do usuário que está fora do controle do aplicativo de teste.

### <a name="programmatic-access"></a>Acesso Programático

O acesso programático fornece a capacidade de imitar, por meio de código, qualquer interação e experiência exposta por entrada tradicional de mouse e teclado. A automação da interface do usuário permite acesso programático por meio de cinco componentes:

-   A árvore de automação da interface do usuário facilita a navegação por meio da estrutura da interface do usuário. A árvore é criada a partir da coleção de **HWND** s. Para obter mais informações, consulte [visão geral da árvore de automação da interface do usuário](uiauto-treeoverview.md).
-   Os elementos de automação são componentes individuais na interface do usuário. Muitas vezes, eles podem ser mais granulares do que um **HWND**.
-   As propriedades de automação fornecem informações específicas sobre elementos da interface do usuário. Para obter mais informações, consulte [visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md).
-   Padrões de controle definem um aspecto específico da funcionalidade de um controle; Eles podem consistir de informações de propriedade, método, evento e estrutura. Para obter mais informações, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).
-   Os eventos de automação fornecem notificações e informações de eventos. Para obter mais informações, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).

## <a name="key-properties-for-test-automation"></a>Propriedades de chave para automação de teste

A capacidade de identificar e subseqüentemente localizar qualquer controle na interface do usuário fornece a base para que os aplicativos de teste automatizados operem nessa interface do usuário. As propriedades de automação da interface do usuário usadas por clientes e provedores para identificar e localizar controles são descritas na tabela a seguir.



| Propriedade     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AutomationId | Distingue exclusivamente um elemento Automation de seus irmãos. O suporte para a propriedade AutomationId não é necessário. Quando está disponível, a propriedade AutomationId de um elemento é a mesma em qualquer instância do aplicativo, independentemente do idioma local. Embora a propriedade AutomationId seja exclusiva entre elementos irmãos, ela pode não ser exclusiva em toda a área de trabalho. Por exemplo, várias instâncias de um aplicativo ou várias exibições de pasta no Microsoft Windows Explorer podem conter elementos com o mesmo AutomationIdProperty, como "SystemMenuBar". Os clientes não devem fazer suposições sobre o AutomationIds exposto por outros aplicativos. Não há garantia de que o AutomationId seja estável em diferentes versões ou compilações de um aplicativo. |
| ControlType  | Identifica o tipo de controle representado por um elemento de automação. Informações significativas podem ser inferidas do conhecimento do tipo de controle. Para obter mais informações, consulte [visão geral de tipos de controle de automação da interface do usuário](uiauto-controltypesoverview.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Name         | Uma cadeia de texto que identifica ou explica a finalidade de um elemento de automação. Ele deve ser usado com cautela porque pode ser localizado. A propriedade Name não é um identificador exclusivo entre irmãos. Para a automação de teste, os clientes devem usar a propriedade AutomationId ou a propriedade runtimeId em vez disso.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| RuntimeId    | Uma matriz de inteiros que representa um identificador para um elemento de automação. O identificador é exclusivo na área de trabalho, mas é garantido que seja exclusivo apenas para a interface do usuário na qual ele foi gerado. Os identificadores podem ser reutilizados ao longo do tempo. Use [**IUIAutomation:: CompareElements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-compareelements) para determinar se o elemento que atualmente tem uma ID de tempo de execução específica é o mesmo elemento que tinha essa ID anteriormente. Além disso, o formato da propriedade runtimeId pode ser alterado. Ele deve ser tratado como um valor opaco e usado apenas para comparação; por exemplo, para determinar se um elemento de automação está no cache.                                                                                                                       |



 

## <a name="related-tools-and-technologies"></a>Ferramentas e tecnologias relacionadas

[Inspecione](inspect-objects.md) (Inspect.exe) é uma ferramenta baseada no Windows que você pode usar para coletar informações de automação da interface do usuário para desenvolvimento e depuração de provedor e cliente. A inspeção está incluída no SDK (Software Development Kit) do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações de segurança de automação da interface do usuário](uiauto-securityoverview.md)
</dt> </dl>

 

 




