---
title: Sobre os padrões de controle Text e TextRange
description: O conteúdo textual de um controle é exposto usando o padrão de controle de texto, que representa o conteúdo de um contêiner de texto como um fluxo de texto.
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- Automação da interface do usuário, suporte a conteúdo textual
- Automação da interface do usuário, visão geral do padrão de texto
- Visão geral da automação da interface do usuário, controles de texto
- Automação da interface do usuário, padrão de controle de texto
- Automação da interface do usuário, TSF (estrutura de serviços de texto)
- Automação da interface do usuário, TSF
- Automação da interface do usuário, desempenho
- padrões de texto, sobre
- padrões de texto, TSF (estrutura de serviços de texto)
- controles de texto, sobre
- conteúdo textual, suporte para
- controles de texto, desempenho
- Padrão de controle de texto
- padrões de controle, texto
- TFS (Estrutura de Serviços de Texto)
- TSF (estrutura de serviços de texto)
- desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9ff1eb75227454e3e9df6035798a304096a958
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105797894"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>Sobre os padrões de controle Text e TextRange

O conteúdo textual de um controle é exposto usando o padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , que representa o conteúdo de um contêiner de texto como um fluxo de texto. O padrão de controle de texto requer o suporte do padrão de controle TextRange para expor atributos de formato e estilo. O padrão de controle TextRange dá suporte ao padrão de controle de texto, representando intervalos de texto separados ou múltiplos, não contíguos (ou faixas) em um contêiner de texto com uma coleção de pontos de extremidade inicial e final. O padrão de controle TextRange oferece suporte a funcionalidades como seleção, comparação, recuperação e passagem.

> [!Note]  
> O padrão de controle de [texto](uiauto-implementingtextandtextrange.md) não fornece um meio para inserir ou modificar texto. No entanto, dependendo do controle, isso pode ser feito usando o padrão de controle de [valor](uiauto-implementingvalue.md) de automação da interface do usuário da Microsoft ou por meio de entrada de teclado direto. Também há um padrão [**Editor**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) que dá suporte à alteração programática em texto.

 

A funcionalidade descrita neste tópico é vital para fornecedores de tecnologia assistencial e seus usuários finais. Tecnologias assistenciais podem usar a automação da interface do usuário para reunir informações completas de formatação de texto para o utilizador e fornecer navegação programática e seleção de texto por [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (caractere, palavra, linha ou parágrafo).

Este tópico contém as seguintes seções:

-   [TextPattern da automação da interface do usuário e a estrutura de serviços de texto](#ui-automation-textpattern-and-the-text-services-framework)
-   [Tipos de controle](#control-types)
-   [Interfaces de provedor](#provider-interfaces)
-   [Interfaces de cliente](#client-interfaces)
-   [Desempenho](#performance)
-   [Padrão de texto e objetos incorporados virtualizados](#text-pattern-and-virtualized-embedded-objects)
-   [Usando o tipo de controle personalizado com o padrão de controle de texto](#using-the-custom-control-type-with-the-text-control-pattern)
-   [Tempo de vida de um intervalo de texto](#lifetime-of-a-text-range)
-   [Tópicos relacionados](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>TextPattern da automação da interface do usuário e a estrutura de serviços de texto

A TSF (estrutura de serviços de texto) é uma estrutura de sistema simples e escalonável que permite serviços de linguagem natural e entrada de texto avançada na área de trabalho e em aplicativos. Além de fornecer interfaces para que os aplicativos exponham seu armazenamento de texto, ele também dá suporte a metadados para o armazenamento de texto.

O TSF foi projetado para aplicativos que precisam injetar entrada em cenários com reconhecimento de contexto. O padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , no entanto, é uma solução somente leitura que é destinada a fornecer acesso otimizado a um armazenamento de texto para leitores de tela e dispositivos de braille.

Tecnologias acessíveis que exigem acesso somente leitura a um armazenamento de texto podem usar o padrão de controle de texto, mas precisarão da funcionalidade do TSF para entrada com reconhecimento de contexto.

Para obter mais informações, consulte [estrutura de serviços de texto](/windows/desktop/TSF/text-services-framework).

## <a name="control-types"></a>Tipos de controle

O tipo de controle de [edição](uiauto-supporteditcontroltype.md) de automação da interface do usuário e o tipo de controle de [documento](uiauto-supportdocumentcontroltype.md) devem suportar o padrão de controle de [texto](uiauto-implementingtextandtextrange.md) Para melhorar a acessibilidade, a Microsoft recomenda que os tipos de controle de texto e [dica de ferramenta](uiauto-supporttooltipcontroltype.md) também ofereçam suporte ao padrão de controle de texto, mas isso não é necessário.

## <a name="provider-interfaces"></a>Interfaces de provedor

Os provedores de automação de interface do usuário dão suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) para um controle implementando as interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) . Essas interfaces expõem informações detalhadas de atributo para texto no controle e fornecem recursos de navegação robustos.

Um provedor não precisará dar suporte a todos os atributos de texto se o controle não tiver suporte para nenhum atributo específico.

Um provedor deve dar suporte aos métodos [**ITextProvider::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) GetSelection e [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) se o controle oferecer suporte à seleção de texto ou ao posicionamento do cursor de texto (ou do cursor do sistema) na área de texto. Se o controle não oferecer suporte a essa funcionalidade, ele não precisará oferecer suporte a nenhum desses métodos. No entanto, o controle deve expor o tipo de seleção de texto compatível com a implementação da propriedade [**ITextProvider:: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) .

Um provedor deve sempre dar suporte às constantes [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , timeunit **\_ Character** e **TextUnit \_**, bem como a qualquer outra pessoa com suporte.

> [!Note]  
> O provedor pode ignorar o suporte para uma [**fileunit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) específica, desferindo-se à próxima unidade maior com suporte na seguinte ordem: **\_ caractere TextUnit**, **\_ formato TextUnit**, **timeunit \_ Word**, **timeunit \_ line**, TextUnit **\_ Paragraph**, **TextUnit \_ Page** e **TextUnit \_ Document**.

 

## <a name="client-interfaces"></a>Interfaces de cliente

Os aplicativos cliente de automação da interface do usuário usam as interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) para acessar o conteúdo textual de um controle de texto. Os clientes usam **IUIAutomationTextPattern** para selecionar trechos de texto chamados de *intervalos de texto* e para recuperar ponteiros para interfaces **IUIAutomationTextRange** para os intervalos. A interface **IUIAutomationTextRange** permite que os clientes manipulem o intervalo de texto e recuperem informações sobre o texto no intervalo, incluindo atributos como nome da fonte, cor de primeiro plano, estilo de sublinhado e assim por diante. Para obter mais informações, consulte [identificadores de atributo de texto](uiauto-textattribute-ids.md).

## <a name="performance"></a>Desempenho

O padrão de controle de **texto** se baseia em chamadas de processo cruzado para a maior parte de sua funcionalidade, portanto, ele não fornece um mecanismo de cache para melhorar o desempenho ao processar o conteúdo. Outros padrões de controle na automação da interface do usuário da Microsoft podem ser acessados usando o método [**IUIAutomationElement:: GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern) .

Uma técnica para melhorar o desempenho é garantir que os clientes de automação da interface do usuário tentem recuperar blocos de texto de tamanho moderado usando o método [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) . Por exemplo, usar **gettext** para recuperar caracteres únicos incorrerá em ocorrências de processo cruzado para cada caractere, enquanto não especificar um comprimento máximo ao chamar **gettext** incorrerá em uma ocorrência em processo cruzado, mas poderá ter alta latência dependendo do tamanho do intervalo de texto.

## <a name="text-pattern-and-virtualized-embedded-objects"></a>Padrão de texto e objetos incorporados virtualizados

Sempre que possível, uma implementação de provedor de [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) deve dar suporte a todo o texto de um documento, incluindo qualquer texto fora do visor. Para objetos de texto fora da tela ou incorporados que são virtualizados, os provedores devem dar suporte ao [padrão de controle VirtualizedItem](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)).

Se um documento for virtualizado enquanto o fluxo de texto inteiro ainda estiver disponível, a propriedade [**ITextProvider::D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) recuperará um intervalo de texto que inclui o documento inteiro. No entanto, chamar o método [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) recuperará uma coleção de objetos virtualizados que representam todos os objetos inseridos no documento. Para interagir com um objeto inserido virtualizado, os clientes devem chamar o método [**IVirtualizedItemProvider:: perceba**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) , o que torna os itens totalmente acessíveis como elementos de automação da interface do usuário. Os clientes devem seguir um processo semelhante para trabalhar com elementos de grade em uma tabela incorporada em que uma parte da tabela está fora da tela e virtualizada.

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>Usando o tipo de controle personalizado com o padrão de controle de texto

Enquanto o padrão de controle de [texto](uiauto-implementingtextandtextrange.md) dá suporte a muitos atributos de texto e objetos incorporados, não é possível definir com antecedência todos os elementos de documento e tipos de apresentação possíveis. Para elementos de documento que não são suportados pelos atributos existentes ou tipos de controle padrão, os provedores podem usar os recursos de extensibilidade fornecidos pelo tipo de controle **personalizado** de automação da interface do usuário.

Para aplicativos e interfaces do usuário que são baseados em apresentações de página, a apresentação de limite e de layout de "Page" também pode ser expressa como um objeto incorporado que tem um tipo de controle personalizado (ou seja, `LocalizedControlType="page"` ). Dessa forma, o objeto incorporado pode hospedar outros elementos de página que não podem facilmente fazer parte do fluxo de texto do documento, como os campos de cabeçalho e rodapé de cada página, como filhos do objeto incorporado "Page". Como alternativa, cada objeto "Page" pode dar suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) de forma independente, o que funciona bem para aplicativos como ferramentas de criação para apresentações de apresentação de slides ou ambientes de publicação de área de trabalho baseados em página.

## <a name="lifetime-of-a-text-range"></a>Tempo de vida de um intervalo de texto

Se possível, um provedor deve garantir que qualquer alteração de texto, como exclusões, inserções e movimentações, seja refletida no intervalo de texto associado. Se a atualização do intervalo de texto não for possível, o provedor deverá gerar um evento [**\_ \_ TextChangedEventId de texto UIA**](uiauto-event-ids.md) para notificar os clientes de que o intervalo de texto não é mais válido e um novo deve ser recuperado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Como a automação da IU dá suporte a objetos inseridos](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Suporte à automação da interface do usuário para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Estrutura de serviços de texto](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 