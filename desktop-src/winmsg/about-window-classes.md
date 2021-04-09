---
description: Cada classe de janela tem um procedimento de janela associado compartilhado por todas as janelas da mesma classe. O procedimento de janela processa mensagens para todas as janelas dessa classe e, portanto, controla seu comportamento e aparência.
ms.assetid: db79fd4b-6a15-4bf9-a0d9-5f6415f6c75f
title: Sobre classes de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b683176c3fd7904cf3f89b385ce0fa393b89e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171311"
---
# <a name="about-window-classes"></a>Sobre classes de janela

Cada classe de janela tem um procedimento de janela associado compartilhado por todas as janelas da mesma classe. O procedimento de janela processa mensagens para todas as janelas dessa classe e, portanto, controla seu comportamento e aparência. Para obter mais informações, consulte [procedimentos de janela](window-procedures.md).

Um processo deve registrar uma classe de janela antes de poder criar uma janela dessa classe. O registro de uma classe de janela associa um procedimento de janela, estilos de classe e outros atributos de classe com um nome de classe. Quando um processo especifica um nome de classe na função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , o sistema cria uma janela com o procedimento de janela, os estilos e outros atributos associados a esse nome de classe.

Esta seção aborda os tópicos a seguir.

-   [Tipos de classes de janela](#types-of-window-classes)
    -   [Classes do sistema](#system-classes)
    -   [Classes globais do aplicativo](#application-global-classes)
    -   [Classes locais do aplicativo](#application-local-classes)
-   [Como o sistema localiza uma classe de janela](#how-the-system-locates-a-window-class)
-   [Registrando uma classe de janela](#registering-a-window-class)
-   [Elementos de uma classe de janela](#elements-of-a-window-class)
    -   [Nome da Classe](#class-name)
    -   [Endereço de procedimento de janela](#window-procedure-address)
    -   [Identificador de Instância](#instance-handle)
    -   [Cursor de classe](#class-cursor)
    -   [Ícones de classe](#class-icons)
    -   [Pincel de plano de fundo de classe](#class-background-brush)
    -   [Menu de classe](#class-menu)
    -   [Estilos de Classe](#class-styles)
    -   [Memória de classe extra](#extra-class-memory)
    -   [Memória de janela extra](#extra-window-memory)

## <a name="types-of-window-classes"></a>Tipos de classes de janela

Há três tipos de classes de janela:

-   [Classes do sistema](#system-classes)
-   [Classes globais do aplicativo](#application-global-classes)
-   [Classes locais do aplicativo](#application-local-classes)

Esses tipos diferem no escopo e em quando e como eles são registrados e destruídos.

### <a name="system-classes"></a>Classes do sistema

Uma classe de sistema é uma classe de janela registrada pelo sistema. Muitas classes de sistema estão disponíveis para todos os processos a serem usados, enquanto outras são usadas apenas internamente pelo sistema. Como o sistema registra essas classes, um processo não pode destruí-las.

O sistema registra as classes do sistema para um processo na primeira vez em que um de seus threads chama um usuário ou uma função do Windows Graphics Device Interface (GDI).

Cada aplicativo recebe sua própria cópia das classes do sistema. Todos os aplicativos de 16 bits baseados no Windows nas mesmas classes do sistema de compartilhamento do VDM, assim como no Windows de 16 bits.

A tabela a seguir descreve as classes de sistema que estão disponíveis para uso por todos os processos.



| Classe     | Descrição                         |
|-----------|-------------------------------------|
| Botão    | A classe de um botão.             |
| ComboBox  | A classe para uma caixa de combinação.          |
| Editar      | A classe para um controle de edição.      |
| ListBox   | A classe para uma caixa de listagem.           |
| MDIClient | A classe para uma janela do cliente MDI. |
| ScrollBar | A classe de uma barra de rolagem.         |
| Estático    | A classe para um controle estático.     |



 

A tabela a seguir descreve as classes de sistema que estão disponíveis somente para uso pelo sistema. Eles estão listados aqui para fins de integridade.



| Classe      | Descrição                                                            |
|------------|------------------------------------------------------------------------|
| ComboLBox  | A classe da caixa de listagem contida em uma caixa de combinação.                   |
| DDEMLEvent | A classe para eventos de DDEML (biblioteca de gerenciamento de troca dinâmica de dados). |
| Mensagem    | A classe para uma janela somente mensagem.                                   |
| \#32768    | A classe de um menu.                                                  |
| \#32769    | A classe da janela da área de trabalho.                                      |
| \#32770    | A classe para uma caixa de diálogo.                                            |
| \#32771    | A classe da janela de comutador de tarefa.                                  |
| \#32772    | A classe para títulos de ícones.                                             |



 

### <a name="application-global-classes"></a>Classes globais do aplicativo

Uma [classe global de aplicativo](#application-global-classes) é uma classe de janela registrada por um executável ou DLL que está disponível para todos os outros módulos no processo. Por exemplo, o. dll pode chamar a função [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) para registrar uma classe de janela que define um controle personalizado como uma classe global de aplicativo para que um processo que carrega o. dll possa criar instâncias do controle personalizado.

Para criar uma classe que possa ser usada em cada processo, crie a classe Window em uma. dll e carregue o. dll em cada processo. Para carregar o. dll em cada processo, adicione seu nome ao valor **de \_ DLLs AppInit** na seguinte chave do registro:

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows**

Sempre que um processo é iniciado, o sistema carrega o. dll especificado no contexto do processo recentemente iniciado antes de chamar sua função de ponto de entrada. O. dll deve registrar a classe durante seu procedimento de inicialização e deve especificar o estilo **cs \_ GLOBALCLASS** . Para obter mais informações, consulte [estilos de classe](#class-styles).

Para remover uma classe global de aplicativo e liberar o armazenamento associado a ela, use a função [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) .

### <a name="application-local-classes"></a>Classes locais do aplicativo

Uma [classe local de aplicativo](#application-local-classes) é qualquer classe de janela que um executável ou. dll registra para seu uso exclusivo. Embora você possa registrar qualquer número de classes locais, é comum registrar apenas uma. Essa classe de janela dá suporte ao procedimento de janela da janela principal do aplicativo.

O sistema destrói uma classe local quando o módulo que o registrou fecha. Um aplicativo também pode usar a função [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) para remover uma classe local e liberar o armazenamento associado a ela.

## <a name="how-the-system-locates-a-window-class"></a>Como o sistema localiza uma classe de janela

O sistema mantém uma lista de estruturas para cada um dos três tipos de classes de janela. Quando um aplicativo chama a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) para criar uma janela com uma classe especificada, o sistema usa o procedimento a seguir para localizar a classe.

1.  Pesquise a lista de classes locais do aplicativo em busca de uma classe com o nome especificado cujo identificador de instância corresponda ao identificador de instância do módulo. (Vários módulos podem usar o mesmo nome para registrar as classes locais no mesmo processo.)
2.  Se o nome não estiver na lista de classes locais do aplicativo, pesquise a lista de classes globais do aplicativo.
3.  Se o nome não estiver na lista de classes globais do aplicativo, pesquise a lista de classes do sistema.

Todas as janelas criadas pelo aplicativo usam esse procedimento, incluindo o Windows criado pelo sistema em nome do aplicativo, como caixas de diálogo. É possível substituir as classes do sistema sem afetar outros aplicativos. Ou seja, um aplicativo pode registrar uma classe local de aplicativo com o mesmo nome de uma classe de sistema. Isso substitui a classe System no contexto do aplicativo, mas não impede que outros aplicativos usem a classe System.

## <a name="registering-a-window-class"></a>Registrando uma classe de janela

Uma classe de janela define os atributos de uma janela, como seu estilo, ícone, cursor, menu e procedimento de janela. A primeira etapa no registro de uma classe de janela é preencher uma estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) com as informações de classe de janela. Para obter mais informações, consulte [elementos de uma classe de janela](#elements-of-a-window-class). Em seguida, passe a estrutura para a função [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Para obter mais informações, consulte [usando classes de janela](using-window-classes.md).

Para registrar uma classe global de aplicativo, especifique o \_ estilo cs GLOBALCLASS no membro **Style** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Ao registrar uma classe local de aplicativo, não especifique o estilo **cs \_ GLOBALCLASS** .

Se você registrar a classe Window usando a versão ANSI de [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa), **RegisterClassExA**, o aplicativo solicitará que o sistema passe parâmetros de texto de mensagens para as janelas da classe criada usando o conjunto de caracteres ANSI; Se você registrar a classe usando a versão Unicode de **RegisterClassEx**, **RegisterClassExW**, o aplicativo solicitará que o sistema passe parâmetros de texto de mensagens para as janelas da classe criada usando o conjunto de caracteres Unicode. A função [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permite que os aplicativos consultem a natureza de cada janela. Para obter mais informações sobre as funções ANSI e Unicode, consulte [convenções para protótipos de função](/windows/desktop/Intl/conventions-for-function-prototypes).

O executável ou DLL que registrou a classe é o proprietário da classe. O sistema determina a propriedade de classe do membro **HINSTANCE** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) passada para a função [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) quando a classe é registrada. Para DLLs, o membro **HINSTANCE** deve ser o identificador para a instância. dll.

A classe não é destruída quando a. dll que a possui é descarregada. Portanto, se o sistema chamar o procedimento de janela para uma janela dessa classe, isso causará uma violação de acesso, pois o. dll que contém o procedimento de janela não está mais na memória. O processo deve destruir todas as janelas usando a classe antes que o. dll seja descarregado e chame a função [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) .

## <a name="elements-of-a-window-class"></a>Elementos de uma classe de janela

Os elementos de uma classe de janela definem o comportamento padrão do Windows que pertence à classe. O aplicativo que registra uma classe de janela atribui elementos à classe definindo membros apropriados em uma estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) e passando a estrutura para a função [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . As funções [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) e [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) recuperam informações sobre uma determinada classe de janela. A função [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) altera os elementos de uma classe local ou global que o aplicativo já registrou.

Embora uma classe de janela completa consista em muitos elementos, o sistema requer apenas que um aplicativo forneça um nome de classe, o endereço de procedimento de janela e um identificador de instância. Use os outros elementos para definir atributos padrão para janelas da classe, como a forma do cursor e o conteúdo do menu para a janela. Você deve inicializar quaisquer membros não utilizados da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) como zero ou **NULL**. Os elementos da classe Window são mostrados na tabela a seguir.



| Elemento                                               | Finalidade                                                                                                                                                                                                                                       |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nome da Classe](#class-name)                             | Distingue a classe de outras classes registradas.                                                                                                                                                                                        |
| [Endereço de procedimento de janela](#window-procedure-address) | Ponteiro para a função que processa todas as mensagens enviadas ao Windows na classe e define o comportamento da janela.                                                                                                                      |
| [Identificador de Instância](#instance-handle)                   | Identifica o aplicativo ou. dll que registrou a classe.                                                                                                                                                                                 |
| [Cursor de classe](#class-cursor)                         | Define o cursor do mouse que o sistema exibe para uma janela da classe.                                                                                                                                                                  |
| [Ícones de classe](#class-icons)                           | Define o ícone grande e o ícone pequeno.                                                                                                                                                                                                    |
| [Pincel de plano de fundo de classe](#class-background-brush)     | Define a cor e o padrão que preenchem a área do cliente quando a janela é aberta ou pintada.                                                                                                                                                 |
| [Menu de classe](#class-menu)                             | Especifica o menu padrão para o Windows que não define explicitamente um menu.                                                                                                                                                                  |
| [Estilos de Classe](#class-styles)                         | Define como atualizar a janela depois de movê-la ou redimensioná-la, como processar cliques duplos do mouse, como alocar espaço para o contexto do dispositivo e outros aspectos da janela.                                                       |
| [Memória de classe extra](#extra-class-memory)             | Especifica a quantidade de memória extra, em bytes, que o sistema deve reservar para a classe. Todas as janelas na classe compartilham a memória extra e podem usá-la para qualquer finalidade definida pelo aplicativo. O sistema inicializa essa memória para zero. |
| [Memória de janela extra](#extra-window-memory)           | Especifica a quantidade de memória extra, em bytes, que o sistema deve reservar para cada janela pertencente à classe. A memória extra pode ser usada para qualquer finalidade definida pelo aplicativo. O sistema inicializa essa memória para zero.          |



 

### <a name="class-name"></a>Nome da Classe

Cada classe de janela precisa de um [nome de classe](#class-name) para distinguir uma classe de outra. Atribua um nome de classe definindo o membro **lpszClassName** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) como o endereço de uma cadeia de caracteres terminada em nulo que especifica o nome. Como as classes de janela são específicas de processo, os nomes de classe de janela precisam ser exclusivos somente dentro do mesmo processo. Além disso, como os nomes de classe ocupam espaço na tabela Atom privada do sistema, você deve manter cadeias de caracteres de nome de classe o mais curta possível.

A função [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname) recupera o nome da classe à qual uma determinada janela pertence.

### <a name="window-procedure-address"></a>Endereço de procedimento de janela

Cada classe precisa de um endereço de procedimento de janela para definir o ponto de entrada do procedimento de janela usado para processar todas as mensagens para o Windows na classe. O sistema passa mensagens para o procedimento quando requer que a janela Execute tarefas, como pintar a área do cliente ou responder à entrada do usuário. Um processo atribui um procedimento de janela a uma classe copiando seu endereço para o membro **lpfnWndProc** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Para obter mais informações, consulte [procedimentos de janela](window-procedures.md).

### <a name="instance-handle"></a>Identificador de Instância

Cada classe de janela requer um identificador de instância para identificar o aplicativo ou. dll que registrou a classe. O sistema requer identificadores de instância para manter o controle de todos os módulos. O sistema atribui um identificador a cada cópia de um executável ou. dll em execução.

O sistema passa um identificador de instância para a função de ponto de entrada de cada executável (consulte [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)) e. dll (consulte [**DllMain**](/windows/desktop/Dlls/dllmain)). O executável ou. dll atribui esse identificador de instância à classe copiando-o para o membro **HINSTANCE** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

### <a name="class-cursor"></a>Cursor de classe

O *cursor de classe* define a forma do cursor quando está na área do cliente de uma janela na classe. O sistema define automaticamente o cursor para a forma determinada quando o cursor entra na área do cliente da janela e garante que ela mantenha essa forma enquanto ela permanece na área do cliente. Para atribuir uma forma de cursor a uma classe de janela, carregue uma forma de cursor predefinida usando a função [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) e, em seguida, atribua o identificador de cursor retornado ao membro **HCursor** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Como alternativa, forneça um recurso de cursor personalizado e use a função **LoadCursor** para carregá-lo dos recursos do aplicativo.

O sistema não requer um cursor de classe. Se um aplicativo definir o membro **hCursor** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) como **NULL**, nenhum cursor de classe será definido. O sistema assume que a janela define a forma do cursor cada vez que o cursor se move para a janela. Uma janela pode definir a forma do cursor chamando a função [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) sempre que a janela receber a mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) . Para obter mais informações sobre cursores, consulte [cursores](/windows/desktop/menurc/cursors).

### <a name="class-icons"></a>Ícones de classe

Um *ícone de classe* é uma imagem que o sistema usa para representar uma janela de uma classe específica. Um aplicativo pode ter dois ícones de classe, um grande e um pequeno. O sistema exibe o ícone de *classe grande* de uma janela na janela de opção de tarefa que aparece quando o usuário pressiona ALT + TAB e, nos modos de exibição de ícone grande da barra de tarefas e do Explorer. O *ícone de classe pequena* aparece na barra de título de uma janela e nas exibições de ícone pequeno da barra de tarefas e do Explorer.

Para atribuir um ícone grande e pequeno a uma classe de janela, especifique as alças dos ícones nos membros **HICON** e **HIconSm** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . As dimensões de ícone devem estar em conformidade com as dimensões obrigatórias para ícones de classe grande e pequena. Para um ícone de classe grande, você pode determinar as dimensões necessárias especificando os valores **SM \_ CXICON** e **SM \_ CYICON** em uma chamada para a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Para um ícone de classe pequena, especifique os valores de **SM \_ CXSMICON** e **SM \_ CYSMICON** . Para obter informações, consulte [ícones](/windows/desktop/menurc/icons).

Se um aplicativo definir os membros **HICON** e **HIconSm** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) como **NULL**, o sistema usará o ícone de aplicativo padrão como os ícones de classe grande e pequeno para a classe Window. Se você especificar um ícone de classe grande, mas não um pequeno, o sistema criará um ícone de classe pequena com base no grande. No entanto, se você especificar um ícone de classe pequena, mas não um grande, o sistema usará o ícone de aplicativo padrão como o ícone de classe grande e o ícone especificado como o ícone de classe pequena.

Você pode substituir o ícone de classe grande ou pequena de uma janela específica usando a mensagem de [**\_ SetIcon do WM**](wm-seticon.md) . Você pode recuperar o ícone de classe grande ou pequena atual usando a mensagem de [**\_ GetIcon do WM**](wm-geticon.md) .

### <a name="class-background-brush"></a>Pincel de plano de fundo de classe

Um *pincel de plano de fundo de classe* prepara a área do cliente de uma janela para o desenho subsequente pelo aplicativo. O sistema usa o pincel para preencher a área do cliente com uma cor sólida ou padrão, removendo, assim, todas as imagens anteriores desse local, independentemente de pertencerem à janela ou não. O sistema notifica uma janela de que seu plano de fundo deve ser pintado enviando a mensagem [**\_ ERASEBKGND do WM**](wm-erasebkgnd.md) para a janela. Para obter mais informações, consulte [pincéis](/windows/desktop/gdi/brushes).

Para atribuir um pincel de plano de fundo a uma classe, crie um pincel usando as funções de GDI apropriadas e atribua o identificador de pincel retornado ao membro **hbrBackground** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

Em vez de criar um pincel, um aplicativo pode definir o membro **hbrBackground** como um dos valores de cor do sistema padrão. Para obter uma lista dos valores de cores do sistema padrão, consulte [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors).

Para usar uma cor padrão do sistema, o aplicativo deve aumentar o valor de cor de fundo em um. Por exemplo, **cor \_** de plano de fundo + 1 é a cor do plano de fundo do sistema. Como alternativa, você pode usar a função [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) para recuperar um identificador para um pincel que corresponde a uma cor do sistema padrão e, em seguida, especificar o identificador no membro **HbrBackground** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

O sistema não exige que uma classe de janela tenha um pincel de plano de fundo de classe. Se esse parâmetro for definido como **NULL**, a janela deverá pintar seu próprio plano de fundo sempre que receber a mensagem [**\_ ERASEBKGND do WM**](wm-erasebkgnd.md) .

### <a name="class-menu"></a>Menu de classe

Um *menu de classe* define o menu padrão a ser usado pelas janelas na classe se nenhum menu explícito é fornecido quando as janelas são criadas. Um menu é uma lista de comandos dos quais um usuário pode escolher ações para o aplicativo executar.

Você pode atribuir um menu a uma classe definindo o membro **lpszMenuName** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) como o endereço de uma cadeia de caracteres terminada em nulo que especifica o nome do recurso do menu. Presume-se que o menu seja um recurso no determinado aplicativo. O sistema carrega automaticamente o menu quando necessário. Se o recurso de menu for identificado por um inteiro e não por um nome, o aplicativo poderá definir o membro **lpszMenuName** para esse inteiro aplicando a macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) antes de atribuir o valor.

O sistema não requer um menu de classe. Se um aplicativo definir o membro **lpszMenuName** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) como **NULL**, o Windows na classe não terá barras de menus. Mesmo que nenhum menu de classe seja fornecido, um aplicativo ainda pode definir uma barra de menus para uma janela ao criar a janela.

Se um menu for fornecido para uma classe e uma janela filho dessa classe for criada, o menu será ignorado. Para obter mais informações, consulte [menus](/windows/desktop/menurc/menus).

### <a name="class-styles"></a>Estilos de Classe

Os estilos de classe definem elementos adicionais da classe Window. Dois ou mais estilos podem ser combinados usando o operador OR ( \| Para atribuir um estilo a uma classe de janela, atribua o estilo ao membro **Style** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Para obter uma lista de estilos de classe, consulte [**estilos de classe de janela**](window-class-styles.md).

### <a name="classes-and-device-contexts"></a>Classes e contextos de dispositivo

Um *contexto de dispositivo* é um conjunto especial de valores que os aplicativos usam para desenhar na área do cliente de suas janelas. O sistema requer um contexto de dispositivo para cada janela na tela, mas permite alguma flexibilidade na forma como o sistema armazena e trata esse contexto de dispositivo.

Se nenhum estilo de contexto de dispositivo for explicitamente fornecido, o sistema assumirá que cada janela usa um contexto de dispositivo recuperado de um pool de contextos mantidos pelo sistema. Nesses casos, cada janela deve recuperar e inicializar o contexto do dispositivo antes de pintar e liberá-lo após a pintura.

Para evitar a recuperação de um contexto de dispositivo sempre que ele precisar pintar dentro de uma janela, um aplicativo pode especificar o estilo **cs \_ OWNDC** para a classe Window. Esse estilo de classe direciona o sistema para criar um contexto de dispositivo privado, ou seja, para alocar um contexto de dispositivo exclusivo para cada janela na classe. O aplicativo só precisa recuperar o contexto uma vez e, em seguida, usá-lo para todas as pinturas subsequentes.

### <a name="extra-class-memory"></a>Memória de classe extra

O sistema mantém uma estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) internamente para cada classe de janela no sistema. Quando um aplicativo registra uma classe de janela, ele pode instruir o sistema a alocar e acrescentar vários bytes adicionais de memória ao final da estrutura **WNDCLASSEX** . Essa memória é chamada de *memória de classe extra* e é compartilhada por todas as janelas que pertencem à classe. Use a memória de classe extra para armazenar qualquer informação que pertença à classe.

Como a memória extra é alocada do heap local do sistema, um aplicativo deve usar a memória de classe extra com moderação. A função [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) falhará se a quantidade de memória de classe extra solicitada for maior que 40 bytes. Se um aplicativo exigir mais de 40 bytes, ele deverá alocar sua própria memória e armazenar um ponteiro para a memória na memória de classe extra.

As funções [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword) e [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) copiam um valor para a memória de classe extra. Para recuperar um valor da memória de classe extra, use as funções [**GetClassWord**](/windows/win32/api/winuser/nf-winuser-getclassword) e [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) . O membro **cbClsExtra** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) especifica a quantidade de memória de classe extra a ser alocada. Um aplicativo que não usa memória de classe extra deve inicializar o membro **cbClsExtra** como zero.

### <a name="extra-window-memory"></a>Memória de janela extra

O sistema mantém uma estrutura de dados interna para cada janela. Ao registrar uma classe de janela, um aplicativo pode especificar um número de bytes adicionais de memória, chamado de *memória de janela extra*. Ao criar uma janela da classe, o sistema aloca e acrescenta a quantidade especificada de memória de janela extra ao final da estrutura da janela. Um aplicativo pode usar essa memória para armazenar dados específicos da janela.

Como a memória extra é alocada do heap local do sistema, um aplicativo deve usar a memória de janela extra com moderação. A função [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) falhará se a quantidade de memória de janela extra solicitada for maior que 40 bytes. Se um aplicativo exigir mais de 40 bytes, ele deverá alocar sua própria memória e armazenar um ponteiro para a memória na memória da janela extra.

A função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) copia um valor para a memória extra. A função [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) recupera um valor da memória extra. O membro **cbWndExtra** da estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) especifica a quantidade de memória de janela extra a ser alocada. Um aplicativo que não usa a memória deve inicializar **cbWndExtra** como zero.

 

 
