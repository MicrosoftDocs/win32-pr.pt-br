---
description: Este tópico descreve os elementos de programação que os aplicativos usam para criar e usar o Windows; gerenciar relações entre o Windows; e tamanho, movimentação e exibição de janelas.
ms.assetid: e325f8dc-004f-44a9-9122-3be5e44764d6
title: Sobre o Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2df510deea689d70bd1ebf5e59cafc92b0389d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169570"
---
# <a name="about-windows"></a>Sobre o Windows

Este tópico descreve os elementos de programação que os aplicativos usam para criar e usar o Windows; gerenciar relações entre o Windows; e tamanho, movimentação e exibição de janelas.

A visão geral inclui os tópicos a seguir.

-   [Janela da área de trabalho](#desktop-window)
-   [Janelas de aplicativos](#application-windows)
    -   [Área do cliente](#client-area)
    -   [Área não cliente](#nonclient-area)
-   [Controles e caixas de diálogo](#controls-and-dialog-boxes)
-   [Atributos da janela](#window-attributes)
    -   [Nome da Classe](#class-name)
    -   [Nome da janela](#window-name)
    -   [Estilo de Janela](#window-style)
    -   [Estilo de janela estendida](#extended-window-style)
    -   [Posição](#position)
    -   [Tamanho](#size)
    -   [Identificador de janela pai ou proprietário](#parent-or-owner-window-handle)
    -   [Manipulador de menu ou identificador de Child-Window](#menu-handle-or-child-window-identifier)
    -   [Identificador de instância do aplicativo](#application-instance-handle)
    -   [Dados de criação](#creation-data)
    -   [Identificador da Janela](#window-handle)
-   [Criação de janela](#creation-data)
    -   [Criação da janela principal](#main-window-creation)
    -   [Mensagens de criação de janela](#window-creation-messages)
    -   [Aplicativos multithread](#multithread-applications)

## <a name="desktop-window"></a>Janela da área de trabalho

Quando você inicia o sistema, ele cria automaticamente a janela da área de trabalho. A *janela da área de trabalho* é uma janela definida pelo sistema que pinta o plano de fundo da tela e serve como a base para todas as janelas exibidas por todos os aplicativos.

A janela da área de trabalho usa um bitmap para pintar o plano de fundo da tela. O padrão criado pelo bitmap é chamado de *papel de parede da área de trabalho*. Por padrão, a janela da área de trabalho usa o bitmap de um arquivo. bmp especificado no registro como o papel de parede da área de trabalho.

A função [**GetDesktopWindow**](/windows/win32/api/winuser/nf-winuser-getdesktopwindow) retorna um identificador para a janela da área de trabalho.

Um aplicativo de configuração do sistema, como um item do painel de controle, altera o papel de parede da área de trabalho usando a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) com o parâmetro *WAction* definido como **SPI \_ SETDESKWALLPAPER** e o parâmetro *lpvParam* especificando um nome de arquivo de bitmap. Em seguida, o **SystemParametersInfo** carrega o bitmap do arquivo especificado, usa o bitmap para pintar o plano de fundo da tela e insere o novo nome do arquivo no registro.

## <a name="application-windows"></a>Janelas de aplicativos

Cada aplicativo gráfico baseado no Windows cria pelo menos uma janela, chamada de *janela principal*, que serve como a interface principal entre o usuário e o aplicativo. A maioria dos aplicativos também cria outras janelas, direta ou indiretamente, para executar tarefas relacionadas à janela principal. Cada janela desempenha uma parte na exibição da saída e no recebimento da entrada do usuário.

Quando você inicia um aplicativo, o sistema também associa um botão da barra de tarefas ao aplicativo. O *botão da barra de tarefas* contém o ícone e o título do programa. Quando o aplicativo está ativo, o botão da barra de tarefas é exibido no estado enviado por push.

Uma janela de aplicativo inclui elementos como uma barra de título, uma barra de menus, o menu de janela (anteriormente conhecido como menu do sistema), o botão minimizar, o botão Maximizar, o botão restaurar, o botão fechar, uma borda de dimensionamento, uma área de cliente, uma barra de rolagem horizontal e uma barra de rolagem vertical. A janela principal de um aplicativo normalmente inclui todos esses componentes. A ilustração a seguir mostra esses componentes em uma janela principal típica.

![janela típica](images/cswin-02.png)

### <a name="client-area"></a>Área do cliente

A *área do cliente* é a parte de uma janela em que o aplicativo exibe a saída, como texto ou elementos gráficos. Por exemplo, um aplicativo de publicação de área de trabalho exibe a página atual de um documento na área do cliente. O aplicativo deve fornecer uma função, chamada de procedimento de janela, para processar a entrada para a janela e exibir a saída na área do cliente. Para obter mais informações, consulte [procedimentos de janela](window-procedures.md).

### <a name="nonclient-area"></a>Área não cliente

A barra de título, a barra de menus, o menu janela, os botões minimizar e maximizar, a borda de dimensionamento e as barras de rolagem são referidos coletivamente como a área não- *cliente* da janela. O sistema gerencia a maioria dos aspectos da área que não são clientes; o aplicativo gerencia a aparência e o comportamento de sua área de cliente.

A *barra de título* exibe um ícone e uma linha de texto definidos pelo aplicativo; Normalmente, o texto especifica o nome do aplicativo ou indica a finalidade da janela. Um aplicativo especifica o ícone e o texto ao criar a janela. A barra de título também torna possível que o usuário mova a janela usando um mouse ou outro dispositivo apontador.

A maioria dos aplicativos inclui uma *barra de menus* que lista os comandos com suporte no aplicativo. Os itens na barra de menus representam as principais categorias de comandos. Clicar em um item na barra de menus normalmente abre um menu pop-up cujos itens correspondem às tarefas em uma determinada categoria. Ao clicar em um comando, o usuário direciona o aplicativo para executar uma tarefa.

O *menu janela* é criado e gerenciado pelo sistema. Ele contém um conjunto padrão de itens de menu que, quando escolhido pelo usuário, definem o tamanho ou a posição de uma janela, fecham o aplicativo ou executam tarefas. Para obter mais informações, consulte [menus](/windows/desktop/menurc/menus).

Os botões no canto superior direito afetam o tamanho e a posição da janela. Quando você clica no *botão Maximizar*, o sistema amplia a janela para o tamanho da tela e posiciona a janela, para que ela cubra toda a área de trabalho, menos a barra de tarefas. Ao mesmo tempo, o sistema substitui o botão Maximizar pelo botão restaurar. Quando você clica no *botão restaurar*, o sistema restaura a janela para o tamanho e a posição anteriores. Quando você clica no *botão minimizar*, o sistema reduz a janela ao tamanho de seu botão da barra de tarefas, posiciona a janela sobre o botão da barra de tarefas e exibe o botão da barra de tarefas em seu estado normal. Para restaurar o aplicativo para o tamanho e a posição anteriores, clique no botão da barra de tarefas. Quando você clica no *botão fechar*, o aplicativo é encerrado.

A *borda de dimensionamento* é uma área ao lado do perímetro da janela que permite que o usuário dimensione a janela usando um mouse ou outro dispositivo apontador.

A *barra de rolagem horizontal* e a *barra de rolagem vertical* convertem a entrada do mouse ou do teclado em valores que um aplicativo usa para deslocar o conteúdo da área do cliente horizontal ou verticalmente. Por exemplo, um aplicativo de processamento de texto que exibe um documento demorado geralmente fornece uma barra de rolagem vertical para permitir que o usuário pressione a página para cima e para baixo no documento.

## <a name="controls-and-dialog-boxes"></a>Controles e caixas de diálogo

Um aplicativo pode criar vários tipos de janelas, além de sua janela principal, incluindo controles e caixas de diálogo.

Um *controle* é uma janela que um aplicativo usa para obter uma parte específica das informações do usuário, como o nome de um arquivo a ser aberto ou o tamanho de ponto desejado de uma seleção de texto. Os aplicativos também usam controles para obter as informações necessárias para controlar um recurso específico de um aplicativo. Por exemplo, um aplicativo de processamento de texto normalmente fornece um controle para permitir que o usuário ative ou desative o texto. Para obter mais informações, consulte [controles do Windows](/windows/desktop/Controls/window-controls).

Os controles são sempre usados em conjunto com outra janela — normalmente, uma caixa de diálogo. Uma *caixa de diálogo* é uma janela que contém um ou mais controles. Um aplicativo usa uma caixa de diálogo para solicitar ao usuário a entrada necessária para concluir um comando. Por exemplo, um aplicativo que inclui um comando para abrir um arquivo exibiria uma caixa de diálogo que inclui controles em que o usuário especifica um caminho e um nome de arquivo. As caixas de diálogo normalmente não usam o mesmo conjunto de componentes de janela, como faz uma janela principal. A maioria tem uma barra de título, um menu de janela, uma borda (sem dimensionamento) e uma área de cliente, mas normalmente não têm uma barra de menus, minimizam e maximizam os botões ou barras de rolagem. Para obter mais informações, consulte [caixas de diálogo](/windows/desktop/dlgbox/dialog-boxes).

Uma *caixa de mensagem* é uma caixa de diálogo especial que exibe uma observação, cuidado ou aviso ao usuário. Por exemplo, uma caixa de mensagem pode informar ao usuário um problema que o aplicativo encontrou durante a execução de uma tarefa. Para obter mais informações, consulte [caixas de mensagens](/windows/desktop/dlgbox/about-dialog-boxes).

## <a name="window-attributes"></a>Atributos da janela

Um aplicativo deve fornecer as seguintes informações ao criar uma janela. (Com exceção do identificador de [janela](#window-handle), que a função de criação retorna para identificar exclusivamente a nova janela.)

-   [Nome da Classe](#class-name)
-   [Nome da janela](#window-name)
-   [Estilo de Janela](#window-style)
-   [Estilo de janela estendida](#extended-window-style)
-   [Posição](#position)
-   [Tamanho](#size)
-   [Identificador de janela pai ou proprietário](#parent-or-owner-window-handle)
-   [Manipulador de menu ou identificador de Child-Window](#menu-handle-or-child-window-identifier)
-   [Identificador de instância do aplicativo](#application-instance-handle)
-   [Dados de criação](#creation-data)
-   [Identificador da Janela](#window-handle)

Esses atributos de janela são descritos nas seções a seguir.

### <a name="class-name"></a>Nome da Classe

Cada janela pertence a uma classe de janela. Um aplicativo deve registrar uma classe de janela antes de criar qualquer Windows dessa classe. A *classe Window* define a maioria dos aspectos da aparência e do comportamento de uma janela. O componente chefe de uma classe de janela é o *procedimento de janela*, uma função que recebe e processa todas as entradas e solicitações enviadas para a janela. O sistema fornece a entrada e as solicitações na forma de *mensagens*. Para obter mais informações, consulte [classes de janela](window-classes.md), procedimentos de [janela](window-procedures.md)e [mensagens e filas de mensagem](messages-and-message-queues.md).

### <a name="window-name"></a>Nome da janela

Um *nome de janela* é uma cadeia de texto que identifica uma janela para o usuário. Uma janela principal, caixa de diálogo ou caixa de mensagem normalmente exibe seu nome de janela em sua barra de título, se presente. Um controle pode exibir seu nome de janela, dependendo da classe do controle. Por exemplo, botões, controles de edição e controles estáticos exibem seus nomes de janela dentro do retângulo ocupado pelo controle. No entanto, controles como caixas de listagem e caixas de combinação não exibem seus nomes de janela.

Para alterar o nome da janela depois de criar uma janela, use a função [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) . Essa função usa as funções [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha) e [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) para recuperar a cadeia de caracteres de nome de janela atual da janela.

### <a name="window-style"></a>Estilo de Janela

Cada janela tem um ou mais estilos de janela. Um estilo de janela é uma constante nomeada que define um aspecto da aparência e do comportamento da janela que não é especificado pela classe da janela. Um aplicativo geralmente define estilos de janela ao criar o Windows. Ele também pode definir os estilos depois de criar uma janela usando a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

O sistema e, até certo ponto, o procedimento de janela para a classe, interprete os estilos de janela.

Alguns estilos de janela se aplicam a todas as janelas, mas se aplicam ao Windows de classes de janela específicas. Os estilos de janela gerais são representados por constantes que começam com o \_ prefixo WS; eles podem ser combinados com o operador OR para formar diferentes tipos de janelas, incluindo janelas principais, caixas de diálogo e janelas filhas. Os estilos de janela específicos de classe definem a aparência e o comportamento do Windows que pertencem às classes de controle predefinidas. Por exemplo, a classe **ScrollBar** especifica um controle de barra de rolagem, mas os estilos do [**SBS \_ na horizontal**](../controls/scroll-bar-control-styles.md) e do **SBS \_ Vert** determinam se um controle de barra de rolagem horizontal ou vertical é criado.

Para obter listas de estilos que podem ser usados pelo Windows, consulte os seguintes tópicos:

-   [**Estilos de janela**](window-styles.md)
-   [Estilos de botão](../controls/button-styles.md)
-   [Estilos de caixa de combinação](../controls/combo-box-styles.md)
-   [Editar estilos de controle](../controls/edit-control-styles.md)
-   [Estilos de caixa de listagem](../controls/list-box-styles.md)
-   [Estilos de controle de edição avançados](../controls/rich-edit-control-styles.md)
-   [Estilos de controle da barra de rolagem](../controls/scroll-bar-control-styles.md)
-   [Estilos de controle estático](../controls/static-control-styles.md)

### <a name="extended-window-style"></a>Estilo de janela estendida

Cada janela pode, opcionalmente, ter um ou mais estilos de janela estendidos. Um *estilo de janela estendida* é uma constante nomeada que define um aspecto da aparência e do comportamento da janela que não é especificado pela classe Window ou pelos outros estilos de janela. Um aplicativo geralmente define os estilos de janela estendidos ao criar o Windows. Ele também pode definir os estilos depois de criar uma janela usando a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Para obter mais informações, consulte [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa).

### <a name="position"></a>Posição

A posição de uma janela é definida como as coordenadas de seu canto superior esquerdo. Essas coordenadas, às vezes chamadas de coordenadas de janela, são sempre relativas ao canto superior esquerdo da tela ou, para uma janela filho, o canto superior esquerdo da área cliente da janela pai. Por exemplo, uma janela de nível superior com as coordenadas (10, 10) é colocada em 10 pixels à direita do canto superior esquerdo da tela e 10 pixels para baixo. Uma janela filho com as coordenadas (10, 10) é colocada em 10 pixels à direita do canto superior esquerdo da área do cliente da janela pai e 10 pixels para baixo.

A função [**WindowFromPoint**](/windows/win32/api/winuser/nf-winuser-windowfrompoint) recupera um identificador para a janela que ocupa um ponto específico na tela. Da mesma forma, as funções [**ChildWindowFromPoint**](/windows/win32/api/winuser/nf-winuser-childwindowfrompoint) e [**ChildWindowFromPointEx**](/windows/win32/api/winuser/nf-winuser-childwindowfrompointex) recuperam um identificador para a janela filho que ocupa um ponto específico na área cliente da janela pai. Embora **ChildWindowFromPointEx** possa ignorar janelas filhas invisíveis, desabilitadas e transparentes, o **ChildWindowFromPoint** não pode.

### <a name="size"></a>Tamanho

O tamanho de uma janela (largura e altura) é fornecido em pixels. Uma janela pode ter zero largura ou altura. Se um aplicativo definir a largura e a altura de uma janela como zero, o sistema definirá o tamanho como o tamanho mínimo padrão da janela. Para descobrir o tamanho mínimo padrão da janela, um aplicativo usa a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) com os sinalizadores **SM \_ CXMIN** e **SM \_ CYMIN** .

Um aplicativo pode precisar criar uma janela com uma área de cliente de um tamanho específico. As funções [**AdjustWindowRect**](/windows/win32/api/winuser/nf-winuser-adjustwindowrect) e [**AdjustWindowRectEx**](/windows/win32/api/winuser/nf-winuser-adjustwindowrectex) calculam o tamanho necessário de uma janela com base no tamanho desejado da área do cliente. O aplicativo pode passar os valores de tamanho resultantes para a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Um aplicativo pode dimensionar uma janela para que seja extremamente grande; no entanto, ele não deve dimensionar uma janela para que ela seja maior que a tela. Antes de definir o tamanho de uma janela, o aplicativo deve verificar a largura e a altura da tela usando [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) com os sinalizadores **SM \_ CXSCREEN** e **SM \_ CYSCREEN** .

### <a name="parent-or-owner-window-handle"></a>Identificador de janela pai ou proprietário

Uma janela pode ter uma janela pai. Uma janela que tem um pai é chamada de *janela filho*. A *janela pai* fornece o sistema de coordenadas usado para posicionar uma janela filho. Ter uma janela pai afeta os aspectos da aparência de uma janela; por exemplo, uma janela filho é recortada para que nenhuma parte da janela filho possa aparecer fora das bordas de sua janela pai.

Uma janela que não tem pai, ou cujo pai é a janela da área de trabalho, é chamada de *janela de nível superior*. Um aplicativo pode usar a função [**EnumWindows**](/windows/win32/api/winuser/nf-winuser-enumwindows) para obter um identificador para cada janela de nível superior na tela. **EnumWindows** passa o identificador para cada janela de nível superior, por sua vez, para uma função de retorno de chamada definida pelo aplicativo, [**EnumWindowsProc**](/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)).

Uma janela de nível superior pode possuir ou pertencer a outra janela. Uma *janela de propriedade* sempre aparece na frente da janela do proprietário, é ocultada quando sua janela do proprietário é minimizada e é destruída quando sua janela do proprietário é destruída. Para obter mais informações, consulte [Windows de propriedade](window-features.md#owned-windows).

### <a name="menu-handle-or-child-window-identifier"></a>Manipulador de menu ou identificador de Child-Window

Uma janela filho pode ter um identificador de *janela filho* , um valor exclusivo definido pelo aplicativo associado à janela filho. Os identificadores de janela filho são especialmente úteis em aplicativos que criam várias janelas filhas. Ao criar uma janela filho, um aplicativo especifica o identificador da janela filho. Depois de criar a janela, o aplicativo pode alterar o identificador da janela usando a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ou pode recuperar o identificador usando a função [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) .

Cada janela, exceto uma janela filho, pode ter um menu. Um aplicativo pode incluir um menu fornecendo um identificador de menu ao registrar a classe da janela ou ao criar a janela.

### <a name="application-instance-handle"></a>Identificador de instância do aplicativo

Cada aplicativo tem um identificador de instância associado a ele. O sistema fornece o identificador de instância para um aplicativo quando o aplicativo é iniciado. Como ele pode executar várias cópias do mesmo aplicativo, o sistema usa identificadores de instância internamente para distinguir uma instância de um aplicativo de outro. O aplicativo deve especificar o identificador de instância em muitas janelas diferentes, incluindo aquelas que criam o Windows.

### <a name="creation-data"></a>Dados de criação

Cada janela pode ter dados de criação definidos pelo aplicativo associados a ela. Quando a janela é criada pela primeira vez, o sistema passa um ponteiro para os dados no procedimento de janela da janela que está sendo criada. O procedimento de janela usa os dados para inicializar variáveis definidas pelo aplicativo.

### <a name="window-handle"></a>Identificador da Janela

Depois de criar uma janela, a função de criação retorna um *identificador de janela* que identifica exclusivamente a janela. Um identificador de janela tem o tipo de dados **HWND** ; um aplicativo deve usar esse tipo ao declarar uma variável que mantém um identificador de janela. Um aplicativo usa esse identificador em outras funções para direcionar suas ações para a janela.

Um aplicativo pode usar a função [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) para descobrir se existe uma janela com o nome de classe ou nome de janela especificado no sistema. Se tal janela existir, **FindWindow** retornará um identificador para a janela. Para limitar a pesquisa às janelas filhas de um aplicativo específico, use a função [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) .

A função [**IsWindow**](/windows/win32/api/winuser/nf-winuser-iswindow) determina se um identificador de janela identifica uma janela válida existente. Há constantes especiais que podem substituir um identificador de janela em determinadas funções. Por exemplo, um aplicativo pode usar **a \_ difusão HWND** nas funções [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) e [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) , ou na **área de \_ trabalho HWND** na função [**MapWindowPoints**](/windows/desktop/api/winuser/nf-winuser-mapwindowpoints) .

## <a name="window-creation"></a>Criação de janela

Para criar janelas de aplicativo, use a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Você deve fornecer as informações necessárias para definir os atributos da janela. **CreateWindowEx** tem um parâmetro, *DwExStyle*, que **CreateWindow** não tem; caso contrário, as funções são idênticas. Na verdade, a **CreateWindow** simplesmente chama **CreateWindowEx** com o parâmetro *dwExStyle* definido como zero. Por esse motivo, o restante desta visão geral refere-se apenas a **CreateWindowEx**.

Esta seção contém os seguintes tópicos:

-   [Criação da janela principal](#main-window-creation)
-   [Mensagens de criação de janela](#window-creation-messages)
-   [Aplicativos multithread](#multithread-applications)

> [!Note]  
> Há funções adicionais para a criação de janelas de finalidade especial, como caixas de diálogo e caixas de mensagem. Para obter mais informações, consulte [**caixa**](/windows/desktop/api/winuser/nf-winuser-dialogboxa), [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga)e [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).

 

### <a name="main-window-creation"></a>Criação da janela principal

Cada aplicativo baseado no Windows deve ter [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) como sua função de ponto de entrada. O **WinMain** executa várias tarefas, incluindo o registro da classe Window para a janela principal e a criação da janela principal. **WinMain** registra a classe da janela principal chamando a função [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) e cria a janela principal chamando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Sua função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) também pode limitar seu aplicativo a uma única instância. Crie um mutex nomeado usando a função [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) . Se [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornar um **erro \_ já \_ existir**, outra instância do aplicativo existirá (ele criou o mutex) e você deverá sair de **WinMain**.

O sistema não exibe automaticamente a janela principal depois de criá-la; em vez disso, um aplicativo deve usar a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) para exibir a janela principal. Depois de criar a janela principal, a função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) do aplicativo chama a **janela** de exibição, passando dois parâmetros: um identificador para a janela principal e um sinalizador especificando se a janela principal deve ser minimizada ou maximizada quando é exibida pela primeira vez. Normalmente, o sinalizador pode ser definido como qualquer uma das constantes começando com o \_ prefixo SW. No entanto, quando o **conwindow** é chamado para exibir a janela principal do aplicativo, o sinalizador deve ser definido como **SW \_ padrão**. Esse sinalizador informa o sistema para exibir a janela conforme orientado pelo programa que iniciou o aplicativo.

Se uma classe de janela foi registrada com a versão Unicode de [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa), a janela recebe apenas mensagens Unicode. Para determinar se uma janela usa o conjunto de caracteres Unicode ou não, chame [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode).

### <a name="window-creation-messages"></a>Window-Creation mensagens

Ao criar qualquer janela, o sistema envia mensagens para o procedimento de janela para a janela. O sistema envia a mensagem do [**WM \_ NCCREATE**](wm-nccreate.md) depois de criar a área não cliente da janela e a mensagem de [**\_ criação do WM**](wm-create.md) depois de criar a área do cliente. O procedimento de janela recebe ambas as mensagens antes que o sistema exiba a janela. Ambas as mensagens incluem um ponteiro para uma estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contém todas as informações especificadas na função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Normalmente, o procedimento de janela executa tarefas de inicialização após o recebimento dessas mensagens.

Ao criar uma janela filho, o sistema envia a mensagem do [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) para a janela pai depois de enviar as mensagens do WM [**\_ NCCREATE**](wm-nccreate.md) e do [**WM \_ Create**](wm-create.md) . Ele também envia outras mensagens durante a criação de uma janela. O número e a ordem dessas mensagens dependem da classe da janela e do estilo e da função usada para criar a janela. Essas mensagens são descritas em outros tópicos deste arquivo de ajuda.

### <a name="multithread-applications"></a>Aplicativos multithread

Um aplicativo baseado no Windows pode ter vários threads de execução, e cada thread pode criar o Windows. O thread que cria uma janela deve conter o código para seu procedimento de janela.

Um aplicativo pode usar a função [**EnumThreadWindows**](/windows/win32/api/winuser/nf-winuser-enumthreadwindows) para enumerar as janelas criadas por um determinado thread. Essa função passa o identificador para cada janela de thread, por sua vez, para uma função de retorno de chamada definida pelo aplicativo, [**EnumThreadWndProc**](/previous-versions/windows/desktop/legacy/ms633496(v=vs.85)).

A função [**GetWindowThreadProcessId**](/windows/win32/api/winuser/nf-winuser-getwindowthreadprocessid) retorna o identificador do thread que criou uma janela específica.

Para definir o estado de exibição de uma janela criada por outro thread, use a função [**ShowWindowAsync**](/windows/win32/api/winuser/nf-winuser-showwindowasync) .

 

 
