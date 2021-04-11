---
title: Unidades de texto da automação da interface do usuário
description: Este tópico descreve as unidades de texto com suporte na automação da interface do usuário da Microsoft \ 32; Padrão de controle TextRange. Os provedores de automação da interface do usuário e os clientes usam unidades de texto para especificar a quantidade pela qual mover ou alterar o tamanho de um intervalo de texto.
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- Automação da interface do usuário, unidades de texto
- unidades de texto, sobre
- Automação da interface do usuário, lista de unidades de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff4257c70b34cea01a149b30dff2bf2fbe691a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294104"
---
# <a name="ui-automation-text-units"></a>Unidades de texto de automação da interface do usuário

Este tópico descreve as unidades de texto com suporte pelo padrão de controle [TextRange](uiauto-implementingtextandtextrange.md) de automação da interface do usuário da Microsoft. Os provedores de automação da interface do usuário e os clientes usam unidades de texto para especificar a quantidade pela qual mover ou alterar o tamanho de um intervalo de texto.

-   [Elementos da API da unidade de texto](#text-unit-api-elements)
-   [Descrições de unidades de texto](#text-unit-descriptions)
    -   [Caractere](#character)
    -   [Formato](#format)
    -   [Word](#word)
    -   [Linha](#line)
    -   [Paragraph](#paragraph)
    -   [Página](#page)
    -   [Documento](#document)
-   [Outros intervalos potenciais](#other-potential-ranges)
-   [Tópicos relacionados](#related-topics)

## <a name="text-unit-api-elements"></a>Elementos da API da unidade de texto

A API de automação da interface do usuário inclui os seguintes métodos que exigem a especificação de uma unidade de texto:

-   [**ITextRangeProvider:: mover**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**ITextRangeProvider::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**IUIAutomationTextRange:: mover**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**IUIAutomationTextRange::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

A enumeração [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) define as unidades de texto que são suportadas por intervalos de texto de automação da interface do usuário. Para especificar a unidade de texto, um membro da enumeração [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) é especificado em uma chamada para um método [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) ou [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) . As unidades de texto, do menor ao maior, são as seguintes:

-   [**Caractere TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Formato TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Palavra de paunidade \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Linha TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Parágrafo do TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Página TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Documento TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Se um controle baseado em texto específico não oferecer suporte à unidade de texto especificada, o provedor deverá responder substituindo a próxima unidade de texto maior que é suportada pelo controle. Por exemplo, se o [**\_ parágrafo TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) for especificado, mas não houver suporte, o método poderá substituir a [**\_ página TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ou o [**\_ documento TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit).

As características linguísticas do texto de origem podem dificultar para um provedor determinar os limites de texto com base na unidade de texto especificada. Para obter ajuda para determinar os limites de texto, um provedor pode usar funções de API do Uniscribe, como [**ScriptBreak**](/windows/desktop/api/usp10/nf-usp10-scriptbreak). Para obter mais informações, consulte [Uniscribe](/windows/desktop/Intl/uniscribe) no site do MSDN.

## <a name="endpoint-inclusivity"></a>Inclusivity do ponto de extremidade

Um ponto de extremidade de unidade de texto pode servir como um ponto de extremidade [inicial](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) e um ponto de extremidade [final](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) para intervalos de texto adjacentes do mesmo tipo. Se o final de uma unidade de texto também for o início de outra unidade de texto, o intervalo que contém o ponto de extremidade [final](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) não compartilhará nenhum atributo ou objeto do intervalo adjacente que contenha o ponto de extremidade [inicial](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) .

Por exemplo, um fluxo de texto, "Olá, **mundo**", contém duas unidades de palavras com atributos de espessura de fonte diferentes (normal e negrito). Nesse caso, o ponto de extremidade [final](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) da unidade de palavra "Olá" e o ponto de extremidade [inicial](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) da unidade de palavra "**World**" são os mesmos, o que resulta no seguinte:

- O intervalo de "Olá" não compartilha o atributo em negrito da unidade de palavra "World" e não retorna o valor de atributo misto para o atributo de texto de espessura da fonte.
- O intervalo de "**mundo**" tem uma única espessura de fonte (negrito) e não compartilha a espessura da fonte da unidade de palavra anterior "Olá".

Aqui está outro exemplo em que um fluxo de texto contém duas unidades de palavras, uma das quais é um link: `[Foo]() Bar` . Nesse caso, o ponto de extremidade [final](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) da unidade de palavra `[Foo]()` e o ponto de extremidade [inicial](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) da "barra" da unidade de palavra são os mesmos, o que resulta no seguinte:

- O link pertence ao intervalo de texto que contém "foo".
- O link é um filho do intervalo de texto "foo" e é incluído pelo [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).
- O intervalo de texto "barra" não tem filhos e e é incluído pelo [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).

**Observações adicionais:**

> Um intervalo degenerado (vazio) em um limite de unidade de texto com um intervalo de texto do mesmo tipo assume as propriedades da unidade de texto imediatamente adjacente.
>
> Chamar [IUIAutomationTextRange:: ExpandToEnclosingUnit](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) em um intervalo de degeneramento em um limite de unidade de texto com um intervalo de texto do mesmo tipo, expande o intervalo de degeneração para a seguinte unidade de texto.

## <a name="text-unit-descriptions"></a>Descrições de unidades de texto

Esta seção descreve cada uma das unidades de texto com suporte pela automação da interface do usuário.

### <a name="character"></a>Caractere

[**TextUnit \_ Character**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) é uma unidade linguística de texto que representa um único caractere. A definição linguística de um caractere varia de acordo com a linguagem. Para o inglês americano, um caractere é normalmente borderado por um espaço ou outro caractere, como uma marca de pontuação, um número ou uma letra.

Caracteres de controle como retornos de carro e a marca Unicode da esquerda para a direita (LTM) não devem ser considerados como caracteres, mas podem ser incluídos em um intervalo de texto que é normalizado com base na unidade de texto do caractere.

Marcas de Pontuação e caracteres de quebra de palavras como espaços devem ser considerados como caracteres.

### <a name="format"></a>Formatar

[**TextUnit \_ O formato**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) é usado para posicionar o limite de um intervalo de texto com base nos atributos de formatação do texto. Por exemplo, se um intervalo de texto estiver posicionado atualmente em um único caractere de uma palavra, especificar o **\_ formato TextUnit** em uma chamada para [**IUIAutomationTextRange:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) expande o intervalo de texto para incluir todo o texto que compartilha todos os mesmos atributos que o caractere único. O intervalo de texto resultante pode ou não incluir a palavra inteira. Além disso, o uso da unidade de texto de formato não expandirá um intervalo de texto no limite de um objeto incorporado, como uma imagem ou um hiperlink.

Ao contrário das outras unidades de texto, que incluem as unidades de texto menores do que elas, o [**\_ formato TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) pode ser menor ou maior do que as outras unidades. Por exemplo, se um documento inteiro compartilhar os mesmos atributos de texto e não contiver objetos incorporados, expandir um intervalo de texto por **\_ formato TextUnit** criaria um novo intervalo que abrange todo o documento, ao passo que expandiria o intervalo de texto por [**\_ palavra da unidade TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) criaria um intervalo menor.

### <a name="word"></a>Word

[**TextUnit \_ O Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) é uma unidade lingüística de texto que representa uma única palavra inteira. A definição lingüística de uma palavra varia por idioma. Para o inglês americano, as palavras normalmente são bordadas por espaços ou caracteres de pontuação.

Quando a [**\_ palavra TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) é usada para definir o limite de um intervalo de texto, o intervalo de texto resultante deve incluir quaisquer caracteres de quebra de palavras que estejam presentes no final da palavra, mas antes do início da próxima palavra.

### <a name="line"></a>Linha

[**TextUnit \_ Linha**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) é uma unidade de texto que representa uma única linha de texto, conforme apresentado no visor do controle. Ao usar a **\_ linha TextUnit** para definir o limite de um intervalo de texto, um provedor deve definir o limite imediatamente após o ponto em que um caractere de controle quebra a linha, ou onde o visor do controle encapsula o texto em uma nova linha. O limite deve ser definido onde uma nova linha é iniciada.

### <a name="paragraph"></a>Paragraph

[**TextUnit \_ O parágrafo**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) é uma unidade lingüística de texto que representa um parágrafo completo. Um parágrafo deve começar logo antes do primeiro caractere de um parágrafo e, normalmente, deve terminar logo após o último caractere. Qualquer linha vazia após um parágrafo deve ser mesclada no parágrafo, a menos que algo na fonte de texto indique o contrário. Normalmente, o limite final de um parágrafo também marca o limite final de uma unidade de texto de [**\_ linha de unidade**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) .

### <a name="page"></a>?

[**TextUnit \_ A página**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) representa uma página de texto completa de um documento. Os limites de uma página devem ser definidos nos pontos imediatos em que uma página é iniciada e termina.

### <a name="document"></a>Documento

[**TextUnit \_ O documento**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) representa todo o conteúdo de um documento com suporte pelo padrão de controle de [texto](uiauto-implementingtextandtextrange.md) . Não deve existir texto fora de um intervalo de texto que contenha um documento. Todos os objetos inseridos em um documento, como notas de anotação que cruzam um limite de página, devem ser tratados como objetos incorporados do documento e não como parte do conteúdo de texto do documento.

## <a name="other-potential-ranges"></a>Outros intervalos potenciais

A especificação de padrão de controle [TextRange](uiauto-implementingtextandtextrange.md) atual não permite que novos valores de unidade de texto sejam adicionados à enumeração [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , nem permite que os valores de unidade de texto existentes sejam redefinidos. Para expor outros intervalos potenciais, como cabeçalhos e anotações, um provedor deve expor esses intervalos como objetos incorporados com um intervalo de texto associado. Dessa forma, você também pode adicionar suporte para os padrões de controle apropriados. Essa solução é mais flexível e extensível do que definir novas unidades de texto.

## <a name="related-topics"></a>Tópicos relacionados

### <a name="reference"></a>Referência

[TextPatternRangeEndpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[ITextRangeProvider:: GetChildren](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>Conceitual

[Suporte à automação da interface do usuário para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)