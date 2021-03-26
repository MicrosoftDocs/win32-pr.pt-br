---
description: Você pode registrar uma lista de propriedades de exibição de conteúdo exclusiva e um padrão de layout para o tipo de arquivo ou item.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Registrar um conjunto de exibição de conteúdo de propriedades e padrão de layout para um tipo de arquivo ou item
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104297809"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a>Como registrar um conjunto exclusivo de exibição de conteúdo de propriedades e padrão de layout para o tipo de arquivo ou item

Você pode registrar uma lista de propriedades de exibição de conteúdo exclusiva e um padrão de layout para o tipo de arquivo ou item. Se o tipo de arquivo ou o item também estiver associado a um tipo, o registro de exibição de conteúdo específico do tipo de arquivo ou item substituirá o registro de tipo. Isso pode ser útil se as propriedades mais importantes para esse item forem diferentes de outros itens do mesmo tipo. Se você não associar o tipo de arquivo ou o item a um tipo de item ou registrar diretamente a exibição de conteúdo, o sistema usará as informações de exibição de conteúdo padrão (armazenadas em uma chave de registro referenciada pelo último elemento na matriz de associação de todos os itens, HKEY \_ classes \_ root \\ \* )

Antes de registrar uma lista de propriedades Personalizada para o tipo de arquivo, você deve entender o modo de resultado da pesquisa e o modo de procura e os padrões de layout disponíveis para você.

## <a name="instructions"></a>Instruções

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a>Etapa 1: Noções básicas sobre o modo de resultado de pesquisa e o modo de procura

A exibição de conteúdo requer a definição de um padrão de layout e um conjunto de listas de propriedades para um item em um conjunto de resultados da pesquisa (modo de resultado da pesquisa) e ao navegar até um local do Shell (modo de procura). Você pode usar os mesmos valores para resultado da pesquisa e procurar, como `Kind.Music` faz. Como alternativa, você pode definir uma lista de propriedades e/ou padrão de layout diferente como `Kind.Document` o faz.

No caso do `Kind.Document` , os usuários geralmente pesquisam palavras no texto do documento. Portanto, incluir mais texto de exemplo no resultado da pesquisa pode ser a melhor opção. O exemplo a seguir ilustra a exibição de conteúdo de navegação de `Kind.Document` .

![procurar exibição de conteúdo de kind.document](images/content-view/browsecontentviewkinddocument.png)

Como os usuários raramente procuram texto específico ao procurar documentos, otimizar sua escolha de propriedades e layout para ajustar mais resultados da pesquisa na tela pode ser a melhor opção. A captura de tela a seguir ilustra a exibição de conteúdo de pesquisa do `Kind.Document` .

### <a name="step-2-understanding-layout-patterns"></a>Etapa 2: Noções básicas sobre padrões de layout

Há quatro padrões de layout: alfa, beta, gama e Delta.

**Layout alfa**

O padrão de layout alfa é otimizado para os resultados da pesquisa de documentos que contêm trechos. Ele tem as seguintes especificações:

-   Linhas: 4
-   Propriedades: 7
-   Layout alfa quando o item tem 350 pixels ou mais de espaço horizontal, conforme mostrado na ilustração a seguir.

    ![padrão de layout alfa](images/content-view/layout1.png)

-   A ilustração a seguir mostra o layout alfa quando o item tem 350 pixels ou mais de espaço horizontal.

    ![Diagrama que mostra um exemplo de layout alfa](images/content-view/alphaviewmore.png)

-   A ilustração a seguir mostra o layout alfa quando o item tem menos de 350 pixels de espaço horizontal.

    ![Captura de tela que mostra um exemplo de layout alfa no Microsoft Word.](images/content-view/layout2.png)

-   A ilustração a seguir mostra o layout alfa quando o item tem menos de 350 pixels de espaço horizontal.

    ![exemplo de layout alfa](images/content-view/alphaviewless.png)

**Layout beta**

O padrão de layout beta é otimizado para resultados de pesquisa de documentos de email que contêm trechos. Ele tem as seguintes especificações:

-   Linhas: 4
-   Propriedades: 5
-   Layout beta quando o item tem 350 pixels ou mais de espaço horizontal, conforme mostrado na ilustração a seguir.

    ![Diagrama que mostra um exemplo de layout beta.](images/content-view/layout3.png)

-   A ilustração a seguir mostra o layout beta quando o item tem 350 pixels ou mais de espaço horizontal.

    ![Captura de tela que mostra um exemplo de layout beta para email.](images/content-view/betaviewmore.png)

-   A ilustração a seguir mostra o layout beta quando o item tem menos de 350 pixels de espaço horizontal.

    ![Diagrama que mostra um exemplo de layout beta com menos de 350 pixels de espaço horizontal.](images/content-view/layout4.png)

-   A ilustração a seguir mostra o layout beta quando o item tem menos de 350 pixels de espaço horizontal:

    ![exemplo de layout beta](images/content-view/betaviewless.png)

**Layout gama**

O padrão de layout gama é semelhante ao alfa, mas usa um layout de duas linhas em vez de quatro. Esse layout é ideal para cenários nos quais você deseja ver um trecho de código, mas deseja ajustar mais itens na tela ou para tipos de arquivo que exigem menos espaço para mostrar as informações mais críticas. O layout gama tem as seguintes especificações:

-   Linhas: 2
-   Propriedades: 4
-   A ilustração a seguir mostra o layout gama quando o item tem 350 pixels ou mais de espaço horizontal.

    ![Diagrama que mostra um exemplo de layout de gama.](images/content-view/layout5.png)

-   A ilustração a seguir mostra o layout gama quando o item tem 350 pixels ou mais de espaço horizontal.

    ![Captura de tela que mostra um exemplo de layout de gama para um item de lista de verificação.](images/content-view/gammaviewmore.png)

-   A ilustração a seguir mostra o layout gama quando o item tem menos de 350 pixels de espaço horizontal.

    ![Diagrama que mostra um exemplo de layout gama com menos de 350 pixels de espaço horizontal.](images/content-view/layout6.png)

-   Exemplo do layout gama quando o item tem menos de 350 pixels de espaço horizontal.

    ![exemplo de layout de gama](images/content-view/gammaviewless.png)

**Layout Delta**

O padrão de layout Delta é otimizado para exibir muitas propriedades mais curtas, como imagens e músicas. Ele tem as seguintes especificações:

-   Linhas: 2
-   Propriedades: 6
-   Layout Delta quando o item tem 700 pixels ou mais de espaço horizontal, conforme mostrado na ilustração a seguir.

    ![Diagrama que mostra um exemplo de layout Delta.](images/content-view/layout7.png)

-   Exemplo do layout Delta quando o item tem 700 pixels ou mais de espaço horizontal.

    ![Captura de tela que mostra um exemplo de layout Delta para um arquivo de música.](images/content-view/deltalayoutmore.png)

-   Layout Delta quando o item tem entre 350 e 700 pixels de espaço horizontal.

    ![Diagrama que mostra um exemplo de layout Delta que tem entre 350 e 700 pixels de espaço horizontal.](images/content-view/layout8.png)

-   Exemplo do layout Delta quando o item tem entre 350 e 700 pixels de espaço horizontal.

    ![exemplo de layout de Delta](images/content-view/deltaviewbetween.png)

-   Layout Delta quando o item tem menos de 350 pixels de espaço horizontal.

    ![exemplo de layout](images/content-view/layout9.png)

-   Exemplo do layout Delta quando o item tem menos de 350 pixels de espaço horizontal.

    ![Captura de tela que mostra um exemplo de layout Delta para um arquivo de música com menos de 350 pixels de espaço horizontal.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a>Etapa 3: registrar Propriedades personalizadas e layout para o tipo de arquivo

Depois de entender o modo de resultado da pesquisa, o modo de procura e os padrões de layout, você pode registrar uma lista de propriedades Personalizada para o tipo de arquivo.

**Para registrar uma lista de propriedades personalizadas e um padrão de layout para o tipo de arquivo.**

1.  Escolha entre os quatro padrões de layout: alfa, beta, gama ou Delta.
2.  Considere as seguintes regras de formatação, que se aplicam igualmente a todos os quatro padrões de layout:
    -   A propriedade 1 é sempre exibida em um tamanho de fonte maior. O tamanho de fonte grande geralmente usado para o nome do item, mas também pode ser usado para a propriedade de âncora ou outro item.
    -   A propriedade 4 destina-se a trechos nos padrões de layout alfa, beta e gama. Essa propriedade é alocada mais espaço nesses padrões e é exibida em uma cor de fonte cinza, em oposição a preto, como as outras propriedades, para ajudá-lo a destacar.
    -   As medidas de pixel abaixo estão em pixels relativos e o tamanho inclui o ícone/miniatura à esquerda das propriedades e o espaço entre o ícone/miniatura e o retângulo de seleção.
    -   A maioria das propriedades tem um tamanho de exibição mínimo. Portanto, eles não serão exibidos se não houver espaço suficiente para eles em um tamanho de exibição específico. O tamanho mínimo geralmente é de 100 pixels de largura.
    -   Cada padrão de layout define o número de linhas e o número de propriedades em cada linha.
3.  Decida quais propriedades você deseja exibir no layout e qual Propriedade deseja exibir em cada local. Ao decidir qual propriedade será exibida em cada posição no layout, considere o comprimento típico da propriedade, sua importância para o usuário e se ela deve ser descartada quando o tamanho da janela for muito pequeno para conter todas as propriedades.
4.  Registre um padrão de layout e uma lista de propriedades para o tipo de arquivo ou tipo de item adicionando as seguintes chaves na chave do registro ProgID para o tipo de arquivo ou item (neste exemplo, para o tipo de arquivo. xyz).

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  Observe as seguintes diretrizes de formatação para registrar Propriedades:

    -   Cada registro começa com `prop:`
    -   Cada propriedade requer o nome completo da propriedade.
    -   As propriedades são separadas por um ponto-e-vírgula sem espaço.
    -   As propriedades são exibidas na ordem definida pelo padrão de layout selecionado.
    -   `~` indica que o rótulo da propriedade não deve ser exibido.
    -   `~System.LayoutPattern.PlaceHolder` deve ser usado se você quiser deixar em branco uma propriedade especificada no padrão de layout.

    A chave do registro de exemplo a seguir ilustra essas diretrizes de formatação.

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    Os valores possíveis para (ContentViewModeForBrowse) incluem o seguinte: prop: ~ System. ItemNameDisplay; System. Author; System. LayoutPattern. PlaceHolder; As palavras-chave System. System. DateModified; ~ System. Size

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Nomes de tipos](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[System. PropList. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[System. PropList. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
