---
title: Como a automação da interface do usuário expõe objetos inseridos
description: Este tópico descreve como a automação da interface do usuário da Microsoft expõe objetos inseridos ou elementos filho, em um documento de texto ou contêiner.
ms.assetid: 5ecf5e94-5329-4abb-aedb-4e303688e5f7
keywords:
- Automação da interface do usuário, visão geral do padrão de texto
- Visão geral da automação da interface do usuário, controles de texto
- Automação da interface do usuário, padrão de controle de texto
- Automação da interface do usuário, visão geral de objetos inseridos
- Automação da interface do usuário, expondo objetos inseridos
- Automação da interface do usuário, cenários para objetos inseridos
- padrões de texto, sobre
- controles de texto, sobre
- Padrão de controle de texto
- padrões de controle, texto
- objetos inseridos
- expondo objetos inseridos
ms.topic: article
ms.date: 08/31/2019
ms.openlocfilehash: 2cb5a571d61353d2c8458b42fb65eac19eab0fb228f1e157539470075e392b8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899301"
---
# <a name="how-ui-automation-exposes-embedded-objects"></a>Como a automação da interface do usuário expõe objetos inseridos

Este tópico descreve como a automação da interface do usuário da Microsoft usa os padrões de controle Text e TextRange para expor objetos inseridos (elementos filho/descendentes) em um documento de texto ou contêiner.

para automação da interface do usuário, um objeto incorporado é qualquer elemento que tenha limites não textuais, como uma imagem, um hiperlink, uma tabela ou um tipo de documento (Microsoft Excel planilha, arquivo de mídia do Microsoft Windows e assim por diante).

> [!NOTE]
> Isso difere da definição de OLE de Component Object Model (COM) (consulte [objetos inseridos](../com/embedded-objects.md)), em que um elemento é criado em um aplicativo e inserido ou vinculado em outro aplicativo. Se o objeto pode ser editado em seu aplicativo original é irrelevante no contexto da automação da interface do usuário.

## <a name="embedded-objects-and-the-ui-automation-tree"></a>Objetos incorporados e a árvore de automação da interface do usuário

Os objetos inseridos são tratados como elementos individuais no modo de exibição de controle da árvore de automação da interface do usuário. Eles são expostos como filhos do contêiner de texto para que possam ser acessados por meio do mesmo modelo de objeto que outros controles na automação da interface do usuário.

A tabela a seguir lista exemplos de elementos de contêiner e não contêiner.

:::row:::
   :::column span="2":::

      **Elementos de contêiner**

   :::column-end:::
   :::column span="":::

      **Elementos que não são de contêiner**

   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::

- Calendário
- Combobox
- DataGrid
- Documento
- Editar
- Agrupar
- Cabeçalho
- HeaderItem
- Lista
- Menu

   :::column-end:::
   :::column span="":::

- MenuBar
- Painel
- SplitButton
- Tab
- Tabela
- Barra de ferramentas
- Árvore
- TreeItem
- Janela

   :::column-end:::
   :::column span="":::

- Link
- Caixas
- Botão

  :::column-end:::
:::row-end:::

A imagem a seguir mostra um contêiner de texto (documento) com uma tabela e imagem inserida.

![ilustração mostrando um documento com uma tabela e uma imagem inserida](images/embeddedtable.jpg)

O modo de exibição de conteúdo de automação da interface do documento anterior é mostrado no diagrama a seguir.

![diagrama da exibição de conteúdo de automação da interface do usuário de um documento com objetos inseridos](images/contenttree.jpg)

### <a name="compatible-and-non-compatible-embedded-objects"></a>Objetos incorporados "compatíveis" e "não compatíveis"

Alguns provedores de automação de interface do usuário usam o mesmo armazenamento de texto para cada objeto TextPattern que eles contêm.  Os objetos apoiados pelo mesmo armazenamento de texto como seu contêiner são chamados de objetos incorporados "compatíveis". Esses objetos podem ser os próprios objetos TextPattern e, nesse caso, seus intervalos de texto são comparáveis aos intervalos de texto obtidos de seu contêiner. Isso permite que os provedores exponham informações do cliente sobre os objetos TextPattern individuais como se fossem um provedor de texto grande.

No entanto, os provedores podem usar diferentes armazenamentos de texto para diferentes objetos TextPattern inseridos dentro de um contêiner de TextPattern. Os objetos não apoiados pelo armazenamento de texto do contêiner são chamados de objetos incorporados "não compatíveis". Esses tipos de objetos inseridos podem ou não ser objetos baseados em TextPattern.  

A tabela a seguir lista alguns exemplos de objetos incorporados compatíveis e não compatíveis.

| Objetos  | Objetos incorporados compatíveis | Objetos inseridos não compatíveis |
| --- | --- | --- |
| Objetos inseridos não TextPattern | Botão no Microsoft Edge<br>Tabela de dados no Microsoft Edge | Botão no RichTextBlock na estrutura XAML da Microsoft<br>Imagens com texto alt em Microsoft Edge<br>ListView com ListItems em RichTextBlock na estrutura XAML da Microsoft |
| Objetos inseridos por TextPattern | Controle de entrada do tipo "texto" em Microsoft Edge<br>Tabela em um documento do Word | elemento TextBox em um documento Microsoft Word |

## <a name="exposing-embedded-objects"></a>Expondo objetos inseridos

Os padrões de controle [Text e TextRange](uiauto-implementingtextandtextrange.md) expõem propriedades e métodos que facilitam a navegação e a consulta de objetos inseridos.

O conteúdo textual (ou texto interno) de um contêiner de texto e um objeto incorporado, como um hiperlink ou célula de tabela, é exposto como um fluxo de texto único e contínuo na exibição de controle e na exibição de conteúdo da árvore de automação da interface do usuário; os limites de objeto são ignorados. Se um cliente de automação de interface do usuário estiver recuperando o texto para recitar, interpretar ou analisar de alguma maneira, o intervalo de texto deverá ser verificado em casos especiais, como uma tabela com conteúdo textual ou outros objetos incorporados. Chame [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) para obter uma interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para cada objeto inserido e, em seguida, chame [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) para obter um intervalo de texto para cada elemento. Isso é feito recursivamente até que todo o conteúdo textual seja recuperado.

> [!NOTE]
> Um intervalo de degeneração (ou recolhido) é onde o ponto de extremidade inicial e o ponto de extremidade final são os mesmos. Os intervalos de degeneração são frequentemente usados para indicar a posição do cursor de texto pelos métodos [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) [GetSelection](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection) e [GetCaretRange](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange) .

O diagrama a seguir mostra um fluxo de texto com objetos incorporados e seus intervalos de intervalo.

![diagrama mostrando um fluxo de texto com objetos incorporados e seus intervalos de intervalo](images/rangespans.jpg)

## <a name="embedded-objects-and-textunit"></a>Objetos incorporados e TextUnit

Um objeto [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) pode ser atravessado e por uma [unidade](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit)textespecificada. Provedores que contêm objetos incorporados podem ser percorridos quase da mesma forma, mas os objetos incorporados afetam a passagem. Aqui estão algumas coisas que você deve conhecer:

- Qualquer objeto inserido não compatível é representado pelo caractere de substituição U + FFFC no repositório de texto do TextPattern do elemento do contêiner. Ele também é considerado uma unidade de caracteres e uma unidade de palavras.
- Os objetos incorporados compatíveis podem consistir em vários caracteres e palavras.
- O elemento delimitador é o elemento inferior que abrange todo o intervalo de texto.
- Os elementos filho de um intervalo também são elementos filho de um elemento de contêiner que é parcial ou completamente colocado dentro do intervalo.
- Idealmente (especialmente no caso de elementos de contêiner, como tabela), um limite de palavra não vai além do limite do objeto. No exemplo a seguir, a palavra "barra" não contém nenhuma posição de texto que esteja fora da `</td>` marca ( `<br \>` não faz parte da palavra "barra").

```Xaml
<table style="width:100%">
  <tr>
    <th>Name</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>Eve Jackson</td>
    <td>Foo Bar</td>
  </tr>
</table>
<br/>
```

- Em geral, `<br \>` é tratado como uma palavra individual, de modo que não ultrapasse um limite de linha.
- Uma exceção à regra anterior é onde uma unidade de texto do Word contém objetos completos dentro dele mesmo. Por exemplo, `<p>Hello <a href="#">link</a> here.</p>` , que inclui contêineres embutidos, tem as palavras "Olá", "link" e "aqui". Em que "link" tem um objeto TextPattern como o elemento delimitador e um objeto de link como seu filho.
- No caso de unidades de caracteres, o objeto é o elemento delimitador (unidades de texto como esta não devem ter filhos).
- Os objetos de anotação não devem ser representados como um objeto inserido. Por exemplo, a presença de outros especificadores de autor em um documento coautoria.
- Os objetos inseridos ocupam pelo menos uma posição de cursor, a anotação é apenas metadados.
- Cada limite de objeto (início e término) é representado por uma quebra de formato no intervalo de documentos TextPattern.
- Para HTML, cada marca HTML não resulta necessariamente em um objeto de automação da interface do usuário. Por exemplo, o conteúdo nas <em></em> marcas de ênfase não precisa ser representado como um elemento, mas sim um fluxo de texto em que UIA_IsItalicAttributeId retorna true.
- O ponto de extremidade inicial é inclusivo e é o ponto de extremidade preferencial, enquanto o ponto de extremidade final é exclusivo. Isso é útil quando o intervalo é degenerado e os pontos de extremidade inicial e final pertencem à mesma posição para esse intervalo.

## <a name="comparing-embedded-objects"></a>Comparando objetos inseridos

Objetos TextPattern aninhados que estão em uma relação filho semelhante e compartilham o mesmo armazenamento de texto de backup são chamados comparáveis. Nesse caso, os intervalos de um dos objetos TextPattern podem ser comparados usando [ITextRangeProvider:: Compare](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare) e [ITextRangeProvider:: CompareEndpoints](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints). Ambos resultam em um valor numérico válido especificando sua posição relativa.

Um objeto não TextPattern inserido em um objeto TextPattern é comparável a TextPattern se o objeto tiver um intervalo válido em TextPattern ([ITextProvider:: RangeFromChild](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild)) e o conteúdo por trás do intervalo de texto não estiver vazio e não for um caractere de substituição.

## <a name="embedded-textpattern-objects-and-the-document-textunit"></a>Objetos TextPattern inseridos e a unidade TextDocument

Para objetos TextPattern inseridos, a unidade de [documento](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) reconhece apenas o conteúdo contido nesse elemento.

### <a name="word-textpattern-element-hierarchy"></a>Hierarquia de elementos de TextPattern do Word

- O elemento Document implementa TextPattern e [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) retorna o intervalo inteiro do documento do Word.
- As páginas individuais do documento implementam TextPattern e [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) retorna o conteúdo dessas páginas individuais (mesmo que as páginas compartilhem o mesmo armazenamento de texto com o documento inteiro de TextPattern).

### <a name="webpage-and-text-input-controls-in-edge"></a>Página da Web e controles de entrada de texto no Edge

- O elemento do painel principal da página da Web implementa TextPattern e expõe todo o conteúdo da página da Web.
- Os controles de entrada de texto individuais dão suporte a TextPattern, em que um intervalo de documentos representa o texto contido em cada campo de entrada (mesmo que eles compartilhem o mesmo armazenamento de texto com a página da Web inteira).

## <a name="common-scenarios"></a>Cenários comuns

Esta seção apresenta exemplos de cenários comuns que envolvem objetos incorporados: hiperlinks, imagens e tabelas. Nos exemplos a seguir, a chave esquerda ({) representa o ponto de extremidade inicial do intervalo de texto e a chave direita (}) representa o ponto de extremidade final.

### <a name="hyperlink-example-1-a-text-range-that-contains-an-embedded-text-hyperlink"></a>Exemplo de hiperlink 1: um intervalo de texto que contém um hiperlink de texto inserido

O intervalo de texto a seguir contém um hiperlink de texto inserido.

  {A URL https://www.microsoft.com é inserida em texto}.

Chamar os métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)e [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) resulta nos comportamentos descritos na tabela a seguir.

| Método chamado                                                                                                                                                                                                                                                     | Resultado                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                  | Retorna a cadeia de caracteres "a URL https://www.microsoft.com é inserida em texto".                                                                               |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                          | Retorna o elemento de automação da interface do usuário mais interno que inclui o intervalo de texto, nesse caso, o elemento Automation que representa o próprio provedor de texto. |
| [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                          | Retorna um elemento de automação da interface do usuário que representa o controle de hiperlink.                                                                                      |
| [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild), onde o elemento de automação da interface do usuário foi retornado pelo método [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) anterior. | Retorna o intervalo que representa " https://www.microsoft.com ".                                                                                            |
### <a name="hyperlink-example-2-a-text-range-that-partially-spans-an-embedded-text-hyperlink"></a>Exemplo de hiperlink 2: um intervalo de texto que abrange parcialmente um hiperlink de texto inserido

O intervalo de texto a seguir abrange parcialmente um hiperlink de texto inserido.

  A URL de https://{www} está inserida no texto.

Chamar os métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)e [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) resulta nos comportamentos descritos na tabela a seguir.

| Método chamado                                                                                            | Resultado                                                                                                         |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Retorna a cadeia de caracteres "www".                                                                                      |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Retorna o elemento de automação de interface do usuário mais interno que inclui o intervalo de texto; Nesse caso, o controle HyperLink. |
| [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                 | Retorna **NULL** porque o intervalo de texto não abrange toda a cadeia de caracteres da URL.                                   |

### <a name="hyperlink-example-3-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Exemplo de hiperlink 3: um intervalo de texto que abrange parcialmente o conteúdo de um contêiner de texto

O intervalo de texto a seguir abrange parcialmente o conteúdo de um contêiner de texto. O contêiner de texto tem um hiperlink de texto inserido que não faz parte do intervalo de texto.

  {A URL} https://www.microsoft.com é inserido no texto.

Chamar os métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)e [**move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) resulta nos comportamentos descritos na tabela a seguir.

| Método chamado                                                                                            | Resultado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Retorna a cadeia de caracteres "a URL".                                                                                                                                                                                                     |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Retorna o elemento de automação de interface do usuário mais interno que inclui o intervalo de texto, nesse caso, o elemento que representa o próprio provedor de texto.                                                                                     |
| [**IUIAutomationTextRange:: mover**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)                               | Move o intervalo de texto span para "https://" porque o texto do hiperlink é composto por palavras individuais. Nesse caso, o hiperlink não é tratado como um único objeto.<br/> A URL {http} está inserida no texto.<br/> |

### <a name="image-example-1-a-text-range-that-contains-an-embedded-image"></a>Exemplo de imagem 1: um intervalo de texto que contém uma imagem inserida

O intervalo de texto a seguir contém uma imagem inserida de um vaivém.

 {A imagem ![ilustração de um vaivém](images/shuttle.jpg) é inserido em texto}.

Chamar os métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)e [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) resulta nos comportamentos descritos na tabela a seguir.

| Método chamado                                                                                                                                                                                                                                                    | Resultado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                 | Retorna a cadeia de caracteres "a imagem é inserida em texto". Qualquer texto ALT associado à imagem não é incluído no fluxo de texto.                |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                         | Retorna o elemento de automação de interface do usuário mais interno que inclui o intervalo de texto, nesse caso, o elemento que representa o próprio provedor de texto. |
| [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                         | Retorna um elemento de automação de interface do usuário que representa o controle de imagem.                                                                               |
| [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) em que o elemento de automação da interface do usuário foi retornado pelo método [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) anterior. | Retorna o intervalo de degeneração.                                                                                                                 |

### <a name="image-example-2-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Exemplo de imagem 2: um intervalo de texto que abrange parcialmente o conteúdo de um contêiner de texto

O intervalo de texto a seguir abrange parcialmente o conteúdo de um contêiner de texto. O contêiner de texto tem uma imagem inserida que não faz parte do intervalo de texto.

 {A imagem} ![ilustração de um vaivém](images/shuttle.jpg) é inserido no texto.

Chamar os métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)e [**move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) resulta nos comportamentos descritos na tabela a seguir.

| Método chamado                                                                                                          | Resultado                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                       | Retorna a cadeia de caracteres "a imagem".                                                                                                                                                                                                                                                 |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)               | Retorna o elemento de automação de interface do usuário mais interno que inclui o intervalo de texto, nesse caso, o elemento que representa o próprio provedor de texto.                                                                                                                                   |
| [**IUIAutomationTextRange:: move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) com parâmetros de (**TextUnit \_ Word**, 2). | Move o intervalo de intervalos de texto para "is". Como apenas objetos inseridos com base em texto são considerados parte do fluxo de texto, a imagem neste exemplo não afeta [**IUIAutomationTextRange:: move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) ou seu valor de retorno, nesse caso, 2. |

### <a name="table"></a>Tabela

### <a name="table-example-1-gets-the-text-container-from-the-content-of-a-cell"></a>Exemplo de tabela 1: Obtém o contêiner de texto do conteúdo de uma célula

A tabela a seguir obtém o contêiner de texto do conteúdo de uma célula.

| Célula com imagem                                            | Célula com texto |
|------------------------------------------------------------|----------------|
| ![ilustração de uma lança](images/shuttle.jpg)           | X              |
| ![ilustração do espaço e de um livro](images/space.jpg) | Y              |
| ![ilustração de um livro](images/microscope.jpg)     | Z              |

Chamar os métodos [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem), [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)e [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) resulta nos comportamentos descritos na tabela a seguir.

| Método chamado                                                                                                                                                                                                                       | Resultado                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) com parâmetros (0, 0).                                                                                                                        | Retorna o Automação da Interface do Usuário que representa o conteúdo da célula da tabela, nesse caso, o elemento é um controle de texto.                                                               |
| [**iuiautomationtextpattern::rangefromchild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)                                                                                                                                  | retorna o intervalo da imagem ![ilustração de uma lança](images/shuttle.jpg).                                                                                                            |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para o objeto retornado pelo método [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) anterior. | Retorna o Automação da Interface do Usuário que representa a célula da tabela. Nesse caso, o elemento é um controle de texto que dá suporte ao padrão de controle [TableItem.](uiauto-implementingtableitem.md) |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para o objeto retornado pelo **método GetEnclosingElement** anterior.                                                    | Retorna o Automação da Interface do Usuário que representa a tabela.                                                                                                                                   |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para o objeto retornado pelo **método GetEnclosingElement** anterior.                                                    | Retorna o Automação da Interface do Usuário que representa o próprio provedor de texto.                                                                                                                 |

### <a name="table-example-2-gets-the-text-content-of-a-cell"></a>Exemplo de tabela 2: obtém o conteúdo de texto de uma célula

A tabela no exemplo anterior obtém o conteúdo de texto de uma célula.

Chamar os métodos [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) e [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) resulta nos comportamentos descritos na tabela a seguir.

| Método chamado                                                                                                                                                                                                                                                          | Resultado                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) com parâmetros (1,1).                                                                                                                                                            | Retorna o Automação da Interface do Usuário que representa o conteúdo da célula da tabela. Nesse caso, o elemento é um controle de texto. |
| [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) em que o elemento Automação da Interface do Usuário é o objeto retornado pelo método [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) anterior. | Retorna "Y".                                                                                                               |

Ao passar por um documento por [**Linha TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), se o intervalo de texto entrar em uma tabela inserida, cada linha de texto em uma célula deverá ser tratada como uma linha.

## <a name="related-topics"></a>Tópicos relacionados

### <a name="conceptual"></a>Conceitual

- [Sobre os padrões de controle Text e TextRange](uiauto-about-text-and-textrange-patterns.md)
- [Automação da Interface do Usuário de texto](uiauto-textattributes.md)
- [Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
- [Automação da Interface do Usuário suporte para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)