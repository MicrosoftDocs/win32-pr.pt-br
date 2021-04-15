---
title: Padrões de controle Text e TextRange
description: Descreve as diretrizes e convenções para implementar ITextProvider, ITextProvider2 e ITextRangeProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- Automação da interface do usuário, implementando padrão de controle de texto
- Automação da interface do usuário, implementando o padrão de controle TextRange
- Automação da interface do usuário, padrão de controle de texto
- Automação da interface do usuário, padrão de controle TextRange
- Automação da interface do usuário, ITextProvider
- Automação da interface do usuário, ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- Implementando o padrão de controle de texto de automação da IU
- Implementando padrão de controle TextRange de automação da interface do usuário
- Padrão de controle de texto
- Padrão de controle TextRange
- padrões de controle, ITextProvider
- padrões de controle, ITextRangeProvider
- padrões de controle, implementação de texto de automação da interface do usuário
- padrões de controle, como implementar o TextRange de automação da interface do usuário
- padrões de controle, texto
- padrões de controle, TextRange
- interfaces, ITextProvider
- interfaces, ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53429dc8ec137a83b6a40db377b5c84aeb36120
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555966"
---
# <a name="text-and-textrange-control-patterns"></a>Padrões de controle Text e TextRange

Descreve as diretrizes e convenções para implementar [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider), [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)e [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider), incluindo informações sobre propriedades e métodos. O padrão de controle de **texto** permite que aplicativos e controles exponham um modelo de objeto de texto simples, permitindo que os clientes recuperem conteúdo textual, atributos de texto e objetos incorporados de controles baseados em texto.

Para dar suporte ao padrão de controle de **texto** , os controles implementam as interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) . Os tipos de controle que devem dar suporte ao padrão de controle de **texto** incluem os tipos de controle de [documento](uiauto-supportdocumentcontroltype.md) e de [edição](uiauto-supporteditcontroltype.md) e qualquer outro tipo de controle que permita que o usuário insira texto ou selecione texto somente leitura.

O padrão de controle de **texto** pode ser usado com outros padrões de controle de automação da interface do usuário da Microsoft para dar suporte a vários tipos de objetos inseridos no texto, incluindo tabelas, hiperlinks e botões de comando.

As interfaces [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) incluem vários métodos para adquirir intervalos de texto. Um *intervalo de texto* é um objeto que representa um trecho de texto contíguo, ou vários trechos de texto separados, em um contêiner de texto. Um método **ITextProvider** adquire um intervalo de texto que representa o documento inteiro, enquanto outros adquirem intervalos de texto que representam alguma parte do documento, como o texto selecionado, o texto visível ou um objeto inserido no texto.

Um objeto de intervalo de texto é representado pelo padrão de controle **TextRange** , que é implementado por meio da interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) . O padrão de controle **TextRange** fornece métodos e propriedades usados para expor informações sobre o texto no intervalo, mover os pontos de extremidade do intervalo, selecionar ou desmarcar o texto, rolar o intervalo para a exibição e assim por diante.

Para obter mais informações sobre os padrões de controle **Text** e **TextRange** , consulte [suporte à automação da interface do usuário para conteúdo textual](uiauto-ui-automation-textpattern-overview.md).

A partir do Windows 8.1 provedores podem implementar a interface [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) . Isso permite invocar menus de contexto associados a um intervalo de texto. Isso dá suporte a cenários como a correção automática de texto ou a seleção de candidatos do IME (editor de método de entrada).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ITextProvider**](#required-members-for-itextprovider)
-   [Membros necessários para **ITextRangeProvider**](#required-members-for-itextrangeprovider)
-   [Suporte a intervalos de texto](#supporting-text-ranges)
    -   [Manipulando um intervalo de texto por unidade de texto](#manipulating-a-text-range-by-text-unit)
    -   [Selecionando texto em um intervalo de texto](#selecting-text-in-a-text-range)
    -   [Adquirindo texto de um intervalo de texto](#acquiring-text-from-a-text-range)
    -   [Implementando o subcontextmenu](#implementing-showcontextmenu)
-   [Interoperabilidade com o cursor do sistema](#interoperability-with-the-system-caret)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **texto** , observe as seguintes diretrizes e convenções:

-   Qualquer controle que habilite o acesso ao texto (por exemplo, inserção de texto ou seleção de texto somente leitura) deve dar suporte ao padrão de controle de **texto** .
-   O padrão de controle de **texto** pode ser usado com qualquer elemento de interface do usuário que apresente texto, até mesmo um rótulo estático em um controle de botão padrão. No entanto, ele não é necessário em controles de texto estáticos que não podem ser selecionados ou não têm um ponto de inserção.
-   Para garantir que o texto esteja totalmente acessível, os controles que implementam [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) também devem oferecer suporte à interface [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) . O **IValueProvider** complementa o **ITextProvider** fornecendo uma maneira programática de alterar o texto. Ele também oferece maior compatibilidade com aplicativos cliente de tecnologia assistencial, incluindo aqueles baseados em tecnologias herdadas, como o Microsoft Acessibilidade Ativa. Quando ambos os padrões de controle são implementados, o evento **TextChanged** ([**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)) e o evento **AutomationPropertyChanged** ([**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md)) são equivalentes à propriedade **Value** ([**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md)). Os dois eventos devem ter suporte.
-   O padrão de controle de **texto** dá suporte a apenas um fluxo de texto e um visor por controle. Se o aplicativo oferece várias exibições de documento em painéis, cada exibição (controle) deve dar suporte a [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) de forma independente.
-   O método [**ITextProvider:: getseleções**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) pode retornar um único intervalo de texto que representa o texto atualmente selecionado. Se um controle oferecer suporte à seleção de várias extensões não contíguas de texto, o método **GetSelection** deverá retornar uma matriz que contenha uma interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) para cada intervalo selecionado de texto.
-   O padrão de controle de **texto** representa o ponto de inserção como um intervalo de texto degenerado (vazio). O método [**ITextProvider:: getseleções**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) deve retornar um intervalo de texto degenerado quando o ponto de inserção existir e nenhum texto for selecionado. Para obter mais informações, consulte [interoperabilidade com o cursor do sistema](#interoperability-with-the-system-caret).
-   O método [**ITextProvider:: GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges) pode retornar um único intervalo de texto se um intervalo de texto contíguo estiver visível no visor ou puder retornar uma matriz de intervalos de texto não contíguos que representem várias linhas de texto parcialmente visíveis.
-   O método [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) deve retornar um intervalo degenerado se o elemento filho não contiver nenhum texto. Como um objeto incorporado pode incluir texto, o método **RangeFromChild** nem sempre pode retornar um intervalo de texto degenerado. Para obter mais informações, consulte [como a automação da interface do usuário expõe objetos inseridos](uiauto-textpattern-and-embedded-objects-overview.md).
-   O método [**ITextProvider:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) executa testes de clique na área do documento usando as coordenadas de tela especificadas. O intervalo de texto resultante deve ser consistente com o ponto de inserção ou a seleção resultante do clique no local nas coordenadas da tela especificada. Por exemplo, se uma imagem residir nas coordenadas de tela especificadas, o intervalo de texto resultante deverá ser o mesmo que o intervalo de texto que o método [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) adquiriria para a imagem. Da mesma forma, se um aplicativo cliente solicitar um intervalo de texto para o local no centro do cursor do sistema (o ponto de inserção), o intervalo de texto resultante deverá ser o mesmo que o local do cursor do sistema.
-   A propriedade [**ITextProvider::D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) sempre deve fornecer um intervalo de texto que inclua todo o texto suportado pela implementação [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) correspondente.
-   O [**evento \_ \_ TextChangedEventId de texto UIA**](uiauto-event-ids.md) deve ser gerado depois que qualquer alteração de texto ocorrer, mesmo se a alteração não estiver visível no visor. Por exemplo, o provedor deve gerar o evento mesmo se o usuário colar exatamente o mesmo texto sobre o texto selecionado.
-   O [**\_ \_ TextSelectionChangedEventId de texto UIA**](uiauto-event-ids.md) deve ser gerado sempre que a seleção de texto é alterada ou sempre que o ponto de inserção (circunflexo) se move entre o texto.

Ao implementar o padrão de controle **TextRange** , observe as seguintes diretrizes e convenções:

-   Todos os métodos do padrão de controle **TextRange** devem executar operações de texto, independentemente do estado de visibilidade do texto. A visibilidade de um intervalo de texto sempre pode ser determinada consultando o atributo de texto **IsHidden** ([**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)).
-   Se possível, um provedor deve garantir que qualquer alteração de texto, como exclusões, inserções e movimentações, seja refletida nos objetos de intervalo de texto associados (instâncias da interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) ) e gere um evento de [**\_ \_ TextChangedEventId de texto UIA**](uiauto-event-ids.md) . Os clientes podem usar o evento como uma dica para confirmar as alterações editoriais feitas no texto de um controle.
-   Todos os objetos de intervalo de texto usados pelos métodos [**ITextRangeProvider:: Compare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare), [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)e [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) devem ser pares da mesma implementação de padrão de controle de **texto** .
-   Embora não seja necessário, o valor *pRetVal* recuperado pelo método [**ITextRangeProvider:: CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints) pode indicar a distância, em caracteres ([**\_ caractere TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)), entre os dois pontos de extremidade. No entanto, os aplicativos cliente não devem depender da precisão de *pRetVal* além de seu valor positivo ou negativo.
-   Os métodos [**ITextRangeProvider:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit), [**move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)e [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) exigem uma consideração cuidadosa da unidade de texto especificada. Para obter mais informações, consulte manipulando um TextRange por unidade de texto.
-   Para obter os requisitos de implementação relacionados aos métodos [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select), [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)e [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) , consulte selecionando texto em um intervalo de texto.
-   Os métodos [**ITextRangeProvider:: FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) pesquisam para frente ou para trás para uma única cadeia de texto ou atributo de texto correspondente. Eles deverão retornar **NULL** se nenhuma correspondência for encontrada.
-   O método [**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) deve retornar o endereço adquirido da função [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) ou [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) se o atributo associado variar no intervalo ou se o atributo não tiver suporte do controle de texto. A especificação do padrão de controle **TextRange** não permite adicionar novos identificadores de atributo de texto ou alterar como os atributos existentes são definidos.
-   Se possível, o método [**ITextRangeProvider:: GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) deve retornar uma matriz que contém um retângulo delimitador para cada linha de texto totalmente ou parcialmente visível em um intervalo de texto. Se isso não for possível, o provedor poderá retornar uma matriz que contém os retângulos delimitadores de apenas linhas totalmente visíveis; no entanto, isso limita a capacidade de um aplicativo cliente de descrever com precisão como o texto é apresentado na tela.
-   O método [**ITextRangeProvider:: GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) deve retornar todos os elementos filho inseridos em um intervalo de texto, mas não precisa retornar nenhum filho dos elementos filho. Por exemplo, se um intervalo de texto contiver uma tabela que tenha um número de células filho, o método **GetChildren** poderá retornar apenas o elemento TABLE e não os elementos Cell. Por motivos de desempenho ou arquitetura, um provedor pode não ser capaz de expor todos os objetos inseridos hospedados em um documento na árvore de automação. Nesse caso, o provedor deve, pelo menos, dar suporte à enumeração de objetos filho por meio do método **GetChildren** e, como uma opção, oferecer suporte ao padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) para o suporte de desvirtualização.
-   O método [**ITextRangeProvider:: GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement) normalmente retorna o provedor de texto que fornece o intervalo de texto. No entanto, se o provedor de texto oferecer suporte a objetos filho, como tabelas ou hiperlinks, o elemento delimitador poderá ser um descendente do provedor de texto. O elemento retornado por **GetEnclosingElement** deve ser o elemento mais próximo do intervalo de texto especificado. Por exemplo, se o intervalo de texto estiver em uma célula de uma tabela, **GetEnclosingElement** deverá retornar a célula que a contém, em vez do elemento table.
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
| [**8i**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | Método      | Nenhum  |
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
| [**Não**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | Método      | Nenhum  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | Método      | Nenhum  |



 

As propriedades e os métodos adicionais a seguir são necessários para implementar a interface [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) .



| Membros necessários                                                      | Tipo de membro | Observações                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | Método      | Consulte a seção "Implementando o subcontextmenu" |



 

O padrão de controle **TextRange** não tem eventos associados.

## <a name="supporting-text-ranges"></a>Suporte a intervalos de texto

Esta seção descreve como um provedor deve implementar vários métodos das interfaces [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) e [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) para dar suporte ao padrão de controle **TextRange** .

### <a name="manipulating-a-text-range-by-text-unit"></a>Manipulando um intervalo de texto por unidade de texto

A interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) fornece vários métodos para manipular e navegar em intervalos de texto em um controle baseado em texto. Os métodos [**ITextRangeProvider:: move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)e [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) movem um intervalo de texto ou um de seus pontos de extremidade pela unidade de texto especificada, como caractere, palavra, parágrafo e assim por diante. Para obter mais informações, consulte [unidades de texto de automação da interface do usuário](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

Apesar de seu nome, o método [**ITextRangeProvider:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) não expande necessariamente um intervalo de texto. Em vez disso, ele "normaliza" um intervalo de texto movendo os pontos de extremidade para que o intervalo abranja a unidade de texto especificada. O intervalo será expandido se for menor que a unidade especificada, ou reduzido se for maior que a unidade especificada. É fundamental que o método **ExpandToEnclosingUnit** sempre normalizasse os intervalos de texto de maneira consistente; caso contrário, outros aspectos da manipulação de intervalo de texto por unidade de texto seriam imprevisíveis. O diagrama a seguir mostra como o **ExpandToEnclosingUnit** normaliza um intervalo de texto movendo os pontos de extremidade do intervalo.

![diagrama mostrando posições de ponto de extremidade de intervalo de texto antes e depois de uma chamada para ExpandToEnclosingUnit](images/expandtoenclosingunit.jpg)

Se o intervalo de texto começar no início de uma unidade de texto e terminar no início de, ou antes, no próximo limite de unidade de texto, o ponto de extremidade final será movido para o próximo limite de unidade de texto (consulte 1 e 2 no diagrama anterior).

Se o intervalo de texto começar no início de uma unidade de texto e terminar em, ou após, o próximo limite de unidade, o ponto de extremidade final permanecerá ou será movido para trás para o próximo limite de unidade após o ponto de extremidade inicial (consulte 3 e 4 na ilustração anterior). Se houver mais de um limite de unidade de texto entre os pontos de extremidade inicial e final, o ponto de extremidade final será movido para trás para o próximo limite de unidade após o ponto final de partida, resultando em um intervalo de texto que é uma unidade de texto de comprimento.

Se o intervalo de texto for iniciado em um meio da unidade de texto, o ponto de extremidade inicial será movido para trás até o início da unidade de texto, e o ponto de extremidade final será movido para frente ou para trás, conforme necessário, para o próximo limite de unidade após o ponto de extremidade inicial (consulte de 5 a 8 no diagrama anterior).

Quando o método [**ITextRangeProvider:: move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) é chamado, o provedor normaliza o intervalo de texto pela unidade de texto especificada, usando a mesma lógica de normalização que o método [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) . Em seguida, o provedor move o intervalo para trás ou para frente pelo número especificado de unidades de texto. Ao mover o intervalo, o provedor deve ignorar os limites de todos os objetos inseridos no texto. (No entanto, o limite de unidade em si pode ser afetado pela existência de um objeto incorporado). O diagrama a seguir demonstra como o método **mover** move um intervalo de texto, unidade por unidade, entre objetos incorporados e limites de unidade de texto.

![diagrama mostrando como o método mover move os pontos de extremidade de intervalo entre os limites de objeto e de unidade de texto](images/move.jpg)

O método [**ITextRangeProvider:: MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit) move um dos pontos de extremidade para frente ou para trás pela unidade de texto especificada, como mostra a ilustração a seguir.

![diagrama mostrando como o moveendpointbyunit move o ponto de extremidade de um intervalo](images/moveendpointbyunit.gif)

O método [**ITextRangeProvider:: MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange) permite que um aplicativo cliente defina um ponto de extremidade de um intervalo de texto para o mesmo local que o ponto de extremidade especificado de um segundo intervalo de texto.

### <a name="selecting-text-in-a-text-range"></a>Selecionando texto em um intervalo de texto

A interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) inclui vários métodos para controlar a seleção de texto em um controle baseado em texto.

O método [**ITextRangeProvider:: SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) deve selecionar o texto que corresponde a um intervalo de texto e remover a seleção anterior, se houver, do controle de texto. Se **Select** for chamado em um intervalo de texto degenerado, o provedor deverá mover o ponto de inserção para o local do intervalo de texto sem selecionar nenhum texto.

Se um controle oferecer suporte à seleção de vários conjuntos de texto não contíguos, os métodos [**ITextRangeProvider:: AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) e [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) adicionarão intervalos de texto a e os removerão da coleção de intervalos de texto selecionados. Se o controle oferecer suporte apenas a um intervalo de texto selecionado por vez, mas a operação de seleção resultar na seleção de vários intervalos de texto não contíguos, o provedor deverá retornar um erro **E \_ INVALIDOPERATION** ou deverá estender ou truncar a seleção atual. A propriedade [**ITextProvider:: SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) deve indicar se um controle dá suporte à seleção de uma ou várias extensões de texto ou nenhuma.

Se um controle baseado em texto oferecer suporte a inserções de texto, chamar [**ITextRangeProvider:: AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) ou [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) em um intervalo de texto degenerado no controle deve mover o ponto de inserção, mas não deve selecionar nenhum texto.

### <a name="acquiring-text-from-a-text-range"></a>Adquirindo texto de um intervalo de texto

O método [**ITextRangeProvider:: gettext**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext) deve retornar o texto sem formatação de um intervalo de texto. O texto sem formatação deve incluir todos os caracteres de controle encontrados no texto de origem, como retornos de carro e a marca Unicode da esquerda para a direita (LRM). O texto sem formatação não deve incluir marcas de marcação, como HTML, que possam estar presentes no texto de origem. Além disso, todos os códigos de escape no texto de origem devem ser convertidos para os equivalentes de texto sem formatação. Por exemplo, " &nbsp; " deve ser convertido em um caractere de espaço simples.

Se um objeto inserido abranger um intervalo de texto, o texto sem formatação deverá incluir o texto interno do objeto, mas não o texto alternativo (a propriedade Name do objeto incorporado), pois ele pode estar inconsistente com o texto interno descritivo. Para obter mais informações, consulte [como a automação da interface do usuário expõe objetos inseridos](uiauto-textpattern-and-embedded-objects-overview.md).

### <a name="implementing-showcontextmenu"></a>Implementando o subcontextmenu

[**ITextRangeProvider2:: o addcontextmenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) sempre deve mostrar o menu de contexto no ponto de extremidade inicial do intervalo. Isso deve ser equivalente ao que aconteceria se o usuário pressionasse a tecla do menu de contexto ou SHIFT + F10 com o ponto de inserção no início do intervalo.

Se a exibição do menu de contexto normalmente resultar no deslocamento do ponto de inserção para um determinado local, ele deverá fazer isso para invocar [**Procontextmenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) programaticamente para o suporte de automação da interface do usuário também.

## <a name="interoperability-with-the-system-caret"></a>Interoperabilidade com o cursor do sistema

O suporte correto ao ponto de inserção é essencial para muitos aplicativos cliente, incluindo aqueles não baseados na automação da interface do usuário. No padrão de controle de **texto** , o ponto de inserção é representado por um intervalo de texto degenerado (vazio) na posição do cursor do sistema. Quando o ponto de inserção é movido, um controle deve gerar o evento **Textselectionchanged** ([**UIA \_ Text \_ TextSelectionChangedEventId**](uiauto-event-ids.md)). Alguns aplicativos cliente dependem desse evento para monitorar o local do ponto de inserção e controlar a seleção de texto.

Quando um controle contém o texto selecionado, o design atual do padrão de controle de **texto** não fornece uma maneira de associar diretamente o local do ponto de inserção a um intervalo de texto específico. O provedor deve manter o controle da seleção de texto e definir o local do ponto de inserção adequadamente. Como selecionar o texto normalmente é feito movendo o ponto de inserção enquanto mantém pressionada a tecla SHIFT ou CTRL, ou ambos, um provedor pode rastrear a seleção de texto verificando o estado dessas chaves sempre que a seleção é alterada.

Como a estrutura de acessibilidade fornece suporte interno para o cursor do sistema, mas não para um cursor personalizado, os controles baseados em texto devem usar o cursor do sistema sempre que possível. Os controles que usam um cursor personalizado podem garantir que o cursor seja acessível criando um cursor do sistema que tenha as mesmas dimensões que o cursor personalizado e posicionando o cursor do sistema no mesmo local da interface do usuário do controle como o cursor personalizado — ou seja, no ponto de inserção. Como alternativa, um controle que usa um cursor personalizado pode implementar um provedor Microsoft Acessibilidade Ativa para o [**\_ cursor OBJID**](object-identifiers.md) para fornecer informações de acessibilidade diretamente para o seu cursor personalizado.

Para obter mais informações sobre o cursor do sistema, consulte [Cursors](/windows/desktop/menurc/carets).

Para testar se o controle expõe corretamente o local do cursor do sistema, use as ferramentas [inspecionar](inspect-objects.md) e [acessar o Inspetor de eventos](accessible-event-watcher.md) .

As coordenadas de tela do centro do bitmap de cursor do sistema devem sempre corresponder ao local do ponto de inserção. Dessa forma, um cliente pode usar as coordenadas da tela de cursor em uma chamada para [**ITextProvider:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) para recuperar um intervalo de texto que representa precisamente o local do ponto de inserção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Tipo de controle de texto](uiauto-supporttextcontroltype.md)
</dt> <dt>

[Padrão de controle editor](textedit-control-pattern.md)
</dt> <dt>

[Padrão de controle textchild](textchild-control-pattern.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Suporte à automação da interface do usuário para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 