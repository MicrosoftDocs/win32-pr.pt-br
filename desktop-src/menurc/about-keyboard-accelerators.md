---
title: Sobre aceleradores de teclado
description: Este tópico discute aceleradores de teclado.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Windows Interface do Usuário, entrada do usuário
- Windows Interface do Usuário, aceleradores de teclado
- entrada do usuário, aceleradores de teclado
- capturando entrada do usuário, aceleradores de teclado
- aceleradores de teclado
- Aceleradores
- WM_COMMAND mensagem
- WM_SYS mensagem COMMAND
- tabelas de acelerador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e97f0b4997d15d55601e571270276e7d7a3bd4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120371"
---
# <a name="about-keyboard-accelerators"></a>Sobre aceleradores de teclado

Os aceleradores estão intimamente relacionados aos menus – ambos fornecem ao usuário acesso ao conjunto de comandos de um aplicativo. Normalmente, os usuários dependem dos menus de um aplicativo para aprender o conjunto de comandos e, em seguida, alternar para o uso de aceleradores à medida que se tornam mais proficientes com o aplicativo. Os aceleradores fornecem acesso mais rápido e direto aos comandos do que os menus. No mínimo, um aplicativo deve fornecer aceleradores para os comandos mais usados. Embora os aceleradores normalmente gerem comandos que existem como itens de menu, eles também podem gerar comandos que não têm itens de menu equivalentes.

Esta seção aborda os tópicos a seguir.

-   [Tabelas de acelerador](#accelerator-tables)
-   [Criação de tabela de acelerador](#accelerator-table-creation)
-   [Atribuições de teclas de acelerador](#accelerator-keystroke-assignments)
-   [Aceleradores e menus](#accelerators-and-menus)
-   [Estado da interface do usuário](#ui-state)

## <a name="accelerator-tables"></a>Tabelas de acelerador

Uma tabela de acelerador consiste em uma matriz de [**estruturas ACCEL,**](/windows/win32/api/winuser/ns-winuser-accel) cada uma definindo um acelerador individual. Cada **estrutura ACCEL** inclui as seguintes informações:

-   A combinação de teclas do acelerador.
-   O identificador do acelerador.
-   Vários sinalizadores. Isso inclui um que especifica se o sistema deve fornecer comentários visuais realçando o item de menu correspondente, se algum, quando o acelerador é usado

Para processar os pressões de teclas de acelerador para um thread especificado, o desenvolvedor deve chamar a função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) no loop de mensagem associado à fila de mensagens do thread. A **função TranslateAccelerator** monitora a entrada do teclado para a fila de mensagens, verificando se há combinações de teclas que corresponderem a uma entrada na tabela do acelerador. Quando **TranslateAccelerator** encontra uma combinação, ele converte a entrada do teclado (ou seja, as mensagens [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) e [**WM \_ KEYDOWN)**](/windows/desktop/inputdev/wm-keydown) em uma mensagem [**WM \_ COMMAND**](wm-command.md) ou [**WM \_ SYSCOMMAND**](wm-syscommand.md) e, em seguida, envia a mensagem para o procedimento de janela da janela especificada. A ilustração a seguir mostra como os aceleradores são processados.

![modelo de processamento do acelerador de teclado](images/cskac-01.png)

A [**mensagem \_ WM COMMAND**](wm-command.md) inclui o identificador do acelerador que fez [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) gerar a mensagem. O procedimento de janela examina o identificador para determinar a origem da mensagem e, em seguida, processa a mensagem de acordo.

As tabelas de acelerador existem em dois níveis diferentes. O sistema mantém uma única tabela de acelerador de todo o sistema que se aplica a todos os aplicativos. Um aplicativo não pode modificar a tabela do acelerador de sistema. Para ver uma descrição dos aceleradores fornecidos pela tabela do acelerador de sistema, consulte [Atribuições de teclas de](#accelerator-keystroke-assignments)acelerador.

O sistema também mantém tabelas de acelerador para cada aplicativo. Um aplicativo pode definir qualquer número de tabelas de acelerador para uso com suas próprias janelas. Um identificador exclusivo de 32 bits (**HACCEL**) identifica cada tabela. No entanto, apenas uma tabela de acelerador pode estar ativa por vez para um thread especificado. O handle para a tabela de acelerador passado para a [**função TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) determina qual tabela de acelerador está ativa para um thread. A tabela do acelerador ativo pode ser alterada a qualquer momento passando um alça de tabela de acelerador diferente para **TranslateAccelerator**.

## <a name="accelerator-table-creation"></a>Accelerator-Table criação

Várias etapas são necessárias para criar uma tabela de acelerador para um aplicativo. Primeiro, um compilador de recursos é usado para criar recursos de tabela de acelerador e adicioná-los ao arquivo executável do aplicativo. Em tempo de operação, [**a função LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) é usada para carregar a tabela do acelerador na memória e recuperar o alça para a tabela do acelerador. Esse alça é passado para a [**função TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para ativar a tabela do acelerador.

Uma tabela de acelerador também pode ser criada para um aplicativo em tempo de executar passando uma matriz de estruturas [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) para a [**função CreateAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) Esse método dá suporte a aceleradores definidos pelo usuário no aplicativo. Assim como a [**função LoadAccelerators,**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) **CreateAcceleratorTable** retorna um alça de tabela de acelerador que pode ser passado para [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para ativar a tabela do acelerador.

O sistema destrói automaticamente as tabelas de acelerador carregadas por [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) ou criadas por [**CreateAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) No entanto, um aplicativo pode liberar recursos enquanto está em execução, destrói tabelas de acelerador não mais necessárias chamando a [**função DestroyAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)

Uma tabela de acelerador existente pode ser copiada e modificada. A tabela do acelerador existente é copiada usando a [**função CopyAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) Depois que a cópia é modificada, um handle para a nova tabela de acelerador é recuperado chamando [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Por fim, o alça é passado [**para TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para ativar a nova tabela.

## <a name="accelerator-keystroke-assignments"></a>Atribuições de teclas de acelerador

Um código de caractere ASCII ou um código de chave virtual pode ser usado para definir o acelerador. Um código de caractere ASCII diferencia as minúsculas do acelerador. Portanto, usar o caractere ASCII "C" define o acelerador como ALT+C em vez de ALT+c. No entanto, aceleradores sensíveis a minúsculas podem ser confusos de usar. Por exemplo, o acelerador ALT+C será gerado se a tecla CAPS LOCK estiver inoC ou se a tecla SHIFT estiver inocíntea, mas não se ambas estão inoc baixo.

Normalmente, os aceleradores não precisam diferenciação de minúsculas, portanto, a maioria dos aplicativos usa códigos de chave virtual para aceleradores em vez de códigos de caractere ASCII.

Evite aceleradores que conflitam com o menu mnemônico de um aplicativo, pois o acelerador substitui o mnemônico, o que pode confundir o usuário. Para obter mais informações sobre mnemônicos de menu, consulte [Menus](menus.md).

Se um aplicativo definir um acelerador que também é definido na tabela do acelerador de sistema, o acelerador definido pelo aplicativo substituirá o acelerador do sistema, mas somente dentro do contexto do aplicativo. No entanto, evite essa prática, pois ela impede que o acelerador de sistema executa sua função padrão na interface do usuário. Os aceleradores de todo o sistema são descritos na lista a seguir:



| Acelerador                 | Descrição                                                                                                      |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ESC          | Alterna para o próximo aplicativo.                                                                     |
| ALT+F4           | Fecha um aplicativo ou uma janela.                                                                    |
| ALT+HÍFEN       | Abre o menu **Janela** para uma janela de documento.                                                      |
| ALT+TELA DE IMPRESSÃO | Copia uma imagem na janela ativa para a área de transferência.                                              |
| ALT+BARRA DE ESPAÇOS     | Abre o menu **Janela** da janela principal do aplicativo.                                          |
| ALT+TAB          | Alterna para o próximo aplicativo.                                                                     |
| CTRL+ESC         | Alterna **para** o menu Iniciar.                                                                       |
| CTRL+F4          | Fecha a janela de documento ou grupo ativo.                                                           |
| F1               | Inicia o arquivo de ajuda do aplicativo, se houver um.                                                    |
| TELA DE IMPRESSÃO     | Copia uma imagem na tela para a área de transferência.                                                     |
| SHIFT+ALT+TAB    | Alterna para o aplicativo anterior. O usuário deve pressionar e manter pressionada ALT+SHIFT enquanto pressiona TAB. |



 

## <a name="accelerators-and-menus"></a>Aceleradores e menus

O uso de um acelerador é o mesmo que escolher um item de menu: ambas as ações faz com que o sistema envie uma mensagem [**WM \_ COMMAND**](wm-command.md) ou [**WM \_ SYSCOMMAND**](wm-syscommand.md) para o procedimento de janela correspondente. A mensagem de **\_ comando do WM** inclui um identificador que o procedimento de janela examina para determinar a origem da mensagem. Se um acelerador gerar a mensagem de **\_ comando do WM** , o identificador será o do acelerador. Da mesma forma, se um item de menu gerou a mensagem de **\_ comando do WM** , o identificador é o do item de menu. Como um acelerador fornece um atalho para escolher um comando em um menu, um aplicativo geralmente atribui o mesmo identificador ao acelerador e ao item de menu correspondente.

Um aplicativo processa uma mensagem [**de \_ comando**](wm-command.md) do Accelerator WM exatamente da mesma forma que a mensagem de **\_ comando do WM** do item de menu correspondente. No entanto, a mensagem de **\_ comando do WM** contém um sinalizador que especifica se a mensagem foi originada de um acelerador ou de um item de menu, no caso de aceleradores devem ser processados de forma diferente de seus itens de menu correspondentes. A mensagem do [**WM \_ SYSCOMMAND**](wm-syscommand.md) não contém esse sinalizador.

O identificador determina se um acelerador gera [**um \_ comando do WM**](wm-command.md) ou uma mensagem [**\_ SYSCOMMAND do WM**](wm-syscommand.md) . Se o identificador tiver o mesmo valor de um item de menu no menu do sistema, o acelerador gerará uma mensagem do **WM \_ SYSCOMMAND** . Caso contrário, o acelerador gera uma mensagem de **\_ comando do WM** .

Se um acelerador tiver o mesmo identificador de um item de menu e o item de menu estiver esmaecido ou desabilitado, o acelerador será desabilitado e não gerará um [**\_ comando do WM**](wm-command.md) ou uma mensagem do [**WM \_ SYSCOMMAND**](wm-syscommand.md) . Além disso, um acelerador não gerará uma mensagem de comando se a janela correspondente for minimizada.

Quando o usuário usa um acelerador que corresponde a um item de menu, o procedimento de janela recebe as mensagens do [**WM \_ INITMENU**](wm-initmenu.md) e do [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) como se o usuário tivesse selecionado o item de menu. Para obter informações sobre como processar essas mensagens, consulte [menus](menus.md).

Um acelerador que corresponde a um item de menu deve ser incluído no texto do item de menu.

## <a name="ui-state"></a>Estado da interface do usuário

O Windows permite que os aplicativos ocultem ou mostrem vários recursos em sua interface do usuário. Essas configurações são conhecidas como o estado da interface do usuário. O estado da interface do usuário inclui as seguintes configurações:

-   indicadores de foco (como retângulos de foco em botões)
-   aceleradores de teclado (indicados por sublinhados em rótulos de controle)

Uma janela pode enviar mensagens para solicitar uma alteração no estado da interface do usuário, pode consultar o estado da interface do usuário ou impor um determinado estado para suas janelas filhas. Essas mensagens são as seguintes.



| Mensagem                                       | Descrição                                |
|-----------------------------------------------|--------------------------------------------|
| [**CHANGEUISTATE do WM \_**](wm-changeuistate.md) | Indica que o estado da interface do usuário deve ser alterado. |
| [**QUERYUISTATE do WM \_**](wm-queryuistate.md)   | Recupera o estado da interface do usuário para uma janela.       |
| [**UPDATEUISTATE do WM \_**](wm-updateuistate.md) | Altera o estado da interface do usuário.                      |



 

Por padrão, todas as janelas filhas de uma janela de nível superior são criadas com o mesmo estado de interface do usuário que seu pai.

O sistema manipula o estado da interface do usuário para controles em caixas de diálogo. Na criação da caixa de diálogo, o sistema inicializa o estado da interface do usuário de acordo. Todos os controles filho herdam esse estado. Depois que a caixa de diálogo é criada, o sistema monitora os pressionamentos de tecla do usuário. Se as configurações de estado da interface do usuário estiverem ocultas e o usuário navegar usando o teclado, o sistema atualizará o estado da interface do usuário. Por exemplo, se o usuário pressionar a tecla Tab para mover o foco para o próximo controle, o sistema chamará o [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) para tornar os indicadores de foco visíveis. Se o usuário pressionar a tecla Alt, o sistema chamará o **WM \_ CHANGEUISTATE** para tornar os aceleradores de teclado visíveis.

Se um controle oferecer suporte à navegação entre os elementos da interface do usuário que ele contém, ele poderá atualizar seu próprio estado de interface do usuário. O controle pode chamar o [**WM \_ QUERYUISTATE**](wm-queryuistate.md) para recuperar e armazenar em cache o estado inicial da interface do usuário. Sempre que o controle recebe uma mensagem do [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) , ele pode atualizar seu estado de interface do usuário e enviar uma mensagem do [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) para seu pai. Cada janela continuará a enviar a mensagem para seu pai até atingir a janela de nível superior. A janela de nível superior envia a mensagem do **WM \_ UPDATEUISTATE** para as janelas na árvore de janelas. Se uma janela não passar na mensagem do **WM \_ CHANGEUISTATE** , ela não alcançará a janela de nível superior e o estado da interface do usuário não será atualizado.

 

 