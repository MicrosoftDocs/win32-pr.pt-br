---
title: Sobre aceleradores de teclado
description: Este tópico discute aceleradores de teclado.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Windows Interface do usuário, entrada do usuário
- Windows Interface do usuário, aceleradores de teclado
- entrada do usuário, aceleradores de teclado
- capturando entrada do usuário, aceleradores de teclado
- aceleradores de teclado
- aceleradores
- WM_COMMAND mensagem
- WM_SYS mensagem de comando
- tabelas do acelerador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b81240feb0ca21028c9d1813f4c8004e1c3bb932fe1ec8767e3719c26e7a5db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870723"
---
# <a name="about-keyboard-accelerators"></a>Sobre aceleradores de teclado

Os aceleradores estão fortemente relacionados aos menus – ambos fornecem ao usuário acesso ao conjunto de comandos de um aplicativo. Normalmente, os usuários dependem dos menus de um aplicativo para aprender o conjunto de comandos e, em seguida, alternar para usar aceleradores à medida que se tornam mais proficientes com o aplicativo. Os aceleradores fornecem acesso mais rápido e direto a comandos do que os menus. No mínimo, um aplicativo deve fornecer aceleradores para os comandos mais comumente usados. Embora os aceleradores normalmente gerem comandos que existem como itens de menu, eles também podem gerar comandos que não têm itens de menu equivalentes.

Esta seção aborda os tópicos a seguir.

-   [Tabelas do acelerador](#accelerator-tables)
-   [Aceleração-criação de tabela](#accelerator-table-creation)
-   [Atribuições de teclas do acelerador](#accelerator-keystroke-assignments)
-   [Aceleradores e menus](#accelerators-and-menus)
-   [Estado da interface do usuário](#ui-state)

## <a name="accelerator-tables"></a>Tabelas do acelerador

Uma tabela de acelerador consiste em uma matriz de estruturas [**da aceleração extra**](/windows/win32/api/winuser/ns-winuser-accel) , cada uma definindo um acelerador individual. Cada estrutura **da aceleração extra** inclui as seguintes informações:

-   A combinação de teclas do acelerador.
-   O identificador do acelerador.
-   Vários sinalizadores. Isso inclui um que especifica se o sistema deve fornecer comentários visuais, destacando o item de menu correspondente, se houver, quando o acelerador for usado

Para processar pressionamentos de teclas do acelerador para um thread especificado, o desenvolvedor deve chamar a função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) no loop de mensagem associado à fila de mensagens do thread. A função **TranslateAccelerator** monitora a entrada do teclado na fila de mensagens, verificando combinações de chaves que correspondem a uma entrada na tabela do acelerador. Quando **TranslateAccelerator** encontra uma correspondência, ele converte a entrada do teclado (isto é, as mensagens [**do WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) e do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) ) em [**um \_ comando do WM**](wm-command.md) ou em uma mensagem do [**WM \_ SYSCOMMAND**](wm-syscommand.md) e, em seguida, envia a mensagem para o procedimento de janela da janela especificada. A ilustração a seguir mostra como os aceleradores são processados.

![modelo de processamento do acelerador de teclado](images/cskac-01.png)

A mensagem de [**\_ comando do WM**](wm-command.md) inclui o identificador do acelerador que causou o [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para gerar a mensagem. O procedimento de janela examina o identificador para determinar a origem da mensagem e, em seguida, processa a mensagem de acordo.

As tabelas do acelerador existem em dois níveis diferentes. O sistema mantém uma única tabela de acelerador de sistema que se aplica a todos os aplicativos. Um aplicativo não pode modificar a tabela do acelerador de sistema. Para obter uma descrição dos aceleradores fornecidos pela tabela do acelerador de sistema, consulte [atribuições de teclas de aceleração](#accelerator-keystroke-assignments).

O sistema também mantém tabelas de acelerador para cada aplicativo. Um aplicativo pode definir qualquer número de tabelas de acelerador para uso com suas próprias janelas. Um **HACCEL**(identificador exclusivo de 32 bits) identifica cada tabela. No entanto, apenas uma tabela de acelerador pode estar ativa por vez para um thread especificado. O identificador para a tabela aceleradora passada para a função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) determina qual tabela de acelerador está ativa para um thread. A tabela do acelerador ativo pode ser alterada a qualquer momento, passando um identificador de tabela de aceleração diferente para **TranslateAccelerator**.

## <a name="accelerator-table-creation"></a>Criação de Accelerator-Table

Várias etapas são necessárias para criar uma tabela de acelerador para um aplicativo. Primeiro, um compilador de recurso é usado para criar recursos de tabela de aceleração e adicioná-los ao arquivo executável do aplicativo. Em tempo de execução, a função [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) é usada para carregar a tabela aceleradora na memória e recuperar o identificador para a tabela de aceleração. Esse identificador é passado para a função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para ativar a tabela de acelerador.

Uma tabela de acelerador também pode ser criada para um aplicativo em tempo de execução, passando uma matriz de estruturas [**da aceleração extra**](/windows/win32/api/winuser/ns-winuser-accel) para a função [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) . Esse método oferece suporte a aceleradores definidos pelo usuário no aplicativo. Como a [**função de**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) **LoadAccelerators, o createacelerator** retorna um identificador de tabela de aceleração que pode ser passado para [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para ativar a tabela de acelerador.

O sistema destrói automaticamente as tabelas de acelerador carregadas por [**objectaccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) ou criadas por [**createaceleration**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). No entanto, um aplicativo pode liberar recursos enquanto está em execução, destruindo tabelas de acelerador que não são mais necessárias chamando a função [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .

Uma tabela de acelerador existente pode ser copiada e modificada. A tabela de acelerador existente é copiada usando a função [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) . Depois que a cópia é modificada, um identificador para a nova tabela de acelerador é recuperado chamando [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Por fim, o identificador é passado para [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) a fim de ativar a nova tabela.

## <a name="accelerator-keystroke-assignments"></a>Atribuições de teclas do acelerador

Um código de caractere ASCII ou um código de chave virtual pode ser usado para definir o acelerador. Um código de caractere ASCII torna o acelerador diferencia maiúsculas de minúsculas. Portanto, o uso do caractere ASCII "C" define o acelerador como ALT + C em vez de ALT + c. No entanto, os aceleradores que diferenciam maiúsculas de minúsculas podem confundir o uso. Por exemplo, o acelerador ALT + C será gerado se a chave de CAPS LOCK estiver inoperante ou se a tecla SHIFT estiver inoperante, mas não se ambas estiverem inativas.

Normalmente, os aceleradores não precisam diferenciar maiúsculas de minúsculas, portanto, a maioria dos aplicativos usa códigos de chave virtual para aceleradores em vez de códigos de caracteres ASCII.

Evite os aceleradores que entram em conflito com os mnemônicos do menu de um aplicativo, pois o acelerador substitui o mnemônico, que pode confundir o usuário. Para obter mais informações sobre mnemônicos de menu, consulte [menus](menus.md).

Se um aplicativo definir um acelerador que também esteja definido na tabela do acelerador de sistema, o acelerador definido pelo aplicativo substituirá o acelerador do sistema, mas somente dentro do contexto do aplicativo. No entanto, evite essa prática porque ela impede que o acelerador do sistema execute sua função padrão na interface do usuário. Os aceleradores de todo o sistema são descritos na lista a seguir:



| Acelerador                 | Descrição                                                                                                      |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT + ESC          | Alterna para o próximo aplicativo.                                                                     |
| ALT+F4           | Fecha um aplicativo ou uma janela.                                                                    |
| ALT+HÍFEN       | Abre o menu **janela** de uma janela de documento.                                                      |
| ALT + TELA DE IMPRESSÃO | Copia uma imagem na janela ativa para a área de transferência.                                              |
| ALT+BARRA DE ESPAÇOS     | Abre o menu **janela** da janela principal do aplicativo.                                          |
| ALT+TAB          | Alterna para o próximo aplicativo.                                                                     |
| CTRL + ESC         | Alterna para o menu **Iniciar** .                                                                       |
| CTRL+F4          | Fecha a janela de grupo ou documento ativo.                                                           |
| F1               | Inicia o arquivo de ajuda do aplicativo, se houver.                                                    |
| TELA DE IMPRESSÃO     | Copia uma imagem na tela para a área de transferência.                                                     |
| SHIFT + ALT + TAB    | Alterna para o aplicativo anterior. O usuário deve pressionar e manter pressionada a tecla ALT + SHIFT enquanto pressiona TAB. |



 

## <a name="accelerators-and-menus"></a>Aceleradores e menus

O uso de um acelerador é o mesmo que escolher um item de menu: as duas ações fazem com que o sistema envie um [**\_ comando do WM**](wm-command.md) ou uma mensagem do [**WM \_ SYSCOMMAND**](wm-syscommand.md) para o procedimento de janela correspondente. A **mensagem \_ COMANDO WM** inclui um identificador que o procedimento de janela examina para determinar a origem da mensagem. Se um acelerador gerou a **mensagem WM \_ COMMAND,** o identificador é o do acelerador. Da mesma forma, se um item de menu gerou a mensagem **WM \_ COMMAND,** o identificador é o do item de menu. Como um acelerador fornece um atalho para escolher um comando em um menu, um aplicativo geralmente atribui o mesmo identificador ao acelerador e ao item de menu correspondente.

Um aplicativo processa uma mensagem [**DE COMANDO WM \_ do acelerador**](wm-command.md) exatamente da mesma maneira que a mensagem **WM \_ COMMAND** do item de menu correspondente. No entanto, a mensagem **WM \_ COMMAND** contém um sinalizador que especifica se a mensagem foi originada de um acelerador ou de um item de menu, caso os aceleradores deverão ser processados de forma diferente dos itens de menu correspondentes. A [**\_ mensagem WM SYSCOMMAND**](wm-syscommand.md) não contém esse sinalizador.

O identificador determina se um acelerador gera uma mensagem [**WM \_ COMMAND**](wm-command.md) ou [**WM \_ SYSCOMMAND.**](wm-syscommand.md) Se o identificador tiver o mesmo valor de um item de menu no menu Sistema, o acelerador gerará uma mensagem **\_ WM SYSCOMMAND.** Caso contrário, o acelerador gerará uma **mensagem \_ WM COMMAND.**

Se um acelerador tiver o mesmo identificador de um item de menu e o item de menu estiver es cinza ou desabilitado, o acelerador será desabilitado e não gerará uma mensagem [**WM \_ COMMAND**](wm-command.md) ou [**WM \_ SYSCOMMAND.**](wm-syscommand.md) Além disso, um acelerador não gerará uma mensagem de comando se a janela correspondente for minimizada.

Quando o usuário usa um acelerador que corresponde a um item de menu, o procedimento de janela recebe as mensagens [**WM \_ INITMENU**](wm-initmenu.md) e [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) como se o usuário tivesse selecionado o item de menu. Para obter informações sobre como processar essas mensagens, consulte [Menus](menus.md).

Um acelerador que corresponde a um item de menu deve ser incluído no texto do item de menu.

## <a name="ui-state"></a>Estado da interface do usuário

Windows habilita aplicativos a ocultar ou mostrar vários recursos em sua interface do usuário. Essas configurações são conhecidas como o estado da interface do usuário. O estado da interface do usuário inclui as seguintes configurações:

-   indicadores de foco (como retângulos de foco em botões)
-   aceleradores de teclado (indicados por sublinhados em rótulos de controle)

Uma janela pode enviar mensagens para solicitar uma alteração no estado da interface do usuário, pode consultar o estado da interface do usuário ou impor um determinado estado para suas janelas filho. Essas mensagens são as a seguir.



| Mensagem                                       | Descrição                                |
|-----------------------------------------------|--------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | Indica que o estado da interface do usuário deve mudar. |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | Recupera o estado da interface do usuário de uma janela.       |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | Altera o estado da interface do usuário.                      |



 

Por padrão, todas as janelas filho de uma janela de nível superior são criadas com o mesmo estado de interface do usuário que seu pai.

O sistema trata o estado da interface do usuário para controles nas caixas de diálogo. Na criação da caixa de diálogo, o sistema inicializa o estado da interface do usuário de acordo. Todos os controles filho herdam esse estado. Depois que a caixa de diálogo é criada, o sistema monitora os controles de teclas do usuário. Se as configurações de estado da interface do usuário estão ocultas e o usuário navega usando o teclado, o sistema atualiza o estado da interface do usuário. Por exemplo, se o usuário pressionar a tecla Tab para mover o foco para o próximo controle, o sistema [**chamará WM \_ CHANGEUISTATE**](wm-changeuistate.md) para tornar os indicadores de foco visíveis. Se o usuário pressionar a tecla Alt, o sistema **chamará WM \_ CHANGEUISTATE** para tornar os aceleradores de teclado visíveis.

Se um controle dá suporte à navegação entre os elementos de interface do usuário que ele contém, ele pode atualizar seu próprio estado de interface do usuário. O controle pode chamar [**WM \_ QUERYUISTATE**](wm-queryuistate.md) para recuperar e armazenar em cache o estado inicial da interface do usuário. Sempre que o controle recebe uma mensagem [**WM \_ UPDATEUISTATE,**](wm-updateuistate.md) ele pode atualizar seu estado de interface do usuário e enviar uma mensagem [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) para seu pai. Cada janela continuará a enviar a mensagem para seu pai até atingir a janela de nível superior. A janela de nível superior envia a **mensagem WM \_ UPDATEUISTATE** para as janelas na árvore de janelas. Se uma janela não passar a mensagem **WM \_ CHANGEUISTATE,** ela não alcançará a janela de nível superior e o estado da interface do usuário não será atualizado.

 

 