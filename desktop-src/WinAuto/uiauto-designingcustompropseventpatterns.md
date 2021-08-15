---
title: Criar propriedades personalizadas, eventos e padrões de controle
description: O design de um padrão de propriedade, evento ou controle personalizado deve ser útil em uma ampla variedade de implementações de controle.
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- Automação da interface do usuário, propriedades personalizadas
- Automação da interface do usuário, visão geral de eventos
- Visão geral da automação da interface do usuário, padrões de controle
- Automação da interface do usuário, criando Propriedades personalizadas
- Automação da interface do usuário, criação de eventos
- Automação da interface do usuário, design de padrões de controle
- Automação da interface do usuário, WinEvents
- Propriedades personalizadas, criando
- eventos, criando
- eventos, WinEvents
- padrões de controle, design
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5b95d7daa3570e8b4b9b1d61c7c5f5590c6456d83190195e57af66811f1672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324792"
---
# <a name="design-custom-properties-events-and-control-patterns"></a>Criar propriedades personalizadas, eventos e padrões de controle

O design de um padrão de propriedade, evento ou controle personalizado deve ser útil em uma ampla variedade de implementações de controle. Designs específicos de controle ou aplicativo que são úteis apenas em cenários limitados devem ser evitados. O design deve seguir o exemplo das propriedades de automação da interface do usuário da Microsoft, eventos e padrões de controle existentes, que foram cuidadosamente especificados para atender às necessidades de uma ampla variedade de aplicativos de acessibilidade e de teste automatizados.

A implementação da especificação de um padrão de propriedade, evento ou controle personalizado envolve a cooperação e o contrato de partes nos lados do cliente e do provedor e exige que ambas as partes implementem a especificação de forma consistente. As empresas são incentivadas a trabalhar com organizações do setor, como a [AIA (Accessibility Interoperability Alliance)](https://www.atia.org/) , para projetar e publicar a especificação para a propriedade personalizada, evento ou padrão de controle. Dessa forma, o consenso pode ser alcançado e a interoperabilidade com a maior variedade de aplicativos pode ser garantida.

Este tópico contém as seguintes seções:

-   [Quando usar propriedades e eventos personalizados](#when-to-use-custom-properties-and-events)
-   [Criando Propriedades personalizadas](#designing-custom-properties)
-   [Criando eventos personalizados](#designing-custom-events)
    -   [Eventos personalizados de automação de interface do usuário e WinEvents](#custom-ui-automation-events-and-winevents)
-   [Criando padrões de controle personalizados](#designing-custom-control-patterns)
-   [Tipos de controle personalizados](#custom-control-types)
-   [Tópicos relacionados](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a>Quando usar propriedades e eventos personalizados

Antes de criar uma propriedade personalizada, evento ou padrão de controle, verifique se a automação da interface do usuário não fornece uma solução existente. Por exemplo, a criação de um padrão de controle "click" personalizado não é necessária porque o padrão de controle [Invoke](uiauto-implementinginvoke.md) já descreve essa funcionalidade.

Se você decidir que um padrão de propriedade, evento ou controle personalizado é necessário, verifique se ele não é muito vago ou genérico. Por exemplo, um padrão de controle chamado "Mostrar" não é útil porque a visibilidade de um controle pode ser indicada por uma propriedade de disponibilidade no elemento, como [**UIA \_ IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) ou [**UIA \_ IsScrollItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md).

Antes de implementar uma solução personalizada, confirme cuidadosamente que ela é necessária e, em seguida, crie a funcionalidade completamente.

## <a name="designing-custom-properties"></a>Criando Propriedades personalizadas

A automação da interface do usuário inclui dois tipos básicos de propriedades: propriedades do elemento Automation e propriedades de padrão de controle. As propriedades do elemento Automation consistem em um conjunto comum de propriedades, como Name, AcceleratorKey e ClassName, que são expostas por todos os elementos de automação da interface do usuário, independentemente do tipo de controle. As propriedades de padrão de controle são expostas por um controle por meio de um padrão de controle específico. Cada padrão de controle tem um conjunto correspondente de propriedades de padrão de controle que o controle deve expor. Por exemplo, um controle que dá suporte ao padrão de controle de [grade](uiauto-implementinggrid.md) expõe as propriedades ColumnCount e RowCount.

Uma propriedade de elemento de automação personalizada ou propriedade de padrão de controle deve aderir às seguintes diretrizes de design:

-   Uma propriedade personalizada deve ter um dos seguintes tipos de dados especificados pela enumeração [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) . Nenhum outro tipo de dados tem suporte para propriedades personalizadas.
    -   **\_Bool UIAutomationType**
    -   **UIAutomationType \_ duplo**
    -   **\_Elemento UIAutomationType**
    -   **UIAutomationType \_ int**
    -   **Ponto de UIAutomationType \_**
    -   **\_Cadeia de caracteres UIAutomationType**
-   Se a propriedade personalizada contiver dados de cadeia de caracteres ([**BSTR**](/previous-versions/windows/desktop/automat/bstr)), a especificação deverá indicar se a propriedade é localizável (ou seja, se a cadeia de caracteres pode ser convertida em diferentes idiomas da interface do usuário).
-   A propriedade personalizada não deve se sobrepor aos recursos ou à funcionalidade de propriedades existentes.

## <a name="designing-custom-events"></a>Criando eventos personalizados

Os aplicativos usam notificações de eventos de automação da interface do usuário para responder a alterações e ações envolvendo itens da interface do usuário. A maioria das propriedades tem eventos de alteração de propriedade associados que a automação da interface do usuário gera quando o valor da propriedade é alterado. Se você introduzir uma propriedade personalizada, deverá considerar a introdução de qualquer evento personalizado correspondente que também possa ser necessário.

Um evento personalizado deve aderir às seguintes diretrizes de design:

-   O evento personalizado deve ser "sem estado". Ele não pode ser associado a uma propriedade ou valor específico.
-   O evento personalizado não deve se sobrepor à definição ou à função de qualquer evento existente.

### <a name="custom-ui-automation-events-and-winevents"></a>Eventos personalizados de automação de interface do usuário e WinEvents

[WinEvents](winevents-infrastructure.md) são um mecanismo útil de comunicação entre processos e eventos na plataforma Microsoft Windows. No entanto, a introdução de uma nova ID de WinEvent é arriscada porque pode causar colisões com outros aplicativos ou o sistema operacional, resultando no sistema se tornar instável. Para evitar colisões, a Microsoft definiu várias categorias diferentes de WinEvents e, para cada categoria, definiu um ou mais intervalos de valores para uso como IDs WinEvent. Para obter mais informações, consulte [alocação de IDs WinEvent](allocation-of-winevent-ids.md).

Eventos de automação de interface do usuário personalizados evitam conflitos alocando a ID do evento internamente na estrutura de automação da interface do usuário.

## <a name="designing-custom-control-patterns"></a>Criando padrões de controle personalizados

Um padrão de controle é uma interface com propriedades, métodos e eventos que definem uma parte discreta da funcionalidade disponível a partir de um elemento de automação. Os métodos de padrão de controle permitem que os clientes de automação da interface do usuário manipulem um aspecto específico do controle. As propriedades e os eventos do padrão de controle fornecem informações sobre algum aspecto do controle e fornecem informações sobre o estado do elemento de automação que implementa o padrão de controle.

Um padrão de controle personalizado deve aderir às seguintes diretrizes de design:

-   Um padrão de controle personalizado deve abranger um cenário específico. Por exemplo, o padrão de controle de [IsContainer](uiauto-implementingitemcontainer.md) é destinado a consultar um objeto contido independentemente do estado de virtualização, mas não enumera ou conta os objetos contidos.
-   Um padrão de controle personalizado não deve se sobrepor aos recursos dos padrões de controle existentes. Por exemplo, os padrões de controle [Invoke](uiauto-implementinginvoke.md) e [ExpandCollapse](uiauto-implementingexpandcollapse.md) não devem ser combinados e apresentados como um novo padrão de controle. Reutilize os padrões de controle existentes ou defina cenários exclusivos com novos padrões de controle.
-   Vários padrões de controle personalizados podem ser criados juntos para dar suporte a cenários complexos. Por exemplo, os padrões de controle [Selection](uiauto-implementingselection.md) e [SelectionItem](uiauto-implementingselectionitem.md) funcionam juntos para dar suporte a cenários de seleção de objetos gerais.

## <a name="custom-control-types"></a>Tipos de controle personalizados

Embora este tópico se concentre em como registrar Propriedades personalizadas de automação de interface do usuário, eventos e padrões de controle, também é possível introduzir novos tipos de controle. Diferentemente de propriedades personalizadas, eventos e padrões de controle, um tipo de controle personalizado não pode ser registrado programaticamente em tempo de execução porque, na verdade, é apenas um valor potencial da propriedade ControlType de automação da interface do usuário. No entanto, uma ID de tipo de controle personalizado pode ser definida, publicada e disponibilizada para outros clientes e provedores usarem. Para obter mais informações sobre tipos de controle, consulte [visão geral de tipos de controle de automação da interface do usuário](uiauto-controltypesoverview.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Registrando Propriedades personalizadas, eventos e padrões de controle](uiauto-regcustompropseventpatterns.md)
</dt> <dt>

[Visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md)
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 