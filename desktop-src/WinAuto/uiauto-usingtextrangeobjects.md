---
title: Usando intervalos de texto
description: Este tópico descreve como usar as propriedades e os métodos da interface IUIAutomationTextRange para acessar e manipular o conteúdo textual de um controle baseado em texto.
ms.assetid: 66BC7324-5322-4996-AF62-766936559F0E
keywords:
- clientes, usando objetos de intervalo de texto
- controles baseados em texto
- clientes, intervalos de texto
- clientes, padrão de controle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c409f39d437135854463e83c361a9afd22204758c360119bd0033e4fd11416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563972"
---
# <a name="using-text-ranges"></a>Usando intervalos de texto

Este tópico descreve como usar as propriedades e os métodos da interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) para acessar e manipular o conteúdo textual de um controle baseado em texto. Ele contém as seções a seguir:

-   [O que é um intervalo de texto?](#using-text-ranges)
-   [Adquirindo objetos de intervalo de texto](#acquiring-text-range-objects)
-   [Selecionando texto em um intervalo de texto](#selecting-text-in-a-text-range)
-   [Recuperando texto de um intervalo de texto](#retrieving-text-from-a-text-range)
-   [Recuperando atributos de texto de um intervalo de texto](#retrieving-text-attributes-from-a-text-range)
-   [Recuperando objetos inseridos de um intervalo de texto](#retrieving-embedded-objects-from-a-text-range)
-   [Manipulando um intervalo de texto](#manipulating-a-text-range)
-   [Rolando um intervalo de texto para exibição](#scrolling-a-text-range-into-view)
-   [Recuperando o elemento delimitador de um intervalo de texto](#retrieving-the-enclosing-element-of-a-text-range)
-   [Comparando e clonando intervalos de texto](#comparing-and-cloning-text-ranges)
-   [Recuperando anotações](#retrieving-annotations)
    -   [Recuperando tipos de anotações de um intervalo de texto](#retrieving-annotations-types-from-a-text-range)
    -   [Recuperando todas as anotações de um intervalo de texto](#retrieving-all-annotations-from-a-text-range)
    -   [Recuperando informações sobre uma anotação específica](#retrieving-information-about-a-particular-annotation)
    -   [Recuperando o texto de destino da anotação](#retrieving-the-annotation-target-text)
-   [Recuperando estilos visuais](#retrieving-visual-styles)
-   [Invocando menus de contexto de intervalos de texto](#invoking-context-menus-from-text-ranges)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-a-text-range"></a>O que é um intervalo de texto?

O modelo de objeto de texto de automação da interface do usuário da Microsoft baseia-se no conceito do *intervalo de texto*. Um intervalo de texto é um objeto que expõe a interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) e representa um trecho contíguo de texto em um controle baseado em texto. Cada intervalo de texto tem um ponto de extremidade inicial e um ponto de extremidade final, e todo o conteúdo textual entre os dois pontos de extremidade é considerado parte do intervalo. Um intervalo de texto cujo ponto de extremidade inicial e final estão no mesmo local é chamado de intervalo de texto *degenerado* (ou vazio). Um intervalo de texto degenerado é usado para marcar um local específico dentro do texto de um controle, como o local do ponto de inserção de texto.

## <a name="acquiring-text-range-objects"></a>Adquirindo objetos de intervalo de texto

Os aplicativos cliente adquirem objetos de intervalo de texto usando as propriedades e os métodos da interface [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) . A propriedade [**IUIAutomationTextRangePattern::D ocumentrange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_documentrange) recupera um intervalo de texto que representa o conteúdo textual inteiro de um controle baseado em texto, enquanto outros métodos adquirem intervalos de texto que representam uma parte do conteúdo, como o texto selecionado, o texto visível ou um objeto inserido no texto.

Os métodos [**IUIAutomationTextRangePattern:: GetVisibleRanges**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getvisibleranges) e [**GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) podem recuperar matrizes de objetos de intervalo de texto. Se um controle for parcialmente obscurecido por uma janela sobreposta ou outro objeto, **GetVisibleRanges** retornará uma matriz que contém um objeto de intervalo de texto para cada linha de texto parcialmente visível. Da mesma forma, se um controle baseado em texto der suporte à seleção de vários spans separados de texto, **Getselecting** retornará uma matriz que contém um objeto de intervalo de texto para cada span selecionado.

O método [**IUIAutomationTextRangePattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) permite que um aplicativo cliente recupere um intervalo de texto que inclui um objeto inserido no conteúdo textual. O cliente especifica o ponteiro de interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de um objeto incorporado, como uma imagem, uma tabela ou um hiperlink, e o método retorna um intervalo de texto que inclui o objeto. No entanto, se o objeto incorporado não tiver nenhum texto associado a ele, o método retornará um intervalo de texto degenerado.

Um aplicativo cliente pode usar o método [**IUIAutomationTextRangePattern:: RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) para recuperar um intervalo de texto para o texto visível ou para o objeto inserido mais próximo das coordenadas de tela especificadas.

## <a name="selecting-text-in-a-text-range"></a>Selecionando texto em um intervalo de texto

A interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) inclui vários métodos que permitem que um aplicativo cliente controle a seleção de texto em um controle baseado em texto.

Os aplicativos cliente podem usar o método [**IUIAutomationTextRange:: SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-select) para selecionar o texto que corresponde a um intervalo de texto e remover a seleção anterior, se houver, do controle de texto. Chamar **Select** com um intervalo de texto degenerado move o ponto de inserção para o local do intervalo de texto sem selecionar nenhum texto.

Se um controle oferecer suporte à seleção de vários trechos de texto separados, um cliente poderá usar os métodos [**IUIAutomationTextRange:: AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) e [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) para adicionar intervalos de texto e removê-los da coleção de intervalos de texto selecionados. Se o controle oferecer suporte a apenas um intervalo de texto selecionado por vez, mas a operação de seleção resultar na seleção de vários intervalos de texto não contíguos, o método retornará um erro de **\_ INVALIDOPERATION** ou estenderá ou truncará a seleção atual. Um aplicativo cliente pode descobrir se um controle dá suporte à seleção de uma ou várias extensões de texto, ou nada, verificando a propriedade [**IUIAutomationTextPattern:: SupportedTextSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_supportedtextselection) .

Se um controle baseado em texto oferecer suporte a inserções de texto, chamar [**IUIAutomationTextRange:: AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) ou [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) em um intervalo de texto degenerado no controle moverá o ponto de inserção, mas não selecionará nenhum texto.

## <a name="retrieving-text-from-a-text-range"></a>Recuperando texto de um intervalo de texto

Os aplicativos cliente podem usar o método [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) para recuperar o texto sem formatação de um intervalo de texto. O texto sem formatação inclui todos os caracteres de controle encontrados no texto de origem, como retornos de carro e a marca Unicode da esquerda para a direita (LRM). O texto sem formatação não inclui nenhuma marca de marcação, como HTML, que possa estar presente no texto de origem. Além disso, todos os códigos de escape no texto de origem são convertidos em equivalentes de texto sem formatação. Por exemplo, " &nbsp; " é convertido em um caractere de espaço simples.

Se um objeto inserido abranger um intervalo de texto, o texto sem formatação incluirá o texto interno do objeto, mas não o texto alternativo (a propriedade Name do objeto incorporado). Para obter mais informações, consulte [como a automação da interface do usuário expõe objetos inseridos](uiauto-textpattern-and-embedded-objects-overview.md).

O método [**IUIAutomationTextRange:: FindText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findtext) pesquisa um intervalo de texto para uma cadeia de caracteres específica e, se for encontrado, retorna um novo intervalo de texto que abrange a cadeia de caracteres.

## <a name="retrieving-text-attributes-from-a-text-range"></a>Recuperando atributos de texto de um intervalo de texto

Os atributos de texto determinam o estilo de formatação do texto em um controle baseado em texto e incluem itens como cor de primeiro plano, estilo de marcador, tamanho da fonte e assim por diante. A automação da interface do usuário dá suporte a vários atributos de texto e define um identificador para cada atributo com suporte. Um aplicativo cliente pode consultar um intervalo de texto para o valor de um atributo de texto específico, especificando um identificador de atributo em uma chamada para o método [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) , juntamente com um ponteiro para uma estrutura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) que recebe o valor do atributo. Para obter informações detalhadas sobre cada atributo de texto compatível com a automação da interface do usuário, consulte [identificadores de atributo de texto](uiauto-textattribute-ids.md).

O valor recuperado por [**GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) representa o valor do atributo em todo o intervalo de texto. Se todo o texto no intervalo compartilhar o mesmo valor para o atributo especificado, esse valor será retornado por **GetAttributeValue**. No entanto, se o valor do atributo varia entre o intervalo de texto, **GetAttributeValue** retorna um ponteiro [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para um objeto de token estático chamado objeto **ReservedMixedAttribute** . Para descobrir se o valor de um atributo varia em um intervalo de texto, um aplicativo cliente deve comparar os resultados de **GetAttributeValue** com o objeto **ReservedMixedAttribute** recuperado da propriedade [**IUIAutomation:: ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservedmixedattributevalue) .

Um controle baseado em texto não é necessário para dar suporte a todos os atributos de texto de automação da interface do usuário. Se um cliente chamar o método [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) e passar o identificador de um atributo sem suporte, o método retornará um ponteiro [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para um objeto de token estático chamado objeto **ReservedNotSupported** . Para descobrir se um atributo específico tem suporte, um aplicativo cliente deve comparar os resultados de **GetAttributeValue** com o objeto **ReservedNotSupported** recuperado da propriedade [**IUIAutomation:: ReservedNotSupportedValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue) .

Os aplicativos cliente podem usar o método [**IUIAutomationTextRange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) para pesquisar um intervalo de texto para texto que tenha um atributo de texto específico. Se for encontrado, o método retornará um novo intervalo de texto que abrange o texto correspondente. Observe que **FindAttribute** retorna um intervalo de texto para texto correspondente, mesmo se o texto não estiver visível.

## <a name="retrieving-embedded-objects-from-a-text-range"></a>Recuperando objetos inseridos de um intervalo de texto

Um intervalo de texto pode incluir objetos incorporados, como tabelas, imagens, hiperlinks e assim por diante. Um aplicativo cliente pode recuperar uma coleção de todos os objetos inseridos em um intervalo chamando o método [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) . Objetos inseridos que se sobrepõem com o intervalo, mas que não estão totalmente entre si, também estão incluídos na coleção. Se o intervalo não contiver objetos incorporados, **GetChildren** recuperará uma coleção vazia.

Embora isso dependa do provedor do controle baseado em texto, o método [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) normalmente não retorna nenhum filho dos elementos inseridos. Por exemplo, se um intervalo de texto contiver uma tabela que tenha um número de células filho, o método **GetChildren** normalmente retornará apenas o elemento TABLE e não os elementos Cell.

Por motivos de desempenho ou arquitetura, [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) pode não conseguir recuperar objetos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para todos os objetos inseridos em um intervalo de texto. Em vez disso, o provedor pode retornar uma coleção que inclui itens virtualizados. Para obter mais informações, consulte [trabalhando com itens virtualizados](uiauto-workingwithvirtualizeditems.md).

## <a name="manipulating-a-text-range"></a>Manipulando um intervalo de texto

A interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) fornece vários métodos para manipular e navegar em intervalos de texto em um controle baseado em texto. Os métodos [**IUIAutomationTextRange:: move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)e [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) movem um intervalo de texto ou um de seus pontos de extremidade pela unidade de texto especificada, como caractere, palavra, parágrafo e assim por diante. Para obter mais informações, consulte [unidades de texto de automação da interface do usuário](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

Apesar de seu nome, o método [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) não expande necessariamente um intervalo de texto. Em vez disso, ele "normaliza" um intervalo de texto movendo os pontos de extremidade para que o intervalo abranja exatamente a unidade de texto especificada. O intervalo será expandido se for menor que a unidade especificada, ou reduzido se for maior que a unidade especificada. O diagrama a seguir mostra como o **ExpandToEnclosingUnit** normaliza um intervalo de texto movendo os pontos de extremidade do intervalo.

![diagrama mostrando posições de ponto de extremidade antes e depois de uma chamada para ExpandToEnclosingUnit](images/expandtoenclosingunit.jpg)

Se o intervalo de texto começar no início de uma unidade de texto e terminar no início de, ou antes, no próximo limite de unidade de texto, o ponto de extremidade final será movido para o próximo limite de unidade de texto (consulte 1 e 2 na ilustração anterior).

Se o intervalo de texto começar no início de uma unidade de texto e terminar em, ou após, o próximo limite de unidade, o ponto de extremidade final permanecerá ou será movido para trás para o próximo limite de unidade após o ponto de extremidade inicial (consulte 3 e 4 na ilustração anterior). Se houver mais de um limite de unidade de texto entre os pontos de extremidade inicial e final, o ponto de extremidade final será movido para trás para o próximo limite de unidade após o ponto final de partida, resultando em um intervalo de texto que é uma unidade de texto de comprimento.

Se o intervalo de texto for iniciado no meio de uma unidade de texto, o ponto de extremidade inicial será movido para trás até o início da unidade de texto e o ponto de extremidade final será movido para frente ou para trás, conforme necessário, para o próximo limite de unidade após o ponto de extremidade inicial (consulte de 5 a 8 na ilustração anterior).

Quando o método [**IUIAutomationTextRange:: move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) é chamado, o provedor normaliza o intervalo de texto pela unidade de texto especificada. Em seguida, o provedor move o intervalo para trás ou para frente pelo número especificado de unidades de texto. Ao mover o intervalo, o provedor ignora os limites de quaisquer objetos inseridos no texto. (No entanto, o limite de unidade em si pode ser afetado pela existência de um objeto inserido). O diagrama a seguir demonstra como o **método Move** move um intervalo de texto, unidade por unidade, entre objetos inseridos e limites de unidade de texto.

![diagrama mostrando como o método de movimentação move os pontos de extremidade de intervalo entre limites de objeto e unidade de texto](images/move.jpg)

O [**método IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit) move um dos pontos de extremidade para frente ou para trás pela unidade de texto especificada. A ilustração a seguir mostra como um ponto de extremidade avança.

![diagrama mostrando como moveendpointbyunit move o ponto de extremidade de um intervalo](images/moveendpointbyunit.gif)

O [**método IUIAutomationTextRange::MoveEndpointByRange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyrange) permite que um aplicativo cliente defina um ponto de extremidade de um intervalo de texto para o mesmo local que o ponto de extremidade especificado de um segundo intervalo de texto.

## <a name="scrolling-a-text-range-into-view"></a>Rolar um intervalo de texto para a exibição

O [**método IUIAutomationTextRange::ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-scrollintoview) rola um intervalo de texto para que o texto seja visível no viewport do controle baseado em texto. Ao chamar **ScrollIntoView**, um cliente pode especificar se o texto deve ser alinhado com a parte superior ou inferior do viewport.

## <a name="retrieving-the-enclosing-element-of-a-text-range"></a>Recuperando o elemento delimitar de um intervalo de texto

Um aplicativo cliente pode usar o método [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para recuperar o ponteiro da interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) do elemento mais interno que inclui um intervalo de texto. O elemento delimitar normalmente é o provedor de texto que fornece o intervalo de texto. No entanto, se o provedor de texto for compatível com elementos filho, como tabelas ou hiperlinks, o elemento delimitador poderá ser um descendente do provedor de texto.

## <a name="comparing-and-cloning-text-ranges"></a>Comparando e clonando intervalos de texto

A interface [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) inclui dois métodos para comparar intervalos de texto. O [**método IUIAutomationTextRange::Compare**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-compareendpoints) compara os pontos de extremidade inicial e final de dois intervalos de texto e retorna **TRUE** se ambos os pontos de extremidade são os mesmos. O **método IUIAutomationTextRange::CompareEndpoints** compara o ponto de extremidade inicial ou final dos dois intervalos. O valor de retorno será zero se os pontos de extremidade são iguais ou um valor positivo ou negativo que indica as posições relativas dos dois pontos de extremidade.

Os aplicativos cliente podem usar [**o método IUIAutomationTextRange::Clone**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-clone) para criar uma cópia exata do intervalo de texto. O novo intervalo de texto pode ser manipulado independentemente do intervalo de texto original.

## <a name="retrieving-annotations"></a>Recuperando anotações

Um intervalo de texto pode incluir anotações se o controle baseado em texto dá suporte a elas. Há muitos tipos diferentes de anotações. O arquivo de header UIAutomationClient.h define um conjunto de valores constantes nomeados que identificam os tipos de anotações que Automação da Interface do Usuário dá suporte. Para obter mais informações, consulte [**Identificadores de tipo de anotação**](uiauto-annotation-type-identifiers.md).

Alguns tipos de anotações são representados por um elemento de automação que dá suporte ao padrão de controle [Annotation](uiauto-implementingannotation.md) ( interface [**IUIAutomationAnnotationPattern).**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) Outros tipos de anotações são expostos por meio do padrão [de controle TextRange.](uiauto-about-text-and-textrange-patterns.md) Por exemplo, um provedor pode expor um indicador de erro de ortografia simples fazendo com que o método [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) retorne um atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) [**de AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)e um valor nulo para o atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)

### <a name="retrieving-annotations-types-from-a-text-range"></a>Recuperando tipos de anotações de um intervalo de texto

Você pode recuperar uma lista dos tipos de anotações que estão presentes em um intervalo de texto usando o [**método IUIAutomationTextRange::GetAttributeValue.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) Ao chamar o método , especifique uma ID de atributo de texto [**de UIA \_ AnnotationTypesAttributeId**](uiauto-textattribute-ids.md) e um ponteiro para um parâmetro do [**tipo VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant). Quando o método retorna, o parâmetro **VARIANT** contém uma lista de identificadores de tipo de anotação, um para cada tipo de anotação no intervalo de texto. Para obter mais informações, consulte [**Identificadores de tipo de anotação**](uiauto-annotation-type-identifiers.md).

### <a name="retrieving-all-annotations-from-a-text-range"></a>Recuperando todas as anotações de um intervalo de texto

Para recuperar as anotações de um intervalo de texto, chame o método [**IUIAutomationTextRange::GetAttributeValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) especificando uma ID de atributo de texto [**de UIA \_ AnnotationObjectsAttributeId**](uiauto-textattribute-ids.md) e um ponteiro para um parâmetro do tipo [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant). Quando o método retorna, o parâmetro **VARIANT** contém uma interface [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) que representa uma matriz de elementos de automação, um para cada anotação no intervalo de texto. A [**propriedade IUIAutomationElementArray::Length**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-get_length) indica o número de elementos na matriz e o método [**IUIAutomationElementArray::GetElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-getelement) recupera a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para um elemento específico.

### <a name="retrieving-information-about-a-particular-annotation"></a>Recuperando informações sobre uma anotação específica

Para recuperar informações sobre uma anotação específica, primeiro recupere a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para o elemento de anotação, conforme descrito na seção anterior. Em seguida, recupere a interface [**IUIAutomationAnnotationPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) para a anotação chamando o método [**IUIAutomationElement::GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) com uma ID de padrão de controle [**de UIA \_ AnnotationPatternId**](uiauto-controlpattern-ids.md), um identificador de interface de \_ IID IUIAutomationAnnotationPattern e o endereço de uma variável que recebe o ponteiro **IUIAutomationAnnotation** para a anotação. Consulte as propriedades da interface **IUIAutomationAnnotation** para recuperar o nome do tipo de anotação e a ID do tipo, o nome do autor da anotação, a data e a hora da anotação e a interface **IUIAutomationElement** para o elemento que está sendo anotado.

### <a name="retrieving-the-annotation-target-text"></a>Recuperando o texto de destino da anotação

Normalmente, uma anotação se aplica a algum subconjunto do texto em um intervalo de texto. Depois de recuperar a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para uma anotação, você pode passar a interface para o método [**IUIAutomationTextRange2::RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) para recuperar um intervalo de texto que contém o texto que é o destino da anotação.

## <a name="retrieving-visual-styles"></a>Recuperando estilos visuais

Um provedor implementa o padrão de controle [Estilos](/windows/desktop/WinAuto/uiauto-implementingstyles) para descrever um elemento de interface do usuário que tem um estilo específico, cor de preenchimento, padrão de preenchimento ou forma. Isso é especialmente útil ao descrever elementos em um documento, que frequentemente têm esses estilos. Estilos como esse geralmente carregam informações úteis para clientes com deficiências; por exemplo, os estilos podem descrever uma determinada cadeia de caracteres como o título de um documento ou um determinado objeto de fluxograma como um losango ou um círculo.

Você pode usar o método [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) para recuperar os nomes e identificadores dos estilos visuais usados em um intervalo de texto. Use o [**atributo de texto UIA \_ StyleNameAttributeId**](uiauto-textattribute-ids.md) para recuperar os nomes de estilo e [**\_ StyleIdAttributeId**](uiauto-textattribute-ids.md) da UIA para recuperar os identificadores de estilo.

Um controle baseado em texto que dá suporte a estilos visuais pode implementar o padrão de controle [Estilos](/windows/desktop/WinAuto/uiauto-implementingstyles) para permitir que os clientes acessem informações sobre um estilo visual usado pelo controle. Os clientes acessam o padrão de controle Estilos por meio da interface [**IUIAutomationStylesPattern.**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) Você pode recuperar essa interface chamando o método [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) ou [**GetCurrentPatternAs,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) especificando [**UIA \_ StylesPatternId**](uiauto-controlpattern-ids.md) como o identificador de padrão de controle.

A interface [**IUIAutomationStylesPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) inclui propriedades e métodos que fornecem as seguintes informações sobre um estilo visual:

-   O nome do estilo visual, como "Normal" ou "Título 1".
-   O identificador do estilo visual. Para obter mais informações, consulte [**Identificadores de estilo**](uiauto-style-identifiers.md).
-   A cor usada para preencher o controle baseado em texto.
-   A cor do padrão usado para preencher o controle baseado em texto.
-   A forma do controle baseado em texto.
-   As propriedades estendidas; ou seja, uma lista de valores e nomes de estilo específicos do controle.

## <a name="invoking-context-menus-from-text-ranges"></a>Invocando menus de contexto de intervalos de texto

Começando com Windows 8.1, os intervalos de texto podem dar suporte à interface [**IUIAutomationTextRange2.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange2) Essa interface dá suporte ao [**método ShowContextMenu.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange2-showcontextmenu) Você pode chamar esse método para invocar qualquer menu de contexto associado a um intervalo de texto. O cenário para isso é a correção automática de intervalos de texto ou seleção de candidato do IME. Nesses casos, é exibido um menu de contexto que dá suporte à interação do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Padrões de controle Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Automação da Interface do Usuário suporte para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 