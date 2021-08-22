---
title: Padrões de controle Text e TextRange
description: Descreve diretrizes e convenções para implementar ITextProvider, ITextProvider2 e ITextRangeProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle de texto
- Automação da Interface do Usuário, implementando o padrão de controle TextRange
- Automação da Interface do Usuário,Padrão de controle de texto
- Automação da Interface do Usuário, padrão de controle TextRange
- Automação da Interface do Usuário,ITextProvider
- Automação da Interface do Usuário,ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- implementando um Automação da Interface do Usuário de controle de texto
- implementando Automação da Interface do Usuário de controle TextRange
- Padrão de controle de texto
- Padrão de controle TextRange
- padrões de controle, ITextProvider
- padrões de controle, ITextRangeProvider
- padrões de controle, implementando Automação da Interface do Usuário Text
- padrões de controle, implementando Automação da Interface do Usuário TextRange
- padrões de controle, Texto
- padrões de controle, TextRange
- interfaces, ITextProvider
- interfaces, ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99baf1af267e67ffe3f75a83fb970c991e9ebe5674497db2a2edad8d9cc328b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826977"
---
# <a name="text-and-textrange-control-patterns"></a>Padrões de controle Text e TextRange

Descreve diretrizes e convenções para implementar [**ITextProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider), incluindo informações sobre propriedades e métodos. O **padrão controle** Texto permite que aplicativos e controles exponham um modelo de objeto de texto simples, permitindo que os clientes recuperem conteúdo textual, atributos de texto e objetos inseridos de controles baseados em texto.

Para dar suporte ao **padrão de** controle Texto, os controles implementam as interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextProvider2.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) Os tipos de controle que devem [](uiauto-supporteditcontroltype.md) dar [](uiauto-supportdocumentcontroltype.md) suporte ao padrão de controle Texto incluem os tipos de controle Editar e Documento e qualquer outro tipo de controle que permita ao usuário inserir texto ou selecionar texto somente leitura. 

O **padrão de** controle De texto pode ser usado com outros padrões de controle do Microsoft Automação da Interface do Usuário para dar suporte a vários tipos de objetos inseridos no texto, incluindo tabelas, hiperlinks e botões de comando.

As interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) incluem vários métodos para adquirir intervalos de texto. Um *intervalo de* texto é um objeto que representa um intervalo contíguo de texto ( ou vários intervalos de texto não contíguos ) em um contêiner de texto. Um **método ITextProvider** adquire um intervalo de texto que representa todo o documento, enquanto outros adquirem intervalos de texto que representam alguma parte do documento, como o texto selecionado, o texto visível ou um objeto inserido no texto.

Um objeto de intervalo de texto é representado pelo padrão de **controle TextRange,** que é implementado por meio da interface [**ITextRangeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) O padrão de controle **TextRange** fornece métodos e propriedades usados para expor informações sobre o texto no intervalo, mover os pontos de extremidade do intervalo, selecionar ou desmarcar texto, rolar o intervalo para a exibição e assim por diante.

Para obter mais informações sobre os **padrões de** controle **Text e TextRange,** consulte Suporte Automação da Interface do Usuário para conteúdo [textual.](uiauto-ui-automation-textpattern-overview.md)

Começando com Windows 8.1 provedores podem implementar a interface [**ITextRangeProvider2.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) Isso permite invocar menus de contexto associados a um intervalo de texto. Isso dá suporte a cenários como a correção automática de texto ou a seleção de candidato do IME (Editor de Método de Entrada).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ITextProvider**](#required-members-for-itextprovider)
-   [Membros necessários para **ITextRangeProvider**](#required-members-for-itextrangeprovider)
-   [Suporte a intervalos de texto](#supporting-text-ranges)
    -   [Manipulando um intervalo de texto por unidade de texto](#manipulating-a-text-range-by-text-unit)
    -   [Selecionando texto em um intervalo de texto](#selecting-text-in-a-text-range)
    -   [Adquirindo texto de um intervalo de texto](#acquiring-text-from-a-text-range)
    -   [Implementando ShowContextMenu](#implementing-showcontextmenu)
-   [Interoperabilidade com o Sistema Desalocar](#interoperability-with-the-system-caret)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle** De texto, observe as seguintes diretrizes e convenções:

-   Qualquer controle que habilita o acesso ao texto (por exemplo, inserir texto ou selecionar texto somente leitura) deve dar suporte ao padrão **de Controle** de texto.
-   O **padrão de** controle Texto pode ser usado com qualquer elemento de interface do usuário que apresente texto, até mesmo um rótulo estático em um controle de botão padrão. No entanto, não é necessário em controles de texto estáticos que não podem ser selecionados ou não têm um ponto de inserção.
-   Para garantir que o texto seja totalmente acessível, os controles que implementam [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) também devem dar suporte à interface [**IValueProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) **IValueProvider** complementa **ITextProvider** fornecendo uma maneira programática de alterar o texto. Ele também oferece maior compatibilidade com aplicativos cliente de tecnologia adaptativa, incluindo aqueles baseados em tecnologias herdada, como Microsoft Active Accessibility. Quando ambos os padrões de controle são implementados, o evento **TextChanged** ([**UIA \_ \_ TextChangedEventId**](uiauto-event-ids.md)) e **o evento AutomationPropertyChanged** ([**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md)) são equivalentes para a propriedade **Value** ([**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md)). Ambos os eventos devem ter suporte.
-   O **padrão de** controle Texto dá suporte a apenas um fluxo de texto e um viewport por controle. Se o aplicativo oferecer várias exibições de documento em painéis, cada exibição (controle) deverá dar suporte a [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) independentemente.
-   O [**método ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) pode retornar um único intervalo de texto que representa o texto selecionado no momento. Se um controle for compatível com a seleção de vários intervalos não contíguos de texto, o método **GetSelection** deverá retornar uma matriz que contenha uma interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) para cada intervalo de texto selecionado.
-   O **padrão de** controle Texto representa o ponto de inserção como um intervalo de texto degenere (vazio). O [**método ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) deve retornar um intervalo de texto degeneração quando o ponto de inserção existir e nenhum texto for selecionado. Para obter mais informações, [consulte Interoperabilidade com o System Caret](#interoperability-with-the-system-caret).
-   O método [**ITextProvider::GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges) poderá retornar um único intervalo de texto se um intervalo contíguo de texto estiver visível no viewport ou retornar uma matriz de intervalos de texto não contíguos que representam várias linhas parcialmente visíveis de texto.
-   O [**método ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) deverá retornar um intervalo degeneres se o elemento filho não contiver texto. Como um objeto inserido pode incluir texto, o **método RangeFromChild** nem sempre pode retornar um intervalo de texto degenerado. Para obter mais informações, [consulte Como Automação da Interface do Usuário expõe objetos inseridos.](uiauto-textpattern-and-embedded-objects-overview.md)
-   O [**método ITextProvider::RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) executa testes de acerto na área do documento usando as coordenadas de tela especificadas. O intervalo de texto resultante deve ser consistente com o ponto de inserção ou a seleção resultante do clique no local nas coordenadas de tela especificadas. Por exemplo, se uma imagem residir nas coordenadas de tela especificadas, o intervalo de texto resultante deverá ser o mesmo que o intervalo de texto que o método [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) adquiriria para a imagem. Da mesma forma, se um aplicativo cliente solicitar um intervalo de texto para o local no centro do sistema (o ponto de inserção), o intervalo de texto resultante deverá ser o mesmo que o local de aplicação do sistema.
-   A [**propriedade ITextProvider::D ocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) sempre deve fornecer um intervalo de texto que inclua todo o texto com suporte pela implementação [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) correspondente.
-   O [**evento \_ \_ TextChangedEventId**](uiauto-event-ids.md) da UIA deve ser gerado após qualquer alteração de texto ocorrer, mesmo que a alteração não seja visível no viewport. Por exemplo, o provedor deve acionou o evento mesmo se o usuário colar exatamente o mesmo texto sobre o texto selecionado.
-   A [**\_ \_ TextSelectionChangedEventId**](uiauto-event-ids.md) da UIA deve ser acionada sempre que a seleção de texto mudar ou sempre que o ponto de inserção (adição) se mover entre o texto.

Ao implementar o padrão **de controle TextRange,** observe as seguintes diretrizes e convenções:

-   Todos os métodos do padrão de **controle TextRange** devem executar operações de texto, independentemente do estado de visibilidade do texto. A visibilidade de um intervalo de texto sempre pode ser determinada consultando o atributo de texto **IsHidden** ([**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)).
-   Se possível, um provedor deve garantir que todas as alterações de texto, como exclusões, inserções e movimentações, sejam refletidas nos objetos de intervalo de texto associados (instâncias da interface [**ITextRangeProvider)**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) e aumente um evento [**\_ \_ TextChangedEventId da UIA.**](uiauto-event-ids.md) Os clientes podem usar o evento como uma dica para confirmar alterações editoriais feitas no texto de um controle.
-   Todos os objetos de intervalo de texto usados pelos métodos [**ITextRangeProvider::Compare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare), [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)e  [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) devem ser pares da mesma implementação de padrão de controle de texto.
-   Embora não seja necessário, o valor *pRetVal* recuperado pelo método [**ITextRangeProvider::CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints) pode indicar a distância, em caracteres ([**Caractere TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)), entre os dois pontos de extremidade. No entanto, os aplicativos cliente não devem depender da precisão de *pRetVal além* de seu valor positivo ou negativo.
-   Os [**métodos ITextRangeProvider::ExpandToEnclosingUnit,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)e [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) exigem uma consideração cuidadosa da unidade de texto especificada. Para obter mais informações, consulte Manipulando um TextRange por unidade de texto.
-   Para requisitos de implementação relacionados aos métodos [**ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select), [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)e [**RemoveFromSelection,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) consulte Selecionando texto em um intervalo de texto.
-   Os [**métodos ITextRangeProvider::FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) pesquisam para frente ou para trás uma única cadeia de caracteres de texto ou atributo de texto correspondente. Eles deverão retornar **NULL** se nenhuma corresponder for encontrada.
-   O método [**ITextRangeProvider::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) deve retornar o endereço adquirido da função [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) ou [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) se o atributo associado variar no intervalo ou se o atributo não tiver suporte no controle de texto. A **especificação do padrão** de controle TextRange não permite adicionar novos identificadores de atributo de texto nem alterar como os atributos existentes são definidos.
-   Se possível, o método [**ITextRangeProvider::GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) deverá retornar uma matriz que contenha um retângulo delimitador para cada linha de texto totalmente ou parcialmente visível em um intervalo de texto. Se isso não for possível, o provedor poderá retornar uma matriz que contém os retângulos delimitadores de apenas linhas totalmente visíveis; no entanto, isso limita a capacidade de um aplicativo cliente de descrever com precisão como o texto está sendo apresentado na tela.
-   O [**método ITextRangeProvider::GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) deve retornar todos os elementos filho inseridos em um intervalo de texto, mas não precisa retornar nenhum filho dos elementos filho. Por exemplo, se um intervalo de texto contiver uma tabela com várias células filho, o **método GetChildren** poderá retornar apenas o elemento table e não os elementos de célula. Por motivos de desempenho ou arquitetura, um provedor pode não conseguir expor todos os objetos inseridos hospedados em um documento na árvore de automação. Nesse caso, o provedor deve, pelo menos, dar suporte à enumeração de objetos filho por meio do método **GetChildren** e, como uma opção, dar suporte ao padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) para suporte à des virtualização.
-   O [**método ITextRangeProvider::GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement) normalmente retorna o provedor de texto que fornece o intervalo de texto. No entanto, se o provedor de texto for compatível com objetos filho, como tabelas ou hiperlinks, o elemento delimitador poderá ser um descendente do provedor de texto. O elemento retornado por **GetEnclosingElement** deve ser o elemento mais próximo do intervalo de texto especificado. Por exemplo, se o intervalo de texto estiver em uma célula de uma tabela, **GetEnclosingElement** deverá retornar a célula que a contém, em vez do elemento table.
-   O método [**ITextRangeProvider:: gettext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) deve retornar o texto sem formatação no intervalo. Para obter mais informações, consulte adquirindo texto de um intervalo de texto.
-   Chamar [**ITextRangeProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview) deve alinhar o texto no visor do controle de texto conforme especificado pelo parâmetro *alignToTop* . Embora não haja nenhum requisito em termos de alinhamento horizontal, o intervalo de texto deve ser visível tanto horizontal como verticalmente. Ao avaliar o parâmetro *alignToTop* , um provedor deve levar em consideração a orientação do controle de texto e a direção do fluxo do texto. Por exemplo, se *alignToTop* for **true** para um controle de texto orientado verticalmente contendo texto que flua da direita para a esquerda, o provedor deverá alinhar o intervalo de texto com o lado direito do visor.
-   Ao mover um documento por [**\_ linha TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), se o intervalo de texto entrar em uma tabela inserida, cada linha de texto em uma célula deverá ser tratada como uma linha.

## <a name="required-members-for-itextprovider"></a>Membros necessários para **ITextProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) .



| Membros necessários                                                                                        | Tipo de membro | Observações |
|---------------------------------------------------------------------------------------------------------|-------------|-------|
| [**DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)                                             | Propriedade    | Nenhum  |
| [**SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)                           | Propriedade    | Nenhum  |
| [**Getseleções**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)                                               | Método      | Nenhum  |
| [**GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)                                       | Método      | Nenhum  |
| [**RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)                                           | Método      | Nenhum  |
| [**RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)                                           | Método      | Nenhum  |
| [**\_TextChangedEventId de texto UIA \_**](uiauto-event-ids.md)                   | Evento       | Nenhum  |
| [**\_TextSelectionChangedEventId de texto UIA \_**](uiauto-event-ids.md) | Evento       | Nenhum  |



 

As propriedades e os métodos adicionais a seguir são necessários para implementar a interface [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) .



| Membros necessários                                                         | Tipo de membro | Observações |
|--------------------------------------------------------------------------|-------------|-------|
| [**GetCaretRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)         | Método      | Nenhum  |
| [**RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) | Método      | Nenhum  |



 

## <a name="required-members-for-itextrangeprovider"></a>Membros necessários para **ITextRangeProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) .



| Membros necessários                                                                 | Tipo de membro | Observações |
|----------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)               | Método      | Nenhum  |
| [**Clone**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | Método      | Nenhum  |
| [**Comparar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)                             | Método      | Nenhum  |
| [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)           | Método      | Nenhum  |
| [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) | Método      | Nenhum  |
| [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)                 | Método      | Nenhum  |
| [**FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)                           | Método      | Nenhum  |
| [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)         | Método      | Nenhum  |
| [**GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) | Método      | Nenhum  |
| [**GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)                     | Método      | Nenhum  |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)     | Método      | Nenhum  |
| [**GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)                             | Método      | Nenhum  |
| [**Mover**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)                                   | Método      | Nenhum  |
| [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)       | Método      | Nenhum  |
| [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)     | Método      | Nenhum  |
| [**Selecionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | Método      | Nenhum  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | Método      | Nenhum  |



 

As seguintes propriedades e métodos adicionais são necessários para implementar a interface [**ITextRangeProvider2.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2)



| Membros necessários                                                      | Tipo de membro | Observações                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | Método      | Consulte a seção "Implementando ShowContextMenu" |



 

O **padrão de controle TextRange** não tem eventos associados.

## <a name="supporting-text-ranges"></a>Suporte a intervalos de texto

Esta seção descreve como um provedor deve implementar vários métodos das interfaces [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) e [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) para dar suporte ao padrão de controle **TextRange.**

### <a name="manipulating-a-text-range-by-text-unit"></a>Manipulando um intervalo de texto por unidade de texto

A interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) fornece vários métodos para manipular e navegar por intervalos de texto em um controle baseado em texto. Os métodos [**ITextRangeProvider::Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)e [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) movem um intervalo de texto ou um de seus pontos de extremidade pela unidade de texto especificada, como caractere, palavra, parágrafo e assim por diante. Para obter mais informações, consulte [Automação da Interface do Usuário unidades de texto](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

Apesar do nome, o [**método ITextRangeProvider::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) não necessariamente expande um intervalo de texto. Em vez disso, ele "normaliza" um intervalo de texto movendo os pontos de extremidade para que o intervalo abarque a unidade de texto especificada. O intervalo será expandido se for menor que a unidade especificada ou reduzido se for maior que a unidade especificada. É essencial que o **método ExpandToEnclosingUnit** sempre normalize intervalos de texto de maneira consistente; caso contrário, outros aspectos da manipulação de intervalo de texto por unidade de texto seriam imprevisíveis. O diagrama a seguir mostra **como ExpandToEnclosingUnit** normaliza um intervalo de texto movendo os pontos de extremidade do intervalo.

![diagrama mostrando as posições do ponto de extremidade do intervalo de texto antes e depois de uma chamada para expandtoenclosingunit](images/expandtoenclosingunit.jpg)

Se o intervalo de texto começar no início de uma unidade de texto e terminar no início ou antes do próximo limite de unidade de texto, o ponto de extremidade final será movido para o próximo limite de unidade de texto (consulte 1 e 2 no diagrama anterior).

Se o intervalo de texto começar no início de uma unidade de texto e terminar no próximo limite de unidade, o ponto de extremidade final permanecerá ou será movido para trás para o próximo limite de unidade após o ponto de extremidade inicial (consulte 3 e 4 na ilustração anterior). Se houver mais de um limite de unidade de texto entre os pontos de extremidade inicial e final, o ponto de extremidade final será movido para trás para o próximo limite de unidade após o ponto de extremidade inicial, resultando em um intervalo de texto que tem uma unidade de texto de comprimento.

Se o intervalo de texto for iniciado em um meio da unidade de texto, o ponto de extremidade inicial será movido para trás para o início da unidade de texto e o ponto de extremidade final será movido para frente ou para trás, conforme necessário, para o próximo limite de unidade após o ponto de extremidade inicial (consulte 5 a 8 no diagrama anterior).

Quando o método [**ITextRangeProvider::Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) é chamado, o provedor normaliza o intervalo de texto pela unidade de texto especificada, usando a mesma lógica de normalização que o [**método ExpandToEnclosingUnit.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) Em seguida, o provedor move o intervalo para trás ou para frente pelo número especificado de unidades de texto. Ao mover o intervalo, o provedor deve ignorar os limites de quaisquer objetos inseridos no texto. (No entanto, o limite de unidade em si pode ser afetado pela existência de um objeto inserido). O diagrama a seguir demonstra como o **método Move** move um intervalo de texto, unidade por unidade, entre objetos inseridos e limites de unidade de texto.

![diagrama mostrando como o método de movimentação move os pontos de extremidade de intervalo entre limites de objeto e unidade de texto](images/move.jpg)

O [**método ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) move um dos pontos de extremidade para frente ou para trás pela unidade de texto especificada, como mostra a ilustração a seguir.

![diagrama mostrando como moveendpointbyunit move o ponto de extremidade de um intervalo](images/moveendpointbyunit.gif)

O [**método ITextRangeProvider::MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) permite que um aplicativo cliente defina um ponto de extremidade de um intervalo de texto para o mesmo local que o ponto de extremidade especificado de um segundo intervalo de texto.

### <a name="selecting-text-in-a-text-range"></a>Selecionando texto em um intervalo de texto

A interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) inclui vários métodos para controlar a seleção de texto em um controle baseado em texto.

O [**método ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) deve selecionar o texto que corresponde a um intervalo de texto e remover a seleção anterior, se for o caso, do controle de texto. Se **Select** for chamado em um intervalo de texto degenere, o provedor deverá mover o ponto de inserção para o local do intervalo de texto sem selecionar nenhum texto.

Se um controle dá suporte à seleção de vários intervalos de texto diferentes, os métodos [**ITextRangeProvider::AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) e [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) adicionam intervalos de texto e os removem da coleção de intervalos de texto selecionados. Se o controle dá suporte apenas a um intervalo de texto selecionado por vez, mas a operação de seleção resultaria na seleção de vários intervalos de texto não adjacentes, o provedor deve retornar um erro **E \_ INVALIDOPERATION** ou deve estender ou truncar a seleção atual. A [**propriedade ITextProvider::SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) deve indicar se um controle dá suporte à seleção de um ou vários intervalos de texto ou nenhum.

Se um controle baseado em texto for compatível com inserções de texto, chamar [**ITextRangeProvider::AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) ou [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) em um intervalo de texto cada vez maior no controle deverá mover o ponto de inserção, mas não deve selecionar nenhum texto.

### <a name="acquiring-text-from-a-text-range"></a>Adquirindo texto de um intervalo de texto

O [**método ITextRangeProvider::GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) deve retornar o texto sem formatar de um intervalo de texto. O texto sem-texto deve incluir todos os caracteres de controle encontrados no texto de origem, como retornos de carro e a marca unicode da esquerda para a direita (LRM). O texto sem formatação não deve incluir marcas de marcação como HTML que possam estar presentes no texto de origem. Além disso, todos os códigos de escape no texto de origem devem ser convertidos em equivalentes de texto sem-texto. Por exemplo, " &nbsp; " deve ser convertido em um caractere de espaço simples.

Se um objeto inserido abranger um intervalo de texto, o texto sem-texto deverá incluir o texto interno do objeto, mas não o texto alternativo (a propriedade name do objeto inserido) porque ele pode ser inconsistente com o texto interno descritivo. Para obter mais informações, [consulte Como Automação da Interface do Usuário expõe objetos inseridos.](uiauto-textpattern-and-embedded-objects-overview.md)

### <a name="implementing-showcontextmenu"></a>Implementando ShowContextMenu

[**ITextRangeProvider2::ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) sempre deve mostrar o menu de contexto no ponto de extremidade inicial do intervalo. Isso deve ser equivalente ao que aconteceria se o usuário pressionasse a tecla de menu de contexto ou SHIFT + F10 com o ponto de inserção no início do intervalo.

Se mostrar o menu de contexto normalmente resultaria na movimentação do ponto de inserção para um determinado local, ele deverá fazer isso para invocar programaticamente [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) para Automação da Interface do Usuário suporte também.

## <a name="interoperability-with-the-system-caret"></a>Interoperabilidade com o Sistema Desalocar

O suporte correto ao ponto de inserção é essencial para muitos aplicativos cliente, incluindo aqueles não baseados em Automação da Interface do Usuário. No padrão **de controle** De texto, o ponto de inserção é representado por um intervalo de texto degenerado (vazio) na posição do atromento do sistema. Quando o ponto de inserção é  movimentado, um controle deve acioná-lo ([**Texto \_ \_ UIA TextSelectionChangedEventId**](uiauto-event-ids.md)). Alguns aplicativos cliente dependem desse evento para monitorar o local do ponto de inserção e manter o controle da seleção de texto.

Quando um controle contém o texto  selecionado, o design atual do padrão de controle De texto não fornece uma maneira de associar diretamente o local do ponto de inserção a um intervalo de texto específico. O provedor deve manter o controle da seleção de texto e definir o local do ponto de inserção adequadamente. Como a seleção de texto normalmente é feita movendo o ponto de inserção enquanto mantém a tecla SHIFT ou CTRL, ou ambos, um provedor pode acompanhar a seleção de texto verificando o estado dessas chaves sempre que a seleção é muda.

Como a estrutura de acessibilidade fornece suporte integrado para o aparador do sistema, mas não para um aparador personalizado, os controles baseados em texto devem usar o aparador do sistema sempre que possível. Os controles que usam um a caret personalizado podem garantir que o a carete seja acessível criando um a careta do sistema que tenha as mesmas dimensões que o a caret personalizado e posicionando o caret do sistema no mesmo local na interface do usuário do controle que o a careta personalizado, ou seja, no ponto de inserção. Como alternativa, um controle que usa um caret personalizado pode implementar um provedor de Microsoft Active Accessibility para [**OBJID \_ CARET**](object-identifiers.md) a fim de fornecer informações de acessibilidade diretamente para o seu a caret personalizado.

Para obter mais informações sobre o caret do sistema, consulte [Carets](/windows/desktop/menurc/carets).

Para testar se o controle expõe corretamente a localização do a carete do sistema, use as ferramentas [Inspecionar](inspect-objects.md) e Acessível [Do Inspecionador de](accessible-event-watcher.md) Eventos.

As coordenadas de tela do centro do bitmap do sistema devem sempre corresponder ao local do ponto de inserção. Dessa forma, um cliente pode usar as coordenadas da tela de afiação em uma chamada para [**ITextProvider::RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) para recuperar um intervalo de texto que representa com precisão o local do ponto de inserção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Tipo de controle de texto](uiauto-supporttextcontroltype.md)
</dt> <dt>

[Padrão de controle TextEdit](textedit-control-pattern.md)
</dt> <dt>

[Padrão de controle TextChild](textchild-control-pattern.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Automação da Interface do Usuário suporte para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 