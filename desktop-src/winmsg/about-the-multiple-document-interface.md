---
description: Cada documento em um aplicativo MDI (interface de vários documentos) é exibido em uma janela filho separada dentro da área do cliente da janela principal do aplicativo.
ms.assetid: 35dff281-3b11-4954-85cf-a0f1c9ed346a
title: Sobre a interface de vários documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071d3bebad8e6aba48b69b66fd41f9f7933c1d9785ae38512003aaf1bd9a19e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705992"
---
# <a name="about-the-multiple-document-interface"></a>Sobre a interface de vários documentos

Cada documento em um aplicativo MDI (interface de vários documentos) é exibido em uma janela filho separada dentro da área do cliente da janela principal do aplicativo. Os aplicativos MDI típicos incluem aplicativos de processamento de palavras que permitem que o usuário trabalhe com vários documentos de texto e aplicativos de planilha que permitem que o usuário trabalhe com vários gráficos e planilhas. Para obter mais informações, consulte estes tópicos.

-   [Estrutura, cliente e Windows](#frame-client-and-child-windows)
-   [Criação de janela filho](#child-window-creation)
-   [Ativação da janela filho](#child-window-activation)
-   [Menus de vários documentos](#multiple-document-menus)
-   [Vários aceleradores de documento](#multiple-document-accelerators)
-   [Tamanho e disposição da janela filho](#child-window-size-and-arrangement)
-   [Ícone Título Windows](#icon-title-windows)
-   [Dados da janela filho](#child-window-data)
    -   [Estrutura da janela](#window-structure)
    -   [Propriedades da janela](#window-properties)

## <a name="frame-client-and-child-windows"></a>Estrutura, cliente e Windows

Um aplicativo MDI tem três tipos de janelas: uma janela de quadro, uma janela de cliente MDI, bem como várias janelas filho. A *janela do quadro* é como a janela principal do aplicativo: ela tem uma borda deizing, uma barra de título, um menu de janela, um botão minimizar e um botão maximizar. O aplicativo deve registrar uma classe de janela para a janela de quadro e fornecer um procedimento de janela para dar suporte a ela.

Um aplicativo MDI não exibe a saída na área do cliente da janela do quadro. Em vez disso, ele exibe a janela do cliente MDI. Uma *janela de cliente MDI* é um tipo especial de janela filho pertencente à classe de janela pré-registro **MDICLIENT.** A janela do cliente é um filho da janela do quadro; ele serve como a plano de fundo para janelas filho. Ele também fornece suporte para criar e manipular janelas filho. Por exemplo, um aplicativo MDI pode criar, ativar ou maximizar janelas filho enviando mensagens para a janela do cliente MDI.

Quando o usuário abre ou cria um documento, a janela do cliente cria uma janela filho para o documento. A janela do cliente é a janela pai de todas as janelas filho MDI no aplicativo. Cada janela filho tem uma borda deizing, uma barra de título, um menu de janela, um botão minimizar e um botão maximizar. Como uma janela filho é recortada, ela é limitada à janela do cliente e não pode aparecer fora dela.

Um aplicativo MDI pode dar suporte a mais de um tipo de documento. Por exemplo, um aplicativo de planilha típico permite que o usuário trabalhe com gráficos e planilhas. Para cada tipo de documento compatível, um aplicativo MDI deve registrar uma classe de janela filho e fornecer um procedimento de janela para dar suporte às janelas que pertencem a essa classe. Para obter mais informações sobre classes de janela, consulte [Classes de janela](window-classes.md). Para obter mais informações sobre procedimentos de janela, consulte [Procedimentos de janela.](window-procedures.md)

A seguir está um aplicativo MDI típico. Ele é denominado Multipad.

![janela de quadro do aplicativo mdi multipad e janela do cliente](images/csmdi-01.png)

## <a name="child-window-creation"></a>Criação de janela filho

Para criar uma janela filho, um aplicativo MDI chama a função [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) ou envia a mensagem [**WM \_ MDICREATE**](wm-mdicreate.md) para a janela do cliente MDI. Uma maneira mais eficiente de criar uma janela filho MDI é chamar a função [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) especificando o estilo estendido **\_ \_ MDICHILD do WS EX.**

Para destruir uma janela filho, um aplicativo MDI envia uma mensagem [**WM \_ MDIDESTROY**](wm-mdidestroy.md) para a janela do cliente MDI.

## <a name="child-window-activation"></a>Ativação da janela filho

Qualquer número de janelas filho pode aparecer na janela do cliente a qualquer momento, mas apenas uma pode estar ativa. A janela filho ativa é posicionada na frente de todas as outras janelas filho e sua borda é realçada.

O usuário pode ativar uma janela filho inativa clicando nele. Um aplicativo MDI ativa uma janela filho enviando uma mensagem [**WM \_ MDIACTIVATE**](wm-mdiactivate.md) para a janela do cliente MDI. À medida que a janela do cliente processa essa mensagem, ela envia uma mensagem **WM \_ MDIACTIVATE** para o procedimento de janela da janela filho a ser ativada e para o procedimento de janela da janela filho que está sendo desativada.

Para impedir que uma janela filho seja ativa, manipular a mensagem [**WM \_ NCACTIVATE**](wm-ncactivate.md) para a janela filho retornando **FALSE.**

O sistema mantém o controle da posição de cada janela filho na pilha de janelas sobrepostas. Esse empilhamento é conhecido como Ordem [Z.](window-features.md) O usuário pode ativar a próxima janela filho na ordem Z clicando em **Próximo** no menu da janela na janela ativa. Um aplicativo ativa a próxima janela filho (ou anterior) na ordem Z enviando uma mensagem [**WM \_ MMAXXT**](wm-mdinext.md) para a janela do cliente.

Para recuperar o handle para a janela filho ativa, o aplicativo MDI envia uma mensagem [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md) para a janela do cliente.

## <a name="multiple-document-menus"></a>Menus de vários documentos

A janela de quadro de um aplicativo MDI deve incluir uma barra de menus com um menu de janela. O menu da janela deve incluir itens que organizam as janelas filho dentro da janela do cliente ou que fecham todas as janelas filho. O menu de janela de um aplicativo MDI típico pode incluir os itens na tabela a seguir.



| Item de menu         | Finalidade                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Tile**          | Organiza as janelas filho em um formato de lado para que cada uma apareça inteiramente na janela do cliente.                       |
| **Cascata**       | Organiza janelas filho em um formato em cascata. As janelas filho se sobrepõem umas às outras, mas a barra de título de cada uma delas é visível. |
| **Organizar Ícones** | Organiza os ícones de janelas filho minimizadas na parte inferior da janela do cliente.                                     |
| **Fechar tudo**     | Fecha todas as janelas filho.                                                                                                |



 

Sempre que uma janela filho é criada, o sistema anexa automaticamente um novo item de menu ao menu da janela. O texto do item de menu é o mesmo que o texto na barra de menus da nova janela filho. Clicando no item de menu, o usuário pode ativar a janela filho correspondente. Quando uma janela filho é destruída, o sistema remove automaticamente o item de menu correspondente do menu da janela.

O sistema pode adicionar até dez itens de menu ao menu da janela. Quando a décimo janela filho é criada, o sistema adiciona o item **Mais Windows** ao menu da janela. Clicar nesse item exibe a caixa **de diálogo Selecionar** Janela. A caixa de diálogo contém uma caixa de listagem com os títulos de todas as janelas filho MDI disponíveis no momento. O usuário pode ativar uma janela filho clicando em seu título na caixa de listagem.

Se o aplicativo MDI dá suporte a vários tipos de janelas filho, adapte a barra de menus para refletir as operações associadas à janela ativa. Para fazer isso, forneça recursos de menu separados para cada tipo de janela filho compatível com o aplicativo. Quando um novo tipo de janela filho é ativado, o aplicativo deve enviar uma mensagem [**WM \_ MDISETMENU**](wm-mdisetmenu.md) para a janela do cliente, passando para ela o identificador para o menu correspondente.

Quando não houver nenhuma janela filho, a barra de menus deverá conter apenas itens usados para criar ou abrir um documento.

Quando o usuário está navegando pelos menus de um aplicativo MDI usando chaves de cursor, as chaves se comportam de maneira diferente de quando o usuário está navegando pelos menus típicos de um aplicativo. Em um aplicativo MDI, o controle passa do menu de janela do aplicativo para o menu de janela da janela filho ativa e, em seguida, para o primeiro item na barra de menus.

## <a name="multiple-document-accelerators"></a>Vários aceleradores de documento

Para receber e processar chaves de acelerador para suas janelas filho, um aplicativo MDI deve incluir a [**função TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) em seu loop de mensagem. O loop deve chamar **TranslateMDISysAccel** antes de chamar a [**função TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) ou [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)

As teclas de acelerador no menu da janela para uma janela filho MDI são diferentes daquelas para uma janela filho não MDI. Em uma janela filho MDI, a combinação de teclas ALT+ – (menos) abre o menu da janela, a combinação de teclas CTRL+F4 fecha a janela filho ativa e a combinação de teclas CTRL+F6 ativa a próxima janela filho.

## <a name="child-window-size-and-arrangement"></a>Tamanho e disposição da janela filho

Um aplicativo MDI controla o tamanho e a posição de suas janelas filho enviando mensagens para a janela do cliente MDI. Para maximizar a janela filho ativa, o aplicativo envia a mensagem [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md) para a janela do cliente. Quando uma janela filho é maximizada, sua área de cliente preenche completamente a janela do cliente MDI. Além disso, o sistema oculta automaticamente a barra de título da janela filho e adiciona o ícone de menu da janela filho e o botão Restaurar à barra de menus do aplicativo MDI. O aplicativo pode restaurar a janela do cliente para seu tamanho e posição originais (pré-otimizadas) enviando à janela do cliente uma mensagem [**WM \_ MDIRESTORE.**](wm-mdirestore.md)

Um aplicativo MDI pode organizar suas janelas filho em um formato em cascata ou em um formato de parte. Quando as janelas filho são em cascata, as janelas aparecem em uma pilha. A janela na parte inferior da pilha ocupa o canto superior esquerdo da tela e as janelas restantes são deslocadas vertical e horizontalmente para que a borda esquerda e a barra de título de cada janela filho sejam visíveis. Para organizar janelas filho no formato em cascata, um aplicativo MDI envia a mensagem [**WM \_ MDICASCADE.**](wm-mdicascade.md) Normalmente, o aplicativo envia essa mensagem quando o usuário clica em **Cascata** no menu da janela.

Quando as janelas filhas são enlados, o sistema exibe cada janela filho em sua totalidade, sobrepondo nenhuma das janelas. Todas as janelas são dimensionadas, conforme necessário, para caber na janela do cliente. Para organizar as janelas filhas no formato de bloco, um aplicativo MDI envia uma mensagem do [**WM \_ MDITILE**](wm-mditile.md) para a janela do cliente. Normalmente, o aplicativo envia essa mensagem quando o usuário clica em **bloco** no menu janela.

Um aplicativo MDI deve fornecer um ícone diferente para cada tipo de janela filho com suporte. O aplicativo especifica um ícone ao registrar a classe de janela filho. O sistema exibe automaticamente o ícone de uma janela filho na parte inferior da janela do cliente quando a janela filho é minimizada. Um aplicativo MDI direciona o sistema para organizar ícones de janela filho enviando uma mensagem do [**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md) para a janela do cliente. Normalmente, o aplicativo envia essa mensagem quando o usuário clica em **organizar ícones** no menu janela.

## <a name="icon-title-windows"></a>Título do ícone Windows

Como as janelas filhas MDI podem ser minimizadas, um aplicativo MDI deve evitar manipular janelas de título de ícone como se fossem janelas filho MDI normais. O título do ícone janelas aparece quando o aplicativo enumera janelas filhas da janela do cliente MDI. Janelas de título de ícone diferem de outras janelas filhas, no entanto, no caso de propriedade de uma janela filho MDI.

Para determinar se uma janela filho é uma janela de título de ícone, use a função [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) com o \_ índice de proprietário GW. Janelas sem título retornam **NULL**. Observe que esse teste é insuficiente para janelas de nível superior, porque os menus e caixas de diálogo são janelas de propriedade.

## <a name="child-window-data"></a>Dados da janela filho

Como o número de janelas filhas varia dependendo de quantos documentos o usuário abre, um aplicativo MDI deve ser capaz de associar dados (por exemplo, o nome do arquivo atual) a cada janela filho. Há duas maneiras de fazer isso:

-   Armazene os dados da janela filho na estrutura da janela.
-   Use as propriedades da janela.

### <a name="window-structure"></a>Estrutura da janela

Quando um aplicativo MDI registra uma classe de janela, ele pode reservar espaço extra na estrutura de janela para dados de aplicativo específicos para essa classe específica do Windows. Para armazenar e recuperar dados nesse espaço extra, o aplicativo usa as funções [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Para manter uma grande quantidade de dados para uma janela filho, um aplicativo pode alocar memória para uma estrutura de dados e, em seguida, armazenar o identificador na memória que contém a estrutura no espaço extra associado à janela filho.

### <a name="window-properties"></a>Propriedades da janela

Um aplicativo MDI também pode armazenar dados por documento usando as propriedades da janela. Os *dados por documento* são dados específicos para o tipo de documento contido em uma janela filho específica. As propriedades são diferentes de espaço extra na estrutura de janela, pois você não precisa alocar espaço extra ao registrar a classe de janela. Uma janela pode ter qualquer número de propriedades. Além disso, onde os deslocamentos são usados para acessar o espaço extra em estruturas de janela, as propriedades são referenciadas por nomes de cadeia de caracteres. Para obter mais informações sobre as propriedades da janela, consulte [Propriedades da janela](window-properties.md).

 

 
