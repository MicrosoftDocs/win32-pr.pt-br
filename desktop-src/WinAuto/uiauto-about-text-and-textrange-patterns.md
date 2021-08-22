---
title: Sobre os padrões de controle Text e TextRange
description: O conteúdo textual de um controle é exposto usando o padrão de controle Texto, que representa o conteúdo de um contêiner de texto como um fluxo de texto.
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- Automação da Interface do Usuário, suporte a conteúdo textual
- Automação da Interface do Usuário, visão geral do padrão de texto
- Automação da Interface do Usuário,visão geral dos controles de texto
- Automação da Interface do Usuário,Padrão de controle de texto
- Automação da Interface do Usuário,Estrutura de Serviços de Texto (TSF)
- Automação da Interface do Usuário,TSF
- Automação da Interface do Usuário, desempenho
- padrões de texto, sobre
- padrões de texto, Estrutura de Serviços de Texto (TSF)
- controles de texto, sobre
- conteúdo textual, suporte para
- controles de texto, desempenho
- Padrão de controle de texto
- padrões de controle, Texto
- TFS (Estrutura de Serviços de Texto)
- TSF (Estrutura de Serviços de Texto)
- desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04112e0233db056c5ff3e81b68256229aa45f60cfdb1258e565e10aea1cd43ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052354"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>Sobre os padrões de controle Text e TextRange

O conteúdo textual de um controle é exposto usando o padrão [de](uiauto-implementingtextandtextrange.md) controle Texto, que representa o conteúdo de um contêiner de texto como um fluxo de texto. O padrão de controle Text requer o suporte do padrão de controle TextRange para expor atributos de formato e estilo. O padrão de controle TextRange dá suporte ao padrão de controle Text representando intervalos de texto contíguos ou múltiplos e não contíguos (ou intervalos) em um contêiner de texto com uma coleção de pontos de extremidade e de início. O padrão de controle TextRange dá suporte a funcionalidades como seleção, comparação, recuperação e travessia.

> [!Note]  
> O [padrão de](uiauto-implementingtextandtextrange.md) controle Texto não fornece um meio de inserir ou modificar texto. No entanto, dependendo do controle, isso pode ser feito usando o padrão de controle Microsoft Automação da Interface do Usuário [Value](uiauto-implementingvalue.md) ou por meio da entrada direta do teclado. Também há um padrão [**TextEdit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) que dá suporte à alteração programática em texto.

 

A funcionalidade descrita neste tópico é vital para fornecedores de tecnologia adaptativa e seus usuários finais. As tecnologias adaptativas podem usar Automação da Interface do Usuário para coletar informações completas de formatação de texto para o usuário e fornecer navegação programática e seleção de texto por [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (caractere, palavra, linha ou parágrafo).

Este tópico contém as seguintes seções:

-   [Automação da Interface do Usuário TextPattern e o Estrutura de Serviços de Texto](#ui-automation-textpattern-and-the-text-services-framework)
-   [Tipos de controle](#control-types)
-   [Interfaces do provedor](#provider-interfaces)
-   [Interfaces do cliente](#client-interfaces)
-   [Desempenho](#performance)
-   [Padrão de texto e objetos inseridos virtualizados](#text-pattern-and-virtualized-embedded-objects)
-   [Usando o tipo de controle personalizado com o padrão de controle de texto](#using-the-custom-control-type-with-the-text-control-pattern)
-   [Tempo de vida de um intervalo de texto](#lifetime-of-a-text-range)
-   [Tópicos relacionados](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>Automação da Interface do Usuário TextPattern e o Estrutura de Serviços de Texto

Estrutura de Serviços de Texto (TSF) é uma estrutura de sistema simples e escalonável que permite serviços de linguagem natural e entrada de texto avançada na área de trabalho e em aplicativos. Além de fornecer interfaces para aplicativos exporem seu armazenamento de texto, ele também dá suporte a metadados para o armazenamento de texto.

O TSF foi projetado para aplicativos que precisam injetar entrada em cenários com contexto. O [padrão de](uiauto-implementingtextandtextrange.md) controle De texto, no entanto, é uma solução somente leitura que se destina a fornecer acesso otimizado a um armazenamento de texto para leitores de tela e dispositivos Decle.

Tecnologias acessíveis que exigem acesso somente leitura a um armazenamento de texto podem usar o padrão de controle de texto, mas precisarão da funcionalidade do TSF para entrada com reconhecimento de contexto.

Para obter mais informações, [consulte Estrutura de Serviços de Texto](/windows/desktop/TSF/text-services-framework).

## <a name="control-types"></a>Tipos de controle

O Automação da Interface do Usuário [tipo de controle Editar](uiauto-supporteditcontroltype.md) e o [tipo](uiauto-supportdocumentcontroltype.md) de controle Documento devem dar suporte ao padrão [de controle](uiauto-implementingtextandtextrange.md) Texto. Para acessibilidade aprimorada, a Microsoft recomenda que os tipos de controle [ToolTip](uiauto-supporttooltipcontroltype.md) e Text também deem suporte ao padrão de controle Texto, mas isso não é necessário.

## <a name="provider-interfaces"></a>Interfaces do provedor

Automação da Interface do Usuário provedores de [](uiauto-implementingtextandtextrange.md) texto suportam o padrão de controle text para um controle implementando as interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextRangeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) Essas interfaces expõem informações detalhadas de atributo para texto no controle e fornecem funcionalidades de navegação robustas.

Um provedor não precisará dar suporte a todos os atributos de texto se o controle não tiver suporte para nenhum atributo específico.

Um provedor deve dar suporte aos métodos [**ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) e [**ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) se o controle dá suporte à seleção de texto ou posicionamento do cursor de texto (ou cursor do sistema) na área de texto. Se o controle não dá suporte a essa funcionalidade, ele não precisa dar suporte a nenhum desses métodos. No entanto, o controle deve expor o tipo de seleção de texto compatível implementando a propriedade [**ITextProvider::SupportedTextSelection.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)

Um provedor sempre deve dar suporte às constantes [**TextUnit,**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) Caractere **TextUnit \_** e **Documento TextUnit, \_** bem como quaisquer outras que ele seja capaz de dar suporte.

> [!Note]  
> O provedor pode ignorar o suporte para um [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) específico, adiando para a próxima maior unidade com suporte na seguinte ordem: Caractere **TextUnit, \_** **Formato TextUnit, \_** **TextUnit \_ Word,** **Linha TextUnit, \_** Parágrafo **\_ TextUnit,** **Página TextUnit \_** e **Documento TextUnit \_**.

 

## <a name="client-interfaces"></a>Interfaces do cliente

Automação da Interface do Usuário aplicativos cliente usam as interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) para acessar o conteúdo textual de um controle de texto. Os clientes **usam IUIAutomationTextPattern** para selecionar intervalos de texto chamados *intervalos* de texto e para recuperar ponteiros para interfaces **IUIAutomationTextRange** para os intervalos. A interface **IUIAutomationTextRange** permite que os clientes manipulem o intervalo de texto e recuperem informações sobre o texto no intervalo, incluindo atributos como nome da fonte, cor de primeiro plano, estilo sublinhado e assim por diante. Para obter mais informações, consulte [Identificadores de atributo de texto.](uiauto-textattribute-ids.md)

## <a name="performance"></a>Desempenho

O **padrão de** controle De texto depende de chamadas entre processos para a maioria de sua funcionalidade, portanto, ele não fornece um mecanismo de cache para melhorar o desempenho quando processa o conteúdo. Outros padrões de controle no Microsoft Automação da Interface do Usuário podem ser acessados usando o [**método IUIAutomationElement::GetCachedPattern.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)

Uma técnica para melhorar o desempenho é garantir que Automação da Interface do Usuário clientes tentam recuperar blocos de texto de tamanho moderado usando o [**método IUIAutomationTextRange::GetText.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) Por exemplo, o uso de **GetText** para recuperar caracteres individuais incorre em acertos entre processos para cada caractere, enquanto não especificar um comprimento máximo ao chamar **GetText** incorre em um acerto entre processos, mas pode ter alta latência dependendo do tamanho do intervalo de texto.

## <a name="text-pattern-and-virtualized-embedded-objects"></a>Padrão de texto e objetos inseridos virtualizados

Sempre que possível, uma implementação de provedor [**de ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) deve dar suporte a todo o texto de um documento, incluindo qualquer texto fora do viewport. Para texto fora da tela ou objetos inseridos que são virtualizados, os provedores devem dar suporte ao padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)).

Se um documento for virtualizado enquanto todo o fluxo de texto ainda estiver disponível, a propriedade [**ITextProvider::D ocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) recuperará um intervalo de texto que inclui todo o documento. No entanto, chamar [**o método ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) recuperará uma coleção de objetos virtualizados que representam todos os objetos inseridos no documento. Para interagir com um objeto inserido virtualizado, os clientes devem chamar o método [**IVirtualizedItemProvider::Realize,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) que torna os itens totalmente acessíveis como Automação da Interface do Usuário elementos. Os clientes devem seguir um processo semelhante para trabalhar com elementos de grade em uma tabela inserida em que uma parte da tabela está fora da tela e virtualizada.

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>Usando o tipo de controle personalizado com o padrão de controle de texto

Embora o [padrão de](uiauto-implementingtextandtextrange.md) controle De texto seja compatível com muitos atributos de texto e objetos inseridos, não é possível definir com antecedência todos os possíveis elementos de documento e tipos de apresentação. Para elementos de documento que não são suportados pelos atributos existentes ou tipos de controle padrão, os provedores podem usar os recursos de extensibilidade fornecidos pelo tipo de controle Automação da Interface do Usuário Personalizado. 

Para aplicativos e interfaces do usuário baseadas em apresentações de página, o limite e a apresentação de layout de "page" também podem ser expressos como um objeto inserido que tem um tipo de controle personalizado (ou seja, `LocalizedControlType="page"` ). Dessa forma, o objeto inserido pode hospedar outros elementos de página que não podem fazer parte facilmente do fluxo de texto do documento, como os campos de rodapé e de rodapé de cada página, como filhos do objeto inserido de "página". Como alternativa, cada objeto de [](uiauto-implementingtextandtextrange.md) "página" pode dar suporte ao padrão de controle de texto de forma independente, o que funciona bem para aplicativos como ferramentas de autor para apresentações de apresentação de slides ou ambientes de publicação de área de trabalho baseados em página.

## <a name="lifetime-of-a-text-range"></a>Tempo de vida de um intervalo de texto

Se possível, um provedor deve garantir que todas as alterações de texto, como exclusões, inserções e movimentações, sejam refletidas no intervalo de texto associado. Se a atualização do intervalo de texto não for possível, o provedor deverá agarr um evento [**\_ \_ TextChangedEventId**](uiauto-event-ids.md) da UIA para notificar os clientes de que o intervalo de texto não é mais válido e um novo deve ser recuperado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Como Automação da Interface do Usuário dá suporte a objetos inseridos](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Automação da Interface do Usuário suporte para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Estrutura de Serviços de Texto](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 