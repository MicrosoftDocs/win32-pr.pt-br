---
title: Sobre os controles da barra de ferramentas
description: Uma barra de ferramentas é um controle que contém um ou mais botões.
ms.assetid: b5a00a81-8d23-4844-8b0a-776e7cceced8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f615da972f14bb88c4915504c089dd6b40d9aca
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424146"
---
# <a name="about-toolbar-controls"></a>Sobre os controles da barra de ferramentas

Uma barra de ferramentas é um controle que contém um ou mais botões. Cada botão, quando clicado por um usuário, envia uma mensagem de comando para a janela pai. Normalmente, os botões em uma barra de ferramentas correspondem aos itens no menu do aplicativo, fornecendo uma maneira adicional e mais direta para que o usuário acesse os comandos de um aplicativo.

A captura de tela a seguir mostra uma janela que contém uma barra de ferramentas simples para operações de arquivo. O aplicativo habilitou estilos visuais. O botão salvar é "quente" porque o cursor estava passando por ele quando a captura de tela foi tomada. A aparência real do controle varia dependendo do sistema operacional e do tema selecionado pelo usuário.

![captura de tela de uma janela com uma barra de ferramentas de três botões; um botão está quente](images/tb-withstyles.png)

A captura de tela a seguir mostra o mesmo controle em um aplicativo que foi compilado sem estilos visuais habilitados.

![captura de tela de uma janela sem estilos visuais: nenhum dos botões parece quente](images/tb-wostyles.png)

Os tópicos a seguir discutem os recursos a serem considerados ao planejar uma barra de ferramentas. Para obter informações específicas sobre implementação e código de exemplo, consulte [usando controles da barra de ferramentas](using-toolbar-controls.md).

-   [Especificando o tamanho e a posição da barra de ferramentas](#specifying-toolbar-size-and-position)
-   [Barras de ferramentas transparentes](#transparent-toolbars)
-   [Barras de ferramentas de estilo de lista](#list-style-toolbars)
-   [Definindo imagens de botão](#defining-button-images)
    -   [Definindo imagens de botão usando bitmaps](#defining-button-images-by-using-bitmaps)
    -   [Definindo imagens de botão usando listas de imagens](#defining-button-images-by-using-image-lists)
-   [Definindo texto para botões](#defining-text-for-buttons)
-   [Adicionando botões da barra de ferramentas](#adding-toolbar-buttons)
    -   [Estilos de botão da barra de ferramentas](#toolbar-button-styles)
    -   [Estados do botão de barra de ferramentas](#toolbar-button-states)
    -   [Identificador de comando](#command-identifier)
    -   [Tamanho e posição do botão](#button-size-and-position)
-   [Habilitando a personalização](#enabling-customization)
-   [Habilitando o acompanhamento a quente](#enabling-hot-tracking)

## <a name="specifying-toolbar-size-and-position"></a>Especificando o tamanho e a posição da barra de ferramentas

Se você criar uma barra de ferramentas usando [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), a função permitirá que você especifique em pixels a altura e a largura da barra de ferramentas.

> [!Note]  
> Não [**é recomendável usar CreateToolbarEx,**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) pois ele não dá suporte a novos recursos de barras de ferramentas, incluindo listas de imagens. Para obter mais informações sobre como criar barras de ferramentas, consulte [Usando controles de barra de ferramentas](using-toolbar-controls.md).

 

A [**função CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) não tem parâmetros para especificar o tamanho da barra de ferramentas. O procedimento da janela da barra de ferramentas define automaticamente o tamanho e a posição da janela da barra de ferramentas. A altura é baseada na altura dos botões na barra de ferramentas. A largura é igual à largura da área de cliente da janela pai. Para alterar as configurações de tamanho automático, envie uma [**mensagem TB \_ SETBUTTONSIZE.**](tb-setbuttonsize.md) Os estilos de controle comuns [**CCS \_ TOP**](common-control-styles.md) e [**CCS \_ BOTTOM**](common-control-styles.md) determinam se a barra de ferramentas está posicionada ao longo da parte superior ou inferior da área do cliente. Por padrão, uma barra de ferramentas tem o **estilo CCS \_ TOP.**

Além disso, o procedimento da janela barra de ferramentas ajusta automaticamente o tamanho da barra de ferramentas sempre que recebe um [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) ou uma mensagem de dimensionamento de [**TB \_**](tb-autosize.md) . Um aplicativo deve enviar qualquer uma dessas mensagens sempre que o tamanho da janela pai for alterado ou depois de enviar uma mensagem que requer o ajuste do tamanho da barra de ferramentas — por exemplo, uma mensagem de [**TB \_ SetButtons**](tb-setbuttonsize.md) .

Os comportamentos de dimensionamento e posicionamento padrão da barra de ferramentas podem ser desativados definindo os estilos de controle comum de [**ccs \_ noResize**](common-control-styles.md) e [**ccs \_ NOPARENTALIGN**](common-control-styles.md) . Os controles de barra de ferramentas hospedados por controles Rebar devem definir esses estilos porque o controle rebar dimensiona e posiciona a barra de ferramentas.

## <a name="transparent-toolbars"></a>Barras de ferramentas transparentes

Os controles da barra de ferramentas dão suporte a uma aparência transparente que permite que a área do cliente na barra de ferramentas seja mostrada. Há dois tipos de barras de ferramentas transparentes, aquelas com botões simples e aquelas com botões tridimensionais. Se você quiser que seu aplicativo corresponda à interface do Windows, use a barra de ferramentas de estilo transparente.

A captura de tela a seguir mostra os dois tipos de barras de ferramentas transparentes, não usando estilos visuais.

![captura de tela de duas janelas com estilos diferentes de barras de ferramentas, mas ambas as barras de ferramentas são transparentes](images/toolbartrans.jpg)

A captura de tela a seguir mostra uma barra de ferramentas transparente, como pode aparecer no Windows Vista, com os estilos visuais habilitados. A cor do plano de fundo da caixa de diálogo foi alterada para tornar a transparência mais óbvia.

![captura de tela de uma janela no Windows Vista com uma barra de ferramentas transparente](images/tb-transparent.png)

Para criar uma barra de ferramentas transparente, tudo o que você precisa fazer é adicionar [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) ou [**TBSTYLE \_ transparente**](toolbar-control-and-button-styles.md) ao parâmetro de estilo de janela de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Se você não quiser que uma linha apareça para indicar a parte inferior da barra de ferramentas, não use o estilo de janela [**WS \_ Border**](/windows/desktop/winmsg/window-styles) .

> [!Note]  
> Ao usar estilos visuais, as barras de ferramentas podem ser simples por padrão.

 

## <a name="list-style-toolbars"></a>Barras de ferramentas de estilo de lista

Os botões da barra de ferramentas permitem exibir texto e bitmaps. Os botões em uma barra de ferramentas criados com o estilo [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) agem texto à direita do bitmap em vez de abaixo dele.

A captura de tela a seguir mostra uma barra de ferramentas com o estilo de lista.

![captura de tela de uma barra de ferramentas com texto à direita de cada ícone](images/tb-liststyle.png)

Você pode usar o estilo da barra de ferramentas [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) em combinação com o estilo [**\_ TBSTYLE FLAT**](toolbar-control-and-button-styles.md) para criar uma barra de ferramentas com botões simples.

## <a name="defining-button-images"></a>Definindo imagens de botão

Há duas maneiras de especificar as imagens para botões– por bitmaps ou por listas de imagens. Um aplicativo deve escolher qual método usar. Ele não pode usar ambos os métodos com o mesmo controle de barra de ferramentas. Observe que a [**função CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) usa o método bitmap. Os aplicativos que querem usar o método de lista de imagens devem usar a [**função CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar o controle de barra de ferramentas.

### <a name="defining-button-images-by-using-bitmaps"></a>Definindo imagens de botão usando bitmaps

Cada botão em uma barra de ferramentas pode incluir uma imagem bit a bit. Uma barra de ferramentas usa uma lista interna para armazenar as informações necessárias para desenhar as imagens. Quando você chama a [**função CreateToolbarEx,**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) especifica um bitmap monocromático ou de cor que contém as imagens iniciais e a barra de ferramentas adiciona as informações à lista interna de imagens. Você pode adicionar imagens adicionais posteriormente usando a [**mensagem \_ ADDBITMAP de**](tb-addbitmap.md) TB.

Cada imagem tem um índice baseado em zero. A primeira imagem adicionada à lista interna tem um índice de 0, a segunda imagem tem um índice de 1 e assim por diante. [**TB \_ ADDBITMAP**](tb-addbitmap.md) adiciona imagens ao final da lista e retorna o índice da primeira nova imagem adicionada. Para associar a imagem a um botão, é necessário enviar uma mensagem [**\_ ADDBUTTONS de TB**](tb-addbuttons.md) e especificar o índice da imagem depois de adicionar bitmaps à lista de imagens internas.

O Windows pressupõe que todas as imagens de bitmap de uma barra de ferramentas têm o mesmo tamanho. Você especifica o tamanho ao criar a barra de ferramentas usando [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex). Se você usar a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar uma barra de ferramentas, o tamanho das imagens será definido como as dimensões padrão de 16 por 15 pixels. Você pode usar a mensagem [**TB \_ SETBITMAPSIZE**](tb-setbitmapsize.md) para alterar as dimensões das imagens de bitmap, mas deve fazê-lo antes de adicionar qualquer imagem à lista interna.

### <a name="defining-button-images-by-using-image-lists"></a>Definindo imagens de botão usando listas de imagens

Você também pode armazenar imagens de botão em um conjunto de [listas de imagens](image-lists.md). Uma lista de imagens é uma coleção de imagens do mesmo tamanho, cada uma das quais pode ser referenciada por seu índice. As listas de imagens são usadas para gerenciar grandes conjuntos de ícones ou bitmaps. Você pode usar até três listas de imagens diferentes para exibir botões em vários Estados, conforme mostrado na tabela a seguir.



|  Estado        |  Descrição                                                                                                                                                                                            |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Normal   | Botões em seu estado padrão.                                                                                                                                                              |
| Frequente      | Botões que estão sob o ponteiro ou pressionados. Itens ativos têm suporte apenas em controles de barra de ferramentas que têm o estilo [**\_ simples TBSTYLE**](toolbar-control-and-button-styles.md) . |
| Desabilitado | Botões que estão desabilitados.                                                                                                                                                                   |



 

Depois que a barra de ferramentas é destruída, os aplicativos devem liberar qualquer lista de imagens que tenham criado.

## <a name="defining-text-for-buttons"></a>Definindo texto para botões

Cada botão pode exibir uma cadeia de caracteres, além de, ou em vez de, uma imagem. Uma barra de ferramentas mantém uma lista interna que contém todas as cadeias de caracteres disponíveis para botões da barra de ferramentas. Você adiciona cadeias de caracteres à lista interna usando a mensagem [**TB \_ AddString**](tb-addstring.md) , especificando o endereço do buffer que contém as cadeias de caracteres a serem adicionadas. Cada cadeia de caracteres deve ser terminada em nulo e a última cadeia de caracteres deve ser terminada com dois caracteres nulos.

Cada cadeia de caracteres tem um índice de base zero. A primeira cadeia de caracteres adicionada à lista interna de cadeias de caracteres tem um índice de 0, a segunda cadeia de caracteres tem um índice de 1 e assim por diante. [**TB \_ ADDSTRING**](tb-addstring.md) adiciona cadeias de caracteres ao final da lista e retorna o índice da primeira nova cadeia de caracteres. Você usa o índice de uma cadeia de caracteres para associar a cadeia de caracteres a um botão.

Usar [**TB \_ ADDSTRING**](tb-addstring.md) não é a única maneira de adicionar cadeias de caracteres a uma barra de ferramentas. Você pode exibir uma cadeia de caracteres em um botão passando um ponteiro de cadeia de caracteres no membro **iString** da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que é passada para [**\_ ADDBUTTONS de TB.**](tb-addbuttons.md) Além disso, você pode usar [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) para atribuir texto a um botão de barra de ferramentas.

## <a name="adding-toolbar-buttons"></a>Adicionando botões da barra de ferramentas

Se você usar a função [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) para criar uma barra de ferramentas, poderá adicionar botões à barra de ferramentas preenchendo uma matriz de estruturas [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) e especificando o endereço da matriz na chamada de função. No entanto, [**a função CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) não tem um parâmetro para passar uma **estrutura TBBUTTON.** **CreateWindowEx** cria uma barra de ferramentas vazia que você preenche enviando uma mensagem [**\_ ADDBUTTONS de TB,**](tb-addbuttons.md) especificando o endereço de uma **estrutura TBBUTTON.**

Depois que uma barra de ferramentas é criada, você pode adicionar botões enviando uma [**mensagem TB \_ INSERTBUTTON**](tb-insertbutton.md) ou [**TB \_ ADDBUTTONS.**](tb-addbuttons.md) Cada botão é descrito por uma estrutura [**TBBUTTON,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que define os atributos do botão, incluindo os índices de sua cadeia de caracteres e bitmap, bem como seu estilo, estado, identificador de comando e valor de 32 bits definido pelo aplicativo.

> [!Note]  
> Se você usar a [**função CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar uma barra de ferramentas, deverá enviar a mensagem [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) antes de adicionar qualquer botão. A mensagem passa o tamanho da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) para a barra de ferramentas.

 

### <a name="toolbar-button-styles"></a>Estilos de botão da barra de ferramentas

O estilo de um botão determina como o botão é exibido e como ele responde à entrada do usuário. Por exemplo, o estilo do [**\_ botão BTNS**](toolbar-control-and-button-styles.md) cria um botão da barra de ferramentas que se comporta como um botão de ação padrão. Um botão que tem o estilo de [**\_ verificação BTNS**](toolbar-control-and-button-styles.md) é semelhante a um botão de push padrão, exceto pelo fato de alternar entre os Estados pressionados e não prensados sempre que o usuário clicar nele.

Você pode criar grupos de botões da barra de ferramentas que atuam como botões de opção usando o [**\_ grupo BTNS**](toolbar-control-and-button-styles.md) ou o estilo de [**BTNS \_ check-in**](toolbar-control-and-button-styles.md) . Isso faz com que um botão permaneça pressionado até que o usuário escolha outro botão no grupo. Um grupo é definido como uma coleção contígua de botões, tudo com o estilo BTNS ou **BTNS \_** do **\_ grupo** de verificação.

O estilo [**BTNS \_ Sep**](toolbar-control-and-button-styles.md) cria uma pequena lacuna entre os botões ou desenha um entalhe entre os botões em barras de ferramentas simples. Um botão com o estilo **BTNS \_ Sep** não recebe a entrada do usuário.

A versão 5,80 dos controles comuns introduziu alguns novos estilos de botão da barra de ferramentas e renomeou alguns dos estilos mais antigos. Todos os sinalizadores de estilo de botão agora começam com BTNS \_ XXX em vez de TBSTYLE \_ xxx. Para obter uma listagem e uma discussão sobre os estilos de botão, consulte [controle da barra de ferramentas e estilos de botão](toolbar-control-and-button-styles.md).

### <a name="toolbar-button-states"></a>Estados de botão da barra de ferramentas

Cada botão em uma barra de ferramentas tem um estado. A barra de ferramentas atualiza o estado de um botão para refletir as ações do usuário, como clicar no botão. O estado indica se o botão está pressionado ou não pressionado, habilitado ou desabilitado, oculto ou visível. Embora um aplicativo defina o estado inicial de um botão ao adicionar o botão à barra de ferramentas, ele pode alterar e recuperar o estado enviando mensagens de [**TB \_ SetState**](tb-getstate.md) e [**TB \_ SetState**](tb-setstate.md) para a barra de ferramentas. Para obter uma lista de Estados de botão da barra de ferramentas, consulte [Estados da barra de ferramentas](toolbar-button-states.md).

### <a name="command-identifier"></a>Identificador de comando

Cada botão tem um identificador de comando definido pelo aplicativo associado a ele. Os identificadores de botão geralmente são definidos em um arquivo de header de aplicativo. Por exemplo, um botão Colar pode ser definido como:


```
#define ID_PASTE 100
```



Quando o usuário seleciona um botão, a barra de ferramentas envia à janela pai uma mensagem [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) ou [**WM \_ NOTIFY**](wm-notify.md) que inclui o identificador de comando do botão. A janela pai examina o identificador de comando e executa o comando associado ao botão. Para obter informações sobre quando os controles enviam mensagens **WM \_ COMMAND** e quando enviam **WM \_ NOTIFY,** consulte a seção Comentários da documentação [**do WM \_ NOTIFY.**](wm-notify.md)

### <a name="button-size-and-position"></a>Tamanho e posição do botão

Uma barra de ferramentas acompanha seus botões atribuindo a cada botão um índice de posição. O índice é baseado em zero; ou seja, o botão mais à esquerda tem um índice de 0, o próximo botão à direita tem um índice de 1 e assim por diante. Um aplicativo deve especificar o índice de um botão ao enviar mensagens para recuperar informações sobre o botão ou definir os atributos do botão.

Uma barra de ferramentas atualiza os índices de posição à medida que os botões são inseridos e removidos. Um aplicativo pode recuperar o índice de posição atual de um botão usando a [**mensagem \_ TB COMMANDTOINDEX.**](tb-commandtoindex.md) A mensagem especifica o identificador de comando de um botão e a janela da barra de ferramentas usa o identificador para localizar o botão e retornar seu índice de posição.

Todos os botões em uma barra de ferramentas têm o mesmo tamanho. A [**função CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) exige que você de definir o tamanho inicial dos botões ao criar a barra de ferramentas. Quando você usa a [**função CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o tamanho inicial é definido para as dimensões padrão de 24 por 22 pixels. Você pode usar a [**mensagem TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) para alterar o tamanho do botão, mas você deve fazer isso antes de adicionar qualquer botão à barra de ferramentas. A [**mensagem \_ GETITEMRECT**](tb-getitemrect.md) de TB recupera as dimensões atuais dos botões.

Quando você adiciona uma cadeia de caracteres que é maior do que qualquer cadeia de caracteres atualmente na barra de ferramentas, a barra de ferramentas redefine automaticamente a largura de seus botões. A largura é definida para acomodar a cadeia de caracteres mais longa na barra de ferramentas.

## <a name="enabling-customization"></a>Habilitando a personalização

Uma barra de ferramentas tem recursos de personalização internos que você pode disponibilizar para o usuário fornecendo à barra de ferramentas o estilo de controle comum [**\_ ajustável da CCS**](common-control-styles.md) . Os recursos de personalização permitem que o usuário arraste um botão para uma nova posição ou remova um botão arrastando-o para fora da barra de ferramentas. Além disso, o usuário pode clicar duas vezes na barra de ferramentas para exibir a caixa de diálogo Personalizar barra de ferramentas, que permite ao usuário adicionar, excluir e reorganizar botões da barra de ferramentas. Para exibir a caixa de diálogo, use a mensagem de [**\_ personalização de TB**](tb-customize.md) . Um aplicativo determina se os recursos de personalização estão disponíveis para o usuário e controla a extensão na qual o usuário pode personalizar a barra de ferramentas.

Como parte do processo de personalização, os aplicativos geralmente precisam salvar e restaurar o estado de uma barra de ferramentas. Por exemplo, muitos aplicativos armazenam o estado da barra de ferramentas antes que o usuário comece a personalizar a barra de ferramentas caso o usuário posteriormente queira restaurar a barra de ferramentas ao seu estado original. O controle Toolbar não mantém automaticamente um registro de seu estado de prepersonalização. Seu aplicativo deve salvar o estado da barra de ferramentas para restaurá-lo. Para obter mais informações, consulte [usando controles da barra de ferramentas](using-toolbar-controls.md).

## <a name="enabling-hot-tracking"></a>Habilitando o controle de acesso

Acompanhamento dinâmico significa que, quando o ponteiro se move sobre um item, a aparência do botão é alterada. Quando os estilos visuais são habilitados, as barras de ferramentas dão suporte ao acompanhamento dinâmico por padrão. Caso contrário, somente os controles da barra de ferramentas criados com o estilo [**\_ plano de TBSTYLE**](toolbar-control-and-button-styles.md) dão suporte ao acompanhamento de quente. Você pode usar outros estilos de janela em combinação com **TBSTYLE \_ Flat** para produzir barras de ferramentas que habilitam o controle de acesso, mas têm uma aparência diferente de uma barra de ferramentas simples. Para obter mais informações, consulte [usando controles da barra de ferramentas](using-toolbar-controls.md).

 

 