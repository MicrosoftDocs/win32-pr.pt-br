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

Cada documento em um aplicativo MDI (interface de vários documentos) é exibido em uma janela filho separada dentro da área do cliente da janela principal do aplicativo. Aplicativos MDI típicos incluem aplicativos de processamento de texto que permitem ao usuário trabalhar com vários documentos de texto e aplicativos de planilha que permitem que o usuário trabalhe com vários gráficos e planilhas. Para obter mais informações, consulte estes tópicos.

-   [Windows de quadro, cliente e filho](#frame-client-and-child-windows)
-   [Criação de janela filho](#child-window-creation)
-   [Ativação de janela filho](#child-window-activation)
-   [Vários menus de documentos](#multiple-document-menus)
-   [Vários aceleradores de documentos](#multiple-document-accelerators)
-   [Tamanho e organização da janela filho](#child-window-size-and-arrangement)
-   [Título do ícone Windows](#icon-title-windows)
-   [Dados da janela filho](#child-window-data)
    -   [Estrutura da janela](#window-structure)
    -   [Propriedades da janela](#window-properties)

## <a name="frame-client-and-child-windows"></a>Windows de quadro, cliente e filho

Um aplicativo MDI tem três tipos de janelas: uma janela de quadro, uma janela de cliente MDI, bem como várias janelas filhas. A *janela do quadro* é como a janela principal do aplicativo: ela tem uma borda de dimensionamento, uma barra de título, um menu de janela, um botão minimizar e um botão Maximizar. O aplicativo deve registrar uma classe de janela para a janela do quadro e fornecer um procedimento de janela para dar suporte a ela.

Um aplicativo MDI não exibe a saída na área do cliente da janela do quadro. Em vez disso, ele exibe a janela do cliente MDI. Uma *janela de cliente MDI* é um tipo especial de janela filho que pertence à classe de janela **MdiClient**. A janela do cliente é um filho da janela do quadro; Ele serve como o segundo plano para janelas filhas. Ele também fornece suporte para criar e manipular janelas filhas. Por exemplo, um aplicativo MDI pode criar, ativar ou maximizar as janelas filhas enviando mensagens para a janela do cliente MDI.

Quando o usuário abre ou cria um documento, a janela do cliente cria uma janela filho para o documento. A janela do cliente é a janela pai de todas as janelas filhas MDI no aplicativo. Cada janela filho tem uma borda de dimensionamento, uma barra de título, um menu de janela, um botão de minimização e um botão de maximização. Como uma janela filho é recortada, ela é confinada na janela do cliente e não pode aparecer fora dela.

Um aplicativo MDI pode dar suporte a mais de um tipo de documento. Por exemplo, um aplicativo de planilha típico permite que o usuário trabalhe com gráficos e planilhas. Para cada tipo de documento compatível, um aplicativo MDI deve registrar uma classe de janela filho e fornecer um procedimento de janela para dar suporte às janelas que pertencem a essa classe. Para obter mais informações sobre classes de janela, consulte [classes de janela](window-classes.md). Para obter mais informações sobre procedimentos de janela, consulte [procedimentos de janela](window-procedures.md).

A seguir está um aplicativo MDI típico. Ele é denominado Multipad.

![janela de quadro do aplicativo Multipad MDI e janela do cliente](images/csmdi-01.png)

## <a name="child-window-creation"></a>Criação de janela filho

Para criar uma janela filho, um aplicativo MDI chama a função [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) ou envia a mensagem [**\_ MDICREATE do WM**](wm-mdicreate.md) para a janela do cliente MDI. Uma maneira mais eficiente de criar uma janela filho MDI é chamar a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , especificando o estilo estendido **WS \_ ex \_ MDICHILD** .

Para destruir uma janela filho, um aplicativo MDI envia uma mensagem do [**WM \_ MDIDESTROY**](wm-mdidestroy.md) para a janela do cliente MDI.

## <a name="child-window-activation"></a>Ativação de janela filho

Qualquer número de janelas filhas pode aparecer na janela do cliente a qualquer momento, mas apenas uma pode estar ativa. A janela filho ativa é posicionada na frente de todas as outras janelas filhas e sua borda é realçada.

O usuário pode ativar uma janela filho inativa clicando nela. Um aplicativo MDI ativa uma janela filho enviando uma mensagem do [**WM \_ MDIACTIVATE**](wm-mdiactivate.md) para a janela do cliente MDI. À medida que a janela do cliente processa essa mensagem, ela envia uma mensagem do **WM \_ MDIACTIVATE** para o procedimento de janela da janela filho a ser ativada e para o procedimento de janela da janela filho sendo desativada.

Para impedir que uma janela filho seja ativada, manipule a mensagem do [**WM \_ NCACTIVATE**](wm-ncactivate.md) na janela filho retornando **false**.

O sistema mantém o controle da posição de cada janela filho na pilha de janelas sobrepostas. Esse empilhamento é conhecido como a [ordem Z](window-features.md). O usuário pode ativar a próxima janela filha na ordem Z clicando em **Avançar** no menu janela na janela ativa. Um aplicativo ativa a próxima janela filho (ou anterior) na ordem Z enviando uma mensagem do [**WM \_ MDINEXT**](wm-mdinext.md) para a janela do cliente.

Para recuperar o identificador para a janela filho ativa, o aplicativo MDI envia uma mensagem do [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md) para a janela do cliente.

## <a name="multiple-document-menus"></a>Vários menus de documentos

A janela do quadro de um aplicativo MDI deve incluir uma barra de menus com um menu de janela. O menu janela deve incluir itens que organizam as janelas filhas na janela do cliente ou que fecham todas as janelas filhas. O menu janela de um aplicativo MDI típico pode incluir os itens na tabela a seguir.



| Item de menu         | Finalidade                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Tile**          | Organiza as janelas filhas em um formato de bloco para que cada uma apareça em sua totalidade na janela do cliente.                       |
| **Cascade**       | Organiza as janelas filhas em um formato em cascata. As janelas filhas se sobrepõem uma à outra, mas a barra de título de cada uma é visível. |
| **Organizar Ícones** | Organiza os ícones de janelas filho minimizadas ao longo da parte inferior da janela do cliente.                                     |
| **Fechar tudo**     | Fecha todas as janelas filhas.                                                                                                |



 

Sempre que uma janela filho é criada, o sistema anexa automaticamente um novo item de menu ao menu janela. O texto do item de menu é o mesmo que o texto na barra de menus da nova janela filho. Ao clicar no item de menu, o usuário pode ativar a janela filho correspondente. Quando uma janela filho é destruída, o sistema remove automaticamente o item de menu correspondente do menu janela.

O sistema pode adicionar até dez itens de menu ao menu janela. quando a décima janela filho é criada, o sistema adiciona **mais Windows** item ao menu janela. Clicar neste item exibe a caixa de diálogo **selecionar janela** . A caixa de diálogo contém uma caixa de listagem com os títulos de todas as janelas filho MDI disponíveis no momento. O usuário pode ativar uma janela filho clicando em seu título na caixa de listagem.

Se o aplicativo MDI oferecer suporte a vários tipos de janelas filhas, personalize a barra de menus para refletir as operações associadas à janela ativa. Para fazer isso, forneça recursos de menu separados para cada tipo de janela filho ao qual o aplicativo dá suporte. Quando um novo tipo de janela filho é ativado, o aplicativo deve enviar uma mensagem do [**WM \_ MDISETMENU**](wm-mdisetmenu.md) para a janela do cliente, passando a ele o identificador para o menu correspondente.

Quando não existir nenhuma janela filho, a barra de menus deverá conter apenas os itens usados para criar ou abrir um documento.

Quando o usuário está navegando pelos menus de um aplicativo MDI usando chaves de cursor, as chaves se comportam de maneira diferente do que quando o usuário está navegando por meio de menus de um aplicativo típico. Em um aplicativo MDI, o controle passa do menu janela do aplicativo para o menu janela da janela filho ativa e, em seguida, para o primeiro item na barra de menus.

## <a name="multiple-document-accelerators"></a>Vários aceleradores de documentos

Para receber e processar chaves do acelerador para suas janelas filhas, um aplicativo MDI deve incluir a função [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) em seu loop de mensagem. O loop deve chamar **TranslateMDISysAccel** antes de chamar a função [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) ou [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .

Teclas de aceleração no menu janela de uma janela filho MDI são diferentes daquelas para uma janela filho não-MDI. Em uma janela filho MDI, a combinação de teclas ALT + – (menos) abre o menu janela, a combinação de teclas CTRL + F4 fecha a janela filho ativa e a combinação de teclas CTRL + F6 ativa a próxima janela filha.

## <a name="child-window-size-and-arrangement"></a>Tamanho e organização da janela filho

Um aplicativo MDI controla o tamanho e a posição de suas janelas filhas enviando mensagens para a janela do cliente MDI. Para maximizar a janela filho ativa, o aplicativo envia a mensagem do [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md) para a janela do cliente. Quando uma janela filho é maximizada, sua área de cliente preenche completamente a janela do cliente MDI. Além disso, o sistema oculta automaticamente a barra de título da janela filho e adiciona o botão do menu da janela filho e a botões restaurar à barra de menus do aplicativo MDI. O aplicativo pode restaurar a janela do cliente para seu tamanho original (premaximizado), enviando a janela do cliente uma mensagem do [**WM \_ MDIRESTORE**](wm-mdirestore.md) .

Um aplicativo MDI pode organizar suas janelas filhas em um formato em cascata ou em bloco. Quando as janelas filhas são colocadas em cascata, as janelas aparecem em uma pilha. A janela na parte inferior da pilha ocupa o canto superior esquerdo da tela, e as janelas restantes são deslocadas vertical e horizontalmente para que a borda esquerda e a barra de título de cada janela filho fiquem visíveis. Para organizar as janelas filhas no formato Cascade, um aplicativo MDI envia a mensagem do [**WM \_ MDICASCADE**](wm-mdicascade.md) . Normalmente, o aplicativo envia essa mensagem quando o usuário clica em **cascata** no menu janela.

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

 

 
